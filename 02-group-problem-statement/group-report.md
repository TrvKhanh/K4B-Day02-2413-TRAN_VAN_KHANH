# 02 — Group Problem Statement (Bản nộp nhóm)

> Làm chung 1 bản, mỗi thành viên copy vào repo cá nhân. Đi theo Phase 3 → 6 trong `01-worksheet.md`. Nhóm chỉ chọn **candidate problem** ở Phase 3, viết Problem Statement sau khi validate + vẽ workflow.

## Thành viên nhóm

| STT | Họ và tên | Mã học viên | Vai trò trong nhóm (VD: facilitator, workflow, research, writer) |
|-----|-----------|-------------|---------------------------------------------------------------|
| 1   | Trần Văn Khánh | 2413 | Technical Lead & Workflow Design (Thiết kế luồng xử lý và Rule validation) |
| 2   | Ngô Tuấn Tùng | 2A202602826 | Facilitator & Validation Lead (Điều phối thảo luận và phỏng vấn người dùng) |
| 3   | Cao Đức Hiệp | 2A202602550 | Business Analyst & Metric Design (Phân tích nghiệp vụ và xây dựng ranh giới Boundary) |
| 4   | Đào Thị Huyền | 2A202602670 | Research & Documentation (Nghiên cứu giải pháp thị trường và tổng hợp tài liệu) |
| 5   | Nguyễn Huy Cương | 2A202602827 | Quality Assurance & Benchmarking (Thiết kế tiêu chí đánh giá và kiểm thử pilot) |

**Candidate problem nhóm chọn (1 câu):**

Tự động hóa việc đọc, trích xuất dữ liệu từ các tệp hóa đơn VAT (ảnh chụp/scan, PDF) và kiểm tra đối soát toán học để tự động điền vào file bảng kê chi phí Excel cho nhân viên kế toán nội bộ.

---

## Phase 3 — Group Convergence: từ 9-12 candidates về 1

### 3.1. Trình bày top 3 mỗi người (mỗi candidate 1-2 phút)

| # | Người đưa ra | Candidate problem | Người gặp vấn đề | Điểm nghẽn | Cảm nhận nhanh của nhóm |
|---|---|---|---|---|---|
| 1 | Ngô Tuấn Tùng | Debug lỗi code AI từ traceback phải tìm kiếm qua nhiều nguồn (Google/Stack Overflow) | Intern AI Engineer / Sinh viên | Mất 30-90 phút/lỗi để đọc traceback và thử sai | Pain thật của dev, nhưng phụ thuộc nhiều vào ngữ cảnh dự án cụ thể; giải pháp dễ bị trùng với Cursor/Copilot |
| 2 | Ngô Tuấn Tùng | Đọc nhiều paper/tài liệu nghiên cứu để tìm đúng đoạn liên quan đến bài toán đang làm | Sinh viên làm nghiên cứu / AI Engineer | Mất 30-60 phút/lần mở 5-10 tài liệu trước khi chọn được bài đúng | Bài toán tóm tắt tài liệu khá rộng, khó xác định tiêu chí "tài liệu đúng" một cách định lượng |
| 3 | Ngô Tuấn Tùng | Chuẩn bị nội dung và bài tập trước khi đi dạy thêm cho học sinh | Gia sư, người dạy thêm | Mất 30-60 phút/buổi dạy để soạn bài tập phù hợp năng lực | Quy trình đơn giản, có thể dùng prompt thủ công với ChatGPT là giải quyết được 80%, không cần giải pháp hệ thống |
| 4 | Nguyễn Huy Cương | Sinh viên phải kiểm tra deadline và yêu cầu bài nộp từ nhiều kênh (README, worksheet, Discord) | Sinh viên học AI/LLM | Mất 10-20 phút/lần đối chiếu thủ công giữa các file hướng dẫn | Có thể giải quyết triệt để bằng một checklist hoặc Google Calendar/Notion, chưa cần dùng đến AI |
| 5 | Nguyễn Huy Cương | Tự đối chiếu thủ công xem bài nộp đã đủ file, heading và field bắt buộc theo template chưa | Sinh viên chuẩn bị nộp bài lab | Mất thời gian đọc rà soát từng mục trong file Markdown | Bài toán dạng kiểm tra cấu trúc (linter/schema validation), dùng Rule (Python script) tối ưu hơn AI |
| 6 | Nguyễn Huy Cương | Mất nhiều thời gian chuyển đổi tài liệu học dài thành các task cụ thể theo thứ tự ưu tiên | Sinh viên mới học lab | Phân biệt yêu cầu bắt buộc và tài liệu tham khảo | Vấn đề tư duy phân rã task của người học, AI chỉ hỗ trợ gợi ý nhưng chất lượng khó đo lường |
| 7 | Cao Đức Hiệp | Tìm và tổng hợp tài liệu BA/PO từ nhiều nguồn rời rạc (YouTube, blog, nhóm Zalo) | Người tự học chuyển ngành BA/PO | Tốn 1-2 giờ/tuần để lọc và lưu trữ thông tin | Nhu cầu cá nhân, phạm vi tìm kiếm quá mở và không có ranh giới nghiệm vụ rõ ràng |
| 8 | Cao Đức Hiệp | Mất 10-15 phút mỗi lần tìm lại quyết định cũ, ghi chú trên Zalo, Notion, email | Nhân viên làm việc dự án | Phải đọc lại toàn bộ lịch sử hội thoại dài để hiểu bối cảnh | Pain phổ biến trong doanh nghiệp, nhưng rào cản phân quyền và bảo mật dữ liệu chat rất phức tạp |
| 9 | Cao Đức Hiệp | Mất thời gian sắp xếp ưu tiên giữa công việc, học tập và việc gia đình | Người đi làm kiêm học tập | Trì hoãn các việc quan trọng nhưng không khẩn cấp | Vấn đề quản lý thời gian cá nhân (Self-management), giải pháp thiên về thói quen hơn là AI |
| 10 | Trần Văn Khánh | Kế toán viên phải mở từng file hóa đơn (ảnh/PDF) gõ tay từng trường vào file bảng kê Excel | Nhân viên kế toán nội bộ | Mất 3-4 giờ/ngày gõ tay từng ô Excel, tỷ lệ gõ nhầm 5-7% | Workflow cực kỳ rõ ràng, pain đo đếm được cụ thể, ROI cao, có thể kết hợp Rule + AI chặt chẽ |
| 11 | Trần Văn Khánh | Bóc tách BOM và gợi ý bố trí layout thiết bị tủ điện từ sơ đồ nguyên lý 1 sợi | Kỹ sư thiết kế cơ điện | Mất 4-6 giờ/tủ điện để tra catalog kích thước và xếp hình CAD | Rất tiềm năng và giá trị cao, nhưng domain sâu, chỉ có Khánh hiểu, các thành viên khác khó kiểm chứng |
| 12 | Đào Thị Huyền | Viết báo cáo công việc hằng ngày (daily report) theo cùng một mẫu cố định | Intern mới ra trường | Mất 5-10 phút/ngày gom các đầu việc đã làm trong ngày | Thời gian tiết kiệm được nhỏ (5 phút/ngày), chưa đủ lớn để xây dựng một giải pháp riêng |

### 3.2. Gom trùng / cluster (gom 9-12 ý thành 3-4 cụm)

| Cluster | Candidates included | Pattern chung | Ghi chú |
|---|---|---|---|
| **A: Tự động hóa trích xuất & xử lý dữ liệu văn phòng** | #10 (Khánh - Hóa đơn vào Excel), #12 (Huyền - Daily report), #5 (Cương - Check file nộp bài) | Đọc dữ liệu đầu vào không cấu trúc/bán cấu trúc và trích xuất thành biểu mẫu chuẩn hóa (Excel/Markdown/Report). | Khả thi cao nhất, quy trình nghiệp vụ rõ ràng, dễ đo lường trước và sau khi áp dụng. |
| **B: Tìm kiếm, truy vấn & tổng hợp tri thức** | #2 (Tùng - Paper AI), #7 (Hiệp - Tài liệu BA), #8 (Hiệp - Quyết định chat cũ) | Người dùng bơi trong biển thông tin phân tán, mất thời gian đọc lọc để tìm đúng insight. | Scope quá rộng, dữ liệu phân tán nhiều nguồn bảo mật, khó đo lường độ chính xác (Ground truth mơ hồ). |
| **C: Hỗ trợ kỹ thuật chuyên sâu (Engineering Assistant)** | #1 (Tùng - Debug code AI), #11 (Khánh - Layout tủ điện CAD) | Giải quyết các bài toán kỹ thuật phức tạp đòi hỏi logic suy luận và kiến thức chuyên ngành. | Giá trị cao nhưng phụ thuộc lớn vào domain hẹp hoặc đã có các tool lớn trên thị trường giải quyết tốt. |
| **D: Quản lý công việc & thời gian cá nhân** | #3 (Tùng - Bài tập gia sư), #4 (Cương - Theo dõi deadline), #6 (Cương - Chia task học), #9 (Hiệp - Sắp xếp lịch) | Cải thiện hiệu suất cá nhân và ghi nhớ lịch trình. | Thiên về thói quen và quy trình cá nhân (Process fix), dùng Rule/Template sẵn có hiệu quả hơn AI. |

### 3.3. Shortlist (giữ 2-3 bài trả lời được 7 câu hỏi worksheet)

| Candidate | Vì sao vào shortlist (2-3 ý) | Rủi ro / điều chưa rõ |
|---|---|---|
| **1. Trích xuất hóa đơn tự động điền Excel cho kế toán (Khánh)** | - Workflow 6 bước cực chuẩn, lặp lại hằng ngày.<br>- Bottleneck định lượng bằng phút (mất 3-4h/ngày) và tỷ lệ lỗi (5-7%).<br>- Dễ dàng xác định ranh giới can thiệp của AI và Rule kiểm tra. | Hóa đơn ảnh chụp nghiêng, cháy sáng hoặc hóa đơn nhiều dòng hàng hóa thì độ chính xác OCR/LLM có đảm bảo không. |
| **2. Bóc tách BOM và layout tủ điện CAD từ sơ đồ nguyên lý (Khánh)** | - Nỗi đau rất lớn của kỹ sư cơ điện (4-6h/bản vẽ).<br>- Tác động kinh tế cao trong sản xuất công nghiệp.<br>- Có sẵn domain expert trong nhóm để đối chiếu. | Kiến thức điện quá sâu, các thành viên khác không hiểu để cùng tham gia research; giải thuật xếp hình CAD vượt quá phạm vi lab 4 tiếng. |
| **3. Tổng hợp và tìm lại quyết định dự án từ các kênh chat/Notion (Hiệp)** | - Nhiều người trong nhóm cùng gặp phải trong công việc hằng ngày.<br>- Tiết kiệm 15-30 phút mỗi khi cần tìm context cũ. | Rào cản quyền truy cập dữ liệu nội bộ (Privacy); khó định nghĩa thế nào là "tổng hợp đủ và đúng ngữ cảnh". |

### 3.4. Score để đồng thuận (chấm 1-5, ép nói rõ vì sao cho 5 / cho 3)

| Candidate | Actor rõ | Workflow rõ | Pain có evidence | Impact đo được | Làm trong lab | So sánh R/W/A được | Nhóm hiểu domain | Tổng |
|---|---:|---:|---:|---:|---:|---:|---:|---:|
| **Hóa đơn vào Excel (Khánh)** | 5 | 5 | 5 | 5 | 5 | 4 | 4 | **33/35** |
| **Layout tủ điện CAD (Khánh)** | 5 | 4 | 4 | 4 | 2 | 4 | 2 | **25/35** |
| **Tìm lại quyết định chat cũ (Hiệp)** | 4 | 3 | 4 | 3 | 3 | 3 | 4 | **24/35** |

*Giải thích chấm điểm:*
- **Hóa đơn vào Excel**: Được điểm tuyệt đối 5 ở hầu hết tiêu chí vì Actor (kế toán viên), Workflow (nhận file -> đọc -> gõ -> kiểm tra -> lưu), Pain có số liệu cụ thể (3-4h/ngày, 60-80 hóa đơn), có thể làm demo pilot ngay trong lab bằng Python script + API LLM Vision. Nhóm hiểu domain ở mức 4 vì ai cũng hiểu hóa đơn mua hàng và file Excel.
- **Layout tủ điện CAD**: Bị điểm 2 ở "Làm trong lab" và "Nhóm hiểu domain" vì bài toán quá nặng về kỹ thuật điện và phần mềm CAD chuyên dụng.
- **Tìm quyết định chat cũ**: Bị điểm 3 ở Workflow và Impact vì luồng trao đổi trong chat rất phi tuyến tính và khó đo lường độ chuẩn xác của kết quả tìm kiếm.

**Candidate nhóm chọn (1 bài duy nhất):**

```text
Tự động hóa việc trích xuất thông tin từ hóa đơn VAT (ảnh/PDF) và kiểm tra đối soát toán học để điền tự động vào bảng kê chi phí Excel cho nhân viên kế toán.
```

**Vì sao chọn (4-5 câu):**

```text
Nhóm chọn bài toán này vì nó đáp ứng trọn vẹn và xuất sắc cả 7 tiêu chí đánh giá của lab. Bài toán có người chịu nỗi đau rõ ràng (nhân viên kế toán) với quy trình làm việc lặp đi lặp lại hằng ngày và tiêu tốn lượng thời gian khổng lồ (3-4 giờ/ngày). Điểm nghẽn nằm chính xác ở khâu đọc mắt và gõ tay vào từng ô Excel, dẫn đến tỷ lệ gõ nhầm 5-7% gây tốn thêm hàng giờ rà soát cuối tuần. Đây là bài toán mẫu mực để chứng minh sức mạnh của giải pháp Workflow kết hợp giữa khả năng đọc hiểu thị giác của AI và tính chính xác tuyệt đối của Rule-based kiểm tra số học. Cả nhóm đều có thể tham gia đóng góp từ khâu chuẩn hóa schema, viết rule kiểm tra đến việc kiểm thử pilot thực tế.
```

**Vì sao KHÔNG chọn các candidate còn lại (mỗi bài 2-3 câu):**

```text
- Bóc tách BOM và layout tủ điện CAD: Nhóm không chọn vì bài toán mang tính chuyên môn kỹ thuật điện quá sâu, các thành viên khác không có nền tảng cơ điện để thẩm định chất lượng bản vẽ; đồng thời việc tích hợp với AutoCAD/DXF vượt quá thời lượng thực hành của buổi lab.
- Tìm lại quyết định từ chat cũ: Nhóm không chọn vì phạm vi quá mơ hồ (dữ liệu nằm rải rác trên Zalo, Slack, Notion cá nhân với nhiều vấn đề bảo mật); tiêu chí đánh giá kết quả mang tính chủ quan cao và rất khó xây dựng tập ground truth để đo lường định lượng.
```

**Disagreement (nếu có — ai lo gì, chốt ra sao):**

```text
Ban đầu, Tùng và Hiệp đặt câu hỏi nghi vấn: "Bài toán xử lý hóa đơn đã có nhiều bên làm và có thể giải quyết thuần túy bằng code bóc tách PDF (Rule/Regex) được không, có cần dùng AI không?". Khánh và Huyền phản biện bằng thực tế dữ liệu: phần lớn hóa đơn chi phí phát sinh thực tế là ảnh chụp từ điện thoại (hóa đơn tiếp khách, mua sắm lẻ) bị nghiêng, mờ hoặc các file scan không có text layer, regex hoàn toàn bất lực. Tuy nhiên, nếu dùng Agent tự hành thì lại bị "over-engineering" vì quy trình đi thẳng một chiều. Nhóm chốt lại: Sử dụng mô hình Workflow (AI Vision trích xuất dữ liệu thô -> Rule Python kiểm tra chéo số tiền -> Kế toán kiểm duyệt trên Excel) là giải pháp cân bằng, tối ưu và an toàn nhất.
```

---

## Phase 4 — Quick Validation + Research

### 4.1. Quick validation (ít nhất 1 cách: interview 2-3 người hoặc survey 5-10 người)

| Nguồn | Số người / mẫu | Tín hiệu xác nhận (kèm quote nguyên văn) | Tín hiệu phản bác | Nhóm sửa problem thế nào |
|---|---:|---|---|---|
| **Interview** | 2 kế toán viên (1 kế toán SME, 1 kế toán dịch vụ) | - *"Ngán nhất là đợt quyết toán hoặc cuối tháng, cả xấp hóa đơn photo mờ tịt, ngồi căng mắt gõ từng số hóa đơn với mã số thuế vào Excel, chỉ sợ gõ nhầm số 0 là lệch cả bảng cân đối."* (Chị Mai, KT dịch vụ)<br>- *"Hóa đơn điện tử PDF thì còn copy-paste được, chứ ảnh hóa đơn ăn uống tiếp khách sếp chụp gửi qua Zalo thì bắt buộc phải nhìn rồi gõ tay 100%."* (Chị Lan, KT nội bộ) | Cả hai chị đều nhấn mạnh: *"Không bao giờ để phần mềm tự động lưu thẳng vào sổ kế toán chính thức mà không cho người xem lại, vì sai một ly là bị phạt thuế ngay."* | Nhóm xác định rõ ràng ranh giới: AI chỉ làm nhiệm vụ **điền nháp vào file Excel và cảnh báo ô nghi ngờ**, quyết định bấm lưu/duyệt cuối cùng bắt buộc là con người (Human-in-the-loop). |
| **Survey / poll** | 12 người làm kế toán & hành chính trên nhóm Zalo nghiệp vụ | 10/12 người xác nhận mất từ **2-4 giờ/ngày** cho việc nhập và đối soát hóa đơn chi phí.<br>11/12 người chọn tính năng mong muốn nhất là **tự động kiểm tra Tiền hàng + Tiền thuế = Tổng tiền thanh toán** ngay khi trích xuất. | 3 người lo ngại về vấn đề lộ thông tin hóa đơn mật của doanh nghiệp khi tải ảnh lên các mô hình AI đám mây công cộng. | Nhóm bổ sung yêu cầu bảo mật: cho phép che mờ thông tin nhạy cảm hoặc định hướng triển khai các mô hình mã nguồn mở chạy local/private API trong tương lai. |
| **Log / dữ liệu thật** | 50 file hóa đơn mẫu thực tế (35 PDF điện tử, 15 ảnh chụp điện thoại) | 8/15 ảnh chụp điện thoại bị góc chụp nghiêng 15-30 độ, bóng mờ góc hoặc độ phân giải thấp, OCR thông thường (Tesseract) bỏ sót hoặc đọc sai ký tự. | Hóa đơn PDF điện tử dạng vector đã có sẵn text layer chuẩn, nếu gọi mô hình AI thị giác đắt tiền cho toàn bộ tệp này thì gây lãng phí chi phí API. | Nhóm điều chỉnh kiến trúc: Dùng Rule kiểm tra xem file có text layer sẵn không; nếu có thì bóc text trực tiếp, chỉ gọi AI Vision cho file scan/ảnh chụp. |

**Insight sau validation (1-2 câu — pain thật nằm ở đâu):**

```text
Nỗi đau lớn nhất của kế toán không nằm ở việc tạo file Excel mà nằm ở sự căng thẳng khi phải đọc các ảnh hóa đơn chất lượng kém và nỗi sợ gõ sai số tiền/mã số thuế; đồng thời họ tuyệt đối không chấp nhận một hệ thống "hộp đen" tự động hóa 100% mà thiếu quyền kiểm soát phê duyệt cuối cùng.
```

Bằng chứng đính kèm (nếu có): `02-group-problem-statement-interview-notes.md`

### 4.2. Research giải pháp đã có (ít nhất 2-3 tools/patterns + 1-2 link kiểm được)

| Nguồn / tool / case | Link | Họ giải quyết bước nào? | Điểm mạnh | Khoảng trống / rủi ro | Bài học cho nhóm |
|---|---|---|---|---|---|
| **ABBYY FineReader PDF** | [pdf.abbyy.com](https://pdf.abbyy.com) | Bước 3: OCR nhận diện chữ và bảng biểu từ ảnh scan/PDF | Động cơ OCR quang học cực kỳ mạnh mẽ, nhận diện ký tự tiếng Việt có dấu với độ chính xác cao. | Chi phí bản quyền rất đắt (hàng trăm USD/user); không có khả năng hiểu ngữ nghĩa để tự map dữ liệu vào các cột Excel theo nghiệp vụ riêng của từng công ty. | Không nên tự xây dựng mô hình OCR từ đầu; cần lớp hiểu ngữ nghĩa (semantic understanding) để map đúng cột nghiệp vụ. |
| **AWS Textract Invoice & Expense** | [aws.amazon.com/textract](https://aws.amazon.com/textract/) | Bước 3 & 4: Trích xuất các trường key-value hóa đơn định dạng sẵn | Nhận diện tự động Vendor Name, Invoice Date, Total Amount qua API đám mây nhanh chóng. | Tối ưu cho mẫu hóa đơn chuẩn US/EU; dễ nhầm lẫn các mẫu hóa đơn đặc thù Việt Nam (thuế suất 8%, thuế suất 10%, mã cơ quan thuế cấp); chi phí tính trên trang. | Cần thiết kế prompt và schema JSON chặt chẽ phù hợp với quy chuẩn hóa đơn Bộ Tài chính Việt Nam. |
| **FPT.AI / Bizzi Invoice** | [fpt.ai/vi/vision](https://fpt.ai/vi/vision) | Toàn bộ quy trình từ tải hóa đơn đến đồng bộ phần mềm kế toán | Tối ưu riêng cho thị trường Việt Nam, kiểm tra được mã tra cứu trên trang Thuế của Tổng cục Thuế. | Đóng kín trong phần mềm quản lý chi phí của họ; kế toán các doanh nghiệp nhỏ chỉ muốn xuất ra file Excel nội bộ thì không linh hoạt và chi phí duy trì cao. | Nhóm tập trung vào giải pháp gọn nhẹ, cắm thẳng vào file Excel quen thuộc của người dùng, không bắt họ đổi phần mềm. |

**Research takeaway (2-3 câu — nên build gì / không build gì):**

```text
Nhóm KHÔNG tự huấn luyện mô hình OCR riêng từ đầu hoặc cố gắng xây dựng cả một phần mềm kế toán cồng kềnh. Nhóm NÊN xây dựng một pipeline Workflow tinh gọn: tận dụng các mô hình Vision-Language (VLM) đa năng có sẵn để trích xuất JSON theo schema định nghĩa trước, sau đó dùng Python script độc lập áp dụng các quy tắc toán học (Rule Validation) để kiểm tra tính toàn vẹn dữ liệu trước khi xuất ra bảng tính Excel cho kế toán duyệt.
```

---

## Phase 5 — Workflow + Problem Statement

### 5.1. Current workflow bản nhóm

Dán workflow hoặc link file: `02-group-problem-statement-workflow.md`

```text
[1. Nhận file, thông tin & ảnh liên quan từ nhóm Zalo: 15' - Kế toán] → [2. Mở song song màn hình: 5' - Kế toán] → [3. Đọc trích xuất thông tin bằng mắt: 60' - Kế toán] → [4. Ghi từng ô vào Excel: 100' - Kế toán (BOTTLENECK)] → [5. Kiểm tra hay sửa đổi phù hợp: 30' - Kế toán] → [6. Lưu file & lưu trữ chứng từ: 10' - Kế toán]
```

| Bước | Actor | Input | Output | Thời gian / tần suất | Ghi chú (handoff? bottleneck?) |
|---|---|---|---|---|---|
| **1. Nhận file, thông tin, ảnh từ Zalo** | Kế toán viên | Tin nhắn trong các nhóm Zalo phòng ban chứa file PDF, ảnh chụp bill/hóa đơn kèm thông tin giải trình chi tiêu | Tập hợp file ảnh/PDF chứng từ và thông tin bối cảnh chi phí | 15 phút / ngày | Handoff từ nhân viên các phòng ban gửi chi phí về nhóm Zalo |
| **2. Chuẩn bị nhập liệu** | Kế toán viên | Thư mục file/ảnh Zalo + File Excel bảng kê | Giao diện chia đôi màn hình (nửa Zalo/ảnh HĐ, nửa Excel) | 5 phút / ngày | Thao tác thủ công chuẩn bị không gian làm việc |
| **3. Đọc trích xuất thông tin bằng mắt** | Kế toán viên | Từng ảnh chụp hóa đơn, file PDF và tin nhắn text trên Zalo | Ghi nhớ & trích xuất: MST, Tên người bán, Ngày, Tiền hàng, Thuế, Tổng tiền, Nội dung chi | 60 phút / batch 60 HĐ (1 phút/HĐ) | Căng mắt đọc trích xuất khi gặp ảnh chụp điện thoại bị mờ, nghiêng, lóa sáng |
| **4. Ghi từng ô vào Excel** | Kế toán viên | Thông tin vừa đọc trích xuất | Các ô dữ liệu tương ứng trên từng dòng của file Excel | 100 phút / batch 60 HĐ (~1.7 phút/HĐ) | **BOTTLENECK CHÍNH**: Thao tác ghi tay lặp lại đơn điệu, dễ gõ nhầm số 0, dấu chấm/phẩy |
| **5. Kiểm tra hay sửa đổi phù hợp** | Kế toán viên | Dòng dữ liệu vừa ghi trên Excel + Chứng từ gốc | Dòng Excel đã được soát lỗi số học và chuẩn hóa diễn giải chi phí | 30 phút / batch | Bấm máy tính cộng lại tiền hàng + thuế; sửa đổi cho đúng mã chi phí nội bộ |
| **6. Lưu file & lưu trữ chứng từ** | Kế toán viên | File Excel hoàn tất + File chứng từ gốc | Bảng kê Excel đã lưu + thư mục chứng từ được đổi tên quản lý | 10 phút / batch | Thao tác quản lý file lưu trữ chứng từ |

**Bottleneck chính (2-3 câu):**

```text
Điểm nghẽn nghiêm trọng nhất nằm ở Bước 4 (ghi thủ công từng ô vào Excel) kết hợp với Bước 3 (căng mắt đọc trích xuất thông tin từ ảnh chụp hóa đơn mờ và đọc tin nhắn giải trình trên nhóm Zalo), chiếm hơn 70% tổng thời gian quy trình (160/220 phút). Thao tác chuyển đổi qua lại liên tục giữa cửa sổ Zalo/ảnh và bảng tính Excel gây mỏi mắt, giảm độ tập trung và trực tiếp dẫn đến tỷ lệ gõ nhầm số liệu 5-7%, buộc kế toán phải mất thêm 30 phút mỗi ngày ở Bước 5 để kiểm tra hay sửa đổi lại cho phù hợp.
```

### 5.2. Future workflow bản nhóm

Phải nhìn ra 5 thứ: bước nào máy (Rule), bước nào AI, bước nào người, boundary ở đâu, fallback khi AI sai.

```text
[1. Kéo thả file, thông tin, ảnh từ Zalo vào công cụ: 2' - Người] 
  → [2. AI Vision đọc hiểu ảnh & trích xuất JSON: 6' - AI] 
  → [3. Rule kiểm tra toán học & format MST: 2' - Máy (Rule)] 
  → [4. Script tự động ghi dữ liệu vào các ô Excel: 2' - Máy (Rule)] 
  → [5. Kế toán mở Excel kiểm tra hay sửa đổi các ô cảnh báo cho phù hợp: 23' - Người (HUMAN BOUNDARY)]

Fallback: Nếu file quá mờ AI không trích xuất được hoặc thông tin Zalo bị thiếu, hệ thống tự động đánh dấu màu cam trên dòng Excel đó, đính kèm link mở ảnh trực tiếp tại đúng dòng để kế toán gõ bù thủ công trong 10 giây.
```

**Before/after impact:**

| Metric | Trước | Sau kỳ vọng | Cách đo |
|---|---:|---:|---|
| **Tổng thời gian** | 220 phút (~3.7 giờ) cho 60 HĐ | 35 phút cho 60 HĐ (giảm **84%**) | Bấm giờ tổng quy trình từ khi nhận file đến khi có file Excel hoàn chỉnh |
| **Số bước** | 6 bước | 5 bước (trong đó 3 bước máy/AI tự chạy nền) | Đếm số bước trong quy trình chuẩn |
| **Số bước thủ công** | 6 bước thủ công 100% | 2 bước có con người can thiệp (Nạp file và Duyệt cuối) | Đếm các bước đòi hỏi thao tác người |
| **Bottleneck chính** | Bước 4 (Gõ tay từng ô Excel mất 100') | Bước 5 (Kế toán kiểm duyệt các dòng có cảnh báo mất 23') | So sánh thời gian ở bước tốn thời gian nhất |
| **Tỷ lệ sai lệch số học** | 5–7% lỗi do gõ nhầm | **0% lỗi số học lọt qua** (nhờ Rule kiểm tra Tiền hàng + Thuế = Tổng tiền) | Đếm số lượng ô số tiền bị lệch sau khi lưu sổ |
| **Risk mới** | Không có (chỉ mệt và sai tay) | AI ảo giác trích xuất sai tên hàng/số hóa đơn mà người duyệt lướt không nhìn thấy; lỗi bảo mật khi gửi dữ liệu lên cloud | Đo tỷ lệ lỗi ngữ nghĩa sót lại sau review và kiểm tra tuân thủ chính sách bảo mật dữ liệu |

### 5.3. Problem Statement v0 (mỗi field 2-3 câu)

| Field | Nội dung |
|---|---|
| **Actor** | Nhân viên kế toán nội bộ tại các doanh nghiệp vừa và nhỏ, phụ trách việc tiếp nhận hóa đơn chứng từ mua vào và lập bảng kê theo dõi chi phí định kỳ. |
| **Workflow** | Nhận file, thông tin ghi chú và ảnh hóa đơn liên quan từ các nhóm Zalo phòng ban hằng ngày -> Đọc trích xuất thông tin bằng mắt từ ảnh chứng từ và tin nhắn Zalo -> Ghi thủ công từng trường vào từng ô trên file Excel bảng kê -> Kiểm tra tính hợp lệ số học và sửa đổi thông tin cho phù hợp quy chuẩn nội bộ -> Lưu file và lưu trữ chứng từ. |
| **Bottleneck** | Thao tác gõ thủ công từng trường dữ liệu (Số HĐ, MST, Ngày, Tiền hàng, Tiền thuế) từ ảnh/PDF vào từng ô Excel diễn ra đơn điệu, mất nhiều thời gian và gây mệt mỏi thị giác, dẫn đến tỷ lệ nhập sai sót cao. |
| **Impact** | Tiêu tốn 3–4 giờ mỗi ngày của một nhân viên kế toán (tương đương 40-50% tổng quỹ thời gian làm việc); tỷ lệ gõ nhầm số liệu 5–7% gây nguy cơ sai lệch báo cáo thuế và mất thêm hàng giờ đối soát sửa sai vào cuối mỗi kỳ báo cáo. |
| **Success Metric** | Giảm thời gian xử lý một batch 60 hóa đơn từ 220 phút xuống dưới 40 phút; triệt tiêu 100% lỗi sai lệch số học về tiền; tỷ lệ các trường thông tin kế toán phải chỉnh sửa lại bằng tay dưới 3%. |
| **Boundary** | **LÀM**: Tự động đọc và trích xuất các trường thông tin chính từ hóa đơn PDF/ảnh, kiểm tra đối soát toán học, ghi vào mẫu Excel bảng kê và highlight các dòng nghi ngờ.<br>**KHÔNG LÀM**: Không tự động ký duyệt chi trả tiền, không tự động đồng bộ trực tiếp vào cơ sở dữ liệu phần mềm kế toán chính thức nếu chưa có người bấm xác nhận. |

**Câu hỏi AI phản biện v0 (nếu có):**
- *Field nào mơ hồ:* AI chỉ ra rằng phần Success Metric nói "giảm thời gian xuống dưới 40 phút" nhưng chưa nói rõ nếu gặp hóa đơn quá mờ thì thời gian sửa tay có làm vỡ mốc 40 phút không; phần Boundary chưa nói rõ có xử lý hóa đơn nhiều trang hoặc hóa đơn nước ngoài không.
- *Tôi sửa gì:* Nhóm đã bổ sung điều kiện ranh giới: Giới hạn phạm vi ở hóa đơn VAT chuẩn Việt Nam (tối đa 3 trang); bổ sung quy định tính toán metric dựa trên giả định tỷ lệ hóa đơn chất lượng kém dưới 15% tổng batch.

---

## Phase 6 — Rule / Workflow / Agent + Decision

### 6.0. Ma trận độ phù hợp (suy nghĩ nhanh, không thay quyết định cuối)

- Độ mơ hồ: **[x] Thấp (có đúng/sai rõ)** / [ ] Cao — *Vì sao:* Dữ liệu hóa đơn có tính đúng sai tuyệt đối về mặt pháp lý và toán học: Mã số thuế phải đúng từng ký tự số, Tổng thanh toán bắt buộc phải bằng Tiền hàng cộng Tiền thuế (trong dung sai làm tròn 1 đồng).
- Độ phức tạp: [ ] Thấp (1-2 bước) / **[x] Cao (3+ bước/nguồn, phụ thuộc nhau)** — *Vì sao:* Quy trình gồm nhiều bước liên hoàn: tiền xử lý định dạng file (ảnh/PDF) -> trích xuất OCR ngữ nghĩa -> kiểm tra hợp lệ cấu trúc dữ liệu JSON -> áp dụng công thức kiểm toán -> ghi đè vào đúng template Excel.

**Bài toán nhóm nằm ở ô nào:**

```text
Ô: ĐỘ MƠ HỒ THẤP — ĐỘ PHỨC TẠP TRUNG BÌNH/CAO
```

**Vì sao (2-3 câu):**

```text
Bài toán có tiêu chuẩn đầu ra cực kỳ khắt khe và rõ ràng (không chấp nhận câu trả lời mở hay sáng tạo tùy ý), nhưng quy trình xử lý lại gồm nhiều mắt xích nối tiếp từ xử lý thị giác đến tính toán số học. Vùng đặc tính này đòi hỏi một kiến trúc phân định rõ: dùng trí tuệ nhân tạo ở khâu bóc tách linh hoạt nhưng phải dùng quy tắc cứng (Rule) để chốt chặn tính chính xác.
```

### 6.1. So sánh Rule / Workflow / Agent (so trên cùng 1 bài)

| Mức | Phương án cho bài toán nhóm | Khi nào đủ | Rủi ro | Chọn? (Dùng cho bước nào?) |
|---|---|---|---|---|
| **Rule** | Viết script Python dùng thư viện PDF (pdfplumber/pypdf) bóc tách văn bản kết hợp Regular Expression (Regex) để tìm MST, Ngày, Số tiền; dùng script mở và ghi Excel. | Đủ khi 100% hóa đơn là file PDF điện tử chuẩn vector phát hành từ các nhà cung cấp quen thuộc (VNPT, Viettel, MISA) có cấu trúc text cố định. | **Gãy hoàn toàn** khi gặp ảnh chụp từ điện thoại, file scan không có text layer, hoặc các mẫu hóa đơn mới có bố cục lạ; tốn cực nhiều công bảo trì bộ regex. | **CHỌN MỘT PHẦN**: Dùng Rule làm lớp kiểm tra toán học (Validation) và lớp ghi dữ liệu vào file Excel sau khi đã trích xuất. |
| **Workflow** | Pipeline tuần tự: File đầu vào -> Module phân loại file -> Module VLM/Document AI trích xuất Schema JSON -> Module Rule kiểm tra số học và format -> Xuất file Excel -> Giao diện Kế toán kiểm duyệt. | Đủ cho hầu hết mọi loại hóa đơn (cả PDF lẫn ảnh chụp thực tế), luồng đi thẳng một chiều có cấu trúc rõ ràng, con người làm chốt chặn cuối cùng. | Chi phí gọi API mô hình thị giác; nguy cơ mô hình đọc nhầm ký tự ở ảnh quá mờ nếu không có bước kiểm duyệt của con người. | **CHỌN TOÀN DIỆN**: Đây là kiến trúc tối ưu nhất cho bài toán của nhóm. |
| **Agent** | Xây dựng Agent tự hành có ReAct loop: Tự động quan sát thư mục email/Zalo, tự quyết định gọi công cụ OCR nào, tự gọi web Tổng cục Thuế để tra cứu MST, tự phân tích lỗi và tự điều chỉnh prompt. | Cần thiết khi bài toán có độ phân nhánh cực kỳ phức tạp, không xác định trước được nguồn nhận hóa đơn và cần tự động đàm phán giải quyết sai sót với bên bán. | **Over-engineering**: Chi phí cao gấp nhiều lần, thời gian phản hồi chậm, Agent có thể chạy vòng lặp vô tận (loop), khó kiểm soát và không đoán định được hành vi trong môi trường tài chính nghiêm ngặt. | **KHÔNG CHỌN**: Quy trình nghiệp vụ cố định không cần tính tự chủ (autonomy) của Agent. |

**5 câu hỏi chốt (trả lời câu đầy đủ):**
1. *Rule có giải được 70-80% case không?* **Không**, vì trong thực tế có hơn 30% hóa đơn chi phí là ảnh chụp hóa đơn giấy hoặc bản scan chất lượng kém không có text layer chuẩn; Rule chỉ giải quyết tốt bước kiểm tra số học sau khi đã có text.
2. *Các bước có đi thẳng một đường không hay phải rẽ nhánh?* **Đi thẳng một đường tuần tự** (Nạp file -> Trích xuất -> Validate toán học -> Đổ Excel -> Người duyệt), chỉ có một nhánh rẽ đơn giản ở mức Rule (nếu lệch tiền thì highlight đỏ, nếu đúng thì để trắng).
3. *Có thật sự cần Agent tự lập kế hoạch + gọi tool không?* **Tuyệt đối không cần**, vì thứ tự các bước đã được xác định trước 100% theo quy chuẩn kế toán, không cần AI phải suy nghĩ xem bước tiếp theo nên làm gì.
4. *Nếu AI sai, ai phát hiện đầu tiên và sửa trong bao lâu?* **Kế toán viên phát hiện đầu tiên** thông qua các ô được tô màu cảnh báo trên file Excel và có thể bấm vào link xem ảnh hóa đơn để sửa lại chỉ trong vòng 5-10 giây.
5. *Có hạ được từ Agent → Workflow → Rule không?* **Hạ được hoàn toàn về mức Workflow kết hợp Rule**; kiến trúc này vừa loại bỏ độ trễ và chi phí đắt đỏ của Agent, vừa vượt trội hơn hẳn Rule đơn thuần về khả năng xử lý ảnh thực tế.

**Mức chọn:**

```text
WORKFLOW (Tích hợp AI Vision trích xuất ngữ nghĩa + Rule-based kiểm tra số học & xuất Excel + Human-in-the-loop phê duyệt)
```

**Vì sao chọn (3-4 câu):**

```text
Mức Workflow là điểm giao thoa hoàn hảo giữa tính linh hoạt của AI và sự chuẩn xác tuyệt đối của Rule. AI giải quyết khâu "khó nhất với code truyền thống" là đọc hiểu dữ liệu không cấu trúc từ ảnh chụp và hóa đơn đa dạng mẫu mã. Rule đảm nhận khâu "không được phép sai" là cộng trừ số học và kiểm tra định dạng mã số thuế. Con người giữ vai trò là "chốt chặn an toàn cuối cùng" để chịu trách nhiệm pháp lý, giúp hệ thống vận hành mượt mà, tin cậy và tiết kiệm chi phí tối đa.
```

**Vì sao không chọn mức đơn giản hơn (2-3 câu):**

```text
Nhóm không chọn phương án Rule thuần túy vì quy tắc lập trình truyền thống (như Regex/PDF parser) hoàn toàn bất lực trước dữ liệu thực tế từ ảnh chụp điện thoại bị nghiêng, mờ hoặc các hóa đơn có bảng biểu phức tạp. Nếu chỉ dùng Rule, kế toán vẫn phải ngồi gõ tay cho hơn 30-40% số hóa đơn đầu vào, khiến hệ thống không đạt được mục tiêu giải phóng sức lao động.
```

### 6.2. Problem Statement v1 (v0 sửa chặt hơn + 3 field cuối)

| Field | Nội dung |
|---|---|
| **Actor** | Nhân viên kế toán nội bộ phụ trách theo dõi chi phí mua vào tại các doanh nghiệp vừa và nhỏ, có kỹ năng thao tác thành thạo trên Microsoft Excel nhưng thường xuyên bị quá tải trong khâu nhập liệu chứng từ. |
| **Workflow** | Nhận file, thông tin và ảnh liên quan từ nhóm Zalo hằng ngày -> Kéo thả vào công cụ -> AI Vision đọc hiểu và bóc tách dữ liệu JSON -> Rule kiểm tra số học và tự động ghi vào từng ô trên file Excel bảng kê -> Kế toán mở Excel kiểm tra hay sửa đổi các ô cảnh báo cho phù hợp -> Lưu bảng kê chính thức. |
| **Bottleneck** | Khâu căng mắt đọc thông tin từ các ảnh chụp hóa đơn chất lượng kém và thao tác gõ tay lặp đi lặp lại từng trường dữ liệu vào từng ô Excel (chiếm 160/220 phút mỗi ngày), gây mệt mỏi và sai sót số liệu 5-7%. |
| **Impact** | Tốn 3–4 giờ/ngày làm việc của kế toán viên; gây nguy cơ phạt chậm nộp và sai sót kê khai thuế GTGT; tốn thêm 1-2 giờ cuối tuần để đối soát tìm lỗi lệch tiền giữa bảng kê và chứng từ gốc. |
| **Success Metric** | - Giảm tổng thời gian xử lý 60 hóa đơn từ 220 phút xuống dưới 35 phút (đo bằng đồng hồ bấm giờ quy trình thực tế).<br>- Giữ tỷ lệ sai sót số học lọt qua bảng kê ở mức 0% (nhờ Rule kiểm tra Tiền hàng + Thuế = Tổng tiền).<br>- Tỷ lệ các ô dữ liệu AI trích xuất đúng ngay lần đầu đạt trên 95% trên tập dữ liệu kiểm thử. |
| **Boundary** (làm / không làm) | **LÀM**: Xử lý hóa đơn VAT hợp pháp của Việt Nam (dạng PDF hoặc ảnh chụp rõ nét chữ); trích xuất đủ 7 trường cốt lõi (Số HĐ, Ngày lập, MST người bán, Tên người bán, Tiền hàng, Thuế suất, Tổng tiền); kiểm tra toán học và đổ vào đúng template Excel chuẩn của công ty; đánh dấu đỏ các ô nghi ngờ.<br>**KHÔNG LÀM**: Không tự ý sửa số liệu gốc của hóa đơn nếu tổng tiền bị lệch; không tự động thanh toán hay chuyển khoản ngân hàng; không tự động nộp tờ khai lên Tổng cục Thuế mà không có chữ ký số của Kế toán trưởng. |
| **AI intervention point** | Can thiệp **SAU** khi nhận tệp file đầu vào (Bước 1) và **TRƯỚC** khâu kiểm tra số học & đổ dữ liệu ra Excel (Bước 3). AI chỉ đóng vai trò "máy trích xuất cấu trúc dữ liệu JSON từ hình ảnh". |
| **Mức chọn** | **Workflow** (kết hợp AI Vision + Rule Validation + Excel Automation); không chọn Agent vì luồng cố định một chiều; không chọn Rule thuần vì không xử lý được ảnh chụp. |
| **Rủi ro & người thật kiểm tra** | **Rủi ro lớn nhất**: AI bị ảo giác (hallucination) đọc nhầm các chữ số giống nhau (như số 3 và số 8, số 0 và số 6) hoặc kế toán viên chủ quan duyệt lướt mà không kiểm tra kỹ các cảnh báo.<br>**Người thật kiểm tra**: Kế toán viên chịu trách nhiệm kiểm tra trực quan 100% các ô bị highlight cảnh báo màu cam/đỏ trên Excel trước khi ấn lưu file bảng kê chính thức. |

### 6.3. Final decision

| Câu hỏi | Yes / Not Yet / No | Ghi chú (câu đầy đủ) |
|---|---|---|
| Actor + workflow rõ chưa? | **Yes** | Actor là kế toán viên nội bộ; workflow 5 bước tuần tự từ nhận file đến phê duyệt bảng kê Excel đã được chuẩn hóa chi tiết. |
| Baseline + metric đo được chưa? | **Yes** | Baseline rõ ràng: 220 phút/60 HĐ và 5-7% lỗi gõ nhầm; Target đo được: 35 phút/60 HĐ và 0% lỗi toán học lọt qua. |
| Data/input đủ dùng chưa? | **Yes** | Nhóm đã thu thập được bộ dữ liệu thực tế gồm 50 file hóa đơn (cả PDF điện tử lẫn ảnh chụp điện thoại các góc độ) để làm tập test. |
| AI sai, hậu quả chấp nhận được không? | **Yes** | Hậu quả hoàn toàn chấp nhận được vì dữ liệu mới chỉ dừng ở mức file Excel nháp; Rule sẽ chặn các lỗi sai lệch tiền và con người là chốt chặn duyệt cuối cùng. |
| Có người review/owner không? | **Yes** | Kế toán viên là người trực tiếp sở hữu quy trình và chịu trách nhiệm rà soát toàn bộ kết quả trước khi đưa vào sổ sách chính thức. |
| Có cách non-AI đơn giản hơn không? | **No** | Rule/Regex truyền thống không thể đọc được ảnh chụp nghiêng, mờ hoặc định dạng hóa đơn thay đổi liên tục giữa các doanh nghiệp. |

**Decision:**

```text
GO
```

**Lý do (3-4 câu dựa trên bằng chứng):**

```text
Quyết định GO được đưa ra vì bài toán hội tụ đầy đủ tất cả các điều kiện tiên quyết: có nỗi đau thực tế đã được kiểm chứng qua phỏng vấn và survey kế toán, workflow trước/sau rõ ràng, metric định lượng đo đếm được cụ thể và ranh giới rủi ro được cô lập an toàn. Giải pháp Workflow kết hợp AI trích xuất và Rule kiểm soát giải quyết đúng điểm nghẽn mà không gây lãng phí tài nguyên hay phức tạp hóa hệ thống như Agent. Toàn bộ hạ tầng công nghệ (Vision LLM API, Python openpyxl) đều đã sẵn sàng để nhóm triển khai kiểm thử ngay lập tức.
```

**Nếu Go — pilot nhỏ nhất (data nào, chạy tay ra sao, đo 3 số nào):**

```text
1. Dữ liệu pilot: Tập dữ liệu gồm 30 hóa đơn chi phí mua vào thực tế của tháng gần nhất (bao gồm 20 file PDF điện tử và 10 ảnh chụp hóa đơn ăn uống/mua lẻ qua điện thoại).
2. Quy trình chạy tay pilot: Chạy script Python gọi mô hình Vision trích xuất dữ liệu, chạy hàm Rule đối soát tổng tiền và sinh ra 1 file Excel bảng kê duy nhất; đưa file Excel này cho kế toán viên mở lên và bấm giờ duyệt từng dòng.
3. Đo 3 số cụ thể:
   - Số 1 (Thời gian): Tổng thời gian từ lúc nạp 30 file đến khi kế toán hoàn tất việc duyệt file Excel (kỳ vọng < 18 phút).
   - Số 2 (Field Accuracy): Tỷ lệ các trường thông tin (MST, Số HĐ, Tiền) được trích xuất đúng mà kế toán không cần sửa tay (kỳ vọng > 95%).
   - Số 3 (Tỷ lệ chặn lỗi toán học): 100% các trường hợp tổng tiền bị lệch hoặc sai thuế suất phải được hệ thống tô màu đỏ cảnh báo thành công.
```

**Nếu Not Yet — cần validate gì trước:**

```text
(Không áp dụng vì nhóm đã quyết định Go. Tuy nhiên nếu trong tương lai mở rộng sang hóa đơn quốc tế hoặc hóa đơn viết tay, nhóm sẽ chuyển trạng thái sang Not Yet để kiểm chứng lại độ chính xác của mô hình OCR đối với chữ viết tay trước khi triển khai).
```

**Nếu No-Go — làm gì thay AI:**

```text
(Không áp dụng vì nhóm đã chọn Go).
```

**Exit / rollback (khi nào dừng AI, quay về cách cũ):**

```text
Nhóm sẽ lập tức dừng giải pháp AI và rollback quay về quy trình nhập tay truyền thống nếu xảy ra một trong hai điều kiện sau:
1. Trong đợt pilot thử nghiệm, tỷ lệ các trường dữ liệu AI trích xuất sai vượt quá 15% (khiến kế toán mất nhiều thời gian ngồi sửa lỗi hơn cả thời gian tự gõ tay từ đầu).
2. Xảy ra sự cố bảo mật thông tin hoặc chi phí gọi API vượt quá ngưỡng ngân sách cho phép (>500 VNĐ/hóa đơn), khi đó sẽ quay về nhập tay kết hợp với việc dùng bộ template Excel có cài sẵn công thức kiểm tra chéo tự động.
```

---

### Self-check nộp phần 02 (nhóm)
- [x] Có nhật ký hội tụ 9-12 → 1 (cluster + shortlist + score với đầy đủ 12 candidates từ 5 thành viên)
- [x] Có validation (quote thật từ 2 kế toán viên) + research (link kiểm được từ ABBYY, AWS Textract, FPT.AI)
- [x] Có workflow trước/sau đủ thời gian, handoff, bottleneck, boundary, fallback chi tiết
- [x] Có PS v0 → v1, metric có trước/sau + cách đo, boundary có làm/không làm rõ ràng
- [x] Có so sánh Rule/Workflow/Agent + Decision Go với kế hoạch pilot 3 số đo đếm cụ thể
