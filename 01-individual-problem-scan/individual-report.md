# 01 — Individual Problem Scan

> Điền theo Phase 1 + Phase 2 trong `01-worksheet.md`. Tự scan trước, dùng AI sau để phản biện. Không copy ví dụ Weekly Report.

## Thông tin cá nhân

- Họ và tên: Trần Văn Khánh
- Mã học viên: 2413
- Vai trò / bối cảnh: Sinh viên năm 4 ngành Công nghệ Thông tin / AI Engineer thực tập tại dự án tự động hóa
- Công việc hằng tuần:
  - Thiết kế và tối ưu flow xử lý tài liệu, OCR và trích xuất dữ liệu hóa đơn/chứng từ để tự động điền vào bảng kê Excel cho bộ phận kế toán.
  - Nghiên cứu và xây dựng Agent hỗ trợ đọc sơ đồ nguyên lý 1 sợi (single-line diagram) để bóc tách vật tư và gợi ý layout tủ điện công nghiệp.
  - Viết prompt, thiết kế schema JSON và chạy benchmark/eval đánh giá chất lượng trích xuất của LLM trên các bộ dữ liệu thực tế.
  - Xử lý các ca lỗi dữ liệu đầu vào: ảnh scan mờ, format bảng biểu trong PDF bị gãy, viết script regex vá lỗi tạm thời.
  - Học tập các môn chuyên ngành trên trường, làm bài tập lớn/đồ án nhóm, phân chia task và review code cùng các bạn sinh viên.

---

## Phase 1 — Scan 5+ problems 

| # | Lăng kính (Lặp lại / Tốn thời gian / AI có thể tốt hơn / Pain từ người khác) | Problem quan sát được | Ai chịu ảnh hưởng? | Dấu hiệu thật (số + bằng chứng) |
|---|---|---|---|---|
| 1 | Tốn thời gian | Kế toán viên phải mở từng file hóa đơn VAT (ảnh chụp/scan điện thoại, file PDF) để gõ tay từng trường (Số HĐ, MST, Ngày, Tên người bán, Tiền hàng, Tiền thuế) vào file bảng kê chi phí Excel | Nhân viên kế toán nội bộ | Mất **3–4 giờ/ngày**, trung bình **60–80 hóa đơn/ngày**; tỷ lệ gõ nhầm mã số thuế hoặc tiền thuế ~**5-7%** phải đối soát lại cuối tuần |
| 2 | AI có thể tốt hơn | Phân loại hạng mục chi phí và gán cột mã chi phí trong file Excel theo dõi từ nội dung diễn giải sao kê ngân hàng (nội dung viết tắt, không dấu, lộn xộn) | Kế toán tổng hợp | Mất **2–3 giờ mỗi cuối tháng**; phải nhắn tin hỏi đi hỏi lại 10-15 người ở các phòng ban khác nhau để xác nhận nội dung chi |
| 3 | Tốn thời gian | Kỹ sư điện bóc tách bảng kê vật tư (BOM) và sắp xếp layout thiết bị (Aptomat, Relay, Contactor, Terminal) vào khung tủ điện từ sơ đồ nguyên lý 1 sợi (Single-line diagram) | Kỹ sư thiết kế tủ điện | Mất **4–6 giờ cho 1 bản vẽ tủ tiêu chuẩn**; khoảng **30% bản vẽ** bị xung đột kích thước ray hoặc thiếu chỗ chứa máng dây khi lắp ráp thật |
| 4 | Pain từ người khác | Khách hàng yêu cầu đổi nhãn hiệu thiết bị tủ điện ( từ Schneider sang LS/Mitsubishi), kỹ sư phải tra catalog từng hãng để lấy kích thước WxHxD và chỉnh lại toàn bộ file AutoCAD | Kỹ sư thiết kế tủ điện | Tốn **45–60 phút/lần đổi spec**; trung bình 1 dự án tủ điện bị yêu cầu đổi thiết bị **3–5 lần** trước khi chốt thi công |
| 5 | Lặp lại | AI Engineer phải ngồi kiểm tra bằng mắt (manual eval) từng test case output JSON của LLM sau mỗi lần tinh chỉnh system prompt hoặc đổi model | AI Engineer (bản thân) | Mất **1.5–2 giờ/lần đổi prompt**; phải soi từng trường trong tập 40–50 mẫu hóa đơn để xem có bị mất dữ liệu hay ảo giác không |
| 6 | Lặp lại | Viết các hàm regex và logic code xử lý ngoại lệ (post-processing) khi LLM/OCR trả về chuỗi JSON bị gãy ngoặc, nhầm lẫn số 0 với chữ O, dấu phẩy với dấu chấm | AI Engineer (bản thân) | Gặp **4–5 lần/tuần**; mỗi lần mất **30–45 phút** debug và vá code parser tạm bợ |
| 7 | AI có thể tốt hơn | Bóc tách cấu trúc bảng biểu (table extraction) nhiều cột từ tài liệu kỹ thuật / datasheet thiết bị điện dạng PDF | AI Engineer, Kỹ sư điện | Tool OCR thông thường (PaddleOCR/Tesseract) làm mất cấu trúc cột/hàng; dev phải ngồi căn tọa độ bounding box thủ công **1–2 giờ/tài liệu** |
| 8 | Lặp lại | Định dạng danh mục tài liệu tham khảo theo chuẩn IEEE/APA cho các bài báo cáo bài tập lớn, tiểu luận môn học | Sinh viên, Bạn cùng nhóm | Mất **60–90 phút mỗi báo cáo đồ án**; thường xuyên bị giảng viên nhắc nhở vì sai thứ tự tác giả, thiếu link DOI hoặc lệch font |
| 9 | Tốn thời gian | Review code và giải quyết merge conflict trong repo Git đồ án nhóm (3–4 sinh viên làm chung) do các bạn commit thẳng vào branch main, code không format chuẩn linter | Lead kỹ thuật nhóm đồ án (bản thân) | Mất **2–3 giờ mỗi cuối tuần** để ngồi dọn conflict và hướng dẫn các bạn format lại code |
| 10 | Pain từ người khác | Giảng viên hướng dẫn phản biện đồ án qua comment file PDF/Word với nhận xét chung chung ("Cần tối ưu thuật toán", "Dữ liệu chưa thuyết phục"), sinh viên không rõ phải sửa dòng code nào | Sinh viên trong nhóm | Mất **2–3 ngày** chờ phản hồi qua email hoặc phải đợi đến buổi thông qua đồ án trực tiếp để hỏi lại chi tiết |

> Gợi ý tự soi: tuần trước mất nhiều thời gian nhất vào việc gì? Việc gì hay trì hoãn? Người khác hay hỏi lại câu gì? Workflow nào ai cũng biết là chậm?

**AI đã dùng ở Phase 1 (nếu có):**
- Prompt đã hỏi: "Tôi là AI Engineer đang làm dự án nhập liệu hóa đơn vào Excel và agent vẽ tủ điện CAD, hãy chỉ ra các điểm nghẽn thực tế mà người làm quy trình này hay gặp phải ngoài khâu OCR thuần túy?"
- Ý dùng được: AI chỉ ra điểm nghẽn ở khâu đối soát và gõ vào các cột phân loại trong file Excel theo mẫu sẵn của kế toán, cũng như việc kỹ sư điện tốn thời gian tra cứu kích thước vật lý (WxHxD) khi đổi nhãn hiệu thiết bị.
- Ý bỏ vì không phải pain thật: AI gợi ý "Dùng AI tự động sinh báo cáo tài chính hoàn chỉnh cho kế toán". Ý này bị loại ngay vì quá rộng, viển vông, kế toán cần kiểm soát tính pháp lý từng dòng số liệu chứ không bao giờ để AI tự làm hết.

**Self-check Phase 1:**
- [x] Đủ 5+ dòng, mỗi dòng có actor + số đo cụ thể (10 dòng, có thời gian, tần suất, tỷ lệ lỗi cụ thể)
- [x] Dùng ít nhất 3/4 lăng kính (Đã dùng đủ cả 4 lăng kính: Lặp lại, Tốn thời gian, AI có thể tốt hơn, Pain từ người khác)
- [x] Không có dòng chung chung kiểu "mất nhiều thời gian" (Mọi dòng đều có số phút, số giờ, số lần rõ ràng)

---

## Phase 2 — Top 3 Problem Cards

### 2.1. Chọn top 3

Giữ bài nào: actor cụ thể, workflow vẽ được 3-7 bước, bottleneck ở 1 bước, impact đo được. Loại bài quá rộng.

| Rank | Problem (copy từ bảng scan) | Vì sao chọn (2-3 ý) | Điều còn chưa chắc |
|---|---|---|---|
| 1 | Kế toán viên phải mở từng file hóa đơn VAT để gõ tay từng trường dữ liệu vào file bảng kê chi phí Excel | 1. Workflow cực kỳ chuẩn hóa, lặp lại hằng ngày.<br>2. Bottleneck rõ ở khâu đọc ký tự mờ và gõ tay từng ô Excel.<br>3. Impact đo đếm được ngay bằng phút và tỷ lệ gõ nhầm. | Hóa đơn scan từ điện thoại bị mờ/nghiêng/cháy sáng thì OCR/LLM có nhận diện chính xác 100% các dòng chi tiết không. |
| 2 | Kỹ sư điện bóc tách BOM và sắp xếp layout thiết bị vào khung tủ điện từ sơ đồ nguyên lý 1 sợi | 1. Pain lớn của kỹ sư cơ điện, tốn nhiều thời gian (4-6h/tủ).<br>2. Ràng buộc vật lý rõ ràng (kích thước tủ, khoảng cách tản nhiệt).<br>3. Dự án thực tế đang có sẵn kỹ sư điện để kiểm chứng. | Quy chuẩn bố trí tủ điện của từng xưởng có khác nhau nhiều không, khó đóng gói thành rule tổng quát. |
| 3 | AI Engineer phải chạy eval thủ công bằng mắt để kiểm tra chất lượng output JSON của LLM sau mỗi lần tinh chỉnh prompt | 1. Pain trực tiếp của bản thân khi làm AI Engineer.<br>2. Tốn thời gian lặp lại vô ích (1.5-2h/lần đổi prompt).<br>3. Giải quyết được bài toán regressed error trong pipeline AI. | Chi phí gọi LLM-as-a-judge để tự động chấm điểm có bị cao quá không so với việc kiểm tra bằng rule. |

### 2.2. Problem Cards chi tiết (lặp lại cho cả 3 cards)

---

#### Problem Card #1 — Trích xuất hóa đơn tự động điền bảng kê Excel cho kế toán

```text
Problem 1 câu:
Nhân viên kế toán mất 3–4 giờ mỗi ngày để mở từng file hóa đơn scan/PDF và gõ tay từng trường thông tin vào file bảng kê Excel, dễ sai sót số tiền và mã số thuế.

Actor:
Nhân viên kế toán nội bộ phụ trách theo dõi chi phí mua vào.

Thời điểm / bối cảnh:
Mỗi buổi chiều hằng ngày khi nhận được tập file hóa đơn điện tử (PDF) và ảnh hóa đơn giấy do các phòng ban gửi về qua email/Zalo.

Current workflow 3-7 bước:
1. Nhận file, thông tin ghi chú kèm ảnh chụp hóa đơn/chứng từ liên quan từ các nhóm Zalo phòng ban (15').
2. Mở song song cửa sổ Zalo/ảnh chứng từ trên một nửa màn hình và file Excel bảng kê trên nửa màn hình còn lại (5').
3. Đọc trích xuất thông tin bằng mắt: vừa đọc ảnh hóa đơn (Số HĐ, MST, Tiền hàng, Thuế) vừa đọc thông tin ghi chú trên Zalo (mục đích chi, người thanh toán) (60').
4. Ghi thủ công từng trường dữ liệu vào các ô tương ứng trong file Excel bảng kê (100') <-- BOTTLENECK.
5. Kiểm tra tính hợp lệ (cộng tiền hàng + thuế có khớp tổng tiền không) và sửa đổi nội dung cho phù hợp quy chuẩn danh mục chi phí (30').
6. Lưu file Excel và đổi tên lưu trữ file ảnh/PDF chứng từ (10').

Bottleneck:
Bước 4 (ghi thủ công từng dòng dữ liệu từ ảnh/PDF vào từng ô Excel) kết hợp Bước 3 (căng mắt đọc trích xuất thông tin từ ảnh chụp mờ trên Zalo), chiếm hơn 70% thời gian, rất mỏi mắt và dễ gõ nhầm số liệu.

Impact:
Mất 3-4 giờ/ngày (~18-20 giờ/tuần), chiếm gần 50% thời gian làm việc của 1 kế toán viên; tỷ lệ nhập sai số liệu 5-7% dẫn tới việc phải tốn thêm 1-2 giờ cuối tuần để đối soát lại sổ sách.

Success metric:
- Baseline: Mất trung bình 3 phút/hóa đơn gõ tay vào Excel, tỷ lệ sai sót ~6%.
- Target: Giảm xuống dưới 30 giây/hóa đơn (chỉ còn bước review kết quả trích xuất trên Excel), tỷ lệ sai sót cần sửa dưới 2%.
- Đo lường: Bấm giờ xử lý 1 batch 50 hóa đơn và đếm số ô dữ liệu kế toán phải sửa lại trên Excel.

Non-AI alternative:
Dùng phần mềm OCR mã nguồn mở kết hợp Regex (Rule-based): Chỉ hoạt động tốt với hóa đơn điện tử chuẩn có text layer hoặc mẫu hóa đơn cố định. Khi gặp hóa đơn giấy chụp nghiêng, mờ, hoặc mẫu hóa đơn mới lạ, rule-based bị gãy hoàn toàn.

AI hypothesis:
Sử dụng Vision-Language Model / Document Understanding Model để trích xuất trực tiếp các trường dữ liệu theo Schema JSON định sẵn, sau đó dùng script Python tự động ghi vào các cột của file Excel; kế toán chỉ cần mở file Excel lên để duyệt (Human-in-the-loop).

Quick gut:
[ ] No AI / process fix
[ ] Rule
[x] Workflow (OCR/VLM trích xuất + Python script xuất Excel + Kế toán review)
[ ] Agent
[ ] Chưa biết
```

**Draft workflow Card #1** (ASCII):

```text
CURRENT STATE — 220 phút (~3.7 giờ) cho 60 hóa đơn

[1. Nhận file, info, ảnh từ nhóm Zalo: 15'] → [2. Mở song song màn hình: 5'] → [3. Đọc trích xuất thông tin bằng mắt: 60'] → [4. Ghi từng ô vào Excel: 100'] <-- BOTTLENECK → [5. Kiểm tra & sửa đổi phù hợp: 30'] → [6. Lưu file & chứng từ: 10']

FUTURE STATE — 35 phút cho 60 hóa đơn

[1. Kéo thả batch file vào folder: 2'] → [2. AI trích xuất JSON & Script tự điền Excel: 8' (chạy nền)] → [3. Kế toán mở Excel duyệt & chỉnh ô cảnh báo: 25'] <-- HUMAN BOUNDARY

Fallback: Nếu AI gặp file quá mờ không đọc được độ tin cậy thấp (<80%), hệ thống highlight màu đỏ ô Excel đó và mở popup ảnh hóa đơn tại đúng vị trí để kế toán gõ tay bổ sung.
```

File đính kèm (nếu vẽ riêng): `01-individual-problem-scan-workflow-card-1.png`

---

#### Problem Card #2 — Bóc tách BOM và layout sơ bộ thiết bị tủ điện từ sơ đồ nguyên lý

```text
Problem 1 câu:
Kỹ sư cơ điện mất 4–6 giờ để đọc sơ đồ nguyên lý 1 sợi, tra cứu kích thước từng linh kiện và sắp xếp thủ công vị trí trên bản vẽ CAD tủ điện, dễ dẫn đến xung đột không gian vật lý khi lắp ráp.

Actor:
Kỹ sư thiết kế tủ điện tại xưởng sản xuất hoặc công ty cơ điện.

Thời điểm / bối cảnh:
Khi nhận được bản vẽ sơ đồ nguyên lý điện (Single-line diagram) từ phòng thiết kế hệ thống và cần lên bản vẽ bố trí thiết bị (General Arrangement - GA) để xưởng gia công vỏ tủ và lắp ráp.

Current workflow 3-7 bước:
1. Đọc sơ đồ nguyên lý điện để hiểu danh sách thiết bị cần dùng (30').
2. Bóc tách thủ công danh mục thiết bị (BOM) gồm mã MCB, MCCB, Contactor, Relay ra sổ tay/Excel (60').
3. Tra cứu catalog các hãng (Schneider, LS, ABB) để lấy kích thước W x H x D của từng thiết bị (60') <-- BOTTLENECK 1.
4. Mở AutoCAD, vẽ khung tủ và các thanh ray DIN rail / máng cáp (30').
5. Sắp xếp thủ công từng block linh kiện lên ray, tính toán khoảng cách an toàn tản nhiệt và đi dây (120') <-- BOTTLENECK 2.
6. Kiểm tra lại tổng kích thước xem có bị tràn tủ hoặc kẹt máng dây không (30').

Bottleneck:
Bước 3 (tra cứu thông số kích thước catalog phân tán) và Bước 5 (sắp xếp vị trí thiết bị đảm bảo quy chuẩn khoảng cách và luồng dây điện trên AutoCAD).

Impact:
Tốn 4-6 giờ/tủ điện; khi khách hàng đổi hãng thiết bị phải làm lại từ bước 3; khoảng 30% bản vẽ khi đưa xuống xưởng bị thợ phản ánh là chật ray hoặc đụng nắp tủ, gây lãng phí vật tư và chậm tiến độ giao hàng.

Success metric:
- Baseline: Mất 300 phút để hoàn thành bản vẽ layout tủ điện cơ bản; tỷ lệ va chạm kích thước thực tế ~30%.
- Target: Giảm thời gian xuống còn 60 phút (AI hỗ trợ bóc BOM và sinh layout sơ bộ, kỹ sư chỉ tinh chỉnh); tỷ lệ va chạm kích thước giảm về 0%.
- Đo lường: Thời gian kỹ sư hoàn thành bản vẽ và biên bản nghiệm thu lắp ráp tại xưởng không có lỗi va chạm.

Non-AI alternative:
Sử dụng phần mềm chuyên dụng như EPLAN Pro Panel: Rất mạnh và chính xác nhưng chi phí bản quyền cực kỳ đắt đỏ (hàng chục nghìn USD), yêu cầu cấu hình máy cao và kỹ sư phải được đào tạo bài bản 3-6 tháng; các xưởng vừa và nhỏ tại VN đa số vẫn dùng AutoCAD 2D thông thường.

AI hypothesis:
Dùng Agent phân tích bản vẽ sơ đồ nguyên lý (PDF/DXF) -> trích xuất BOM -> gọi Tool tra cứu cơ sở dữ liệu kích thước thiết bị -> áp dụng thuật toán tối ưu xếp hình 2D (bin-packing có ràng buộc điện) để sinh layout DXF sơ bộ cho kỹ sư review.

Quick gut:
[ ] No AI / process fix
[ ] Rule
[ ] Workflow
[x] Agent (Cần phối hợp nhiều bước: đọc bản vẽ, tra cứu DB linh kiện, tính toán ràng buộc vật lý và xuất file DXF)
[ ] Chưa biết
```

**Draft workflow Card #2:**

```text
CURRENT STATE — 330 phút (~5.5 giờ)

[1. Đọc sơ đồ: 30'] → [2. Bóc BOM tay: 60'] → [3. Tra catalog WxHxD: 60'] <-- BOTTLENECK 1 → [4. Vẽ khung tủ: 30'] → [5. Xếp block linh kiện trên CAD: 120'] <-- BOTTLENECK 2 → [6. Kiểm tra va chạm: 30']

FUTURE STATE — 45 phút

[1. Tải sơ đồ nguyên lý vào hệ thống: 2'] → [2. Agent trích BOM + Tra DB kích thước: 3'] → [3. Tool sinh layout 2D tối ưu tự động: 5'] → [4. Kỹ sư mở file CAD review, chỉnh luồng dây & chốt bản vẽ: 35'] <-- HUMAN BOUNDARY

Fallback: Nếu sơ đồ nguyên lý có ký hiệu lạ mà Agent không nhận diện được, hệ thống giữ nguyên các linh kiện đã nhận biết và đánh dấu vùng chưa rõ để kỹ sư chọn mã thiết bị từ danh sách gợi ý.
```

File đính kèm: `01-individual-problem-scan-workflow-card-2.png`

---

#### Problem Card #3 — Tự động hóa đánh giá (Eval pipeline) chất lượng output JSON của LLM

```text
Problem 1 câu:
AI Engineer mất 1.5–2 giờ mỗi lần cập nhật prompt hoặc đổi mô hình để kiểm tra thủ công từng test case JSON, dễ bỏ sót các lỗi suy giảm chất lượng (regression bugs).

Actor:
AI Engineer (người phát triển ứng dụng LLM/Agent).

Thời điểm / bối cảnh:
Mỗi khi cần cải tiến prompt, thêm trường dữ liệu trích xuất mới, hoặc chuyển đổi giữa các model (VD: từ GPT-4o sang Claude hoặc Gemini Flash) trước khi deploy lên môi trường thử nghiệm.

Current workflow 3-7 bước:
1. Viết xong phiên bản prompt mới trong code hoặc giao diện test (10').
2. Chạy script gửi prompt với batch 40-50 file tài liệu mẫu (15').
3. Mở file kết quả JSON và mở file ground truth (dữ liệu chuẩn) (5').
4. Ngồi đọc bằng mắt đối chiếu từng trường (tên, số tiền, ngày tháng, danh sách dòng hàng) giữa output và nhãn chuẩn (70') <-- BOTTLENECK.
5. Ghi chép thủ công các ca bị sai vào file Excel/Notion để tìm nguyên nhân (20').

Bottleneck:
Bước 4 - Đọc bằng mắt từng trường JSON của 50 test cases (vừa tốn thời gian, vừa mỏi mắt, dễ bỏ qua các lỗi định dạng ngày tháng hoặc sai lệch số thập phân nhỏ).

Impact:
Làm chậm chu kỳ thử nghiệm (iteration cycle) của AI Engineer; mỗi ngày chỉ thử nghiệm được 1-2 phiên bản prompt; nguy cơ đẩy code có bug tiềm ẩn lên production vì không đủ thời gian soi hết mọi test case.

Success metric:
- Baseline: Mất 120 phút cho một lần eval bộ 50 test cases, thực hiện thủ công bằng mắt.
- Target: Giảm xuống dưới 10 phút (chạy script eval tự động tính F1-score/Exact Match, chỉ review các ca bị fail điểm).
- Đo lường: Bấm giờ từ lúc chạy test script đến khi nhận được bảng báo cáo lỗi chi tiết.

Non-AI alternative:
Viết bộ unit test bằng Python so sánh trực tiếp chuỗi hoặc dict matching (Exact Match / DeepDiff): Nhanh và miễn phí, nhưng quá cứng nhắc vì không xử lý được các trường hợp đồng nghĩa hoặc khác biệt nhỏ về định dạng khoảng trắng/dấu câu.

AI hypothesis:
Kết hợp Rule (cho các trường số liệu chính xác như mã số thuế, số tiền) và LLM-as-a-judge (cho các trường ngữ nghĩa như mô tả sản phẩm, lý do chi tiêu) để tự động chấm điểm và sinh báo cáo so sánh diff trực quan.

Quick gut:
[ ] No AI / process fix
[ ] Rule
[x] Workflow (Kết hợp Rule-based schema validation + LLM-as-a-judge cho semantic fields)
[ ] Agent
[ ] Chưa biết
```

**Draft workflow Card #3:**

```text
CURRENT STATE — 120 phút

[1. Sửa prompt: 10'] → [2. Chạy batch 50 mẫu: 15'] → [3. Mở file so sánh: 5'] → [4. Đọc mắt đối soát 50 file: 70'] <-- BOTTLENECK → [5. Ghi log lỗi vào file: 20']

FUTURE STATE — 15 phút

[1. Sửa prompt: 10'] → [2. Chạy pipeline Eval tự động (Rule + LLM Judge): 3'] → [3. AI Engineer đọc Dashboard tóm tắt ca fail & nguyên nhân: 2'] <-- HUMAN BOUNDARY

Fallback: Nếu LLM-as-a-judge cho điểm mâu thuẫn với Rule Exact Match, hệ thống ưu tiên kết quả kiểm tra định dạng của Rule và gắn cờ để dev kiểm tra lại tiêu chí đánh giá.
```

File đính kèm: `01-individual-problem-scan-workflow-card-3.png`

---

### 2.3. Card muốn pitch nhất (chuẩn bị 2 phút)

**Card tôi muốn pitch nhất:**

```text
Problem Card #1: Trích xuất hóa đơn tự động điền bảng kê Excel cho nhân viên kế toán.
```

**Vì sao (2-3 câu: workflow gì, số đo gì, impact gì):**

```text
Đây là bài toán có workflow nghiệp vụ cực kỳ rõ ràng và chuẩn hóa (6 bước từ nhận file, đọc mắt đến gõ tay vào từng cột Excel). Nỗi đau có số liệu chứng minh rất cụ thể: mất 3-4 giờ/ngày, chiếm gần 50% thời gian của kế toán viên với tỷ lệ gõ nhầm 5-7% gây tốn thêm hàng giờ kiểm tra chéo cuối tuần. Giải pháp mang lại ROI tức thì khi cắt giảm hơn 80% thời gian nhập liệu mà vẫn đảm bảo tính an toàn nhờ cơ chế Human-in-the-loop (kế toán chỉ duyệt và chỉnh sửa ô cảnh báo).
```

**Câu hỏi tôi muốn nhóm challenge (1-2 câu hỏi đúng chỗ yếu):**

```text
1. Với các hóa đơn giấy chụp qua điện thoại bị nghiêng, bóng mờ hoặc nhàu nát, nếu AI đọc sai số tiền mà kế toán nhìn lướt qua không phát hiện thì cơ chế kiểm soát rủi ro (validation rule) nào sẽ ngăn chặn lỗi trước khi lưu vào sổ sách?
2. Bài toán này chỉ cần dùng Workflow kết hợp OCR/VLM + Rule kiểm tra toán học (Tiền hàng + Tiền thuế = Tổng thanh toán) hay có thực sự cần thiết phải dùng đến Agent tự hành không?
```

**AI phản biện Card (nếu có):**
- Điểm yếu AI chỉ ra: AI nhận xét rằng nếu chỉ dựa vào mô hình thị giác/LLM để đọc số tiền thì rủi ro ảo giác (hallucination) vẫn tồn tại, và việc đưa dữ liệu tài chính qua API đám mây có thể vi phạm bảo mật nội bộ của doanh nghiệp.
- Tôi sửa gì: Tôi đã bổ sung thêm tầng Rule toán học độc lập (Python script tính toán lại tổng tiền để kiểm tra chéo với số LLM đọc được), highlight đỏ ngay trên Excel nếu tổng tiền lệch 1 đồng; đồng thời làm rõ ranh giới: AI chỉ gợi ý điền trước dữ liệu, kế toán viên vẫn là người bấm nút xác nhận cuối cùng.

### Self-check nộp phần 01
- [x] Có 5+ problems + top 3 Cards đủ field (10 problems, 3 Cards chi tiết đầy đủ 10 trường thông tin)
- [x] Mỗi Card có workflow trước/sau + bottleneck + metric + fallback
- [x] Đã chọn 1 card pitch + câu hỏi challenge
