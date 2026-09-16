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

### Họ và tên — MSSV

- Phần việc và file/commit/PR: Làm UI và báo cáo app.py, eval_group.json, TEAM.md
- Quyết định, khó khăn và cách xử lý: Phần khó là làm sao có API key để test, giải quyết bằng cách dùng gemini 3.1 flash-lite.
- Điều đã học: Học được cách làm UI cho 1 AI agent.
- AI/công cụ đã dùng và cách kiểm tra: Dùng API Gemini để xử lý, Python, Streamlit (xây dựng giao diện UI), VS Code, GitHub. Cách kiểm tra: Chat trực tiếp trên web UI để kiểm tra phản hồi và các hộp thoại gọi tool.
- Thời điểm đã tự nộp URL repo chung trên VLearn: 16/09/2026
