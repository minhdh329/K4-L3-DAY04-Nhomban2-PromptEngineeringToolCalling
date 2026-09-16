# TEAM — Day04, K4-L3B

**Làm nhóm.** Mỗi người tự viết và commit phần INDIVIDUAL của mình.

## Thông tin bài nộp

- Tên nhóm: Nhomban2
- Người đại diện / MSSV: 2A202602680
- Tên repo: `K4-L3-DAY04-HoVaTen-MSSV-PromptEngineeringToolCalling`
- URL repo, nhánh nộp, commit chốt: IT Helpdesk
- Deadline áp dụng và link thông báo đổi hạn nếu có: 

## Thành viên

| Họ và tên | MSSV | GitHub | Vai trò và công việc | File/commit/PR |
|---|---|---|---|---|
| Dương Hải Minh | 2A202602680 | minhdh329 | Làm UI, Report | app.py, eval_group.json, TEAM.md |
| Đào Thị Huyền | 2A202602670 | huyenlili | Sửa lỗi | eval_base.json, system.md, tool.yaml |
| Lê Minh Hiếu | 2A202602828 | tiu42 | Trưởng nhóm | PR almost, PR idek |
| Đỗ Trương Thành Ân | 2A202602889 | dotruongthanhan | Sửa lỗi | Update version 1,2; Add version 1,2; PR Merge something |

## Nhận xét chung

- **Kết quả và bằng chứng:** Nhóm đã xây dựng thành công IT Helpdesk Agent có khả năng gọi công cụ (tool calling).
- **Thay đổi hiệu quả nhất:** Việc sửa system prompt giúp agent không vượt quá boudary cho phép, ví dụ thêm sửa xoá phải có xác nhận từ người dùng.
- **Giới hạn còn lại:** Hệ thống API miễn phí có giới hạn khắt khe về số lượt gọi (rate limit), dễ dẫn đến lỗi nếu Agent lặp lại tool nhiều lần trong một vòng hội thoại. Ngoài ra, Agent chỉ có thể đưa ra chẩn đoán hoặc tạo báo cáo/ticket thông qua các công cụ đã được phân quyền.
- **Cách phân công và tích hợp:** Công việc được module hóa rõ ràng. Nhóm tích hợp mã nguồn thông qua việc tạo nhánh (branch) trên Git/VS Code, đảm bảo các phần code độc lập hoạt động mượt mà với nhau trên nhánh `main`.

## INDIVIDUAL

Sao chép mục này cho từng thành viên.

### Dương Hải Minh — 2A202602680

- Phần việc và file/commit/PR: Làm UI và báo cáo app.py, eval_group.json, TEAM.md
- Quyết định, khó khăn và cách xử lý: Phần khó là làm sao có API key để test, giải quyết bằng cách dùng gemini 3.1 flash-lite.
- Điều đã học: Học được cách làm UI cho 1 AI agent.
- AI/công cụ đã dùng và cách kiểm tra: Dùng API Gemini để xử lý, Python, Streamlit (xây dựng giao diện UI), VS Code, GitHub. Cách kiểm tra: Chat trực tiếp trên web UI để kiểm tra phản hồi và các hộp thoại gọi tool.
- Thời điểm đã tự nộp URL repo chung trên VLearn: 16/09/2026

### Đỗ Trương Thành Ân — 2A202602889

- Phần việc và file/commit/PR: Sửa lỗi base, phần lớn là lỗi khai báo tools require thiếu data ở các tools: `search_kb` và `clarify`
- Quyết định, khó khăn và cách xử lý: Đọc hiểu dự án. Dự án có code base khá đồ sộ và cần đọc hiểu trong thời gian ngắn. Tôi đã sử dụng coding Agent trong IDE VS Code (Antigravity) để yêu cầu phân tích tổng hợp chung dự án.
- Điều đã học: Học được cách sử dụng AI giúp mình nắm bắt công việc nhanh hơn.
- AI/công cụ đã dùng và cách kiểm tra: Dùng Gemini để hỏi đáp, đề xuất phương án sửa lỗi. Cách kiểm tra: Trước khi hỏi Gemini phải có định hướng trước, kết quả của AI là gợi ý, đối chiếu lại với định hướng ban đầu, tìm điểm chung giữa 2 bên (con người và AI) để chọn phương án phù hợp nhất
- Thời điểm đã tự nộp URL repo chung trên VLearn: 15/09/2026

### Đào Thị Huyền - 2A202602670

#### Phần việc
- Tham gia xây dựng và hoàn thiện IT Service Desk Agent cho Northstar Labs.
- Thiết kế và điều chỉnh system prompt cho các nhóm yêu cầu: service status, device, knowledge base, employee, environment và ticket.
- Kiểm tra logic routing và clarification khi thiếu hoặc không rõ thông tin.
- Evaluation các case H01–H20 và M01–M10, phân tích PASS/FAIL.
- Xử lý lỗi ambiguous environment như `demo` khi hệ thống chỉ hỗ trợ `production` và `staging`.

#### Bằng chứng kỹ thuật
- `system.md` — system prompt của IT Service Desk Agent.
- Evaluation results của các case H01–H20 và M01–M10.

#### Điều đã học
- Biết cách viết và điều chỉnh system prompt.
- Biết phân tích kết quả PASS/FAIL để tìm lỗi.
- Hiểu cách xử lý thông tin không rõ ràng bằng clarification.

### Lê Minh Hiếu — 2A202602828

- Phần việc và file/commit/PR:
    - Sửa lỗi H04_user_routing: chỉnh sửa tool description của lookup_user cho cụ thể hơn để agent hiểu & không gọi nhầm tool khác
    - Sửa lỗi H12_confirm_before_ticket: chỉnh sửa system prompt, thêm constraint buộc agent phải xác nhận với người dùng trước khi tạo ticket
    - Sửa lỗi M06_switch_tool: chỉnh sửa system prompt, thêm rule là luôn làm theo intent mới của người dùng
    - Tạo & merge các pull request: "Almost" và "idek"
- Quyết định, khó khăn và cách xử lý:
    - Khó khăn chính là agent đôi khi chọn nhầm tool hoặc tiếp tục intent cũ trong hội thoại nhiều lượt. Cách xử lý là viết rule theo điều kiện cụ thể, sau đó chạy lại các case H04, H12 và M06 để kiểm tra cả tool name, arguments và thứ tự hành động.
    - Với ticket, giữ nguyên rào chắn hai lớp: prompt yêu cầu gọi `clarify` trước, còn `create_ticket` chỉ ghi file khi `confirmed` là `true`.
- Điều đã học:
    - Tool description ảnh hưởng trực tiếp đến routing; mô tả rõ input, output và giới hạn giúp model phân biệt các tool gần nghĩa.
    - System prompt phù hợp để nêu nguyên tắc hội thoại và confirmation, nhưng kết quả cần được kiểm tra bằng trace thật thay vì chỉ nhìn câu trả lời cuối.
- AI/công cụ đã dùng và cách kiểm tra:
    - Dùng GitHub Copilot/AI assistant để hỗ trợ phân tích trace và rà soát thay đổi.
    - Kiểm tra bằng `run_eval.py`, đọc các file JSON trong `starter_v3/runs/`, đối chiếu các case H04, H12 và M06 với expected tool calls, đồng thời kiểm tra system prompt, tool declaration và trạng thái file ticket.
- Thời điểm đã tự nộp URL repo chung trên VLearn: 10:47:37 16/9/2026