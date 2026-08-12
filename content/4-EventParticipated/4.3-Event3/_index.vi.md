---
title: "AWS FCAJ Agent Forge - Deepdive"
date: 2026-08-01
weight: 3
chapter: false
pre: " <b> 4.3. </b> "
---

# Bài thu hoạch: "AWS FCAJ Agent Forge - Deepdive"

### Mục Đích Của Sự Kiện

- Giới thiệu và định nghĩa các khái niệm cốt lõi trong kỷ nguyên GenAI mới: **RAG** (Retrieval-Augmented Generation), **Agentic AI** (Trí tuệ nhân tạo dạng Agent), và **Graph RAG** (RAG dựa trên đồ thị tri thức).
- Tiếp cận các xu hướng Generative AI và AI Agent mới nhất trên nền AWS, đồng thời khai mở tư duy logic và kỹ năng giải quyết vấn đề đột phá cho các "Builder".
- Giúp người học nắm bắt cách đưa các giải pháp AI từ giai đoạn nghiên cứu, thử nghiệm (PoC) lên môi trường thực tế của doanh nghiệp một cách tối ưu và an toàn.

### Danh Sách Diễn Giả

- **Chị Lâm Hoàng Cát Vy** – Senior Systems Analyst - AI Platform Owner - IT Young Talents Program Manager.
- **AWS Study Group** – Đơn vị tổ chức (Host).

---

### Nội Dung Nổi Bật

#### 1. Định nghĩa RAG (Retrieval-Augmented Generation)
- **Khái niệm:** RAG là kỹ thuật tối ưu hóa đầu ra của Large Language Model (LLM) bằng cách truy xuất dữ liệu từ một nguồn tri thức bên ngoài đáng tin cậy (như database nội bộ hoặc tài liệu doanh nghiệp) trước khi sinh câu trả lời.
- **Vai trò:** Giúp mô hình LLM trả lời chính xác, cập nhật thông tin thời gian thực và hạn chế tối đa hiện tượng "ảo giác" (hallucination) mà không cần tốn chi phí fine-tune mô hình.

#### 2. Agentic AI & Trí tuệ tự chủ
- **Khái niệm:** Agentic AI đại diện cho lớp ứng dụng AI có tính tự chủ cao (Autonomous Agents). Không chỉ dừng lại ở việc hỏi - đáp đơn thuần, Agentic AI có khả năng tự lập luận, lên kế hoạch từng bước, và tự động gọi các công cụ (Tools/APIs) để hoàn thành các mục tiêu phức tạp.
- **Khả năng phối hợp:** Xu hướng Multi-Agent (Nhiều Agent cộng tác) cho phép phân tách các công việc lớn thành các task nhỏ và giao cho các Agent chuyên biệt xử lý tự động.

#### 3. Graph RAG - Bước tiến vượt trội
- **Khái niệm:** Graph RAG là sự kết hợp nâng cao giữa RAG truyền thống và Đồ thị tri thức (Knowledge Graph).
- **Cơ chế:** Dữ liệu phi cấu trúc được phân tích để trích xuất các thực thể (Entities) và mối quan hệ (Relationships) giữa chúng, tạo thành một mạng lưới tri thức liên kết chặt chẽ.
- **Điểm ưu việt:** Giúp LLM hiểu rõ ngữ cảnh toàn cục, kết nối các thông tin rời rạc trong hàng nghìn tài liệu để trả lời các câu hỏi mang tính tổng hợp cao mà RAG truyền thống thường bỏ sót.

#### 4. Giải pháp triển khai trên hạ tầng AWS
- Sử dụng **Amazon Bedrock** để kết nối linh hoạt với các mô hình ngôn ngữ lớn hàng đầu (Claude 3.5 Sonnet, Amazon Nova...).
- Thiết lập **Amazon Bedrock Knowledge Bases** để tự động hóa quy trình RAG (Chunking, Embedding, Vector Storage).
- Tích hợp **Amazon Neptune** hoặc các database hỗ trợ đồ thị để lưu trữ Graph dữ liệu cho các giải pháp Graph RAG quy mô lớn.

---

### Những Gì Học Được

#### Tư duy thiết kế & Giải quyết vấn đề
- **Khai mở tư duy logic:** Học cách tiếp cận hệ thống, phân tích vấn đề và cấu trúc dữ liệu theo dạng thực thể - mối quan hệ để áp dụng hiệu quả vào mô hình Graph RAG.
- **Đột phá kỹ năng giải quyết vấn đề:** Hiểu cách kết hợp linh hoạt giữa RAG truyền thống, Graph RAG và Agentic AI để giải quyết triệt để các bài toán nghiệp vụ phức tạp của doanh nghiệp.

#### Kiến trúc kỹ thuật
- Nắm rõ sự khác biệt bản chất và trường hợp sử dụng tối ưu của RAG (phù hợp câu hỏi chi tiết, cục bộ) và Graph RAG (phù hợp câu hỏi bao quát, tổng hợp mối quan hệ).
- Làm chủ cách thiết kế vòng lặp Lập luận - Lập kế hoạch - Thực thi của AI Agent trên Cloud.

---

### Ứng Dụng Vào Công Việc

- **Ứng dụng RAG & Graph RAG:** Nghiên cứu tích hợp RAG vào hệ thống tra cứu tài liệu nghiệp vụ hoặc hỗ trợ người chơi trong dự án game RPG (AI Dungeon Master). Tìm hiểu cách dựng cơ sở dữ liệu đồ thị tri thức để nâng cấp lên Graph RAG.
- **Thiết kế AI Agent tự chủ:** Áp dụng tư duy thiết kế Agentic AI vào các service backend để tự động hóa các luồng xử lý game logic phức tạp và tương tác động với người chơi.
- **Tối ưu hóa hạ tầng trên AWS:** Sử dụng hệ sinh thái AWS Bedrock để xây dựng, triển khai nhanh và vận hành an toàn các ứng dụng AI Agent Serverless.

---

### Trải nghiệm trong event

Tham gia buổi **AWS FCAJ Agent Forge - Deepdive** với sự dẫn dắt của diễn giả **Vy Lâm** đã mang lại cho tôi những trải nghiệm vô cùng quý giá:

- **Sự truyền lửa từ diễn giả:** Thông qua những chia sẻ sâu sắc, thực tế cùng với tinh thần nhiệt huyết, đầy năng lượng, chị Lâm Hoàng Cát Vy đã truyền động lực mạnh mẽ cho các "Builder". 
- **Khai mở tư duy công nghệ:** Sự kiện giúp tôi không chỉ có cơ hội để được tiếp cận các xu hướng Generative AI và AI Agent mới nhất trên nền tảng AWS mà còn được khai mở tư duy logic và kỹ năng giải quyết vấn đề một cách đột phá.
- **Nội dung bài học chất lượng:** Các ví dụ thực tế về RAG, Agentic AI và Graph RAG đã tháo gỡ nhiều thắc mắc của tôi về cách thiết kế và triển khai AI thực tế trong môi trường sản phẩm thực tế.

#### Một số hình ảnh khi tham gia sự kiện
![AWS FCAJ Agent Forge - Deepdive](hinh-anh-sk-3/IMG_20260801_091335.webp)
![AWS FCAJ Agent Forge - Deepdive](hinh-anh-sk-3/IMG_20260801_110623.webp)

> Buổi chia sẻ của chị Vy Lâm đã tiếp thêm năng lượng và định hình rõ nét tư duy thiết kế hệ thống AI Agent & RAG chuyên nghiệp cho tôi, giúp tôi sẵn sàng đón nhận và triển khai các giải pháp AI tiên tiến nhất trên nền tảng AWS.
