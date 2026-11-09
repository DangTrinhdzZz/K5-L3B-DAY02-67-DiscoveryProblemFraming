# Báo cáo nhóm — Day 02 Discovery & Problem Framing

> Bản chung của nhóm, viết trên repo do nhóm trưởng fork. Không copy file này sang repo cá nhân.
> Template chi tiết và prompt mẫu: [docs/01-worksheet.md](../../docs/01-worksheet.md). Bài mẫu: [docs/02-deliverable-example.md](../../docs/02-deliverable-example.md).

## 1. Thông tin nhóm

- Tên nhóm: 67
- Thành viên: Triệu Hải Đăng Trình (2A202603874) — nhóm một thành viên, được coach cho phép do không tìm được thành viên cùng nhóm; xem `TEAM.md`
- Candidate problem được chọn (1 câu): Khi nhận một repo bài lab có nhiều file hướng dẫn, học viên cần xác định và kiểm tra đầy đủ yêu cầu phải làm/nộp để không bỏ sót hoặc sai cấu trúc trước deadline.
- Quyết định cuối: Not Yet (đề xuất dựa trên bằng chứng hiện có; học viên cần xác nhận)

---

## 2. Hội tụ nhóm (CP3)

### 2.1. Pitch

| # | Người đưa ra | Candidate (Job Story ngắn) | Actor | Bottleneck | Câu hỏi phản biện nhận được (ai hỏi) |
|---:|---|---|---|---|---|
| 1 | Triệu Hải Đăng Trình | Xác định và kiểm tra đầy đủ yêu cầu lab từ nhiều file | Học viên làm lab trên GitHub | Hợp nhất yêu cầu rải rác thành checklist | Không có — nhóm một thành viên |
| 2 | Triệu Hải Đăng Trình | Khoanh vùng nguyên nhân khi code/notebook AI lỗi | Học viên làm lab AI/ML | Đối chiếu traceback, dữ liệu và logic để chọn cách sửa | Không có — nhóm một thành viên |
| 3 | Triệu Hải Đăng Trình | Gom code, metric và ảnh vào đúng template báo cáo | Học viên làm lab kỹ thuật | Tìm và ghép bằng chứng đang nằm rải rác | Không có — nhóm một thành viên |

**Hạn chế của bước pitch:** nhóm chỉ có một thành viên nên không có pitch và phản biện nội bộ. Ba Problem Card cá nhân được dùng làm ba candidate; không tạo tên hoặc câu hỏi của người khác.

### 2.2. Cluster

| Cluster | Các candidate | Pattern chung |
|---|---|---|
| A — Hiểu yêu cầu | Xác định/kiểm tra yêu cầu lab | Đọc và hợp nhất nhiều nguồn trước khi hành động |
| B — Chẩn đoán kỹ thuật | Khoanh vùng lỗi code/notebook | Đối chiếu nhiều tín hiệu để tìm nguyên nhân |
| C — Tổng hợp bằng chứng | Hoàn thiện báo cáo đúng template | Tìm, chọn và trình bày bằng chứng từ nhiều nơi |

### 2.3. Opportunity Solution Tree rút gọn

Gốc là **1 outcome**. Nhánh là **opportunity** (nhu cầu, pain), không phải tính năng hay công cụ.

```text
OUTCOME: Giảm thời gian hoàn thành lab mà không tăng số yêu cầu bắt buộc bị bỏ sót
├── Opportunity A: Yêu cầu phải làm/nộp nằm rải rác trong nhiều file
├── Opportunity B: Lỗi kỹ thuật cần đối chiếu nhiều tín hiệu mới khoanh vùng được
└── Opportunity C: Bằng chứng kỹ thuật nằm rải rác khi viết báo cáo
```

Những ý đã gạch bỏ vì là solution đội lốt opportunity:

- “Chatbot đọc repo” — là solution, không phải opportunity.
- “Agent tự làm bài” — là solution, vượt boundary học thuật và không giải thích được bài.
- “Dashboard tiến độ” — là solution; chưa có bằng chứng đây là mức can thiệp cần thiết.

### 2.4. Chấm điểm shortlist (1–5)

| Candidate | Actor rõ | Quy trình rõ | Pain có bằng chứng | Impact đo được | Vừa sức lab | So sánh được No AI/Rule/Workflow/Agent | Nhóm hiểu domain | Tổng |
|---|---:|---:|---:|---:|---:|---:|---:|---:|
| Xác định/kiểm tra yêu cầu lab | 5 | 5 | 4 | 4 | 5 | 5 | 5 | **33** |
| Khoanh vùng lỗi code/notebook | 5 | 4 | 4 | 3 | 3 | 5 | 4 | 28 |
| Gom bằng chứng thành báo cáo | 5 | 5 | 3 | 4 | 5 | 4 | 5 | 31 |

**Candidate được chọn:** Xác định và kiểm tra đầy đủ yêu cầu lab từ nhiều file.

**Vì sao chọn:** actor và quy trình rõ; pain xảy ra ngay trong repo này; baseline 45–90 phút tuy mới là ước lượng nhưng đo lại được; phạm vi đủ nhỏ để thử checklist, Rule và Workflow.

**Vì sao loại các candidate còn lại:** bài debug có biến thiên lớn theo từng lỗi và target khó so sánh; bài viết báo cáo gần với candidate được chọn nhưng phụ thuộc nhiều hơn vào chất lượng nội dung cá nhân và dễ vi phạm boundary nếu AI viết thay.

**Xử lý bất đồng (nếu có):** không có thảo luận hoặc bất đồng nội bộ do nhóm một thành viên. Candidate được chọn theo tổng điểm và bằng chứng hiện có; học viên đã yêu cầu Codex tiếp tục hoàn thiện bài nhưng chưa xác nhận riêng bảng điểm.

---

## 3. Kiểm chứng + research giải pháp đã có (CP4)

### 3.1. Assumption Map

| # | Giả định | Loại (Value / Usability / Feasibility / Viability) | Quan trọng (1–5) | Đã có bằng chứng (1–5) | Kiểm chứng trước? |
|---:|---|---|---:|---:|---|
| 1 | Học viên khác cũng mất ít nhất 30 phút để hiểu yêu cầu ở repo có nhiều file | Value | 5 | 1 | Có |
| 2 | Bỏ sót yêu cầu là rủi ro đáng giải quyết, không chỉ là cảm giác bất tiện | Value | 5 | 2 | Có |
| 3 | Học viên có thể kiểm checklist có dẫn chiếu nguồn trong khoảng 10 phút | Usability | 4 | 1 | Có |
| 4 | Công cụ có thể đọc đủ các file Markdown và giữ liên kết về nguồn | Feasibility | 4 | 3 | Sau |
| 5 | Checklist + script đơn giản chưa giải được phần hợp nhất yêu cầu ngôn ngữ | Feasibility | 5 | 1 | Có |
| 6 | Việc dùng AI để tổng hợp yêu cầu được phép nếu học viên tự kiểm và tự viết bài | Viability | 5 | 3 | Sau |

*Điền 4–6 giả định; xóa dòng thừa.*

Giả định nhóm ưu tiên kiểm chứng: #1, #3 và #5 — quan trọng nhưng hiện gần như chỉ có trải nghiệm của một học viên.

### 3.2. Kiểm chứng

Cách đã dùng: tự hồi tưởng có đối chiếu notebook, commit và lịch sử ChatGPT. **Chưa thực hiện phỏng vấn hoặc survey người khác.** Cách này không đáp ứng đầy đủ yêu cầu kiểm chứng người thật của CP4 và không được trình bày như thể đã phỏng vấn.

Interview snapshot (mỗi buổi phỏng vấn một bảng, hoặc đặt file trong `report/assets/cp4-interview-snapshot-N.md`):

| Trường | Nội dung |
|---|---|
| Người được hỏi (vai trò, không ghi tên thật) | Chưa có người được phỏng vấn |
| Câu nói đáng nhớ nhất (nguyên văn) | Không có — không tạo câu nói giả |
| Lần gần nhất gặp vấn đề này: chuyện gì đã xảy ra? | Chưa có dữ liệu người ngoài nhóm |
| Hiện đang xử lý bằng cách nào (workaround)? | Chưa có dữ liệu người ngoài nhóm |
| Mất bao lâu, bao lần? | Chưa có dữ liệu người ngoài nhóm |
| Insight / opportunity rút ra | Chưa thể kết luận Value cho người khác |

Tổng hợp:

| Nguồn | Số người / số mẫu | Tín hiệu xác nhận | Tín hiệu phản bác |
|---|---:|---|---|
| Tự quan sát của học viên | 1 | Đã mất 45–90 phút/lần và lặp khoảng 3 lần trong 7 ngày theo ước lượng | Không chứng minh người khác có cùng pain; baseline chưa được bấm giờ |
| Phỏng vấn/survey | 0 | Không có | Thiếu kiểm chứng người thật là tín hiệu chống lại quyết định Go |

**Nhóm đã sửa problem thế nào sau kiểm chứng:** thu hẹp actor ban đầu thành “học viên tự làm lab trên GitHub”, không khẳng định mọi học viên đều gặp. Đổi quyết định dự kiến từ Go sang **Not Yet** cho tới khi có ít nhất 3 lần đo trực tiếp và phỏng vấn 2–3 học viên hoặc survey 5–10 người. Bộ câu hỏi và snapshot trống nằm ở `report/assets/cp4-validation-kit.md`.

### 3.3. Research giải pháp đã có

| Công cụ / case / pattern | Link | Giải bước nào trong quy trình? | Điểm mạnh | Khoảng trống / rủi ro | Bài học cho nhóm |
|---|---|---|---|---|---|
| GitHub Copilot Chat trong ngữ cảnh repository | https://docs.github.com/en/copilot/how-tos/copilot-on-github/chat-with-copilot/get-started-with-chat | Hỏi về mục đích, cấu trúc và nội dung file trong repo | Dùng chính file/symbol của repo làm ngữ cảnh; hỗ trợ câu hỏi nối tiếp | Có thể tóm tắt thiếu yêu cầu; phụ thuộc quyền truy cập/gói; vẫn cần mở nguồn kiểm | Dùng để tạo bản nháp checklist có dẫn chiếu, không tự đánh dấu hoàn thành |
| Gemini Notebook (NotebookLM) chat với sources | https://support.google.com/gemininotebook/answer/16179559 | Hợp nhất câu hỏi trên tập tài liệu đã tải lên | Trả lời dựa trên nguồn được chọn và cung cấp citation để quay lại đoạn gốc | Cần đưa nguồn vào notebook; citation không đảm bảo suy luận đầy đủ; dữ liệu riêng tư cần cân nhắc | Citation làm bước human review khả thi hơn, nhưng không thay việc đọc yêu cầu quan trọng |
| GitHub Markdown tasklists | https://docs.github.com/en/get-started/writing-on-github/working-with-advanced-formatting/about-tasklists | Biến yêu cầu đã xác nhận thành checklist theo dõi được | Đơn giản, không cần AI, checkbox hiển thị trực tiếp trên GitHub | Không tự phát hiện/hợp nhất yêu cầu; tasklist block cũ đã retired, tasklist Markdown vẫn dùng được | Bắt đầu bằng checklist/Rule; chỉ thêm AI nếu đo được bước tổng hợp vẫn là bottleneck |

Các link trên đã được mở và kiểm tra ngày 09/11/2026. Research cho thấy đã có công cụ hỗ trợ đọc repo/tài liệu, nhưng chưa chứng minh người dùng cần một hệ thống mới.

---

## 4. Quy trình trước/sau (CP5)

### 4.1. Quy trình hiện tại

Sơ đồ (ASCII, Mermaid hoặc link ảnh trong `report/assets/`):

```text
[Liệt kê file: 3'] → [Đọc README: 7'] → [Đọc rules/checkpoints: 10']
→ [Đọc rubric/submission: 10'] → [Đọc worksheet/mẫu: 10–20']
→ [Hợp nhất checklist: 15–25'] ← BOTTLENECK → [Đối chiếu bài: 10–15']
```

| Bước | Actor | Input | Output | Thời gian / tần suất | Ghi chú |
|---:|---|---|---|---|---|
| 1 | Học viên | Danh sách file trong repo | Danh sách nguồn cần đọc | Khoảng 3 phút/lab | Không có handoff |
| 2 | Học viên | `README.md` | Tổng quan và thứ tự đọc | Khoảng 7 phút/lab | Chuyển ghi chú sang bước 3 |
| 3 | Học viên | Rules và checkpoints | Ràng buộc và sản phẩm từng CP | Khoảng 10 phút/lab | Chuyển ghi chú sang bước 4 |
| 4 | Học viên | Rubric và submission | Điểm, tên file, yêu cầu nộp | Khoảng 10 phút/lab | Chuyển ghi chú sang bước 5 |
| 5 | Học viên | Worksheet, mẫu và ghi chú trước | Checklist hợp nhất để đối chiếu bài | Khoảng 35–60 phút/lab | Tự dùng checklist khi làm/nộp |

**Bottleneck chính:** bước 5 — đọc phần hướng dẫn chi tiết rồi hợp nhất yêu cầu từ mọi nguồn; ước lượng 35–60 phút trong tổng baseline 45–90 phút.

### 4.2. Quy trình tương lai

Ghi rõ bước nào **Rule**, bước nào **AI**, bước nào **con người**, **boundary** ở đâu, **phương án quay về** khi AI sai.

```text
[Rule liệt kê file + trích heading: 2']
→ [AI soạn checklist kèm file/heading nguồn: 3–5']
→ [Học viên mở nguồn, sửa/xác nhận từng mục: 10'] ← CON NGƯỜI
→ [Học viên dùng checklist kiểm bài: 10–15'] ← CON NGƯỜI

BOUNDARY: AI không tự sửa bài, không đánh dấu mục đã hoàn thành, không suy diễn
yêu cầu không có nguồn và không viết reflection thay học viên.
PHƯƠNG ÁN QUAY VỀ: nếu checklist thiếu/sai nguồn, bỏ bản AI và dùng thứ tự đọc
cùng checklist thủ công; giữ nguyên toàn bộ file gốc.
```

### 4.3. Before / after

| Chỉ số | Trước | Sau (kỳ vọng) | Ghi chú |
|---|---:|---:|---|
| Số bước | 7 | 4 | Gộp thao tác cơ học, không bỏ bước kiểm nguồn |
| Tổng thời gian | 45–90 phút (ước lượng) | Target giả thuyết 25–30 phút | Đo bằng bấm giờ 3 lab, chưa phải kết quả đạt được |
| Số bước thủ công | 7/7 | 2/4 | Con người vẫn xác nhận checklist và kiểm bài |
| Bottleneck chính | Hợp nhất yêu cầu: 15–25 phút, cộng thời gian đọc nguồn | Kiểm nguồn: khoảng 10 phút | Bottleneck mới là điểm kiểm soát chất lượng |
| Rủi ro mới phát sinh | — | AI bỏ sót, gộp sai hoặc bịa yêu cầu | Xử lý bằng citation, review và quay về checklist thủ công |

---

## 5. Problem Statement v0 (CP5)

| Trường | Nội dung |
|---|---|
| **Actor** | Học viên tự làm bài lab trên một repository có nhiều file hướng dẫn |
| **Quy trình** | Liệt kê file → đọc tổng quan/rules/checkpoints/rubric/submission/worksheet → hợp nhất checklist → đối chiếu bài |
| **Bottleneck** | Hợp nhất các yêu cầu rải rác, trùng hoặc nằm ở mức chi tiết khác nhau thành một checklist có thể hành động |
| **Impact** | Mất khoảng 45–90 phút/lần theo hồi tưởng, lặp khoảng 3 lần trong 7 ngày; có nguy cơ bỏ sót mục hoặc sai cấu trúc gần deadline |
| **Success Metric** (baseline → target, cách đo) | Baseline 45–90 phút ước lượng → target giả thuyết ≤30 phút; bấm giờ từ lúc mở repo đến khi có checklist đã kiểm ở 3 lab, đồng thời đếm yêu cầu bắt buộc bị bỏ sót (target 0) |
| **Boundary** (AI không được làm gì; khi nào cần con người kiểm tra — HITL) | Không tự sửa/nộp bài, không tạo bằng chứng, không viết reflection; học viên phải mở nguồn và xác nhận từng mục trước khi dùng |

Phản biện nhận được (từ AI hoặc nhóm khác) và nhóm có đồng ý không:

- Codex chỉ ra baseline chưa phải log trực tiếp, target chưa được thử và metric tốc độ chưa đủ. Nhóm đồng ý ở mức cấu trúc: gắn nhãn ước lượng/giả thuyết, thêm cách bấm giờ và metric “0 yêu cầu bắt buộc bị bỏ sót”. Học viên chưa xác nhận riêng bản v0.

---

## 6. Mức can thiệp AI (CP6)

### 6.1. Ma trận độ mơ hồ × độ phức tạp

Bài của nhóm nằm ở ô: độ mơ hồ cao × độ phức tạp trung bình.

Vì sao: nội dung mỗi repo khác nhau và một yêu cầu có thể xuất hiện ở nhiều mức chi tiết; tuy nhiên các bước đọc → trích → hợp nhất → kiểm nguồn đều định sẵn, không cần hệ thống tự quyết quy trình.

### 6.2. So sánh 4 mức

| Mức | Phương án cho bài của nhóm | Đủ khi nào | Rủi ro | Chọn? |
|---|---|---|---|---|
| **No AI** (sửa quy trình) | Thứ tự đọc cố định + checklist thủ công | Repo ngắn, cấu trúc ổn định | Vẫn tốn thời gian hợp nhất ngôn ngữ | Thử đầu tiên |
| **Rule** | Script liệt kê file/heading, kiểm tên và placeholder | Yêu cầu có pattern cố định | Không hiểu yêu cầu diễn đạt bằng văn bản | Dùng cho thao tác cơ học |
| **Workflow** | Rule thu thập → AI soạn checklist có nguồn → người kiểm → người áp dụng | Nhiều file văn bản nhưng các bước cố định | AI bỏ sót/bịa/gộp sai | **Mức đích để pilot** |
| **Agent** | Tự quyết file đọc, sửa bài và lặp đến khi xong | Chỉ khi quy trình không định trước được | Quá nhiều quyền, khó kiểm, vi phạm boundary học thuật | Không chọn |

**Mức chọn:** Workflow, nhưng chỉ pilot sau khi đo No AI/Rule.

**Vì sao không chọn mức đơn giản hơn:** checklist và Rule có thể giảm thao tác tìm file nhưng chưa hợp nhất yêu cầu ngôn ngữ nằm rải rác. Tuy vậy, chưa có dữ liệu chứng minh phần còn lại đủ lớn, nên quyết định hiện tại là Not Yet và pilot phải bắt đầu ở mức đơn giản.

### 6.3. AI Canvas rút gọn

| Thành phần | Nội dung |
|---|---|
| **Prediction** — AI dự đoán / tạo ra gì? | Checklist dự thảo: yêu cầu, file/heading nguồn, checkpoint, điểm và trạng thái |
| **Judgment** — con người cân nhắc, quyết định gì? | Yêu cầu nào bắt buộc, các nguồn có mâu thuẫn không, checklist có thiếu/sai không |
| **Action** — hành động cuối cùng là gì, ai làm? | Học viên sửa/xác nhận checklist rồi tự thực hiện và nộp bài |
| **Outcome** — đo kết quả bằng gì? | Thời gian tạo checklist đã kiểm; số yêu cầu bắt buộc bị bỏ sót; số mục AI không truy được nguồn |
| **Input** — AI cần dữ liệu đầu vào gì mỗi lần chạy? Có sẵn không? | Toàn bộ file hướng dẫn/template được Git theo dõi; có sẵn trong repo |
| **Feedback** — lấy phản hồi ở đâu để cải thiện? | Chênh lệch giữa checklist AI và checklist người đã sửa; lỗi phát hiện ở lần kiểm cuối |

### 6.4. Hai câu hỏi của Google PAIR

- Người dùng muốn **được hỗ trợ (augment)** hay **giao hẳn việc (automate)**? **Augment.** Trong phiên này học viên yêu cầu Codex hỗ trợ hoàn thiện cấu trúc nhưng vẫn phải cung cấp trải nghiệm thật; quy định bài cũng yêu cầu học viên tự giải thích được nội dung. Đây mới là một trường hợp, chưa đủ khái quát.
- AI sai kiểu nào tệ hơn, **báo nhầm** hay **bỏ sót**? **Bỏ sót** yêu cầu bắt buộc nguy hiểm hơn vì có thể làm mất điểm mà học viên không biết. Thiết kế yêu cầu citation cho từng mục, checklist người kiểm và đối chiếu riêng với rubric/submission.

---

## 7. Problem Statement v1 + tiêu chí đánh giá (CP6)

| Trường | Nội dung |
|---|---|
| **Actor** | Học viên tự làm lab trên repo có nhiều file hướng dẫn; hiện mới kiểm chứng với một học viên |
| **Quy trình** | Rule liệt kê nguồn → AI tạo checklist có dẫn chiếu → học viên kiểm nguồn/sửa → học viên dùng checklist kiểm bài |
| **Bottleneck** | Hợp nhất yêu cầu văn bản rải rác thành checklist đầy đủ và truy được nguồn |
| **Impact** | Baseline 45–90 phút/lần theo ước lượng; nguy cơ bỏ sót yêu cầu hoặc sai cấu trúc gần deadline |
| **Success Metric** (baseline → target, cách đo) | ≤30 phút để tạo checklist đã kiểm trong 3 lab liên tiếp; 0 yêu cầu bắt buộc bị bỏ sót; 100% mục checklist có file/heading nguồn |
| **Boundary** | Không tự sửa/nộp bài, không tạo dữ liệu/bằng chứng, không viết reflection; học viên xác nhận từng mục và chịu trách nhiệm quyết định cuối |
| **AI intervention point** | Sau khi Rule thu thập nội dung file, trước bước học viên hợp nhất checklist |
| **Mức chọn** | Workflow (đề xuất pilot sau Rule) |
| **Rủi ro & người kiểm tra** | AI bỏ sót/bịa/gộp sai; học viên mở nguồn kiểm từng mục, quay về checklist thủ công nếu không đạt |

**Thay đổi so với v0 và lý do:** v1 thu hẹp actor theo bằng chứng, chỉ rõ điểm can thiệp, mức Workflow, citation và người kiểm tra; không thay baseline ước lượng thành số liệu giả.

| Trường | v0 | v1 | Vì sao đổi |
|---|---|---|---|
| Actor | Học viên làm lab | Thêm: hiện mới kiểm chứng với một học viên | Tránh khái quát quá bằng chứng |
| Quy trình | Quy trình đọc/hợp nhất hiện tại | Thêm Rule → AI → người kiểm → người áp dụng | Chỉ rõ điểm can thiệp và handoff |
| Success Metric | Thời gian + số yêu cầu bỏ sót | Thêm 100% checklist có nguồn | Phản biện yêu cầu đo cả khả năng kiểm chứng |
| Boundary | Không tự làm/nộp/viết reflection | Thêm học viên xác nhận từng mục và quay về thủ công | Xử lý rủi ro AI bỏ sót/bịa |

**Tiêu chí đánh giá đầu ra của AI (3–5 tiêu chí):**

| # | Tiêu chí | Đạt khi | Không đạt khi |
|---:|---|---|---|
| 1 | Đầy đủ | Mọi yêu cầu bắt buộc trong rubric/submission/checkpoints xuất hiện trong checklist | Thiếu ít nhất một yêu cầu bắt buộc |
| 2 | Truy được nguồn | 100% mục có đúng file và heading nguồn | Có mục không có nguồn hoặc trỏ sai |
| 3 | Không bịa | Không có yêu cầu nào ngoài nội dung repo | Thêm yêu cầu không tồn tại trong nguồn |
| 4 | Tách problem/solution đúng | Checklist mô tả yêu cầu, không tự chọn solution thay học viên | Tự áp đặt công cụ hoặc quyết định chưa được xác nhận |
| 5 | Dễ kiểm | Checklist được học viên kiểm trong ≤10 phút | Mục trùng, mơ hồ hoặc cần đọc lại toàn bộ mới hiểu |

---

## 8. Quyết định (CP6)

### 8.1. Bốn rủi ro

| Rủi ro | Câu hỏi | Mức độ rủi ro (Thấp = an toàn / TB / Cao = nguy hiểm) | Lý do / bằng chứng |
|---|---|---|---|
| **Value** | Người dùng có thật sự cần và sẽ dùng không? | Cao | Chỉ có trải nghiệm hồi tưởng của một học viên; chưa phỏng vấn/survey và chưa đo baseline trực tiếp |
| **Usability** | Người dùng có dùng được, có hiểu và sửa được đầu ra của AI không? | Trung bình | Markdown checklist quen thuộc nhưng chưa đo khả năng kiểm nguồn trong 10 phút |
| **Feasibility** | Có đủ dữ liệu, công cụ, kỹ năng để làm không? | Thấp | File Markdown có sẵn; GitHub Copilot và Gemini Notebook hỗ trợ hỏi trên nguồn, nhưng cần thử độ đầy đủ |
| **Viability** | Có hợp chi phí, pháp lý, quy định tổ chức không? Ai vận hành? | Trung bình | Có thể dùng quy trình thủ công/Rule miễn phí; công cụ AI phụ thuộc gói và chính sách dữ liệu; học viên tự vận hành |

### 8.2. Kết luận

**Quyết định:** **Not Yet** — đề xuất của Codex dựa trên bằng chứng hiện có; học viên cần xác nhận quyết định cuối.

**Lý do:** rủi ro Value đang Cao vì chưa có người thật ngoài tác giả và chưa bấm giờ trực tiếp. Feasibility có tín hiệu tốt từ công cụ sẵn có, nhưng research không thay thế validation.

**Nếu Go — pilot nhỏ nhất:** chưa Go. Pilot sau validation: dùng một repo mới, tạo checklist thủ công/Rule trước; nếu bước hợp nhất vẫn >15 phút thì thử Workflow có AI và citation.

**Nếu Not Yet — cần kiểm chứng gì trước:** phỏng vấn 2–3 học viên hoặc survey 5–10 người; bấm giờ 3 lab; so sánh checklist thủ công/Rule với Workflow trên cùng nguồn; ghi cả yêu cầu bị thiếu và thời gian kiểm.

**Nếu No-Go — nên làm gì thay AI:** dùng thứ tự đọc cố định, Markdown tasklist và script kiểm tên file/placeholder.

**Ngưỡng dừng** (nếu sau … mà … thì quay về …): nếu bất kỳ checklist AI nào bỏ sót yêu cầu bắt buộc, có mục không truy được nguồn, hoặc sau 3 lab không tiết kiệm ít nhất 20 phút so với checklist thủ công/Rule, dừng Workflow và quay về checklist + script.

---

## 9. Hạn chế và hướng tiếp theo

- Nhóm một thành viên nên không có phản biện nội bộ; coach đã cho phép hình thức cá nhân theo xác nhận của học viên.
- Chưa có phỏng vấn/survey người ngoài nhóm; không tạo dữ liệu thay thế. Đây là lý do chính cho quyết định Not Yet.
- Mọi thời gian hiện tại là hồi tưởng/ước lượng, chưa phải log bấm giờ.
- Candidate, bảng điểm và quyết định được Codex đề xuất trong tình huống gấp; học viên cần tự đọc, xác nhận và có khả năng giải thích.
- Bước tiếp theo: dùng `report/assets/cp4-validation-kit.md`, ghi dữ liệu thật và cập nhật actor/metric/quyết định.

## 10. Tài liệu tham khảo

- GitHub Docs, “Getting started with prompts for Copilot Chat on GitHub”, truy cập 09/11/2026: https://docs.github.com/en/copilot/how-tos/copilot-on-github/chat-with-copilot/get-started-with-chat
- Google Help, “Use chat in Gemini Notebook”, truy cập 09/11/2026: https://support.google.com/gemininotebook/answer/16179559
- GitHub Docs, “About tasklists”, truy cập 09/11/2026: https://docs.github.com/en/get-started/writing-on-github/working-with-advanced-formatting/about-tasklists
