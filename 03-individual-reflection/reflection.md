# 03 — Individual Reflection

> Viết bằng lời của bạn (Phase 7 trong `01-worksheet.md`). Có thể dùng AI gợi ý câu hỏi tự soi, không dùng AI viết thay. 8-12 câu, có chuyện cụ thể.

## Thông tin cá nhân

- Họ và tên: Trần Văn Khánh
- Mã học viên: 2413
- Nhóm: Nhóm K4B (Trần Văn Khánh, Ngô Tuấn Tùng, Cao Đức Hiệp, Đào Thị Huyền, Nguyễn Huy Cương)
- Candidate problem nhóm chọn: Tự động hóa việc đọc, trích xuất dữ liệu từ hóa đơn VAT (ảnh/PDF) và kiểm tra đối soát toán học để điền tự động vào bảng kê chi phí Excel cho kế toán nội bộ.

---

## 1. Tôi đã tham gia vào phần nào?

Ghi việc cụ thể + kết quả cụ thể. Không ghi chung chung kiểu "tham gia thảo luận".

| Hoạt động | Tôi đã làm gì? (việc cụ thể) | Kết quả / ảnh hưởng tới nhóm |
|---|---|---|
| Scan cá nhân | Tự rà soát 7 vấn đề thực tế từ công việc làm AI Engineer và dự án tự động hóa hóa đơn đang làm; đo đạc số phút và tỷ lệ lỗi cụ thể. | Cung cấp bài toán Hóa đơn vào Excel (Problem Card #1) làm ứng viên mạnh nhất giúp nhóm có đề tài bám sát thực tế. |
| Pitch Problem Card | Thuyết trình bài toán Hóa đơn vào Excel trong 2 phút với các số liệu bấm giờ rõ ràng: mất 220 phút cho 60 hóa đơn, tỷ lệ gõ nhầm 5-7%. | Thuyết phục cả nhóm đồng ý đây là bài toán có nỗi đau lớn nhất và đo lường được rõ ràng nhất. |
| Challenge bài của bạn khác | Phản biện đề tài kiểm tra file nộp lab của Cương và đề tài debug traceback của Tùng, chỉ ra rằng các bài này dùng Rule hoặc checklist Notion sẽ nhanh và rẻ hơn AI. | Giúp nhóm không chọn nhầm bài toán quá hẹp hoặc bài toán vốn chỉ cần giải quyết bằng thói quen/công cụ phi AI. |
| Gom trùng / cluster | Cùng Hiệp phân loại 12 ý tưởng của cả nhóm thành 4 cụm nghiệp vụ rõ ràng (Xử lý dữ liệu, Tìm kiếm tri thức, Kỹ thuật CAD, Quản lý cá nhân). | Giúp nhóm có cái nhìn tổng quan, không bị phân tán giữa quá nhiều ý tưởng rời rạc. |
| Chọn candidate problem | Giải thích lý do vì sao bài toán tủ điện CAD của mình tuy hay nhưng nhóm nên bỏ qua trong lab 4 tiếng vì domain quá sâu, hướng nhóm dồn lực cho bài hóa đơn. | Tạo sự đồng thuận cao (đạt 33/35 điểm ma trận), giúp nhóm tiết kiệm thời gian và tập trung sâu vào một bài toán khả thi. |
| Validation / research | Cung cấp tập dữ liệu mẫu 50 hóa đơn thực tế (gồm cả ảnh chụp Zalo bị nghiêng/mờ); phân tích kỹ thuật điểm yếu của AWS Textract đối với hóa đơn Việt Nam. | Định hình hướng đi: không tự train lại OCR mà dùng Vision LLM API kết hợp với prompt có Schema JSON chuẩn. |
| Workflow nhóm | Trực tiếp vẽ luồng Before 6 bước (220 phút) và luồng After 5 bước (35 phút); đánh dấu rõ ràng điểm nghẽn và ranh giới con người duyệt. | Cả nhóm nhìn thấy rõ bước nào máy làm, bước nào AI làm và bước nào bắt buộc con người phải giữ quyền quyết định. |
| Problem Statement | Soạn thảo chi tiết các trường trong Problem Statement v0 và v1; thiết lập ranh giới Boundary chặt chẽ (làm gì và tuyệt đối không làm gì). | Bảo vệ tính an toàn và pháp lý của bài toán: AI chỉ điền nháp vào Excel, không tự ý thanh toán hay ghi đè vào phần mềm chính thức. |
| Rule / Workflow / Agent | Trả lời 5 câu hỏi chốt để lập luận so sánh giữa Rule, Workflow và Agent; phân tích vì sao dùng Agent là lãng phí và nguy hiểm. | Giúp nhóm thống nhất chọn mức Workflow kết hợp Rule, không bị rơi vào cái bẫy "thích làm Agent cho ngầu". |
| Decision | Thiết kế kế hoạch chạy pilot với 30 hóa đơn thực tế và định nghĩa 3 chỉ số đo lường định lượng kèm phương án rollback cụ thể. | Đưa ra quyết định Go có căn cứ thực nghiệm vững chắc, sẵn sàng để triển khai code thử nghiệm ngay sau lab. |

**Dấu tay rõ nhất của tôi trong artifact cuối (1-2 câu):**

```text
Dấu tay rõ nhất của tôi là việc đề xuất và bảo vệ thành công kiến trúc Workflow lai (Hybrid): Dùng mô hình AI Vision để đọc hiểu linh hoạt các mẫu hóa đơn ảnh/PDF phức tạp, nhưng bắt buộc kẹp thêm tầng Rule kiểm tra toán học số học độc lập (Tiền hàng + Thuế = Tổng tiền) và tô màu cảnh báo trên Excel trước khi bàn giao cho kế toán duyệt.
```

---

## 2. Bảng dùng AI (mỗi dòng 1 phase có dùng AI — 2 cột cuối bắt buộc)

| Phase | Tôi dùng AI để làm gì? | AI hữu ích ở đâu? | AI sai / hời hợt ở đâu? | Tôi sửa gì bằng nhận định của mình? |
|---|---|---|---|---|
| Scan | Hỏi gợi ý các pain point thường gặp trong quy trình xử lý chứng từ văn phòng. | Gợi ý khâu phân loại chi phí sao kê ngân hàng và việc phải gõ lại thông tin vào các cột Excel theo mẫu riêng của từng công ty. | Đưa ra ý tưởng viển vông: "AI tự động sinh báo cáo tài chính và cân đối dòng tiền hoàn chỉnh". | Tôi loại bỏ ngay ý tưởng đó vì kế toán không bao giờ giao phó trách nhiệm pháp lý cho AI; tôi tập trung thuần túy vào thao tác gõ tay hóa đơn vào Excel. |
| Problem Card | Hỏi cách tính toán và phân bổ thời gian (time breakdown) cho một quy trình nhập liệu. | Cung cấp khung thời gian tham khảo gồm các bước mở file, đọc mắt, gõ tay và kiểm tra chéo. | Đưa ra con số chung chung kiểu "tiết kiệm 50% thời gian" mà không có căn cứ thực tế. | Tôi thay bằng số liệu bấm giờ thực tế từ công việc hằng ngày: 220 phút cho 60 hóa đơn, phân rã chi tiết bước gõ tay tốn 100 phút và dò lỗi tốn 30 phút. |
| Workflow | Nhờ AI gợi ý luồng xử lý tự động hóa tối ưu cho tài liệu scan. | Gợi ý việc dùng schema JSON trung gian giữa khâu OCR và khâu ghi file Excel. | Đề xuất một luồng tự động hóa 100% "Zero-touch" (AI tự đọc và tự nạp thẳng vào cơ sở dữ liệu kế toán mà không cần con người). | Tôi kịch liệt bác bỏ luồng này, thêm vào bước "Kế toán mở Excel duyệt ô cảnh báo" làm chốt chặn Human Boundary bắt buộc. |
| Research | Tra cứu các giải pháp trích xuất hóa đơn hiện có trên thị trường thế giới và Việt Nam. | Liệt kê nhanh các công cụ như ABBYY FineReader, AWS Textract, Bizzi, FPT.AI. | Đánh giá rất hời hợt, cho rằng AWS Textract giải quyết tốt mọi loại hóa đơn mà không biết các mẫu hóa đơn đặc thù tại VN có thuế suất 8%, 10% hay bị đọc nhầm. | Tôi bổ sung phân tích thực tế: Textract dễ nhầm trường với hóa đơn VN và FPT/Bizzi thì đóng kín trong phần mềm riêng, từ đó định hình giải pháp cắm thẳng vào Excel nội bộ. |
| Problem Statement | Nhờ AI viết nháp Problem Statement theo cấu trúc đề cương. | Hỗ trợ diễn đạt câu chữ trôi chảy, rõ ràng ở phần Actor và Workflow. | Bị lỗi nghiêm trọng là "Solution-first": nhảy ngay vào mô tả mô hình LLM, prompt kỹ thuật thay vì tập trung vào nỗi đau và điểm nghẽn nghiệp vụ. | Tôi viết lại hoàn toàn theo hướng Problem-first: làm rõ người chịu ảnh hưởng, số giờ tiêu tốn mỗi ngày và đặt ra ranh giới Boundary cấm AI can thiệp vào nghiệp vụ thanh toán. |
| Rule / Workflow / Agent | Hỏi phản biện xem bài toán này nên dùng Rule, Workflow hay Multi-agent System. | Phân tích rõ được hạn chế của Rule khi gặp ảnh chụp nghiêng và hóa đơn không có text layer. | AI bị "ngáo Agent": cố tình vẽ ra một hệ thống Multi-agent phức tạp gồm Planner Agent, OCR Agent, Validator Agent để nghe có vẻ tân tiến. | Tôi từ chối đề xuất Agent vì bài toán đi thẳng một chiều, việc dùng Agent chỉ làm tăng độ trễ và chi phí API; tôi kiên quyết chọn Workflow kết hợp Rule. |
| Decision | Tham khảo các câu hỏi checklist để đưa ra quyết định Go/No-Go. | Cung cấp khung câu hỏi tốt về khả năng kiểm soát rủi ro và điều kiện pilot. | Phần kế hoạch Rollback rất mơ hồ, chỉ nói "nếu không hiệu quả thì dừng". | Tôi đặt ra ngưỡng định lượng rõ ràng: nếu tỷ lệ trích xuất sai vượt quá 15% hoặc chi phí API >500đ/HĐ thì lập tức rollback về quy trình nhập tay. |

---

## 3. Reflection câu hỏi mở

*(Chọn trả lời tích hợp: Nhóm có lúc nào bị solution-first đòi làm Agent cho ngầu không? / Phần nào có dấu tay của tôi? / Điều khó nhất khi viết Problem Statement? / Nếu làm lại sẽ challenge gì?)*

**Reflection:**

Trong quá trình làm việc nhóm, đã có thời điểm các thành viên suýt rơi vào cái bẫy "solution-first" khi thấy trào lưu AI hiện nay rất chuộng Agent và muốn xây dựng một hệ thống Multi-agent tự hành có khả năng tự mở Zalo tải file rồi tự nộp tờ khai thuế cho "ngầu". Với vai trò Technical Lead, tôi đã phải kéo cả nhóm trở về mặt đất bằng cách phân tích bản chất quy trình: nghiệp vụ kế toán là luồng đi thẳng một chiều, đòi hỏi sự chuẩn xác tuyệt đối về mặt số học, nếu thả một Agent tự do suy luận thì nguy cơ ảo giác và chi phí API sẽ phá nát bài toán. 

Dấu tay rõ nhất của tôi trong bản nộp nhóm là việc bảo vệ thành công kiến trúc Workflow lai: dùng AI ở khâu nó làm tốt nhất là đọc hiểu ảnh mờ, nhưng bắt buộc dùng Rule code cứng để kiểm tra toán học và giữ con người làm chốt chặn cuối cùng. 

Điều khó khăn nhất với tôi và cả nhóm khi hoàn thiện Problem Statement không phải là mô tả điểm nghẽn mà là việc xác định ranh giới (Boundary) và Success Metric định lượng. Ban đầu ai cũng quen ghi chung chung là "giúp kế toán làm nhanh hơn", nhóm đã phải tranh luận gay gắt để quy đổi thành các con số có thể đo được bằng đồng hồ bấm giờ (giảm từ 220 phút xuống 35 phút) và tỷ lệ lỗi số học phải bị triệt tiêu về 0%. Nếu được làm lại từ đầu, tôi sẽ challenge nhóm phỏng vấn thêm người duyệt chi hoặc Kế toán trưởng để đo lường chính xác hơn nỗi sợ rủi ro pháp lý của họ, từ đó thiết kế bộ cảnh báo trên Excel sát với yêu cầu kiểm toán thực tế hơn nữa.

---

## 4. Tự kiểm cuối bài (check trước khi nộp repo)

- [x] [12đ] Cá nhân có 5+ problems + top 3 Problem Cards (Đã hoàn thành 7 problems chi tiết và 3 Problem Cards có workflow Before/After)
- [x] [12đ] Tôi đã pitch rõ + challenge nhóm đúng trọng tâm (ghi ở bảng mục 1 với các dẫn chứng cụ thể)
- [x] Nhóm có nhật ký hội tụ từ candidates về 1 bài (Đầy đủ 12 candidate từ 5 thành viên, cluster 4 cụm, shortlist 3 bài và score ma trận)
- [x] [15đ] Nhóm có workflow trước/sau (Đầy đủ thời gian từng bước, bottleneck 100', handoff, human boundary và fallback)
- [x] [20đ] Nhóm có PS v0/v1 với metric + boundary rõ (Metric có baseline 220' -> 35', boundary phân định rõ làm gì và không làm gì)
- [x] [15đ] Nhóm có so sánh No AI / Rule / Workflow / Agent (So sánh sâu sắc trên cùng bài toán, trả lời trọn vẹn 5 câu hỏi chốt)
- [x] [10đ] Nhóm có Go / Not Yet / No-Go + lý do rõ (Quyết định Go với kế hoạch pilot 30 hóa đơn, đo 3 số và điều kiện rollback rõ ràng)
- [x] [10đ] Reflection này có vai trò thật + AI giúp/sai ở đâu + điều học được + nếu làm lại đổi gì (Bảng dùng AI có đủ 7 phase và đoạn văn tự sự 8-12 câu)
- [x] [6đ] Tôi tự giải thích được mạch problem → workflow → metric → boundary → độ phù hợp AI (Sẵn sàng trả lời vấn đáp logic toàn bộ bài)
