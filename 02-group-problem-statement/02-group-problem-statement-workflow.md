# Sơ đồ Workflow: Trích xuất hóa đơn tự động điền Excel cho Kế toán

> Tài liệu đính kèm minh họa luồng công việc Trước (Current State) và Sau (Future State) của nhóm cho bài toán xử lý hóa đơn kế toán.

---

## 1. Current State Workflow (Hiện tại — 220 phút / 60 hóa đơn)

```mermaid
flowchart TD
    A["[1] Kế toán nhận & gom file từ Email/Zalo<br/><i>(15 phút)</i>"] --> B["[2] Mở chia đôi màn hình: File HĐ & Excel<br/><i>(5 phút)</i>"]
    B --> C["[3] Đọc & bóc tách thông tin bằng mắt<br/><i>(60 phút - Mỏi mắt, ảnh scan mờ)</i>"]
    C --> D["[4] Gõ tay từng trường vào ô Excel<br/><b>BOTTLENECK CHÍNH</b><br/><i>(100 phút - Dễ gõ nhầm số liệu 5-7%)</i>"]
    D --> E["[5]  ối soát thủ công<br/><i>(30 phút - Kiểm tra lệch tiền)</i>"]
    E --> F["[6] Đổi tên file HĐ & lưu trữ thư mục<br/><i>(10 phút)</i>"]
    
    style D fill:#ffcccc,stroke:#ff0000,stroke-width:2px;
    style C fill:#fff2cc,stroke:#d6b656,stroke-width:1px;
    style E fill:#fff2cc,stroke:#d6b656,stroke-width:1px;
```

*Điểm nghẽn chính:* Bước 4 (gõ tay thủ công) và bước 3 (đọc mắt ảnh mờ) chiếm 72% tổng thời gian (160/220 phút), gây mệt mỏi và rủi ro sai lệch dữ liệu thuế.

---

## 2. Future State Workflow (Tương lai — 35 phút / 60 hóa đơn)

```mermaid
flowchart TD
    subgraph HumanInput ["1. Con người (Khởi tạo)"]
        A1["Kế toán kéo thả batch file HĐ vào thư mục input<br/><i>(2 phút)</i>"]
    end

    subgraph AIProcess ["2. AI Engine (Không cấu trúc -> Có cấu trúc)"]
        B1["Vision LLM API đọc hiểu hình ảnh/PDF<br/>Trích xuất JSON theo Schema chuẩn<br/><i>(6 phút - Chạy nền song song)</i>"]
    end

    subgraph RuleValidation ["3. Máy / Rule Engine (Chính xác tuyệt đối)"]
        C1{"Python Rule Engine:<br/>1. Kiểm tra Tiền hàng + Thuế = Tổng tiền<br/>2. Kiểm tra định dạng MST (10/13 số)"}
        C2["Dữ liệu khớp chuẩn:<br/>Ghi vào Excel bảng kê"]
        C3["Phát hiện lệch tiền / OCR mờ:<br/>Highlight ô đỏ/cam + Gắn link ảnh"]
        C4["Tự động đổi tên file theo cú pháp chuẩn<br/><i>(2 phút cho cả bước 3)</i>"]
    end

    subgraph HumanReview ["4. Con người (Kiểm duyệt - Human Boundary)"]
        D1["Kế toán mở file Excel xem kết quả<br/>- Các dòng chuẩn: Lướt nhanh<br/>- Các ô cảnh báo đỏ/cam: Bấm link ảnh đối chiếu<br/><b>HUMAN BOUNDARY PHÊ DUYỆT</b><br/><i>(23 phút)</i>"]
        D2["Lưu bảng kê chính thức & hoàn tất"]
    end

    A1 --> B1
    B1 --> C1
    C1 -- Khớp chuẩn --> C2 --> C4
    C1 -- Lệch tiền / Nghi ngờ --> C3 --> C4
    C4 --> D1
    D1 --> D2

    style HumanReview fill:#d5e8d4,stroke:#82b366,stroke-width:2px;
    style AIProcess fill:#dae8fc,stroke:#6c8ebf,stroke-width:2px;
    style RuleValidation fill:#e1d5e7,stroke:#9673a6,stroke-width:2px;
```

---

## 3. So sánh các chỉ số vận hành (Impact Summary)

| Chỉ số | Trước cải tiến | Sau cải tiến (Kỳ vọng) | Mức cải thiện |
|---|---|---|---|
| **Tổng thời gian xử lý** | 220 phút / batch 60 HĐ | 35 phút / batch 60 HĐ | **Giảm 84%** (Tiết kiệm >3 giờ/ngày) |
| **Thao tác thủ công** | 6 bước thủ công | 2 bước (Nạp file & Duyệt kết quả) | Tự động hóa 66% số bước |
| **Tỷ lệ sai sót số học** | 5–7% do gõ nhầm | **0%** | Nhờ Rule Engine kiểm tra số học trước khi xuất file |
| **Rủi ro vận hành** | Kế toán mệt mỏi, trễ hạn báo cáo | Kế toán chủ quan duyệt lướt | Được khắc phục bằng cơ chế highlight cảnh báo bắt buộc |
