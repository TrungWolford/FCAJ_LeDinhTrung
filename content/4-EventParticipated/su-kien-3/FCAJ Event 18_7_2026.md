TÀI LIỆU CHI TIẾT SỰ KIỆN: AWS FCAJ AGENT FORGE - DEEPDIVE
I. TỔNG QUAN SỰ KIỆN & NGỮ CẢNH CHUYÊN MÔN
	Tên sự kiện: AWS FCAJ Agent Forge - Deepdive.
	Đơn vị tổ chức: AWS Study Group.
	Diễn giả: Chị Lâm Hoàng Cát Vy (Senior Systems Analyst - AI Platform Owner - IT Young Talents Program Manager).
	Chủ đề chính: Định nghĩa RAG (Retrieval-Augmented Generation), Agentic AI, và Graph RAG (Graph Retrieval-Augmented Generation).
	Mục tiêu đào tạo: Giúp các Builder không chỉ tiếp cận các xu hướng Generative AI và AI Agent mới nhất trên nền tảng AWS, mà còn khai mở tư duy logic và kỹ năng giải quyết vấn đề đột phá từ góc độ phân tích hệ thống doanh nghiệp thực tế.
II. NỘI DUNG LÝ THUYẾT CHI TIẾT
1. Định nghĩa RAG (Retrieval-Augmented Generation)
	Khái niệm: RAG là kỹ thuật kết hợp mô hình ngôn ngữ lớn (LLM) với một nguồn tri thức bên ngoài đáng tin cậy. Trước khi LLM sinh câu trả lời, hệ thống sẽ truy xuất (retrieve) thông tin có liên quan từ dữ liệu nội bộ và đưa vào ngữ cảnh của prompt (augment).
	Cơ chế hoạt động: Retrieve (Truy xuất từ Vector Database) -> Augment (Đưa vào prompt ngữ cảnh) -> Generate (LLM sinh phản hồi).
	Ưu điểm: Giảm thiểu hiện tượng ảo giác (hallucination), cung cấp câu trả lời có tính thời sự, chính xác cao mà không cần tốn chi phí và thời gian huấn luyện lại mô hình.
2. Agentic AI & Trí tuệ tự chủ (Autonomous Agents)
	Khái niệm: Khác với LLM thông thường chỉ phản hồi câu lệnh dạng tĩnh, Agentic AI là hệ thống phần mềm thông minh có khả năng tự chủ hoạt động (Autonomous), thực hiện chu trình: Lập luận (Reasoning) -> Lập kế hoạch (Planning) -> Thực thi (Executing) các tác vụ phức tạp nhiều bước.
	Khả năng sử dụng công cụ: Agent có thể quyết định khi nào cần gọi API bên ngoài, gửi email, truy vấn database hoặc gọi webhook để hoàn thành mục tiêu đề ra.
	Mô hình Multi-Agent: Hệ thống gồm nhiều Agent phối hợp cộng tác, phân chia nhiệm vụ chuyên biệt để tự động xử lý các luồng công việc phức tạp mà không cần con người can thiệp liên tục.
3. Graph RAG - Bước tiến đột phá kết hợp Đồ thị tri thức
	Khái niệm: Graph RAG tích hợp mô hình Đồ thị tri thức (Knowledge Graph) vào quy trình RAG truyền thống.
	Cách hoạt động: Dữ liệu phi cấu trúc (văn bản, tài liệu) được phân tích để trích xuất các Thực thể (Entities - như con người, địa điểm, khái niệm) và Mối quan hệ (Relationships) giữa chúng, tạo nên cấu trúc đồ thị mạng lưới liên kết.
	Điểm vượt trội: RAG truyền thống chỉ tìm kiếm ngữ nghĩa theo khối văn bản rời rạc (Vector Similarity). Graph RAG cho phép kết nối toàn cục các thực thể, giúp AI trả lời được những câu hỏi tổng hợp, phân tích mối liên hệ phức tạp chéo tài liệu mà RAG thông thường thường bỏ sót.
4. Triển khai kiến trúc AI tiên tiến trên AWS
	Amazon Bedrock: Đóng vai trò là nền tảng Serverless Managed Service để gọi các LLM tiên tiến nhất (Claude 3.5 Sonnet, Amazon Nova...).
	Bedrock Knowledge Bases: Tự động hóa hoàn toàn quy trình RAG từ khâu cắt nhỏ dữ liệu (Chunking), chuyển đổi vector (Embedding) đến lưu trữ vào Vector Database.
	Amazon Neptune: Database đồ thị được sử dụng để xây dựng và truy vấn mạng lưới Knowledge Graph cho các hệ thống Graph RAG quy mô lớn.
III. TƯ DUY THIẾT KẾ & GIẢI QUYẾT VẤN ĐỀ (TAKEAWAYS)
	Khai mở tư duy logic: Diễn giả Vy Lâm đã nhấn mạnh cách phân tích hệ thống dữ liệu phức tạp dưới dạng đồ thị các mối quan hệ (entities và relations). Tư duy này giúp lập trình viên không chỉ tối ưu hóa Graph RAG mà còn cải thiện kỹ năng mô hình hóa nghiệp vụ thực tế.
	Kỹ năng giải quyết vấn đề đột phá: Sự kết hợp linh hoạt giữa RAG truyền thống, Graph RAG và Agentic AI giúp thiết kế ra những giải pháp tự động hóa thông minh, giải quyết triệt để các rào cản về hiệu năng và bảo mật trong doanh nghiệp.
	Cộng tác làm việc: Định hướng cách thiết kế Multi-Agent để tối đa hóa tính cộng tác tự động giữa các hệ thống AI chuyên trách.
IV. ỨNG DỤNG THỰC TẾ TRONG DỰ ÁN
	Tích hợp RAG/Graph RAG vào Game RPG (AI Dungeon Master): Áp dụng RAG để giúp Dungeon Master AI ghi nhớ cốt truyện và thông tin thế giới game một cách chính xác. Nghiên cứu sử dụng đồ thị tri thức (Graph RAG) để quản lý các mối quan hệ phức tạp giữa NPC, bang hội, và lịch sử sự kiện của người chơi.
	Thiết kế AI Agent tự chủ: Ứng dụng mô hình Lập luận - Lập kế hoạch để xây dựng các NPC thông minh hoặc trợ lý quản trị game có khả năng gọi các API Backend (như trang bị vật phẩm, giao đấu) tự động.
	Xây dựng serverless AI trên AWS: Triển khai nhanh chóng các dịch vụ Bedrock Knowledge Bases để lưu trữ tài liệu hướng dẫn game và vận hành hệ thống AI an toàn với chi phí tối ưu nhất.
