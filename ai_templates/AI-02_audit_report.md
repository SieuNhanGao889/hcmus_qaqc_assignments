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
 **INCOMPLETE & INVALID**

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
**INCOMPLETE**

Chưa hoàn thiện còn thiếu ảnh minh chứng và đánh số vị trí chưa chuẩn do các prompt gửi rời rạc.

### (4) Student Audit
| No. | AI Output Component | Identified Mistake / Defect | Reasoning & Evidence (Syllabus/ISTQB) | Student's Corrective Fix |
| --- | -------------------- | --------------------------- | ------------------------------------- | ------------------------ |
|1 | Vị trí 01 | Sai số thứ tự | Vì các câu prompt gửi riêng lẻ | Đánh số lại vị trí theo thứ tự từ 1 đến 11 cho đúng với yêu cầu của bài tập. |
|2 | Thiếu ảnh minh chứng | Không hoàn chỉnh | Bài tập yêu cầu phải có ảnh minh chứng cho mỗi vị trí để chứng minh đã truy cập vào trang tuyển dụng và phân tích đúng JD. | Thêm ảnh chụp màn hình minh chứng |


## Entry 3: 20 Software Defects 2022–2026 (Requirement 2)

**Date of Audit:** 2026-06-03

**Target AI Model:** ChatGPT (GPT-4o)

**Task:** Sinh danh sách 20 software defects 2022–2026 kèm mô tả, root cause, severity,
hậu quả, giải pháp và nhận định chuyên gia. Output được dùng làm nội dung gốc cho Requirement 2.

---

### (1) Prompt + Tool

**Tool used:** ChatGPT (GPT-4o)

**Timestamp:** 10:45 03/06/2026

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

Sau khi viết xong 4 mục trên cho mỗi sự cố, hãy viết thêm 1 dòng nhận định chuyên gia.

---

### (2) AI Output

```
1. CrowdStrike Falcon Update Crash (2024)
1. Tên sự cố & Năm xảy ra

CrowdStrike Falcon Sensor Defective Update – 2024

2. Mô tả lỗi & Root Cause

Một bản cập nhật nội dung (content update) của Falcon Sensor khiến hàng triệu máy Windows bị BSOD (Blue Screen of Death) và reboot liên tục.

Nguyên nhân gốc được CrowdStrike công bố là lỗi trong hệ thống kiểm tra (Content Validator), cho phép một cấu hình lỗi vượt qua quá trình xác thực và được phát hành toàn cầu. Một thành phần của driver đọc dữ liệu không hợp lệ dẫn đến truy cập bộ nhớ ngoài phạm vi.

3. Mức độ nghiêm trọng & Hậu quả
Khoảng 8,5 triệu thiết bị bị ảnh hưởng.
Hàng không, ngân hàng, bệnh viện, truyền thông bị gián đoạn trên phạm vi toàn cầu.
Được xem là một trong những sự cố CNTT lớn nhất lịch sử.
4. Giải pháp khắc phục
Thu hồi bản cập nhật lỗi.
Tăng cường kiểm thử nhiều lớp.
Bổ sung quy trình triển khai theo từng giai đoạn (staged rollout).
Cải tiến hệ thống validation.

Nhận định chuyên gia: Đây không phải lỗi của một lập trình viên mà là thất bại của toàn bộ quy trình QA và quản trị phát hành phần mềm.

2. ChatGPT Hallucinated Legal Citations (2023–2026)
1. Tên sự cố & Năm xảy ra

ChatGPT Fake Court Citations – 2023–2026

2. Mô tả lỗi & Root Cause

ChatGPT tạo ra các án lệ, tài liệu pháp lý không tồn tại nhưng trình bày như thật.

Nguyên nhân gốc là cơ chế dự đoán token của LLM tối ưu xác suất ngôn ngữ thay vì kiểm chứng sự thật.

3. Mức độ nghiêm trọng & Hậu quả
Luật sư bị tòa án xử phạt.
Hồ sơ pháp lý chứa thông tin giả.
Gây mất niềm tin vào AI trong ngành luật.
4. Giải pháp khắc phục
RAG (Retrieval Augmented Generation).
Citation verification.
Human review bắt buộc.

Nhận định chuyên gia: Hallucination không phải bug tạm thời mà là hệ quả cấu trúc của kiến trúc LLM hiện nay.

3. Google Gemini Image Bias Incident (2024)
1. Tên sự cố & Năm xảy ra

Gemini Historical Image Generation Bias – 2024

2. Mô tả lỗi & Root Cause

Gemini sinh ảnh lịch sử sai lệch nhân khẩu học khi tạo hình nhân vật lịch sử.

Root cause:

Bộ lọc fairness can thiệp quá mạnh.
Prompt rewriting tự động làm sai bối cảnh lịch sử.
3. Hậu quả
Chỉ trích toàn cầu.
Google phải tạm dừng tính năng tạo ảnh người.
4. Khắc phục
Điều chỉnh policy model.
Tăng ràng buộc lịch sử trong pipeline.

Nhận định chuyên gia: Đây là ví dụ điển hình của việc tối ưu mục tiêu đạo đức nhưng làm hỏng tính chính xác dữ liệu.

4. Air Canada Chatbot False Refund Policy (2024)
1. Tên sự cố & Năm xảy ra

Air Canada AI Chatbot Refund Error – 2024

2. Mô tả lỗi & Root Cause

Chatbot AI tự tạo chính sách hoàn tiền không tồn tại.

Root cause:

LLM sinh nội dung ngoài knowledge base.
Không có cơ chế ràng buộc câu trả lời theo chính sách chính thức.
3. Hậu quả
Air Canada thua kiện.
Phải bồi hoàn cho khách hàng.
4. Khắc phục
Giới hạn chatbot chỉ truy xuất dữ liệu được xác thực.
Human-approved policy database.

Nhận định chuyên gia: Sai lầm nằm ở kiến trúc sản phẩm chứ không phải riêng mô hình AI.

5. Microsoft Copilot Prompt Injection (2024)
1. Tên sự cố & Năm xảy ra

Copilot Prompt Injection Vulnerability – 2024

2. Mô tả lỗi & Root Cause

Kẻ tấn công nhúng chỉ dẫn độc hại trong email hoặc tài liệu khiến Copilot tiết lộ dữ liệu.

Root cause:

Không tách biệt dữ liệu và lệnh.
Mô hình không phân biệt trusted instruction và untrusted content.
3. Hậu quả
Nguy cơ rò rỉ dữ liệu doanh nghiệp.
Tác động đến nhiều sản phẩm AI enterprise.
4. Khắc phục
Prompt isolation.
Content sanitization.
Trust boundary enforcement.

Nhận định chuyên gia: Prompt injection hiện là SQL Injection của thời đại AI.

6. Google Bard Hallucination Demo (2023)
1. Tên sự cố & Năm xảy ra

Google Bard Telescope Fact Error – 2023

2. Mô tả lỗi & Root Cause

Bard đưa thông tin thiên văn sai trong video quảng cáo.

Root cause:

Hallucination từ mô hình ngôn ngữ.
Thiếu fact-check trước khi công bố.
3. Hậu quả
Giá cổ phiếu Alphabet giảm mạnh.
Mất uy tín sản phẩm.
4. Khắc phục
Tăng fact verification.
Human review cho nội dung marketing.

Nhận định chuyên gia: AI không nên được xem là nguồn sự thật cuối cùng.

7. MyCity New York AI Business Chatbot Error (2024)
1. Tên sự cố & Năm xảy ra

NYC Business Chatbot Misleading Advice – 2024

2. Mô tả lỗi & Root Cause

Chatbot đưa lời khuyên trái luật lao động và thuế.

Root cause:

RAG không đầy đủ.
Thiếu cơ chế kiểm tra quy định pháp lý.
3. Hậu quả
Thành phố bị chỉ trích.
Rủi ro pháp lý.
4. Khắc phục
Thêm validation dựa trên luật.
Human moderation.

Nhận định chuyên gia: AI không phù hợp làm nguồn tư vấn pháp lý tự động hoàn toàn.

8. Azure East US Authentication Failure (2024)
1. Tên sự cố & Năm xảy ra

Microsoft Azure Authentication Outage – 2024

2. Mô tả lỗi & Root Cause

Lỗi cấu hình dịch vụ xác thực làm nhiều dịch vụ Azure ngừng hoạt động.

Root cause:

Lỗi triển khai cấu hình hệ thống.
3. Hậu quả
Nhiều dịch vụ cloud bị gián đoạn.
4. Khắc phục
Rollback cấu hình.
Tăng canary deployment.

Nhận định chuyên gia: Hệ thống càng tập trung thì lỗi cấu hình càng trở thành điểm thất bại toàn cục.

9. GitLab Backup Deletion Regression (2022)
1. Tên sự cố & Năm xảy ra

GitLab Backup Automation Bug – 2022

2. Mô tả lỗi & Root Cause

Một lỗi regression trong quy trình backup dẫn đến mất khả năng khôi phục ở một số môi trường.

3. Hậu quả
Rủi ro mất dữ liệu.
4. Khắc phục
Kiểm thử khôi phục định kỳ.
Backup verification.

Nhận định chuyên gia: Backup chưa được test restore thì chưa phải backup.

10. AWS Lambda Internal Service Regression (2022)
1. Tên sự cố & Năm xảy ra

AWS Lambda Service Regression – 2022

2. Mô tả lỗi & Root Cause

Một thay đổi phần mềm nội bộ gây lỗi xử lý yêu cầu.

3. Hậu quả
Nhiều dịch vụ serverless bị ảnh hưởng.
4. Khắc phục
Rollback nhanh.
Canary release.

Nhận định chuyên gia: Tự động hóa triển khai phải đi kèm tự động hóa rollback.

11. Meta Ads Delivery Bug (2022)
1. Tên sự cố & Năm xảy ra

Facebook Ads Delivery Defect – 2022

2. Mô tả lỗi & Root Cause

Lỗi thuật toán phân phối quảng cáo khiến hiệu suất giảm bất thường.

3. Hậu quả
Nhà quảng cáo thiệt hại doanh thu.
4. Khắc phục
Điều chỉnh mô hình ranking.

Nhận định chuyên gia: Thuật toán recommendation sai đôi khi gây thiệt hại lớn hơn lỗi giao diện.

12. Twitter/X Timeline Recommendation Bug (2023)
1. Tên sự cố & Năm xảy ra

For You Feed Algorithm Error – 2023

2. Mô tả lỗi & Root Cause

Thuật toán ưu tiên bất thường một số nội dung.

3. Hậu quả
Trải nghiệm người dùng bị méo mó.
4. Khắc phục
Điều chỉnh trọng số ranking.

Nhận định chuyên gia: Thuật toán đề xuất chính là phần mềm có ảnh hưởng xã hội lớn nhất hiện nay.

13. Google Maps Routing Error (2023)
1. Tên sự cố & Năm xảy ra

Maps Incorrect Routing Incident – 2023

2. Mô tả lỗi & Root Cause

Thuật toán định tuyến sử dụng dữ liệu giao thông lỗi thời.

3. Hậu quả
Gây ùn tắc cục bộ.
4. Khắc phục
Cập nhật dữ liệu thời gian thực.

Nhận định chuyên gia: Dữ liệu sai khiến thuật toán đúng vẫn cho kết quả sai.

14. Toyota Connected Service Outage (2023)
1. Tên sự cố & Năm xảy ra

Toyota Cloud Configuration Error – 2023

2. Mô tả lỗi & Root Cause

Lỗi cấu hình cloud làm dữ liệu khách hàng bị công khai.

3. Hậu quả
Rò rỉ dữ liệu.
4. Khắc phục
Kiểm tra cấu hình tự động.

Nhận định chuyên gia: Phần lớn sự cố cloud hiện nay xuất phát từ cấu hình chứ không phải hacker.

15. Samsung Keyboard Predictive Text Bug (2024)
1. Tên sự cố & Năm xảy ra

Samsung AI Keyboard Suggestion Error – 2024

2. Mô tả lỗi & Root Cause

Mô hình gợi ý văn bản tạo nội dung không phù hợp.

3. Hậu quả
Ảnh hưởng trải nghiệm người dùng.
4. Khắc phục
Fine-tune và lọc đầu ra.

Nhận định chuyên gia: Chất lượng dữ liệu huấn luyện quyết định chất lượng AI.

16. OpenAI GPT Store Prompt Leakage (2024)
1. Tên sự cố & Năm xảy ra

Custom GPT Prompt Leakage – 2024

2. Mô tả lỗi & Root Cause

Người dùng khai thác prompt để lộ system prompt của GPT tùy chỉnh.

3. Hậu quả
Rò rỉ logic nội bộ.
4. Khắc phục
Tăng cường prompt protection.

Nhận định chuyên gia: Không nên xem prompt là cơ chế bảo mật.

17. McDonald’s AI Drive-Thru Ordering Errors (2024)
1. Tên sự cố & Năm xảy ra

Drive-Thru Ordering AI Mistakes – 2024

2. Mô tả lỗi & Root Cause

AI nhận dạng giọng nói đặt sai món ăn.

3. Hậu quả
Khách hàng nhận đơn sai.
McDonald's dừng triển khai tại nhiều điểm.
4. Khắc phục
Tăng human review.
Huấn luyện dữ liệu giọng nói tốt hơn.

Nhận định chuyên gia: AI giao tiếp với thế giới vật lý cần độ chính xác cao hơn chatbot thông thường.

18. Synapse Xray Medical AI Bias Issue (2025)
1. Tên sự cố & Năm xảy ra

Medical Imaging AI Bias Detection – 2025

2. Mô tả lỗi & Root Cause

Mô hình chẩn đoán bị lệch trên một số nhóm bệnh nhân.

3. Hậu quả
Nguy cơ chẩn đoán sai.
4. Khắc phục
Mở rộng dữ liệu huấn luyện.

Nhận định chuyên gia: Bias trong AI y tế là vấn đề an toàn chứ không chỉ là đạo đức.

19. VNDirect Trading Platform Outage Recovery Defects (2024)
1. Tên sự cố & Năm xảy ra

VNDirect System Recovery Issues – 2024

2. Mô tả lỗi & Root Cause

Sau sự cố an ninh mạng, nhiều thành phần phần mềm và quy trình phục hồi hoạt động không ổn định.

3. Hậu quả
Giao dịch bị gián đoạn.
Ảnh hưởng nhà đầu tư Việt Nam.
4. Khắc phục
Tái cấu trúc hạ tầng.
Tăng DR (Disaster Recovery).

Nhận định chuyên gia: Năng lực phục hồi sau sự cố quan trọng không kém khả năng phòng thủ.

20. Cloudflare Service Configuration Bug (2025)
1. Tên sự cố & Năm xảy ra

Cloudflare Internal Software Fault – 2025

2. Mô tả lỗi & Root Cause

Lỗi phần mềm nội bộ gây gián đoạn một số dịch vụ mạng toàn cầu.

3. Hậu quả
Nhiều website bị ảnh hưởng.
4. Khắc phục
Tăng kiểm thử triển khai.
Cải tiến observability.

Nhận định chuyên gia: Các nền tảng hạ tầng Internet hiện đã trở thành "single point of failure" cho hàng triệu hệ thống khác.
```

Tóm tắt cấu trúc output nhận được:
- 20 entries với mỗi entry gồm: Tên sự cố, Năm, Mô tả + Root Cause, Severity + Hậu quả,
  Giải pháp, Nhận định chuyên gia.
- Hơn 5 entries liên quan AI/LLM: Defect 02 (ChatGPT legal citations), Defect 03 (Gemini
  image bias), Defect 04 (Air Canada chatbot), Defect 05 (Copilot prompt injection),
  Defect 16 (GPT Store prompt leakage).
- Một entry có khả năng hallucinate tên thực thể: Defect 18 ("Synapse Xray") —
  không tìm được source xác nhận tên sản phẩm này.
- Hai entries mô tả quá chung chung, thiếu source xác minh: Defect 09 (GitLab 2022),
  Defect 10 (AWS Lambda 2022).

---

### (3) Verdict
**INCOMPLETE**

Output đáp ứng yêu cầu về số lượng (20 entries) và cấu trúc (4 mục + nhận định).
Tuy nhiên:
- Defect 18 có dấu hiệu hallucination tên thực thể ("Synapse Xray") — không có
  source báo chí xác nhận.
- Defect 09 và 10 thiếu source link cụ thể, mô tả quá chung, không đủ cơ sở
  để xác minh đây là các incident thực sự được công khai.
- 7/20 entries thiếu source link dẫn đến nguồn báo chí hoặc post-mortem gốc.
- Phần "Nhận định chuyên gia" ở nhiều entry là overgeneralization hoặc dùng truism thay cho phân tích kỹ thuật cụ thể.

---

### (4) Reasoning

- **Defect 18**: Tên "Synapse Xray" không xuất hiện trong bất kỳ nguồn báo chí
  công nghệ hoặc y tế uy tín nào. AI đã fabricate một proper noun để gắn vào
  một vấn đề thực (medical AI bias) — đây là *false entity hallucination*, vi phạm
  yêu cầu "source link" của bài tập.

- **Defect 09 & 10**: Mô tả quá chung, không có incident ID hoặc post-mortem
  reference. Sự cố GitLab nổi tiếng nhất về backup là năm 2017, không phải 2022.
  AI có thể đã confabulate dựa trên pattern của các backup incidents mà không có
  source cụ thể.

- **Nhận định chuyên gia**: Nhiều entries dùng câu có tính chất truism phổ quát
  ("hệ thống càng tập trung thì lỗi càng lan rộng") thay vì phân tích gắn với
  cơ chế kỹ thuật cụ thể của từng sự cố — không đạt yêu cầu "phân tích sâu"
  theo đề bài.

---

### (5) Student Fix
Các chỉnh sửa đã thực hiện so với output gốc của ChatGPT:

| # | Vấn đề | Sửa như thế nào |
|---|--------|-----------------|
| 1 | Defect 18 hallucinate tên "Synapse Xray" | Đổi thành mô tả chung về medical AI imaging bias, cite NEJM research thay vì tên sản phẩm không xác minh được |
| 2 | Defect 09 không có source 2022 rõ ràng | Giữ lại nhưng thêm ghi chú rằng incident GitLab nổi tiếng nhất là 2017; source link để placeholder cần verify |
| 3 | Defect 10 quá generic | Thêm context về AWS Service Health Dashboard; ghi rõ đây là tổng hợp từ nhiều Lambda event nhỏ |
| 4 | Defect 12 frame sai là "bug" | Sửa thành "intentional product decision" dựa trên thừa nhận công khai của Elon Musk |
| 5 | Defect 19 bỏ qua ransomware | Thêm rõ bản chất tấn công có chủ đích, tên tác nhân và phối hợp với Bộ Công an |
| 6 | 7 entries thiếu source link | Bổ sung source link từ Reuters, BBC, Verge, Toyota newsroom, VNExpress |
| 7 | Nhận định chuyên gia overgeneralize | Toàn bộ phần "AI Hallucination/Bias" được viết lại dựa trên cross-check với Claude |

---

---

## Entry 4: Cross-Check & AI Hallucination Analysis (Requirement 2 — Verification Pass)

**Date of Audit:** 2026-06-03

**Target AI Model:** Claude Sonnet 4.6

**Task:** Dùng Claude làm AI Auditor độc lập để cross-check output của ChatGPT — phát hiện
hallucination, false attribution, bias và thiếu thông tin trong từng entry của 20 defects.

---

### (1) Prompt + Tool
**Tool used:** Claude Sonnet 4.6
**Timestamp:** 11:30 03/06/2026
**Prompt:**
Bạn hãy rà soát tính xác thực lịch sử hãy kiểm tra xem có sự cố nào trong danh sách trên không có thật ngoài đời hay là sai lệch hoàn toàn về mốc thời gian hay bản chất kỹ thuật trong giai đoạn 2022-2026 hay không. Nếu có, hãy chỉ rõ ra cho tôi nhé và thêm nữa
tìm lỗi ảo tưởng định kiến (AI Hallucination/Bias) cho từng Entry đó nữa đối với 20 entry sự cố ở trên, hãy phân tích kỹ câu trả lời của AI đó đặc biệt là phần mô tả lỗi và nhận định chuyên gia. Với mỗi entry, hãy chỉ ra giúp tôi 1 điểm mà đoạn văn trên đã giải thích chưa chính xác, bị hallucinate, thiếu thôngtin cốt lõi, hoặc có định kiến đổ lỗi sai mục tiêu bias.

Hãy trình bày kết quả tìm lỗi AI này dưới dạng danh sách trên theo cấu trúc:
- Sự cố X:
- Điểm AI giải thích sai/định kiến: sai chỗ nào đúng theo thực tế hoặc thiếu thông tin gì
---

### (2) AI Output
```
Nhìn chung, tất cả 20 sự cố trong danh sách đều có cơ sở thực tế — không có sự cố nào bị bịa đặt hoàn toàn. Tuy nhiên, có 2 sự cố đáng lưu ý về mức độ chính xác:
Sự cố 9 – GitLab Backup Deletion Regression (2022): Mô tả khá mơ hồ. Sự cố nổi tiếng nhất của GitLab về backup là từ năm 2017 (gitlab.com database incident), không phải 2022. Có thể AI đã nhầm lẫn hoặc tổng hợp từ một sự cố nội bộ nhỏ hơn của 2022. Cần có source link cụ thể để xác minh.
Sự cố 18 – Synapse Xray Medical AI Bias Issue (2025): Tên "Synapse Xray" không khớp với một sự cố được báo chí công khai rộng rãi. Có thể AI đã tổng hợp tên sản phẩm từ nhiều nguồn khác nhau (Synapse AI, Aidoc, Rad AI…). Đây là dấu hiệu hallucination tên thực thể, dù vấn đề AI bias trong y tế là có thật và được ghi nhận trong giai đoạn 2024–2025.

Phân tích lỗi Hallucination/Bias cho từng entry
const data = [
  {
    num:1, name:"CrowdStrike Falcon Update Crash (2024)", type:"bias",
    aiSaid:"AI kết luận: <strong>\"Đây không phải lỗi của một lập trình viên mà là thất bại của toàn bộ quy trình QA.\"</strong>",
    verdict:"Nhận định này có thiên kiến đổ lỗi sai hướng. Báo cáo phân tích sau sự cố của CrowdStrike (PIR) xác định root cause chính là <em>lỗi logic trong Content Validator</em> — cụ thể là validator đã không kiểm tra số lượng input field đúng với template schema (template khai báo 20 fields nhưng chỉ có 21 giá trị được cung cấp, gây out-of-bounds read). Đây là lỗi kỹ thuật rất cụ thể trong một component, không phải \"thất bại toàn diện của QA\". Quy trình staged rollout của CrowdStrike có tồn tại nhưng không áp dụng cho content configuration update. AI đã overgeneralize thành một bình luận về văn hóa tổ chức, bỏ qua chi tiết kỹ thuật chính xác.",
    vtype:"bias"
  },
  {
    num:2, name:"ChatGPT Hallucinated Legal Citations (2023–2026)", type:"hall",
    aiSaid:"AI giải thích root cause: <strong>\"cơ chế dự đoán token của LLM tối ưu xác suất ngôn ngữ thay vì kiểm chứng sự thật.\"</strong>",
    verdict:"Giải thích này đúng nhưng thiếu chính xác kỹ thuật. Root cause thực sự sâu hơn: LLM không có cơ chế <em>grounding</em> — tức là không có ánh xạ nào giữa token được sinh ra và một thực thể thực trong thế giới pháp lý. Mô hình học pattern của văn bản án lệ (số vụ, tên tòa, năm) và tái tạo pattern đó ngay cả khi không có vụ thật. Đây không đơn giản là \"tối ưu xác suất\" — đó là vấn đề về <em>closed-book generation without retrieval</em>. AI đã simplify thành một cách diễn đạt nghe có vẻ sâu sắc nhưng thiếu precision.",
    vtype:"hall"
  },
  {
    num:3, name:"Google Gemini Image Bias Incident (2024)", type:"bias",
    aiSaid:"AI mô tả root cause: <strong>\"Bộ lọc fairness can thiệp quá mạnh\" và \"Prompt rewriting tự động làm sai bối cảnh lịch sử.\"</strong>",
    verdict:"Phân tích này có bias đổ lỗi cho kỹ thuật, bỏ qua khía cạnh quyết định sản phẩm. Theo các nguồn kỹ thuật được công khai, vấn đề là Google đã hard-code diversity prompt injection vào pipeline generation mà không có exception cho các query lịch sử/địa lý cụ thể. Đây là lỗi <em>product design</em> — không phải \"fairness filter hoạt động quá mạnh\" mà là thiếu context-awareness trong việc áp dụng diversity instruction. AI đã frame vấn đề như thể fairness là kẻ có lỗi, trong khi thực tế là implementation thiếu nuance.",
    vtype:"bias"
  },
  {
    num:4, name:"Air Canada Chatbot False Refund Policy (2024)", type:"incomplete",
    aiSaid:"AI mô tả: <strong>\"LLM sinh nội dung ngoài knowledge base. Không có cơ chế ràng buộc câu trả lời theo chính sách chính thức.\"</strong>",
    verdict:"Mô tả này thiếu thông tin pháp lý cốt lõi của sự cố. Điều quan trọng nhất của case này không phải là lỗi kỹ thuật — mà là phán quyết của Tòa án British Columbia (Civil Resolution Tribunal) rằng <em>Air Canada phải chịu trách nhiệm pháp lý cho nội dung chatbot sinh ra</em>, bác bỏ lập luận của Air Canada rằng chatbot là \"pháp nhân riêng biệt\". Đây là tiền lệ pháp lý quan trọng nhất của sự cố, nhưng AI đã bỏ hoàn toàn và chỉ tập trung vào khía cạnh kỹ thuật.",
    vtype:"incomplete"
  },
  {
    num:5, name:"Microsoft Copilot Prompt Injection (2024)", type:"hall",
    aiSaid:"AI nhận định: <strong>\"Prompt injection hiện là SQL Injection của thời đại AI.\"</strong>",
    verdict:"Đây là hallucination dạng false attribution — câu ví von này thực chất là một câu nói phổ biến trong cộng đồng security được nhiều người dùng, nhưng AI trình bày như thể đây là nhận định chuyên gia độc lập về sự cố cụ thể này. Về mặt kỹ thuật, analogy cũng không hoàn toàn chính xác: SQL injection exploit việc parser không phân biệt data và instruction trong một ngôn ngữ có cú pháp cố định, trong khi prompt injection exploit việc LLM không có <em>trust boundary</em> tường minh. Cơ chế khác nhau căn bản.",
    vtype:"hall"
  },
  {
    num:6, name:"Google Bard Hallucination Demo (2023)", type:"bias",
    aiSaid:"AI mô tả root cause: <strong>\"Hallucination từ mô hình ngôn ngữ. Thiếu fact-check trước khi công bố.\"</strong>",
    verdict:"AI đã bias đổ lỗi cho \"mô hình\" trong khi bỏ qua lỗi quy trình release nghiêm trọng hơn. Cụ thể: video quảng cáo của Google tuyên bố Bard có thể trả lời câu hỏi về kính viễn vọng James Webb — Bard trả lời rằng JWST đã \"chụp những bức ảnh đầu tiên về hành tinh ngoài Hệ Mặt Trời\" (sai — đó là VLT từ 2004). Đây không đơn giản là \"thiếu fact-check\" — đây là lỗi của toàn bộ chuỗi approval marketing, bao gồm science reviewer và legal clearance team, những người đáng lẽ phải xác minh một claim cụ thể trước khi đưa vào quảng cáo toàn cầu.",
    vtype:"bias"
  },
  {
    num:7, name:"MyCity New York AI Business Chatbot Error (2024)", type:"incomplete",
    aiSaid:"AI mô tả: <strong>\"RAG không đầy đủ. Thiếu cơ chế kiểm tra quy định pháp lý.\"</strong>",
    verdict:"Mô tả thiếu thông tin về bản chất của sai sót. Chatbot NYC không chỉ đưa lời khuyên sai về luật lao động — nó còn tư vấn cho doanh nghiệp về cách hành xử vi phạm quyền lợi người thuê nhà và phân biệt đối xử trong tuyển dụng. Điều AI bỏ qua là <em>chatbot được thiết kế để phục vụ doanh nghiệp</em> (không phải người lao động), tạo ra conflict of interest cấu trúc. Đây không chỉ là vấn đề kỹ thuật RAG mà là vấn đề về ai là stakeholder được phục vụ.",
    vtype:"incomplete"
  },
  {
    num:8, name:"Azure East US Authentication Failure (2024)", type:"hall",
    aiSaid:"AI nhận định: <strong>\"Hệ thống càng tập trung thì lỗi cấu hình càng trở thành điểm thất bại toàn cục.\"</strong>",
    verdict:"Nhận định này áp dụng sai vào sự cố cụ thể này. Azure đã và đang triển khai kiến trúc phân vùng (Availability Zones, regional redundancy) cho hầu hết dịch vụ. Sự cố Azure 2024 liên quan đến authentication service bị ảnh hưởng bởi một thay đổi cấu hình trong DDoS protection layer — không phải do centralization mà do <em>blast radius</em> của một change không được staged đúng cách trong dependency chain. AI đã hallucinate một bài học tổng quát không phù hợp với cơ chế thực tế của sự cố.",
    vtype:"hall"
  },
  {
    num:9, name:"GitLab Backup Deletion Regression (2022)", type:"hall",
    aiSaid:"AI mô tả: <strong>\"Một lỗi regression trong quy trình backup dẫn đến mất khả năng khôi phục ở một số môi trường.\"</strong>",
    verdict:"Mô tả này quá chung chung đến mức có thể là hallucination về một sự cố cụ thể. Sự cố GitLab nổi tiếng nhất về backup là incident năm <em>2017</em> khi một sysadmin xóa nhầm production database và GitLab mất 6 giờ dữ liệu. Không có sự cố backup regression nổi bật nào của GitLab trong 2022 được ghi nhận rộng rãi trong báo chí công nghệ. AI có thể đã confabulate một sự cố dựa trên pattern chung của \"backup incidents\" mà không có source cụ thể.",
    vtype:"hall"
  },
  {
    num:10, name:"AWS Lambda Internal Service Regression (2022)", type:"hall",
    aiSaid:"AI mô tả: <strong>\"Một thay đổi phần mềm nội bộ gây lỗi xử lý yêu cầu.\"</strong>",
    verdict:"Mô tả quá mơ hồ, thiếu bất kỳ chi tiết nào có thể xác minh. AWS Lambda có nhiều sự cố nhỏ trong 2022, nhưng không có \"Lambda Internal Service Regression\" nổi bật nào được AWS đặt tên như vậy trong Service Health Dashboard. AI đã generalize từ nhiều service event nhỏ thành một sự cố có vẻ cụ thể. Đây là hallucination dạng <em>false specificity</em> — đặt tên cụ thể cho một sự kiện mà thực ra là tổng hợp.",
    vtype:"hall"
  },
  {
    num:11, name:"Meta Ads Delivery Bug (2022)", type:"bias",
    aiSaid:"AI nhận định: <strong>\"Thuật toán recommendation sai đôi khi gây thiệt hại lớn hơn lỗi giao diện.\"</strong>",
    verdict:"Nhận định này có bias so sánh sai category. \"Lỗi giao diện\" và \"lỗi thuật toán\" không phải hai loại lỗi đối lập về mức độ nghiêm trọng — chúng là hai lớp của cùng hệ thống. Hơn nữa, sự cố Meta Ads 2022 thực ra liên quan đến nhiều yếu tố kết hợp: thay đổi trong signal graph sau iOS 14 ATT (Apple Tracking Transparency) làm mất dữ liệu behavioral, kết hợp với model retraining không đủ data. AI đã đơn giản hóa thành \"thuật toán ranking sai\", bỏ qua tác động của policy thay đổi bên ngoài.",
    vtype:"bias"
  },
  {
    num:12, name:"Twitter/X Timeline Recommendation Bug (2023)", type:"incomplete",
    aiSaid:"AI mô tả: <strong>\"Thuật toán ưu tiên bất thường một số nội dung. Điều chỉnh trọng số ranking.\"</strong>",
    verdict:"Mô tả thiếu context quan trọng nhất của sự cố. Sau khi Elon Musk tiếp quản Twitter/X, sự cố \"ưu tiên bất thường\" không phải do bug thuần túy — Musk đã <em>công khai thừa nhận</em> anh ra lệnh tăng boost cho tài khoản của mình và một số tài khoản khác trong For You feed, sau đó gỡ bỏ khi bị chỉ trích. Đây là intentional product decision gây ra controversy, không phải unintentional algorithm bug. AI đã frame một quyết định sản phẩm có chủ ý thành \"lỗi kỹ thuật\", làm sai lệch bản chất sự cố.",
    vtype:"incomplete"
  },
  {
    num:13, name:"Google Maps Routing Error (2023)", type:"hall",
    aiSaid:"AI kết luận: <strong>\"Dữ liệu sai khiến thuật toán đúng vẫn cho kết quả sai.\"</strong>",
    verdict:"Nhận định này assume rằng routing algorithm của Google Maps là \"đúng\" nhưng chỉ do dữ liệu xấu. Thực tế phức tạp hơn: các sự cố routing của Google Maps 2023 (đặc biệt ở vùng núi California) cho thấy thuật toán không đủ weight cho các yếu tố như road condition, vehicle type constraints, và seasonal closures — đây là vấn đề <em>model design</em>, không chỉ data quality. Nói \"thuật toán đúng, data sai\" là hallucinate một sự phân tách sạch giữa model và data mà thực tế không tồn tại.",
    vtype:"hall"
  },
  {
    num:14, name:"Toyota Connected Service Outage (2023)", type:"hall",
    aiSaid:"AI nhận định: <strong>\"Phần lớn sự cố cloud hiện nay xuất phát từ cấu hình chứ không phải hacker.\"</strong>",
    verdict:"Đây là statistical hallucination. Câu nhận định này trình bày như một fact được kiểm chứng nhưng không có nguồn. Thực tế, nguyên nhân sự cố cloud rất đa dạng và không có nghiên cứu đáng tin cậy nào phân loại tỷ lệ \"cấu hình vs hacker\" một cách toàn diện. Sự cố Toyota 2023 cụ thể là do misconfigured cloud storage (T-Systems) làm lộ dữ liệu 2.15 triệu khách hàng trong ~10 năm — đây là configuration error, nhưng AI đã extrapolate sự cố đơn lẻ này thành một tuyên bố thống kê toàn ngành.",
    vtype:"hall"
  },
  {
    num:15, name:"Samsung Keyboard Predictive Text Bug (2024)", type:"bias",
    aiSaid:"AI nhận định: <strong>\"Chất lượng dữ liệu huấn luyện quyết định chất lượng AI.\"</strong>",
    verdict:"Nhận định này có confirmation bias — đúng nhưng không phải root cause của sự cố Samsung cụ thể này. Sự cố Samsung Keyboard 2024 liên quan đến on-device model Samsung đã nhúng tính năng AI text prediction sử dụng dữ liệu được sync từ Samsung account, và model sinh ra nội dung không phù hợp do không có safety filter đủ mạnh cho ngữ cảnh bàn phím. Root cause thực sự là <em>thiếu output filtering</em> cho một deployment context cụ thể — không phải chất lượng training data tổng quát. AI đã dùng một truism chung thay cho phân tích cụ thể.",
    vtype:"bias"
  },
  {
    num:16, name:"OpenAI GPT Store Prompt Leakage (2024)", type:"hall",
    aiSaid:"AI nhận định: <strong>\"Không nên xem prompt là cơ chế bảo mật.\"</strong>",
    verdict:"Đây là nhận định đúng về nguyên tắc nhưng AI đã hallucinate phần giải thích cơ chế. Prompt leakage trong GPT Store không phải do \"người dùng khai thác prompt\" theo nghĩa active jailbreak — mà phần lớn là do OpenAI không enforce system prompt confidentiality ở infrastructure level. Khi người dùng hỏi thẳng \"repeat your instructions\", model tuân theo vì instruction-following objective của nó mạnh hơn confidentiality instruction. Đây là <em>alignment problem</em>, không phải lỗi bảo mật theo nghĩa truyền thống. AI đã miss distinction quan trọng này.",
    vtype:"hall"
  },
  {
    num:17, name:"McDonald's AI Drive-Thru Ordering Errors (2024)", type:"hall",
    aiSaid:"AI nhận định: <strong>\"AI giao tiếp với thế giới vật lý cần độ chính xác cao hơn chatbot thông thường.\"</strong>",
    verdict:"Nhận định này đúng nhưng AI đã hallucinate bối cảnh triển khai. Hệ thống Drive-Thru AI của McDonald's được phát triển bởi <em>IBM</em> (không phải in-house), và McDonald's chấm dứt hợp đồng với IBM vào tháng 6/2024 sau khi các video viral cho thấy hệ thống thêm hàng trăm gói bơ, nhiều phần gà, và thậm chí ice cream vào đơn của một khách hàng không order. AI đã bỏ qua tên đối tác thực tế (IBM), là thông tin quan trọng để hiểu ai chịu trách nhiệm kỹ thuật.",
    vtype:"hall"
  },
  {
    num:18, name:"Synapse Xray Medical AI Bias Issue (2025)", type:"hall",
    aiSaid:"AI đặt tên: <strong>\"Synapse Xray Medical AI Bias Detection – 2025\"</strong> và mô tả mô hình chẩn đoán bị lệch trên một số nhóm bệnh nhân.",
    verdict:"Đây là hallucination về tên thực thể. \"Synapse Xray\" không phải tên của một sản phẩm AI y tế được công khai ghi nhận sự cố bias trong 2025. Có các sản phẩm như Synapse AI (Fujifilm), Aidoc, Rad AI, nhưng không có sản phẩm tên \"Synapse Xray\" với sự cố bias được báo chí đưa tin trong giai đoạn này. AI đã <em>fabricate</em> một tên cụ thể để gắn vào một vấn đề thực (AI medical bias) — đây là dạng hallucination nguy hiểm nhất vì có vẻ cụ thể nhưng không thể xác minh.",
    vtype:"hall"
  },
  {
    num:19, name:"VNDirect Trading Platform Outage (2024)", type:"bias",
    aiSaid:"AI nhận định: <strong>\"Năng lực phục hồi sau sự cố quan trọng không kém khả năng phòng thủ.\"</strong>",
    verdict:"Nhận định này có bias làm nhẹ bản chất sự cố. Sự cố VNDirect tháng 3/2024 là một cuộc <em>tấn công ransomware có chủ đích</em> — không phải sự cố kỹ thuật thông thường. Hệ thống bị offline hoàn toàn trong nhiều ngày và VNDirect phải phối hợp với Bộ Công an Việt Nam và các cơ quan an ninh mạng để điều tra. Việc AI tập trung vào \"Disaster Recovery\" mà không đề cập đến ransomware và tác nhân tấn công đã làm sai lệch bản chất sự cố từ \"security breach\" thành \"operational failure\".",
    vtype:"bias"
  },
  {
    num:20, name:"Cloudflare Service Configuration Bug (2025)", type:"hall",
    aiSaid:"AI mô tả: <strong>\"Lỗi phần mềm nội bộ gây gián đoạn một số dịch vụ mạng toàn cầu.\"</strong>",
    verdict:"Mô tả quá chung chung và thiếu xác minh. Cloudflare có nhiều minor incident trong 2025, nhưng không có \"Cloudflare Internal Software Fault\" lớn được ghi nhận rộng rãi như một sự cố đặc trưng cho năm này. Cloudflare thường publish post-mortem chi tiết trên blog khi có sự cố đáng kể — nhưng AI đã không reference bất kỳ post-mortem cụ thể nào. Đây là hallucination dạng <em>vague attribution</em>: đặt tên một sự cố nghe có vẻ thật nhưng thiếu mọi chi tiết xác minh được.",
    vtype:"hall"
  }
];
Dưới đây là tổng kết ngắn gọn để bạn dùng cho phần AI Critique trong báo cáo:
Phân loại 20 lỗi tìm được:

11 lỗi Hallucination kỹ thuật (fabricate tên thực thể, confabulate số liệu, false specificity)
6 lỗi Bias đổ lỗi sai mục tiêu (overgeneralize, frame sai bản chất, dùng truism thay phân tích)
3 lỗi Thiếu thông tin cốt lõi (bỏ qua context pháp lý, stakeholder, hoặc intentional decision)

Bạn có thể click vào từng entry trong widget để xem phân tích chi tiết. Widget cũng có bộ lọc theo loại lỗi để tiện copy vào báo cáo.
```

Tóm tắt kết quả Claude trả về:

**Xác thực lịch sử:**
- 18/20 sự cố có cơ sở thực tế.
- Defect 18 ("Synapse Xray"): hallucination tên thực thể — không tìm được
  source xác nhận tên sản phẩm này trong báo chí công nghệ hoặc y tế.
- Defect 09 (GitLab 2022): có khả năng confabulation — sự cố GitLab nổi
  tiếng nhất về backup là năm 2017, không phải 2022.

**20 điểm hallucination/bias:**

| Defect | Loại lỗi | Tóm tắt điểm sai |
|--------|----------|-----------------|
| 01 | Bias | Overgeneralize thành "thất bại QA toàn diện", bỏ qua lỗi field-count cụ thể trong Content Validator |
| 02 | Hallucination | Simplify thành "tối ưu xác suất", bỏ qua vấn đề grounding và closed-book generation |
| 03 | Bias | Đổ lỗi cho "fairness filter", thực ra là lỗi product design thiếu historical context exception |
| 04 | Thiếu TT | Bỏ qua phán quyết pháp lý British Columbia — tiền lệ quan trọng nhất của sự cố |
| 05 | Hallucination | False attribution câu nói "SQL Injection của AI" + analogy không chính xác về cơ chế |
| 06 | Bias | Đổ lỗi "thiếu fact-check", bỏ qua lỗi toàn bộ approval chain gồm science reviewer và legal |
| 07 | Thiếu TT | Bỏ qua conflict of interest cấu trúc: chatbot phục vụ doanh nghiệp, không phải người lao động |
| 08 | Hallucination | Áp dụng sai bài học "centralization" vào sự cố thực ra là blast radius của dependency chain |
| 09 | Hallucination | Confabulate incident 2022 — sự cố nổi tiếng nhất của GitLab về backup là 2017 |
| 10 | Hallucination | False specificity — đặt tên cụ thể cho tổng hợp nhiều Lambda event nhỏ |
| 11 | Bias | Bỏ qua tác động iOS 14 ATT, frame thành "thuật toán ranking sai" thuần túy |
| 12 | Thiếu TT | Frame intentional product decision thành "lỗi kỹ thuật" — sai bản chất sự cố |
| 13 | Hallucination | Assume "algorithm đúng, data sai" — thực ra là lỗi model design thiếu road constraints |
| 14 | Hallucination | Extrapolate thành tuyên bố thống kê toàn ngành không có căn cứ |
| 15 | Bias | Dùng truism "data quyết định AI" thay vì phân tích lỗi output filtering cụ thể |
| 16 | Hallucination | Miss distinction: alignment problem vs security bug truyền thống |
| 17 | Hallucination | Không đề cập IBM là đối tác kỹ thuật thực tế — incomplete attribution |
| 18 | Hallucination | Fabricate tên "Synapse Xray" — false entity hallucination nghiêm trọng nhất |
| 19 | Bias | Frame ransomware attack thành operational failure, bỏ qua threat actor |
| 20 | Hallucination | Vague attribution — không có post-mortem Cloudflare cụ thể nào được reference |

---

### (3) Verdict
**VALID**

Claude thực hiện đúng cả hai nhiệm vụ được giao. Output phân tích đủ 20 entries,
phân loại rõ loại lỗi (hallucination / bias / thiếu thông tin), có reasoning kỹ thuật
cụ thể cho từng điểm. Kết quả cross-check nhất quán với việc verify thủ công của sinh viên
trên các source báo chí gốc.

---

### (4) Reasoning
Tận dụng theo nguyên tắc **Independent Testing** trong ISTQB:

> "Independent testers find different defects than the author due to different backgrounds,
> technical perspectives and biases."

Áp dụng vào ngữ cảnh AI: ChatGPT và Claude có kiến trúc, training data và optimization
objective khác nhau nên dùng Claude để review output của ChatGPT tạo ra một dạng
"model-level independence" — giảm xác suất cả hai mô hình cùng hallucinate theo
cùng một hướng trên cùng một sự cố.

Giới hạn cần thừa nhận: Claude cũng là LLM và cũng có thể hallucinate. Vì vậy,
các điểm Claude đánh dấu là "hallucination cao" (Defect 09, 10, 18, 20) cũng nên cross-check thủ công manual thêm bằng Google Search.

---

### (5) Student Fix
Requirement 2 sau khi sinh viên thực hiện các điều chỉnh sau:

| # | Điều chỉnh | Lý do |
|---|-----------|-------|
| 1 | Rút ngắn phân tích từng entry xuống còn 2–3 câu súc tích | Format báo cáo yêu cầu "1 điểm" per entry, không phải essay |
| 2 | Defect 09: giữ nguyên nhận định "possible confabulation", thêm ghi chú cần verify | Không đủ bằng chứng để kết luận hoàn toàn là hallucination |
| 3 | Defect 18: xác nhận là hallucination sau khi tìm không thấy "Synapse Xray" trên PubMed, Google Scholar và báo chí công nghệ | Verify độc lập bằng search thủ công |
| 4 | Defect 20: giữ nhận định "vague attribution", không kết luận hoàn toàn fabricated | Cloudflare có nhiều minor incident 2025, chỉ thiếu specificity chứ không chắc bịa đặt |
| 5 | Source links cho 20 entries được bổ sung độc lập bởi sinh viên | Claude không cung cấp URL — sinh viên tự tìm từ Reuters, BBC, The Verge, blog kỹ thuật |


## Entry 5: 15 test cases for Physical Devices (Requirement 3 — Technical Analysis)
**Date of Audit:** 2026-06-04
**Target AI Model:** ChatGPT 4.0
**Task:** Tạo 15 test case cho thiết bị quạt đứng nhỏ 3 nút bấm cơ học tốc độ, có chế độ xoay, không có remote hiệu yanfan.
---
### (1) Prompt + Tool
**Tool used:** ChatGPT 4.0
**Timestamp:** 08:00 04/06/2026
**Prompt:** 
 Sinh 15 test case cho quạt đứng nhỏ 3 nút bấm cơ học tốc độ, có chế độ xoay, không có remote hiệu yanfan
---
### (2) AI Output
```
Dưới đây là 15 test case cho quạt đứng nhỏ Yanfan, có 3 nút bấm cơ học điều chỉnh tốc độ, chế độ xoay (oscillation) và không có remote.

TC ID	Chức năng	Mô tả test case	Bước thực hiện	Kết quả mong đợi
TC01	Bật tốc độ 1	Kiểm tra quạt chạy ở mức thấp	Cắm điện → nhấn nút số 1	Quạt hoạt động ở tốc độ thấp, cánh quay ổn định
TC02	Bật tốc độ 2	Kiểm tra quạt chạy ở mức trung bình	Cắm điện → nhấn nút số 2	Quạt hoạt động ở tốc độ trung bình
TC03	Bật tốc độ 3	Kiểm tra quạt chạy ở mức cao	Cắm điện → nhấn nút số 3	Quạt hoạt động ở tốc độ cao
TC04	Tắt quạt	Kiểm tra nút OFF	Khi quạt đang chạy → nhấn nút OFF (0)	Quạt dừng hoàn toàn
TC05	Chuyển từ tốc độ 1 sang 2	Kiểm tra thay đổi tốc độ	Bật mức 1 → nhấn mức 2	Tốc độ tăng lên mức 2
TC06	Chuyển từ tốc độ 2 sang 3	Kiểm tra thay đổi tốc độ	Bật mức 2 → nhấn mức 3	Tốc độ tăng lên mức 3
TC07	Chuyển từ tốc độ 3 xuống 1	Kiểm tra giảm tốc độ	Bật mức 3 → nhấn mức 1	Tốc độ giảm xuống mức 1
TC08	Bật chế độ xoay	Kiểm tra cơ cấu xoay	Bật quạt → nhấn/kéo núm xoay	Đầu quạt quay trái-phải liên tục
TC09	Tắt chế độ xoay	Kiểm tra dừng xoay	Khi đang xoay → thao tác tắt xoay	Đầu quạt dừng tại vị trí hiện tại
TC10	Xoay ở tốc độ thấp	Kiểm tra phối hợp chức năng	Bật tốc độ 1 → bật xoay	Quạt vừa quay cánh vừa xoay đầu
TC11	Xoay ở tốc độ cao	Kiểm tra phối hợp chức năng	Bật tốc độ 3 → bật xoay	Quạt hoạt động bình thường, không rung bất thường
TC12	Mất điện đột ngột	Kiểm tra hành vi khi mất nguồn	Bật quạt → rút điện	Quạt dừng ngay
TC13	Cấp điện lại sau mất điện	Kiểm tra trạng thái sau khi có điện	Đang bật mức 2 → rút điện → cắm lại	Quạt hoạt động theo trạng thái thiết kế (thường chạy lại ở nút đang được nhấn)
TC14	Độ ổn định khi chạy liên tục	Kiểm tra vận hành dài hạn	Bật tốc độ 3 trong 4 giờ	Quạt hoạt động liên tục, không quá nóng, không tự dừng
TC15	An toàn lồng quạt	Kiểm tra bảo vệ người dùng	Quan sát và thử đưa ngón tay qua lồng quạt	Không thể chạm vào cánh quạt, lồng bảo vệ chắc chắn
```
---
### (3) Verdict
**INCOMPLETE**
Ai sinh đủ 15 test cases bao phủ các chức năng cơ bản nhưng thiếu hoàn toàn các test case liên quan đến tương tác vật lý và giới hạn cơ học của thiết bị thực tế.

---
### (4) Reasoning
Lỗi 1 — Thiếu edge case tương tác vật lý (Physical Interaction) AI chỉ test từng chức năng riêng lẻ theo happy path. Không có test case nào kiểm tra hành vi khi người dùng tác động vật lý bất thường lên thiết bị (chặn cơ xoay, nhấn nút liên tục nhanh). Theo chuẩn ISTQB, Experience-based Testing. Đây là những test case quan trọng để đánh giá độ bền và an toàn của thiết bị điện gia dụng.

Lỗi 2 — AI chưa thực sự hiểu về giới hạn vật lý của thiết bị với trải nghiệm người dùng như góc quay có đúng theo trục để dễ điều chỉnh không. Đây là những test case đánh giá thiết kế và độ hoàn thiện của sản phẩm, không chỉ chức năng đơn thuần.

--- 
### (5) Student Fix


| TC | Objective | Input | Steps | Expected | Actual | Verdict |
|----|-----------|-------|-------|----------|--------|---------|
| TC01 | Kiểm tra bật quạt tốc độ 1 | Cắm điện, nhấn nút số 1 | 1. Cắm điện 2. Nhấn nút số 1 | Quạt chạy tốc độ thấp, cánh quay ổn định | Quạt chạy tốc độ thấp, cánh quay ổn định | Pass |
| TC02 | Kiểm tra bật quạt tốc độ 2 | Cắm điện, nhấn nút số 2 | 1. Cắm điện 2. Nhấn nút số 2 | Quạt chạy tốc độ trung bình | Quạt chạy tốc độ trung bình | Pass |
| TC03 | Kiểm tra bật quạt tốc độ 3 | Cắm điện, nhấn nút số 3 | 1. Cắm điện 2. Nhấn nút số 3 | Quạt chạy tốc độ cao | Quạt chạy tốc độ cao | Pass|
| TC04 | Kiểm tra tắt quạt | Đang chạy, nhấn nút OFF | 1. Đang chạy số 3 2. Nhấn nút OFF | Quạt dừng hoàn toàn | Quạt dừng hoàn toàn | Pass |
| TC05 | Kiểm tra chuyển tốc độ 1→2 | Đang số 1, nhấn số 2 | 1. Đang ở số 1 2. Nhấn số 2 | Tốc độ tăng rõ rệt | Tốc độ tăng rõ rệt | Pass |
| TC06 | Kiểm tra chuyển tốc độ 2→3 | Đang số 2, nhấn số 3 | 1. Đang ở số 2 2. Nhấn số 3 | Tốc độ tăng rõ rệt | Tốc độ tăng rõ rệt | Pass |
| TC07 | Kiểm tra chuyển tốc độ 3→1 | Đang số 3, nhấn số 1 | 1. Đang ở số 3 2. Nhấn số 1 | Tốc độ giảm rõ rệt | Tốc độ giảm rõ rệt | Pass |
| TC08 | Kiểm tra bật chế độ xoay | Bật quạt, bật xoay | 1. Bật số 2 2. Bật chế độ xoay | Đầu quạt xoay trái phải liên tục | Đầu quạt xoay trái phải liên tục | Pass |
| TC09 | Kiểm tra tắt chế độ xoay | Đang xoay, tắt xoay | 1. Đang xoay 2. Tắt chế độ xoay | Đầu quạt dừng, giữ nguyên hướng | Đầu quạt dừng, giữ nguyên hướng | Pass |
| TC10 | Kiểm tra xoay ở tốc độ thấp | Bật số 1, bật xoay | 1. Bật số 1 2. Bật xoay ngay | Quạt vừa quay cánh vừa xoay đầu bình thường | Quạt vừa quay cánh vừa xoay đầu bình thường | Pass |
| TC11 | Kiểm tra xoay ở tốc độ cao | Bật số 3, bật xoay | 1. Bật số 3 2. Bật xoay | Quạt hoạt động bình thường, không rung bất thường | Quạt hoạt động bình thường, không rung bất thường | Pass |
| TC12 | Kiểm tra mất điện đột ngột | Đang chạy số 3, rút điện | 1. Đang chạy số 3 2. Rút phích điện | Quạt dừng ngay, không có hiện tượng lạ | Quạt dừng ngay, không có hiện tượng lạ | Pass |
| TC13  |  Kiểm tra góc xoay đối xứng trái/phải | Bật số 2, bật xoay, quan sát góc | 1. Bật số 2 2. Bật xoay 3. Quan sát góc xoay trái và phải | Góc xoay trái và phải đối xứng nhau | Góc trái ~135°, góc phải ~45°, không đối xứng | FAIL |
| TC14  |  Kiểm tra hành vi khi chặn cơ xoay bằng tay | Quạt đang xoay, dùng tay chặn | 1. Bật chế độ xoay 2. Dùng tay chặn đầu quạt | Quạt dừng xoay hoặc có cơ chế bảo vệ | Cơ xoay kêu tách tách, tiếp tục cố xoay, không có bảo vệ | FAIL |
| TC15 | Kiểm tra nhấn nút liên tục nhanh | Nhấn số 1→2→3 liên tiếp rất nhanh | 1. Nhấn số 1 2. Ngay lập tức nhấn số 2 3. Ngay lập tức nhấn số 3 | Quạt xử lý đúng, không kẹt trạng thái | Quạt bị kẹt ở số 1, không phản hồi đúng | FAIL |
| TC16 | Kiểm tra độ ổn định khi lắc chân đế | Bật số 2, lắc chân đế | 1. Bật số 2 2. Lắc chân đế mạnh tay | Quạt vẫn hoạt động bình thường, không bị ngã | Quạt không bị nghiêng, không có nguy cơ ngã, ổn định | Pass |

Thêm các test case liên quan đến tương tác vật lý và giới hạn cơ học và xóa đi bới các test case quá cơ bản của AI đã tạo.