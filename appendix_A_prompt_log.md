# Appendix A – Prompt Log

## Session 1 – 02/06/2026

### 23:14 02/06/2026 – Claude Sonnet 4.6
**Prompt:**
Từ context trên bạn hay khảo sát thị trường đi và trả lời:

1. vẽ một cái mindmap dạng văn bản phân cấp về quy trình kiểm thử chuẩn ISTQB và các hoạt động của qaqc
2. rồi hãy trích xuất và gợi ý cho tôi các keywords phổ biến nhất để tìm kiếm job trên LinkedIn hay indeed
3. nhớ là phải gợi ý thêm các từ khóa chuyên biệt để tìm các vị trí qaqc có ứng dụng AI/LLM hoặc automationAI theo xu hướng của năm 2026 nhé

**Purpose:**  Thiết kế mindmap quy trình kiểm thử ISTQB và kaays các keywords tìm việc QA/QC truyền thống và chuyên biệt AI/LLM/Automation-AI trong thị trường hiện nay và tương lai.

---

### 09:21 03/06/2026 – Gemini 1.5 Flash
**Prompt:**

Vị trí 01: [Tên vị trí tuyển dụng] (Ví dụ: Senior Manual Tester - AI Augmented)
**Đường dẫn (Link):** [Dán link trực tiếp vào đây]
**Mức lương (Salary):** 15,000,000 - 22,000,000 VND (hoặc Competitive)
**Mô tả công việc (Job Description):**
    Thực hiện thiết kế test case, test scenario cho hệ thống...
    Sử dụng các công cụ Generative AI để tối ưu hóa quy trình kiểm thử...
**Kỹ năng yêu cầu (Required Skills):** ISTQB Foundation, SQL, Prompt Engineering, ChatGPT/Claude.
**Phân tích tác động của AI (AI Impact Analysis):** Vị trí này cho thấy AI đang đóng vai trò trợ lý đắc lực giúp tăng tốc độ viết test case lên gấp 2 lần. Tuy nhiên, tư duy kiểm thử và kỹ năng xác thực tính đúng đắn của dữ liệu đầu ra từ LLM vẫn phụ thuộc hoàn toàn vào năng lực của kỹ sư con người.
*[Dán ảnh chụp màn hình minh chứng minh đã crop vừa vặn vào đây]*
Bên trên là mẫu bạn hãy điền giúp tôi thông tin của trang page đang mở lưu ý chỉ điền của riêng trang này để đánh giá job nhé đừng điền của các trang khác nhé.

**Purpose:** Phân tích về job posting cụ thể để đánh giá mức độ ứng dụng AI trong công việc QA/QC và tác động của nó đến vai trò của kỹ sư kiểm thử trong hiện tại.

---
## Session 2 – 03/06/2026

### 10:45 03/06/2026 – ChatGPT (GPT-4o)
**Prompt:**
Tôi đang cần nghiên cứu về mấy sự cố công nghệ. Bạn hãy đóng vai một chuyên gia tổng hợp thông tin
và liệt kê cho tôi danh sách đúng 20 sự cố lỗi phần mềm software defects nổi tiếng đã được công khai
trên thế giới hoặc tại Việt Nam trong giai đoạn từ năm 2022 đến năm 2026 nhé.

Yêu cầu cấu trúc danh sách bắt buộc phải có:
- Ít nhất 5 sự cố liên quan trực tiếp đến AI/LLM (như AI hallucination, prompt injection, bias, lỗi chatbot)
- Thời gian: Từ năm 2022 đến năm 2026.

Với mỗi sự cố trong số 20 sự cố, hãy trình bày rõ ràng 4 mục sau bằng tiếng Việt:
1. Tên sự cố & Năm xảy ra
2. Mô tả chi tiết lỗi kèm theo nguyên nhân cốt lõi về mặt kỹ thuật root cause
3. Mức độ nghiêm trọng và hậu quả thực tế ra sao
4. Giải pháp khắc phục của tổ chức hay công ty đó

Sau khi viết xong 4 mục trên cho mỗi sự cố, hãy viết thêm 1 dòng nhận định chuyên gia để đưa ra
một khẳng định mang tính phân tích sâu hoặc quy trách nhiệm cá nhân hoặc hệ thống về nguyên nhân
sâu xa của lỗi đó theo góc nhìn riêng của bạn nhé.

**Purpose:** Tạo ra danh sách 20 software defects 2022–2026 (trong đó ≥5 liên quan AI/LLM) làm
nội dung gốc cho Requirement 2. Output của ChatGPT được dùng như artifact đầu vào để
cross-check và kiểm định bằng Claude ở bước tiếp theo.


---

### 11:30 03/06/2026 – Claude Sonnet 4.6
**Prompt:**
```
    Bạn hãy rà soát tính xác thực lịch sử hãy kiểm tra xem có sự cố nào trong danh sách trên không có thật ngoài đời hay là sai lệch hoàn toàn về mốc thời gian hay bản chất kỹ thuật trong giai đoạn 2022-2026 hay không. Nếu có, hãy chỉ rõ ra cho tôi nhé và thêm nữa
    tìm lỗi ảo tưởng định kiến (AI Hallucination/Bias) cho từng Entry đó nữa đối với 20 entry sự cố ở trên, hãy phân tích kỹ câu trả lời của AI đó đặc biệt là phần mô tả lỗi và nhận định chuyên gia. Với mỗi entry, hãy chỉ ra giúp tôi 1 điểm mà đoạn văn trên đã giải thích chưa chính xác, bị hallucinate, thiếu thôngtin cốt lõi, hoặc có định kiến đổ lỗi sai mục tiêu bias.

    Hãy trình bày kết quả tìm lỗi AI này dưới dạng danh sách trên theo cấu trúc:
    - Sự cố X:
    - Điểm AI giải thích sai/định kiến: sai chỗ nào đúng theo thực tế hoặc thiếu thông tin gì
```
**Purpose:** Dùng Claude làm công cụ cross-check độc lập (second opinion) để kiểm định output của ChatGPT — phát hiện hallucination, false attribution, bias và thiếu thông tin trong từng entry.


## Session 3 – 04/06/2026
### 08:00 04/06/2026 – ChatGPT (GPT-4o)
**Prompt:**
```
    Sinh 15 test case cho quạt đứng nhỏ 3 nút bấm cơ học tốc độ, có chế độ xoay, không có remote hiệu yanfan
```
**Purpose:** Tạo 15 test case cho thiết bị quạt đứng nhỏ 3 nút bấm cơ học tốc độ, có chế độ xoay, không có remote hiệu yanfan.