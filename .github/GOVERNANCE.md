# Quy chế quản trị dự án

Dự án governance-lab của OpenSource-DUT vận hành theo mô hình Đồng thuận mở (Consensus-Seeking) kết hợp Công trạng kỹ thuật (Meritocracy). Quyền hạn đi kèm trách nhiệm và được trao dựa trên đóng góp bền bỉ, với lộ trình thăng tiến công khai.

## 1. Bậc thang thăng tiến

### Cấp 1 — Community Contributor

- Điều kiện: Có ít nhất 01 Pull Request được duyệt và gộp vào dự án; đóng góp có thể là mã nguồn, tài liệu hoặc kiểm thử.
- Trách nhiệm: Tuân thủ quy tắc ứng xử, mô tả rõ đóng góp và tiếp nhận phản hồi review.
- Quyền hạn: Được ghi nhận đóng góp và tham gia thảo luận Issue, Pull Request, RFC. Contributor bên ngoài đóng góp qua fork, không được cấp quyền ghi vào repo gốc.

### Cấp 2 — Reviewer / Triager

- Điều kiện: Có tối thiểu 05 PR chất lượng cao; tích cực hỗ trợ giải đáp và tái hiện lỗi trên Issue Tracker trong 30 ngày.
- Trách nhiệm: Sàng lọc Issue, kiểm tra khả năng tái hiện, xác định loại việc và mức ưu tiên, hỗ trợ người mới.
- Quyền GitHub: Triage; được gán/gỡ nhãn có sẵn, chỉ định người xử lý và đóng/mở Issue hoặc PR, nhưng không được push mã nguồn hoặc merge PR.
- Việc tạo, sửa hoặc xóa định nghĩa nhãn do người có quyền Write hoặc Admin thực hiện theo đề xuất của Triager.

### Cấp 3 — Core Maintainer

- Điều kiện: Đóng góp bền bỉ ít nhất 03 tháng, nắm vững kiến trúc dự án, được 01 Maintainer hiện tại đề cử và đạt 100% đồng thuận của các Core Maintainers đang hoạt động.
- Trách nhiệm: Review mã nguồn, quản lý nhánh main/develop, điều phối công việc và theo dõi ROADMAP.md.
- Quyền GitHub: Write; tạo nhánh, push thay đổi, review và merge PR theo quy trình của dự án, tạo tag phiên bản.

### Cấp 4 — Steering Committee

- Cơ cấu: 03 thành viên thường trực, nhiệm kỳ 01 năm, được cộng đồng Core Maintainers bầu bằng bỏ phiếu kín.
- Trách nhiệm: Ban hành quy chế, giải quyết tranh chấp, xử lý báo cáo an ninh và vi phạm quy tắc ứng xử, quyết định định hướng dự án.
- Quyền GitHub: Admin; quản lý quyền truy cập, cấu hình repository, Secrets và tài sản số của dự án.

## 2. Bổ nhiệm và thành viên danh dự

- Đề cử thăng tiến phải được ghi nhận công khai bằng Issue hoặc PR, kèm bằng chứng đóng góp và kết quả biểu quyết.
- Maintainer không hoạt động liên tục trong 06 tháng được chuyển sang trạng thái Emeritus Member.
- Admin thực hiện thu hồi quyền Write/Admin của người chuyển sang Emeritus để bảo vệ dự án; việc ghi nhận đóng góp lịch sử được giữ nguyên.
- Thành viên có thể chủ động từ nhiệm. Việc khôi phục quyền cần được xem xét lại theo vai trò và sự đồng thuận hiện tại.

## 3. Quy trình RFC và Lazy Consensus

1. Contributor tạo nhánh và gửi PR chứa đề xuất tại docs/rfc/RFC-NNNN.md, nêu tóm tắt, động lực, thay đổi phá vỡ tương thích và các giải pháp thay thế.
2. Project Lead công bố bắt đầu thảo luận, ghi rõ thời điểm bắt đầu, kết thúc và múi giờ. Thời hạn thông thường là 72 giờ; nếu bài thực hành dùng thời hạn mô phỏng ngắn hơn, phải ghi rõ ngay trong PR.
3. Thành viên phản hồi +1 (đồng ý), 0 (trung lập) hoặc -1 (phản đối có lý do kỹ thuật cụ thể).
4. Khi còn phản đối -1 chưa được giải quyết, đề xuất chưa được thông qua. Tác giả cập nhật RFC bằng commit mới trong cùng PR; người phản đối xác nhận rút phản đối khi vấn đề được giải quyết.
5. Khi hết thời hạn và không còn phản đối hợp lệ chưa giải quyết, Project Lead tổng kết quyết định, cập nhật trạng thái RFC thành ACCEPTED và merge PR. Nếu không đạt đồng thuận, ghi nhận việc gia hạn, hoãn hoặc bác bỏ cùng lý do.

Sự im lặng không tự kích hoạt thao tác merge trên GitHub. Việc phê duyệt RFC cũng chưa có nghĩa là tính năng đã được triển khai.

## 4. Quy trình cộng tác và phân quyền

- Mọi thay đổi thường lệ được đề xuất qua PR và được tài khoản khác review trước khi merge. Việc khởi tạo bộ hồ sơ ban đầu là ngoại lệ do Project Lead thực hiện.
- Sinh viên A: @dhtphu05 — Project Lead, Admin; chủ trì và merge RFC sau khi hoàn tất quy trình.
- Sinh viên B: @tphus-810 — Core Maintainer, Write; review, merge PR thông thường và theo dõi roadmap.
- Sinh viên C: @TruongDayNe — Reviewer/Triager, Triage; chỉ thực hiện quyền tương ứng sau khi chấp nhận lời mời truy cập.
- Sinh viên D: Contributor bên ngoài; dùng tài khoản riêng, mở Issue và gửi PR từ fork, không nhận quyền Write trên repo gốc.

Đây là phân công vai trò ban đầu của bài thực hành, không phải bằng chứng các tài khoản đã hoàn thành điều kiện thăng tiến. Trong giai đoạn khởi tạo chưa đủ 03 thành viên Steering Committee, A đảm nhiệm Project Lead; chưa coi đây là hội đồng đủ cơ cấu.

## 5. Quy tắc ứng xử và xử lý tranh chấp

- Thảo luận tập trung vào vấn đề kỹ thuật; không công kích cá nhân hoặc phân biệt đối xử. Chất lượng đóng góp không miễn trừ trách nhiệm ứng xử.
- Project Lead tiếp nhận phản ánh qua kênh liên hệ công khai trong hồ sơ GitHub, thống nhất kênh riêng trước khi chia sẻ thông tin nhạy cảm và bảo vệ người phản ánh.
- Áp dụng bốn mức chế tài theo [Contributor Covenant 2.1](https://www.contributor-covenant.org/version/2/1/code_of_conduct/): Correction, Warning, Temporary Ban, Permanent Ban. Mức xử lý dựa trên tác động và lịch sử vi phạm, không bắt buộc đi tuần tự qua mọi mức.
- Người có xung đột lợi ích phải công khai và không tự quyết định vụ việc liên quan đến mình; nếu chưa có người xử lý độc lập, nhóm đề nghị giảng viên hỗ trợ.

## 6. Kế thừa và rà soát

Danh sách người phụ trách và quy trình chuyển giao khẩn cấp được công bố trong MAINTAINERS.md. GOVERNANCE.md và ROADMAP.md được rà soát hàng quý; thay đổi quy chế được thảo luận công khai qua PR.
