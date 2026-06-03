# AI Audit Report 
## Entry 1: ISTQB Process Mindmap

**Date of Audit:** 2026-06-02 

**Target AI Model:** Claude-4.6-Sonnet

**Task:** Đánh giá lại và điều chỉnh mindmap của quy trình kiểm thử phần mềm theo chuẩn ISTQB do AI tạo ra, phân tích các lỗi sai và đề xuất cách sửa chữa.

---
### (1) Prompt + Tool 
**Tool used:** Claude-4.6-Sonnet
**Timestamp:** 23:14 02/06/2026
**Prompt:**
Từ context trên bạn hay khảo sát thị trường đi và trả lời:
1. vẽ một cái mindmap dạng văn bản phân cấp về quy trình kiểm thử chuẩn ISTQB và các hoạt động của qaqc
2. rồi hãy trích xuất và gợi ý cho tôi các keywords phổ biến nhất để tìm kiếm job trên LinkedIn hay indeed
3. nhớ là phải gợi ý thêm các từ khóa chuyên biệt để tìm các vị trí qaqc có ứng dụng AI/LLM hoặc automationAI theo xu hướng của năm 2026 nhé

### (2) AI Output  

1. ISTQB Testing Process Mindmap
```
QA/QC & Software Testing (ISTQB)
│
├── 1. Test Planning
│   ├── Define test objectives & scope
│   ├── Risk analysis & prioritization
│   ├── Test strategy & approach
│   ├── Resource & schedule planning
│   └── Entry/Exit criteria definition
│
├── 2. Test Monitoring & Control
│   ├── Track test progress vs plan
│   ├── Defect metrics & reporting
│   └── Corrective actions
│
├── 3. Test Analysis
│   ├── Review test basis (requirements, specs)
│   ├── Identify test conditions
│   └── Analyze testability
│
├── 4. Test Design
│   ├── Black-box techniques
│   │   ├── Equivalence Partitioning
│   │   ├── Boundary Value Analysis
│   │   ├── Decision Table
│   │   ├── State Transition
│   │   └── Use Case Testing
│   ├── White-box techniques
│   │   ├── Statement Coverage
│   │   ├── Branch Coverage
│   │   └── Path Coverage
│   └── Experience-based
│       ├── Exploratory Testing
│       ├── Error Guessing
│       └── Checklist-based
│
├── 5. Test Implementation
│   ├── Create test cases & test scripts
│   ├── Prepare test data
│   ├── Set up test environment
│   └── Prioritize test execution order
│
├── 6. Test Execution
│   ├── Run test cases (manual / automated)
│   ├── Log actual results
│   ├── Report & track defects
│   └── Regression testing
│
├── 7. Test Completion
│   ├── Evaluate exit criteria
│   ├── Write test summary report
│   ├── Archive test artifacts
│   └── Lessons learned
│
└── QA/QC Roles
    ├── QA Engineer – process & prevention
    ├── QC Engineer – product & detection
    ├── Test Lead / Test Manager
    ├── Automation Engineer
    ├── Performance Tester
    └── AI/LLM Test Engineer (2026+)
```
2. Keywords tìm job QA/QC trên LinkedIn / Indeed
```
Vị trí phổ biến:
QA Engineer
QC Engineer
Software Tester
Test Engineer
Quality Assurance Engineer
Manual Tester
Automation Tester
SDET (Software Development Engineer in Test)
Test Lead
QA Manager
```
Kết hợp với địa điểm:
```
QA Engineer Vietnam
Software Tester Ho Chi Minh
QA Engineer Remote Vietnam
```
3. Keywords chuyên biệt AI/LLM/Automation-AI 2026
```
AI-augmented testing roles:
AI Test Engineer
LLM QA Engineer
Prompt Testing Engineer
AI Quality Engineer
Generative AI Tester
ML Model Tester
```
Tool/Framework keywords:
```
Selenium + AI
Playwright automation
Cypress automation
AI-powered testing
Testim
Mabl
Applitools
DeepEval
Promptfoo
LLM evaluation
```
Skill keywords để filter job có AI:
```
"AI testing" QA
"LLM" tester
"prompt engineering" QA
"ChatGPT" automation
"Copilot" testing
"generative AI" quality
"RAG" testing
"hallucination testing"
"model evaluation"
```
Search string gợi ý cho LinkedIn:
```
(QA OR "quality assurance") AND (AI OR LLM OR "generative AI")
"AI testing" engineer Vietnam
"automation AI" QA 2025 2026
```

### (3) Verdict:
Chưa hoàn thiện và còn sai sót nhỏ về mặt phân cấp vai trò cấu trúc, vận hành theo slide.

### (4) Audit Table

| No. | AI Output Component | Identified Mistake / Defect | Reasoning & Evidence (Syllabus/ISTQB) | Student's Corrective Fix |
|:---|:---|:---|:---|:---|
| 1 | `4. Test Design` ─> `White-box techniques` | Sai phân cấp vai trò Role Misalignmen vì AI liệt kê các kỹ thuật cấu trúc hộp trắng (Statement, Branch, Path Coverage) ngang hàng với kỹ thuật hộp đen trong quy trình thiết kế của Tester. | Theo slide bài giảng lý thuyết và chuẩn ISTQB, kiểm thử White-box yêu cầu can thiệp sâu vào mã nguồn, thuộc trách nhiệm chính của **Developer** ở mức độ Unit Test. Tester/QC Engineer thông thường chỉ tập trung vào Black-box và Experience-based ở mức System Test. | Di chuyển nhánh White-box ra một vùng bổ trợ độc lập, đính kèm chú thích rõ ràng là "Primarily conducted by Developers during Unit Testing" để tránh chồng chéo nhập nhằng phạm vi công việc. |
| 2 | `Test Completion` ─> `Evaluate exit criteria` | Sequential Logic Error vì AI cho rằng hoạt động đánh giá Exit Criteria vào giai đoạn hoàn thành kiểm thử. | Theo slide bài giảng lý thuyết trên lớp thì việc đánh giá Exit Criteria phải diễn ra liên tục trong mạch **Test Monitoring & Control** hoặc cuối giai đoạn **Test Execution** để quyết định xem có dừng test hay không. Khi đã qua bước `Test Completion` thì cái tiêu chí thoát phải thỏa mãn xong xuôi và tester chỉ làm công tác hậu cần. | Chuyển dịch vị trí của `Evaluate exit criteria` từ mục số `Test Completion` lên mục `Test Monitoring & Control` cho đúng logic hoạt động cốt lõi của chuẩn ISTQB. |
| 3 | Nhánh độc lập `QA/QC Roles` ở cuối sơ đồ | Đứt gãy liên kết cấu trúc vì AI tự tách một nhánh riêng để liệt kê danh từ các Job Title (Automation, Performance, AI Engineer...) mà không gắn vào hành động cụ thể. | Theo yêu cầu vẽ sơ đồ tư duy về quy trình ISTQB gắn với vai trò của QA/QC. Việc liệt kê chức danh một cách rời rạc, thụ động ở cuối sơ đồ làm mất đi giá trị mapping vào thực tế, khiến cấu trúc tổng thể bị khó đọc, khó quan sát trực quan. | Xóa bỏ nhánh độc lập đó. Đưa trực tiếp các Roles này vào từng hành động cụ thể ở 7 bước trên (Ví dụ: Đưa Automation Engineer vào mục `Test Implementation` phụ trách viết test script). |

---

### (5) Student Fix 

```text
QA/QC & Kiểm thử phần mềm (Quy trình chuẩn ISTQB)
│
├── 1. Test Planning
│   ├── Xác định mục tiêu & phạm vi kiểm thử
│   ├── Phân tích rủi ro & ưu tiên hóa
│   ├── Xây dựng Test Strategy & Test Approach
│   └── Lên kế hoạch nguồn lực & lịch trình
│   [Owner: QA | Executor: Test Lead / Test Manager]
│
├── 2. Test Monitoring & Control
│   ├── Theo dõi tiến độ so với kế hoạch
│   ├── Đo lường Defect Metrics & báo cáo
│   └── *** Đánh giá Exit Criteria (liên tục)
│   [Owner: QA | Executor: Test Lead / Test Manager]
│
├── 3. Test Analysis
│   ├── Xem xét Test Basis (yêu cầu, đặc tả)
│   ├── Xác định Test Conditions
│   └── Phân tích Testability
│   [Owner: QA | Executor: QC Engineer]
│
├── 4. Test Design
│   ├── Kỹ thuật Black-box
│   │   ├── Equivalence Partitioning & Boundary Value Analysis
│   │   └── Decision Table & State Transition Testing
│   └── Kỹ thuật Experience-based
│       └── Exploratory Testing & Error Guessing
│   [Owner: QC | Executor: QC Engineer / Manual Tester]
│
├── 5. Test Implementation
│   ├── Chuẩn bị Test Data & môi trường kiểm thử
│   ├── Xây dựng Automation Scripts
│   └── Sắp xếp thứ tự ưu tiên thực thi
│   [Owner: QC | Executor: QC Engineer / Automation Engineer]
│
├── 6. Test Execution
│   ├── Thực thi thủ công
│   ├── Thực thi Automation Scripts
│   ├── Load / Stress / Endurance Testing
│   └── Đánh giá thành phần AI/LLM
│   [Owner: QC | Executor: Manual Tester / Automation Engineer / Performance Tester / AI-LLM Test Engineer]
│
├── 7. Test Completion
│   ├── Viết Test Summary Report
│   ├── Lưu trữ Test Artifacts
│   └── Lessons Learned / Retrospective
│   [Owner: QA | Executor: Test Lead / Test Manager]
│
└── Phụ lục: White-box Testing
    └── Statement, Branch, Path Coverage
    [Owner: Dev | Executor: Developer — Unit Testing, ngoài phạm vi Tester]
```

## Entry 2: Job Analysis/ AI replacement
**Date of Audit:** 2026-06-03

**Target AI Model:** Gemini 1.5 Flash

**Task:** Phân tích một job posting cụ thể để đánh giá mức độ ứng dụng AI trong công việc QA/QC và tác động của nó đến vai trò của kỹ sư kiểm thử trong hiện tại.

---
### (1) Prompt + Tool
```
**Tool used:** Gemini 1.5 Flash
**Timestamp:** 09:21 03/06/2026
**Prompt:**
Vị trí 01: [Tên vị trí tuyển dụng] (Ví dụ: Senior Manual Tester - AI Augmented)
**Đường dẫn (Link):** [Dán link trực tiếp vào đây]
**Mức lương (Salary):** 15,000,000 - 22,000,000 VND (hoặc Competitive)
**Mô tả công việc (Job Description):**
    Thực hiện thiết kế test case, test scenario cho hệ thống...
    Sử dụng các công cụ Generative AI để tối ưu hóa quy trình kiểm thử...
**Kỹ năng yêu cầu (Required Skills):** ISTQB Foundation, SQL, Prompt Engineering, ChatGPT/Claude.
**Phân tích tác động của AI (AI Impact Analysis):** Vị trí này cho
thấy AI đang đóng vai trò trợ lý đắc lực giúp tăng tốc độ viết test case lên gấp 2 lần. Tuy nhiên, tư duy kiểm thử và kỹ năng xác thực tính đúng đắn của dữ liệu đầu ra từ LLM vẫn phụ thuộc hoàn toàn vào năng lực của kỹ sư con người
*[Dán ảnh chụp màn hình minh chứng minh đã crop vừa vặn vào đây]*
Bên trên là mẫu bạn hãy điền giúp tôi thông tin của trang page đang mở lưu ý chỉ điền của riêng trang này để đánh giá job nhé đừng điền của các trang khác nhé.
```

### (2) AI Output
```
    ### Vị trí 01: Process Quality Assurance (QA QC, Agile/Scrum, Jira)
    * **Đường dẫn (Link):** [https://itviec.com/it-jobs/process-quality-assurance-qa-qc-agile-scrum-jira-sabitech-cong-ty-co-phan-cong-nghe-sabi-1415?lab_feature=preview_jd_page]
    * **Mức lương (Salary):** 800 - 1,300 USD
    * **Mô tả công việc (Job Description):**
        - Theo dõi và đảm bảo các dự án tuân thủ quy trình phát triển phần mềm và quy định chất lượng của công ty.
        - Phối hợp với PM/Team để kiểm soát tiến độ, chất lượng và quản lý các rủi ro trong quá trình triển khai dự án.
        - Theo dõi task, timeline, quality checkpoints và hỗ trợ thúc đẩy dự án vận hành đúng kế hoạch.Hỗ trợ kiểm tra, đánh giá process compliance và đề xuất cải tiến nhằm nâng cao hiệu quả vận hành dự án.
        - Hỗ trợ triển khai, đào tạo và duy trì các quy trình nội bộ, tiêu chuẩn chất lượng trong công ty.
        - Phối hợp với các bộ phận liên quan để nâng cao chất lượng sản phẩm và tối ưu quy trình làm việc.
    * **Kỹ năng yêu cầu (Required Skills):** ISTQB Foundation, SQL, Prompt Engineering, ChatGPT/Claude.
    * **Phân tích tác động của AI (AI Impact Analysis):** Vị trí PQA (Process Quality Assurance) tập trung mạnh vào việc giám sát quy trình, giao tiếp liên phòng ban và thúc đẩy con người. AI hiện nay có thể hỗ trợ vị trí này trong việc tự động hóa thu thập dữ liệu báo cáo, phân tích biểu đồ tiến độ (Jira/Excel) hoặc dự đoán rủi ro chậm deadline dựa trên lịch sử dự án. Tuy nhiên, các kỹ năng cốt lõi như đánh giá độ tuân thủ (compliance), xử lý xung đột giữa các team, đào tạo quy trình nội bộ và tư duy cải tiến hệ thống tinh gọn vẫn đòi hỏi sự khéo léo, trí tuệ cảm xúc (EQ) và năng lực quản trị của con người mà AI chưa thể thay thế.

    ### Vị trí 01: Senior/Lead QA Engineer (QE, QC, Automation)
    * **Đường dẫn (Link):** [https://itviec.com/it-jobs/senior-lead-qa-engineer-qe-qc-automation-pizza-hut-digital-technology-3057?lab_feature=preview_jd_page]
    * **Mức lương (Salary):** Negotiable
    * **Mô tả công việc (Job Description):**
        - Xác định và thúc đẩy chiến lược kiểm thử tổng thể cũng như các tiêu chuẩn chất lượng cho nền tảng thương mại điện tử Byte by Yum!.
        - Dẫn dắt chiến lược tự động hóa (automation), đảm bảo các framework kiểm thử có khả năng mở rộng và dễ bảo trì trên cả nền tảng web và thiết bị di động.
        - Thiết lập các thực hành tốt nhất (best practices) cho kiểm thử chức năng, tích hợp, đầu cuối (end-to-end) và kiểm thử hiệu năng.
        - Hỗ trợ triển khai, đào tạo và duy trì các quy trình nội bộ, tiêu chuẩn chất lượng trong công ty.
        - Phối hợp chặt chẽ với các đội ngũ Kỹ thuật (Engineering), Sản phẩm (Product) và DevOps để nhúng quy trình đảm bảo chất lượng vào đường ống CI/CD và vòng đời phát triển phần mềm.
    * **Kỹ năng yêu cầu (Required Skills):** QA QC, Automation Test, Automation Test Frameworks, Leadership, English communication, CI/CD pipeline.
    * **Phân tích tác động của AI (AI Impact Analysis):** Khả năng hỗ trợ: Mặc dù JD không yêu cầu kỹ năng AI, nhưng thực tế các công cụ Generative AI có thể hỗ trợ vị trí này tối ưu hóa việc viết script test tự động (Selenium, Playwright...) và tự động hóa việc tạo hàng loạt test scenario cho hệ thống E-commerce, giúp tăng tốc độ xử lý tác vụ kỹ thuật thô. Khả năng thay thế rất thấp vì  AI hoàn toàn không thể thay thế con người ở vị trí này. Lý do là công việc yêu cầu kỹ năng Leadership để quản lý các đội nhóm phân tán toàn cầu, tư duy chiến lược để định hình tiêu chuẩn chất lượng cho một nền tảng lớn, và khả năng kết nối liên chức năng như DevOps, Product. Đây đều là những kỹ năng mềm và quản trị cốt lõi mà AI chưa thể đảm nhiệm. Con người vẫn đóng vai trò tối cao trong việc thẩm định tính đúng đắn của framework và quản lý quy trình.


    ### Vị trí 01: Automation QA Engineer (QA QC/Tester/Automation Test)
    * **Đường dẫn (Link):** [https://itviec.com/it-jobs/automation-qa-engineer-qa-qc-tester-automation-test-nakivo-0115?lab_feature=preview_jd_page]
    * **Mức lương (Salary):** 1,100 - 1,500 USD
    * **Mô tả công việc (Job Description):**
        - Hợp tác với các nhà phát triển phần mềm và đội ngũ QA để hiểu rõ yêu cầu dự án và tính năng hệ thống.
        - Thiết kế, phát triển và thực thi các kịch bản kiểm thử tự động (test scripts) bằng các công cụ chuẩn công nghiệp.
        - Thiết kế, tạo và quản lý các ca kiểm thử tự động (automation test cases) ứng dụng công nghệ AI.
        - Phát hiện, báo cáo lỗi phần mềm một cách rõ ràng, ngắn gọn và phối hợp xử lý lỗi với các đội ngũ liên quan.
    * **Kỹ năng yêu cầu (Required Skills):** Selenium, Java, Python, C#, Git, API Testing (Postman/RestAssured), Kiến thức về Cloud (AWS, VMware, Hyper-V), Kỹ năng kiểm thử tự động bằng AI (Copilot, Cursor, Perplexity).
    * **Phân tích tác động của AI (AI Impact Analysis):** Vị trí này cho thấy rõ xu hướng "AI-augmented" (AI tăng cường) trong mảng Automation Test. AI (thông qua các công cụ như Copilot, Cursor) đóng vai trò trợ lý đắc lực, hỗ trợ kỹ sư viết code tự động nhanh hơn, tối ưu cấu trúc framework và sinh các kịch bản kiểm thử tự động một cách thông minh. Tuy nhiên, AI không thay thế được con người; kỹ sư QA vẫn đóng vai trò cốt lõi trong việc thiết lập tư duy logic hệ thống, kiểm soát hạ tầng cloud phức tạp (VMware, AWS) và thẩm định tính chính xác của các đoạn mã kiểm thử do AI gợi ý.

    ### Vị trí 01: Senior QC (Automation Tester, QA QC)
    * **Đường dẫn (Link):** [https://itviec.com/it-jobs/senior-qc-automation-tester-qa-qc-pnj-5542?lab_feature=preview_jd_page]
    * **Mức lương (Salary):** 1,000 - 1,500 USD
    * **Mô tả công việc (Job Description):**
        - Kiểm soát chất lượng truyền thống và AI: Phân tích đặc tả yêu cầu; lập kế hoạch và thực hiện kiểm thử chức năng, UI/UX, hành vi AI; kiểm tra các tình huống edge case, misuse, rủi ro nghiệp vụ; đánh giá độ chính xác, tin cậy và tính công bằng của kết quả AI.
        - Kiểm thử tự động và công cụ AI: Phát triển kịch bản test automation; áp dụng các công cụ kiểm thử AI (LLM evaluation, synthetic data); thiết lập hệ thống CI/CD; phát triển công cụ nội bộ hỗ trợ kiểm thử AI.
        - Đảm bảo chất lượng dữ liệu cho AI: Kiểm tra tính đầy đủ, chính xác, đa dạng của dữ liệu huấn luyện; giám sát bảo mật dữ liệu cá nhân và theo dõi hiệu suất mô hình AI theo thời gian.
    * **Kỹ năng yêu cầu (Required Skills):** Tối thiểu 04 năm kinh nghiệm Software Testing Automation (có ứng dụng AI trong testing), tư duy end-user, phân tích rủi ro hệ thống. Điểm cộng: Chứng chỉ ISTQB, Agile hoặc tương đương.
    * **Phân tích tác động của AI (AI Impact Analysis):** Vị trí này phản ánh một bước chuyển dịch lớn: AI không còn là công cụ hỗ trợ (Augmented) mà đã trở thành đối tượng kiểm thử chính (Testing AI Products). Công việc đòi hỏi kỹ sư không chỉ biết dùng AI để viết code automation nhanh hơn, mà phải có năng lực đánh giá chuyên sâu về mô hình (LLM evaluation), xử lý dữ liệu huấn luyện (Data Quality) và kiểm soát các lỗi đặc thù của AI như thiên kiến (fairness) hay ảo tưởng (hallucination). Con người đóng vai trò quyết định trong việc thiết lập "hàng rào quản trị" để đảm bảo AI hoạt động an toàn và chuẩn xác.

    ### Vị trí 01: Software Tester (QA QC, SQL)
    * **Đường dẫn (Link):** [https://itviec.com/it-jobs/software-tester-qa-qc-sql-gene-solutions-0129?lab_feature=preview_jd_page]
    * **Mức lương (Salary):** Nogotiable
    * **Mô tả công việc (Job Description):**
        - Phân tích nghiệp vụ & Xây dựng kịch bản: Nghiên cứu kỹ luồng vận hành (Workflow), tài liệu yêu cầu để viết Test Plan và thiết kế chi tiết bộ Test Case cho các tính năng/thay đổi của hệ thống.
        - Thực hiện kiểm thử: Tiến hành kiểm thử chức năng (Functional), phân quyền (Role-based), giao diện (UI/UX) và kiểm tra dữ liệu trên các trình duyệt Web phổ biến (Chrome, Edge, Firefox, Safari).
        - Quản lý lỗi & Nghiệm thu: Phát hiện, phân tích nguyên nhân, log lỗi lên hệ thống. Theo dõi tiến độ sửa lỗi, thực hiện Re-test, Regression Test và viết báo cáo chất lượng. Hỗ trợ người dùng làm kiểm thử nghiệm thu (UAT).
        - Kiểm tra dữ liệu: Thực hiện truy vấn cơ sở dữ liệu để đối chiếu và xác bóc dữ liệu hiển thị trên Web App đúng với cơ sở dữ liệu.
    * **Kỹ năng yêu cầu (Required Skills):** 1 - 3 năm kinh nghiệm Manual QC; thiết kế test plan/test case; SQL cơ bản - khá (Select, Join...); Postman (API test); Tiếng Anh đọc hiểu.(Copilot, Cursor, Perplexity).
    * **Phân tích tác động của AI (AI Impact Analysis):** Vị trí này hiện tại là một công việc Manual QC thuần túy truyền thống trong lĩnh vực Y tế (Healthcare), bản mô tả công việc chưa đề cập trực tiếp đến việc ứng dụng các công cụ Generative AI. Tuy nhiên, nhìn từ góc độ tối ưu hóa, AI hoàn toàn có thể tác động mạnh mẽ vào hai mảng:
        * Thiết kế Test Case từ Workflow: Kỹ sư có thể dùng AI (như ChatGPT/Claude) để nhập luồng vận hành phức tạp của hệ thống y tế và yêu cầu AI sinh ra các kịch bản kiểm thử (Test scenarios) bao quát, giúp giảm 40-50% thời gian suy nghĩ kịch bản thô.

        * Hỗ trợ viết SQL và API Script: Với yêu cầu truy vấn SQL mức cơ bản-khá và test API bằng Postman, AI đóng vai trò như một trợ lý đắc lực giúp QC sinh nhanh các câu lệnh Query phức tạp (như nhiều tầng Join) hoặc viết các đoạn script test tự động trong Postman.

    Dù vậy, do đặc thù ngành Healthcare đòi hỏi độ chính xác cực cao về dữ liệu khách hàng/bệnh nhân, tư duy logic để kiểm soát logic nội bộ và kỹ năng giao tiếp trực tiếp với Developer/User trong quá trình UAT vẫn là giá trị cốt lõi của con người mà AI chưa thể thay thế tại vị trí này.


    ### Vị trí 01: Manual/Automation Tester - Quality Analyst (QA QC)
    * **Đường dẫn (Link):** [https://itviec.com/it-jobs/manual-automation-tester-quality-analyst-qa-qc-mitek-vietnam-0005?lab_feature=preview_jd_page]
    * **Mức lương (Salary):** Competitive
    * **Mô tả công việc (Job Description):**
        - Thiết kế, phát triển, tài liệu hóa, đào tạo và thực hiện các test case phức tạp cho chu kỳ kiểm thử hồi quy (regression testing).
        - Kiểm thử chức năng (functional testing) các tính năng mới và kiểm thử hồi quy các tính năng hiện có cho mỗi đợt phát hành phần mềm mới.
        - Tham gia họp với các bên liên quan (Stakeholders); phối hợp với các đội ngũ tại Việt Nam và Mỹ để đánh giá, làm rõ yêu cầu và thiết kế sản phẩm.
        - Kiểm thử các ứng dụng trên nền tảng Windows và thực hiện log/báo cáo lỗi (bugs) trong quy trình làm việc Agile.
    * **Kỹ năng yêu cầu (Required Skills):** 3-5 năm kinh nghiệm làm QA, thành thạo tiếng Anh, có kiến thức về quy trình/kỹ thuật test và kinh nghiệm test ứng dụng Windows. Kỹ năng SQL, Agile tốt. (Điểm cộng: Có kinh nghiệm test automation cho Window apps/API và kiến thức về phần mềm ngành Xây dựng nhà ở - Home Building).
    * **Phân tích tác động của AI (AI Impact Analysis):** Mặc dù mô tả công việc (JD) hiện tại của MiTek chưa đề cập trực tiếp đến việc sử dụng các công cụ Generative AI, xu hướng tích hợp AI trong vị trí này là rất lớn. Do tính chất công việc tập trung mạnh vào kiểm thử thủ công (Manual Test Focus) kết hợp với các hệ thống phần mềm đặc thù (Window Applications ngành Home Building), AI có thể đóng vai trò trợ lý giúp tự động hóa việc viết tài liệu kiểm thử và gợi ý các kịch bản test case phức tạp dựa trên yêu cầu sản phẩm ban đầu. Tuy nhiên, vì dự án yêu cầu sự phối hợp chặt chẽ giữa các team global (Việt Nam & Mỹ) để làm rõ yêu cầu nghiệp vụ phức tạp, năng lực cốt lõi của con người như tư duy logic, kỹ năng giao tiếp, hiểu biết sâu sắc về domain kiến thức (ngành xây dựng) và khả năng ra quyết định cuối cùng vẫn là yếu tố then chốt mà AI chưa thể thay thế.
    ![PQA](../req1_jobs/mitek.png)

    ### Vị trí 01: QA Engineer — VibeX-Generated Apps (QA QC, Tester)
    * **Đường dẫn (Link):** [https://itviec.com/it-jobs/qa-engineer-vibex-generated-apps-qa-qc-tester-metacrew-5045?lab_feature=preview_jd_page]
    * **Mức lương (Salary):** Competitive
    * **Mô tả công việc (Job Description):**
        - Kiểm thử toàn diện chất lượng (chức năng, UI, độ phản hồi, hiệu năng, khả năng tiếp cận WCAG) của các ứng dụng web và di động được tạo ra tự động bởi nền tảng AI VibeX.
        - Viết báo cáo lỗi (bug reports), phân loại và phân tích các vấn đề để phân biệt rõ giữa lỗi hệ thống (critical bugs) và giới hạn của AI (AI generation limitations).
        - Sử dụng các công cụ Generative AI (Claude, Gemini,...) để tạo test case tự động, xây dựng kịch bản kiểm thử hồi quy (regression test) cho các sản phẩm có giao diện thay đổi liên tục (generative UI).
        - Phân tích các mô hình lỗi lặp đi lặp lại từ sản phẩm của AI để đề xuất cải tiến prompt và tối ưu hóa đường ống (generation pipeline) của VibeX; phối hợp trực tiếp với đội ngũ kỹ sư toàn cầu.
    * **Kỹ năng yêu cầu (Required Skills):** Thành thạo kiểm thử Web/Mobile (HTML/CSS/JS/DevTools) 3-5 năm, sử dụng tốt các công cụ AI (Prompt Engineering) để tạo test case/ tự động hóa và đọc viết tài liệu bằng tiếng Anh.
    * **Phân tích tác động của AI (AI Impact Analysis):** Đây cũng là một vị trí minh chứng rõ nét cho mô hình "AI-powered Quality Operator" (Vận hành chất lượng bằng AI) thay vì một QA truyền thống. AI đóng vai trò vừa là "đối tượng kiểm thử" vừa là "đồng nghiệp" hỗ trợ. Tác động lớn nhất là việc xóa bỏ các test case kịch bản cố định, bắt buộc kỹ sư phải dùng AI để đối phó với các đầu ra không định hình trước (non-deterministic UI) của Generative AI. Vai trò của con người lúc này dịch chuyển từ việc "tìm lỗi thủ công" sang "phân tích mô hình lỗi" (pattern analysis) để huấn luyện lại AI và cải tiến Prompt hệ thống. Khả năng làm việc cùng AI (AI capability) đã trở thành tiêu chí tuyển dụng số một, vượt qua cả số năm kinh nghiệm truyền thống.

    ### Vị trí 01: Manual Tester (QA QC/English)
    * **Đường dẫn (Link):** [https://itviec.com/it-jobs/manual-tester-qa-qc-english-netcompany-1931?lab_feature=preview_jd_page]
    * **Mức lương (Salary):** Negotiable
    * **Mô tả công việc (Job Description):**
        - Phân tích và thấu hiểu các yêu cầu kỹ thuật và nghiệp vụ (business) từ khách hàng thuộc nhiều lĩnh vực khác nhau.
        - Phối hợp với đội ngũ dự án để thực hiện kiểm thử các ứng dụng một cách có hệ thống và bài bản.
        - Thiết kế, thực thi và đánh giá (review) các test case dựa trên các yêu cầu về chức năng (functional), phi chức năng (non-functional), kỹ thuật và trải nghiệm người dùng (usability).
        - Quản lý, báo cáo kết quả kiểm thử và tiến độ công việc cá nhân.
        - Phát hiện, quản lý lỗi (defects), đánh giá mức độ nghiêm trọng cũng như tầm ảnh hưởng của lỗi đối với giải pháp và phạm vi dự án.
    * **Kỹ năng yêu cầu (Required Skills):** Tốt nghiệp Đại học/Thạc sĩ chuyên ngành CNTT, tiếng Anh giao tiếp và viết tốt (quy trình phỏng vấn 100% bằng tiếng Anh), nắm vững lý thuyết và phương pháp kiểm thử thủ công, có kinh nghiệm sử dụng các công cụ quản lý test và tracking lỗi, chứng chỉ ISTQB là một điểm cộng.
    * **Phân tích tác động của AI (AI Impact Analysis):** Bản mô tả công việc hiện tại của Netcompany vẫn tập trung hoàn toàn vào các kỹ năng kiểm thử truyền thống (Manual Testing chuyên sâu) và kỹ năng mềm như làm việc trong môi trường Agile quốc tế, giao tiếp tiếng Anh với khách hàng. Tuy JD chưa đề cập trực tiếp đến việc sử dụng các công cụ Generative AI, nhưng môi trường làm việc tại đây rất chú trọng cập nhật công nghệ mới ("opportunity to work with the latest technologies"). Trong bối cảnh hiện tại, AI có thể hỗ trợ tối ưu ở bước phân tích yêu cầu nghiệp vụ phức tạp của khách hàng châu Âu và tăng tốc độ viết tài liệu/test case bằng tiếng Anh. Mặc dù vậy, vai trò cốt lõi của kỹ sư con người tại vị trí này vẫn là không thể thay thế, đặc biệt là trong việc tư duy logic để hiểu sâu bài toán của khách hàng, tương tác đa quốc gia và chịu trách nhiệm tối cao cho chất lượng cuối cùng của sản phẩm ("certifying the quality of the solution").

    ### Vị trí 01: Fresher Full-stack Test Engineer (QA/QC/Tester)
    * **Đường dẫn (Link):** [https://vn.indeed.com/jobs?q=qa+qc+tester&l=Th%C3%A0nh+ph%E1%BB%91+H%E1%BB%93+Ch%C3%AD+Minh&from=searchOnDesktopSerp%2Cwhereautocomplete&vjk=105f8525d68c2716]
    * **Mức lương (Salary):** Competitive
    * **Mô tả công việc (Job Description):**
        - Tìm hiểu kiến thức nghiệp vụ (domain) và quy trình kiểm thử của khách hàng để thực hiện các hoạt động test hiệu quả.
        - Phối hợp chặt chẽ với đội ngũ dự án trong các tác vụ hàng ngày và tham gia các buổi sprint demo với khách hàng.
        - Thiết kế, duy trì và thực thi các test case/test script.
        - Phát hiện, báo cáo và theo dõi tiến độ sửa lỗi (defects) trên hệ thống quản lý lỗi.
        - Chuẩn bị, xem xét các tài liệu kiểm thử và báo cáo tiến độ, rủi ro về chất lượng trực tiếp với khách hàng.
    * **Kỹ năng yêu cầu (Required Skills):** Sinh viên năm 4 hoặc mới tốt nghiệp ngành CNTT/Phần mềm (GPA từ 7.5 trở lên). Tiếng Anh lưu loát (Upper-intermediate trở lên) để làm việc trực tiếp với khách hàng nước ngoài. Nền tảng tốt về các phương pháp kiểm thử (Manual, Automation, API, Unit testing) và tư duy lập trình (Python/Java/JavaScript). Điểm cộng: Sử dụng các công cụ AI chat (ChatGPT, Claude, Gemini) để nghiên cứu, fix bug và các trợ lý code AI (GitHub Copilot, Cursor, Claude Code).
    * **Phân tích tác động của AI (AI Impact Analysis):** Vị trí Fresher này minh chứng rất rõ xu hướng "AI-native" trong ngành kiểm thử hiện nay. KMS Technology đã đưa kỹ năng tương tác với AI (Prompt Engineering, sử dụng GitHub Copilot/Cursor để sinh test case, tài liệu và code) thành một lợi thế cạnh tranh lớn ngay từ cấp độ Fresher. AI đóng vai trò như một người "mentor kỹ thuật số" giúp các kỹ sư trẻ tăng tốc độ viết code test và nghiên cứu tài liệu. Tuy nhiên, trách nhiệm cốt lõi như quản lý rủi ro rò rỉ dữ liệu khách hàng (data privacy) và việc thẩm định tính chính xác của kết quả do AI tạo ra vẫn đòi hỏi tư duy phản biện và trách nhiệm tối cao từ con người.

    ### Vị trí 01: MANUAL & AUTOMATION TESTER
    * **Đường dẫn (Link):** [https://topdev.vn/detail-jobs/hn-trung-tam-doi-moi-sang-tao-manual-automation-tester-tong-cong-ty-buu-dien-viet-nam-vietnam-post-2104346?src=topdev_home&medium=superhotjobs]
    * **Mức lương (Salary):** 15,000,000 - 45,000,000 VND
    * **Mô tả công việc (Job Description):**
        - Nghiên cứu, phân tích tài liệu yêu cầu, thiết kế; tham gia xây dựng kế hoạch kiểm thử, thiết kế và viết testcase, checklist, testplan.
        - Thực hiện kịch bản kiểm thử thủ công (Manual) và chuẩn bị dữ liệu, viết & thực thi các kịch bản kiểm thử tự động (Automation).
        - Tích hợp kiểm thử tự động vào quy trình CI/CD; tham gia kiểm thử hiệu năng và test tải hệ thống khi cần thiết.
        - Phối hợp với Developer để quản lý/sửa lỗi trên Jira; hỗ trợ triển khai, đào tạo người dùng và nghiệm thu khách hàng.
    * **Kỹ năng yêu cầu (Required Skills):** Manual Test, Automation Test (Selenium, Cypress, Junit, TestNG, JMeter), Quản lý lỗi (Jira, Confluence, SVN/GitHub), Cơ sở dữ liệu (SQL/NoSQL).
    * **Phân tích tác động của AI (AI Impact Analysis):** Mặc dù tin tuyển dụng này chưa yêu cầu trực tiếp các kỹ năng AI (như Prompt Engineering), nhưng đây là môi trường lý tưởng để AI tác động mạnh mẽ. Việc phải đảm nhiệm song song cả Manual lẫn Automation trên các hệ thống rất lớn của Vietnam Post (như AI, Big Data, CRM, ERP, E-commerce) sẽ tạo áp lực lớn về mặt thời gian. AI có thể được ứng dụng để tự động hóa việc sinh các bộ dữ liệu test (Test Data), gợi ý các test case biên phức tạp từ tài liệu nghiệp vụ, hoặc thậm chí hỗ trợ tối ưu/sửa lỗi các đoạn code script Automation (Selenium/Cypress). Tuy nhiên, do tính chất hệ thống cốt lõi phục vụ quốc gia và cộng đồng, tư duy logic của con người để kiểm soát quy trình CI/CD và thẩm định độ chính xác cuối cùng của hệ thống vẫn là yếu tố quyết định không thể thay thế.

    ### Vị trí 01: QA / QC Intern
    * **Đường dẫn (Link):** [https://www.linkedin.com/jobs/search/?currentJobId=4420929154&f_E=1&keywords=qa%20qc&origin=JOB_SEARCH_PAGE_JOB_FILTER]
    * **Mức lương (Salary):** Competitive
    * **Mô tả công việc (Job Description):**
        - Thực hiện kiểm thử nghiêm ngặt (Rigorous Testing): Thử nghiệm luồng phỏng vấn bằng AI trên nhiều loại thiết bị di động và trình duyệt khác nhau để tìm ra các lỗi thực tế (Edge cases).
        - Thực hiện kiểm thử nghiêm ngặt (Rigorous Testing): Thử nghiệm luồng phỏng vấn bằng AI trên nhiều loại thiết bị di động và trình duyệt khác nhau để tìm ra các lỗi thực tế (Edge cases).
        - Quản lý phát hành (Release Management): Làm việc trực tiếp với đội ngũ Kỹ thuật và Sản phẩm để phê duyệt xuất bản sản phẩm. Có quyền quyết định "Dừng" không cho ship nếu phát hiện lỗi nghiêm trọng.
        - Cải tiến quy trình và Viết tài liệu chất lượng: Dịch các báo cáo lỗi lộn xộn thành các ticket kỹ thuật rõ ràng, chính xác; chủ động phát hiện lỗ hổng trong quy trình test.
    * **Kỹ năng yêu cầu (Required Skills):** Sự tỉ mỉ đến từng chi tiết (Detail-Obsessed), Thành thạo kỹ thuật cơ bản (Biết mở Browser Console/Inspect Element để kiểm tra lỗi network), Tư duy logic cô lập biến để tìm gốc rễ của lỗi, Có sự đồng cảm với người dùng. Điểm cộng: Đam mê sản phẩm công nghệ, phân tích dữ liệu hoặc biết code.
    * **Phân tích tác động của AI (AI Impact Analysis):** Tái định hình đối tượng kiểm thử: Vị trí này cho thấy một khía cạnh rất thực tế khi AI tham gia vào quy trình tuyển dụng (AI Speech-to-Text, AI Interview). Vai trò của kỹ sư QA ở đây không bị AI thay thế, mà ngược lại, AI tạo ra một "môi trường thách thức mới". Con người đóng vai trò tối quan trọng trong việc kiểm thử các kịch bản thực tế mà AI chưa tự lường trước được (như mất kết nối, fragmentation thiết bị từ phân khúc giá rẻ đến cao cấp). Trách nhiệm ra quyết định "Ship hay không Ship" (Green-light) hoàn toàn thuộc về tư duy và sự thẩm định của con người để đảm bảo tính công bằng, mượt mà cho ứng viên khi phỏng vấn qua AI.
```

### (3) Verdict
Chưa hoàn thiện còn thiếu ảnh minh chứng và đánh số vị trí chưa chuẩn do các prompt gửi rời rạc.

### (4) Student Audit
| No. | AI Output Component | Identified Mistake / Defect | Reasoning & Evidence (Syllabus/ISTQB) | Student's Corrective Fix |
| --- | -------------------- | --------------------------- | ------------------------------------- | ------------------------ |
|1 | Vị trí 01 | Sai số thứ tự | Vì các câu prompt gửi riêng lẻ | Đánh số lại vị trí theo thứ tự từ 1 đến 11 cho đúng với yêu cầu của bài tập. |
|2 | Thiếu ảnh minh chứng | Không hoàn chỉnh | Bài tập yêu cầu phải có ảnh minh chứng cho mỗi vị trí để chứng minh đã truy cập vào trang tuyển dụng và phân tích đúng JD. | Thêm ảnh chụp màn hình minh chứng |


