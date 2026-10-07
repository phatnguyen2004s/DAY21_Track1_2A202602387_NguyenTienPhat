# Lab 21 — Phân tích rủi ro AI qua case study thực tế

- Họ và tên: Nguyen Tien Phat
- MSSV / mã học viên: 2A202602387
- Lớp: H201
- Ngành đã chọn: Media / news / social / political assistant

### 1. Industry Risk Snapshot

| Nội dung | Đánh giá của tôi và lý do |
| --- | --- |
| Những tác hại chính có thể xảy ra | Thông tin sai về sự kiện thời sự đến tay người đọc (người dùng thiết bị và người hỏi trợ lý AI); tổ chức tin tức bị gắn tên vào nội dung sai và mất uy tín; người được nhắc đến trong tin (ví dụ người bị buộc tội) bị mô tả sai; niềm tin của công chúng vào tin tức bị xói mòn. |
| Mức độ high-stakes | Trung bình. Thiệt hại với từng cá nhân thường gián tiếp (hiểu sai, mất niềm tin) và có thể đính chính, nên thấp hơn các ngành như y tế. Tuy nhiên tin tức được phân phối ở quy mô rất lớn và có thể thành Cao khi liên quan đến bầu cử, khủng hoảng hoặc vụ án có người bị buộc tội. |
| Dữ liệu nhạy cảm có thể được sử dụng | Nội dung thông báo trên thiết bị người dùng (có thể gồm tin nhắn cá nhân), câu hỏi người dùng gửi cho trợ lý AI, thông tin về người xuất hiện trong tin (người bị buộc tội, nạn nhân), và xu hướng quan tâm chính trị suy ra từ hành vi đọc tin. Bài này không dùng dữ liệu thật của ai. |
| Nhu cầu human review | Cao. Biên tập viên hoặc người kiểm chứng cần duyệt nội dung do AI tạo hoặc tóm tắt trước khi gắn thương hiệu của tòa soạn. Nền tảng cần kiểm thử trên các chủ đề nhạy cảm (vụ án, bầu cử) trước khi bật tính năng. Lý do: lỗi đã xuất hiện dưới tên BBC (case 1), và nghiên cứu EBU/BBC cho thấy 45% câu trả lời có ít nhất một vấn đề đáng kể (case 2). Chuyên gia Jonathan Bright (Alan Turing Institute) cho rằng hiện các hãng chưa có cách đảm bảo mô hình không bịa thông tin ngoài việc có con người giám sát (BBC News, 17/01/2025). |

### 2. Case study 1 — Apple Intelligence tóm tắt sai thông báo tin tức của BBC (2024–2025)

#### Brief Case

- Tổ chức / sản phẩm AI: Apple, tính năng tóm tắt thông báo (notification summaries) của Apple Intelligence. Nội dung bị tóm tắt là thông báo của ứng dụng BBC News.
- Thời gian, địa điểm / bối cảnh: Tháng 12/2024 đến tháng 1/2025. BBC (Anh) phản ánh bản tóm tắt sai về Luigi Mangione, người bị buộc tội trong vụ sát hại CEO UnitedHealthcare Brian Thompson. Tính năng là tùy chọn và chỉ có trên các iPhone mới nhất (theo BBC News, 17/01/2025).
- AI được dùng để làm gì: Gom các thông báo của một ứng dụng và tóm tắt thành một thông báo ngắn hiện trên màn hình khóa, nhằm giảm gián đoạn cho người dùng.
- Vấn đề hoặc sự kiện đáng chú ý: Một thông báo tóm tắt hiển thị "Luigi Mangione shoots himself; Syrian mother hopes Assad pays the price; South Korea police raid Yoon Suk Yeol's office". Nội dung về Mangione là sai. BBC khiếu nại Apple vào tháng 12/2024, nhưng Apple chỉ phản hồi vào tháng 1/2025, hứa cập nhật phần mềm để làm rõ vai trò của AI trong các bản tóm tắt. Theo báo cáo của nhà báo và người dùng mạng xã hội mà BBC dẫn lại, tính năng cũng tóm tắt sai tiêu đề của Sky News, New York Times và Washington Post. Các tổ chức báo chí và Phóng viên Không Biên giới (RSF) gây áp lực yêu cầu rút tính năng. Sau đó Apple tạm tắt tóm tắt cho nhóm ứng dụng News & Entertainment trong các bản beta iOS 18.3, iPadOS 18.3 và macOS Sequoia 15.3, và hiển thị tóm tắt của các ứng dụng khác bằng chữ nghiêng. Phát ngôn viên Apple nói hãng đang cải tiến và sẽ cập nhật trong một bản phần mềm tương lai. Theo TechCrunch, Apple còn thêm cảnh báo "may contain errors". Ngày chính xác của thông báo Mangione: BBC chỉ nói khiếu nại vào tháng 12/2024, 9to5Mac đăng bài ngày 13/12/2024.
- Số liệu có nguồn: Ít nhất 4 tổ chức tin tức (BBC, Sky News, New York Times, Washington Post) bị tóm tắt tiêu đề sai, theo BBC News ngày 17/01/2025. BBC dẫn lại báo cáo của nhà báo và người dùng mạng xã hội cho 3 tổ chức sau, chưa được kiểm chứng độc lập. Ở vụ Mangione, 1 trong 3 tiêu đề được gộp bị tóm tắt sai (hai tiêu đề còn lại về Syria và Hàn Quốc được tóm tắt đúng), theo 9to5Mac ngày 13/12/2024. Về thời gian phản hồi: BBC khiếu nại tháng 12/2024, Apple trả lời tháng 1/2025. Chưa tìm thấy nguồn công bố tỷ lệ lỗi hay số bản tóm tắt sai của tính năng, nên bài không đưa ra tỷ lệ lỗi tổng thể.
- Nguồn:
  - "Apple Intelligence botched a notification summary about Luigi Mangione, and the BBC isn't happy" — 9to5Mac — 13/12/2024 — https://9to5mac.com/2024/12/13/apple-intelligence-summary-luigi-mangione/
  - "Apple pauses AI notification summaries for news after generating false alerts" — TechCrunch — 16/01/2025 — https://techcrunch.com/2025/01/16/apple-pauses-ai-notification-summaries-for-news-after-generating-false-alerts/
  - "Apple suspends error-strewn AI generated news alerts" — BBC News — 17/01/2025 — https://www.bbc.com/news/articles/cq5ggew08eyo
- Phân biệt bằng chứng và nhận định: Các nguồn (BBC News, TechCrunch, 9to5Mac) xác nhận bản tóm tắt sai, việc BBC khiếu nại, việc Apple phản hồi chậm và việc Apple tạm tắt tính năng cho nhóm ứng dụng tin tức. Việc tóm tắt sai tiêu đề của Sky News, New York Times và Washington Post chỉ dựa trên báo cáo của nhà báo và mạng xã hội mà BBC dẫn lại. Nhận định rằng lỗi làm tổn hại uy tín các tòa soạn là phân tích của biên tập viên công nghệ Zoe Kleinman (BBC), không phải số liệu đo được. Phần suy luận của tôi là nguyên nhân kỹ thuật (mô hình gộp nhiều tiêu đề rồi diễn giải sai), vì Apple chưa công bố cách tính năng hoạt động. Chưa có nguồn xác nhận người dùng nào bị thiệt hại cụ thể.

#### Harm Map Worksheet

| Trường | Phân tích của tôi |
| --- | --- |
| High-risk moment | Thông báo tóm tắt do AI tạo hiện trên màn hình khóa dưới tên BBC News, nói về một vụ án đang được chú ý. Người đọc tiếp nhận ngay mà chưa mở bài gốc. |
| Stakeholder bị ảnh hưởng | Người dùng iPhone nhận thông báo; BBC (uy tín, thương hiệu); người được nhắc đến trong tin (người bị buộc tội); công chúng nói chung. |
| Failure mode | Hallucination: bản tóm tắt nêu một sự việc không có trong bài gốc. Có thể kèm Over-reliance, vì thông báo mang tên BBC nên người đọc dễ tin. |
| Layer bắt đầu lỗi | UX là chính: bản tóm tắt AI hiện trong thông báo gắn thương hiệu BBC nên dễ bị đọc như nội dung do BBC viết. Căn cứ: bài BBC nhấn mạnh tiêu đề sai hiển thị cạnh logo của tòa soạn; Apple sau đó sửa ở lớp giao diện (chữ nghiêng, nhãn "may contain errors") và tắt tính năng cho nhóm ứng dụng tin tức. Model là phụ: chuyên gia Jonathan Bright (Alan Turing Institute) nói hallucination là mối lo có thật và hiện chưa có cách đảm bảo ngoài giám sát của con người. Nhưng Apple chưa công bố dữ liệu nội bộ, nên với Model tôi ghi "chưa đủ bằng chứng", chỉ là giả thuyết của tôi. |
| Harm xảy ra là gì? | Đã xảy ra (có nguồn): bản tóm tắt sai về Mangione được hiển thị dưới tên BBC, BBC và RSF phản đối, Apple phải tạm dừng tính năng cho nhóm ứng dụng tin tức. Theo báo cáo BBC dẫn lại, lỗi tương tự cũng xảy ra với Sky News, New York Times và Washington Post. Chưa có nguồn xác nhận: người dùng cụ thể bị ảnh hưởng thế nào, uy tín các tòa soạn giảm bao nhiêu. Phần này là nguy cơ: người dùng tin thông tin sai, tòa soạn bị mất uy tín. |
| Harm lens | Misinformation (thông tin sai). |
| Severity | Medium |
| Scale | Medium. Tính năng là tùy chọn và chỉ có trên các iPhone mới nhất (theo BBC), nên phạm vi hẹp hơn toàn bộ người dùng iPhone. Nhưng lỗi xuất hiện ở ít nhất 4 tổ chức tin tức. Chưa có số liệu về số người nhận bản tóm tắt sai. Đây là đánh giá của tôi. |
| Probability | Medium. BBC mô tả tính năng mắc lỗi lặp lại ("repeated mistakes") và lỗi được ghi nhận ở nhiều tổ chức, nhưng không có tỷ lệ lỗi đo được. Đây là đánh giá của tôi. |
| Frequency | Medium. Lỗi lặp lại trong khoảng 12/2024 – 1/2025 và ở nhiều tổ chức tin tức theo BBC; chưa có số liệu tần suất. |
| Vì sao? | Severity Medium vì nội dung sai là tin nhạy cảm (một người bị buộc tội "tự bắn mình") và bị gắn cạnh logo tòa soạn, nhưng không có nguồn xác nhận hậu quả thể chất. Apple phản hồi chậm (BBC khiếu nại tháng 12/2024, Apple trả lời tháng 1/2025 và chỉ tạm dừng sau áp lực của nhiều tổ chức), nên rủi ro kéo dài ít nhất vài tuần. Scale, Probability và Frequency là đánh giá định tính của tôi do thiếu số liệu. Severity không tự động kéo theo Probability cao. |

### 3. Case study 2 — Nghiên cứu EBU/BBC: trợ lý AI diễn giải sai tin tức (2025)

#### Brief Case

- Tổ chức / sản phẩm AI: EBU (Liên minh Phát thanh Truyền hình châu Âu) phối hợp BBC và 22 tổ chức truyền thông dịch vụ công. Các sản phẩm được kiểm tra là ChatGPT, Copilot, Gemini và Perplexity.
- Thời gian, địa điểm / bối cảnh: Báo cáo công bố tháng 10/2025 (EBU đăng ngày 21/10/2025). Nghiên cứu có 22 tổ chức truyền thông dịch vụ công, 18 quốc gia và 14 ngôn ngữ (tr.6). Phản hồi của các trợ lý được tạo vào cuối tháng 5 và đầu tháng 6/2025, dùng phiên bản miễn phí của ChatGPT, Copilot, Perplexity và Gemini (tr.7).
- AI được dùng để làm gì: Trả lời câu hỏi về tin tức và thời sự.
- Vấn đề hoặc sự kiện đáng chú ý: Báo cáo dùng 30 câu hỏi "cốt lõi" chọn từ câu hỏi thật của khán giả; các tổ chức có thể thêm câu hỏi tùy chỉnh, tổng cộng 3.113 câu hỏi (tr.7, 10). Nhà báo của các đài tham gia chấm 2.709 câu trả lời cho câu hỏi cốt lõi (từ tối đa 2.760 sau khi loại phần bị từ chối hoặc không tạo được; tr.8) theo 5 tiêu chí: chính xác, nguồn trích dẫn, phân biệt ý kiến với sự thật, thêm quan điểm ngoài nguồn và ngữ cảnh. Kết quả cho thấy lỗi mang tính hệ thống ở mọi trợ lý và tổ chức tham gia (tr.3), nhưng mức độ khác nhau giữa các tổ chức: 26% đến 67% câu trả lời có vấn đề đáng kể. Báo cáo nói rõ nghiên cứu không được thiết kế để so sánh giữa các quốc gia hay ngôn ngữ (tr.40).
- Số liệu có nguồn: 45% trong 2.709 câu trả lời có ít nhất một vấn đề đáng kể ("significant"), và 81% có vấn đề ở mức "some" hoặc "significant" (tr.9). Nguồn trích dẫn là nguyên nhân lớn nhất với 31% câu trả lời, gồm thông tin không được nguồn hỗ trợ, không có nguồn, hoặc tuyên bố về nguồn sai hay không kiểm chứng được; tiếp theo là độ chính xác 20% và ngữ cảnh 14% (tr.10). Theo từng trợ lý, tỷ lệ có vấn đề đáng kể là Gemini 76%, Copilot 37%, ChatGPT 36%, Perplexity 30% (tr.10). Riêng về nguồn, Gemini 72% so với ChatGPT 24%, Perplexity và Copilot cùng 15% (tr.10). Cỡ mẫu: Copilot n=675, ChatGPT n=678, Perplexity n=681, Gemini n=675 (tr.9). So sánh BBC với chính BBC, tỷ lệ có vấn đề đáng kể giảm từ 51% (vòng 1, 2/2025) xuống 37% (tr.3). Số liệu đo trên câu hỏi cốt lõi, phiên bản miễn phí, theo đánh giá của nhà báo, nguồn: EBU và BBC, 10/2025.
- Nguồn:
  - "News Integrity in AI Assistants: An international PSM study" (báo cáo đầy đủ, PDF) — EBU và BBC — 10/2025 — https://www.ebu.ch/files/live/sites/ebu/files/Publications/Intelligence/open/EBU-Intelligence-BBC_News_Integrity_in_AI_Assistants_Report_2025.pdf — các trang 3, 6–10, 40
  - "News Integrity in AI Assistants" (trang giới thiệu báo cáo) — EBU — 21/10/2025 — https://www.ebu.ch/research/open/report/news-integrity-in-ai-assistants
- Phân biệt bằng chứng và nhận định: Báo cáo xác nhận các tỷ lệ lỗi trên mẫu 2.709 câu trả lời do nhà báo chấm, ở phiên bản miễn phí của trợ lý, thu thập cuối tháng 5 và đầu tháng 6/2025. Báo cáo không đo hậu quả với người dùng thật, và nói rõ nghiên cứu không được thiết kế để so sánh giữa các quốc gia hay ngôn ngữ (tr.40). Nhận định của tôi: nguyên nhân chính nằm ở khâu dẫn nguồn (Grounding), vì báo cáo ghi nhận vấn đề về nguồn là loại lỗi lớn nhất (31%). Việc người dùng thực tế bị ảnh hưởng thế nào là suy luận của tôi, không phải kết quả đo.

#### Harm Map Worksheet

| Trường | Phân tích của tôi |
| --- | --- |
| High-risk moment | Người dùng hỏi trợ lý AI về một sự kiện thời sự, nhận câu trả lời nghe có vẻ chắc chắn kèm nguồn, rồi dùng luôn mà không mở nguồn kiểm tra. |
| Stakeholder bị ảnh hưởng | Người dùng dùng trợ lý AI để đọc tin; tổ chức tin tức bị trích hoặc gán sai nội dung; công chúng nói chung. Theo Reuters Institute Digital News Report 2025 (khảo sát 48 quốc gia, được dẫn trong báo cáo EBU/BBC, tr.6), 7% người dùng trợ lý AI để đọc tin hằng tuần, tăng lên 15% ở nhóm dưới 25 tuổi. Một khảo sát khác ở 6 quốc gia cho số thấp hơn: 6% hằng tuần (tr.6). Báo cáo EBU/BBC nhấn mạnh các tổ chức tin tức đặc biệt lo ngại khi câu trả lời gán sai một tuyên bố cho họ (tr.3). |
| Failure mode | Hallucination (lỗi chính xác ở 20% câu trả lời, gồm thông tin bịa hoặc lỗi thời theo mô tả của EBU) và trích nguồn sai hoặc thiếu (31%): thông tin không được nguồn hỗ trợ, không có nguồn, hoặc tuyên bố về nguồn sai hay không kiểm chứng được (tr.10). Kèm Over-reliance ở phía người dùng. |
| Layer bắt đầu lỗi | Grounding là chính: vấn đề nguồn là nhóm lỗi lớn nhất (31%, tr.10), tức câu trả lời không dựa đúng vào nguồn được trích. Gemini nổi bật với 72% câu trả lời có vấn đề về nguồn so với tối đa 24% ở các trợ lý còn lại (tr.10). UX là phụ: trích dẫn trông đáng tin nên người dùng dễ bỏ qua bước kiểm tra. Với kiến trúc cụ thể của từng trợ lý tôi ghi "chưa đủ bằng chứng", vì nghiên cứu đo đầu ra chứ không công bố cách các hệ thống hoạt động bên trong. |
| Harm xảy ra là gì? | Đã đo được: câu trả lời sai, thiếu nguồn hoặc lỗi thời ở tỷ lệ nêu trên. Phần này là nguy cơ: người dùng nhận thông tin sai về thời sự, và tổ chức tin tức bị gán sai nội dung. Nghiên cứu không đo hậu quả thực tế với người dùng. |
| Harm lens | Misinformation (thông tin sai). |
| Severity | Medium. Mỗi câu trả lời sai thường gây hại vừa phải, không phải thiệt hại nghiêm trọng đến thể chất. |
| Scale | High. Lỗi xuất hiện ở cả 4 trợ lý phổ biến. Người dùng trợ lý AI để đọc tin là thiểu số (7% hằng tuần, 15% ở nhóm dưới 25 tuổi, tr.6) nhưng ở quy mô toàn cầu là số lượng lớn, và báo cáo mô tả vai trò của trợ lý AI đang ngày càng tăng. Đây là đánh giá của tôi. |
| Probability | High, tính trên mẫu: 45% trong 2.709 câu trả lời có ít nhất một vấn đề đáng kể (tr.9). Tỷ lệ đang cải thiện: so sánh BBC với chính BBC giảm từ 51% xuống 37% (tr.3), nhưng vẫn cao. Lưu ý đây là xác suất câu trả lời lỗi, không phải xác suất người dùng bị hại thực tế. |
| Frequency | High. Báo cáo ghi nhận lỗi mang tính hệ thống ở mọi trợ lý và tổ chức tham gia (tr.3), nhưng khác nhau nhiều giữa các tổ chức: 26% đến 67% (tr.40). Chưa có số liệu về tần suất người dùng gặp lỗi trong thực tế. |
| Vì sao? | Severity Medium vì từng câu trả lời sai chủ yếu gây hiểu sai thông tin, không gây tổn hại thể chất. Probability và Frequency cao vì tỷ lệ lỗi đo được lớn và xuất hiện ở mọi trợ lý và tổ chức tham gia. Scale dựa trên số người dùng trợ lý AI để đọc tin và là đánh giá của tôi. Giới hạn: nghiên cứu đo câu trả lời của phiên bản miễn phí vào tháng 5–6/2025, không đo hậu quả với người dùng, và không được thiết kế để so sánh giữa quốc gia (tr.40). Mỗi tổ chức chỉ đánh giá khoảng 30 câu trả lời cho mỗi trợ lý (tr.40). |
