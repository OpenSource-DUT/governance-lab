# Bản đồ lộ trình phát triển

Lộ trình của governance-lab được rà soát hàng quý bởi Project Lead và các Maintainers; khi đủ cơ cấu, Steering Committee đảm nhiệm việc rà soát. Các mục chưa đánh dấu là kế hoạch, chưa phải kết quả đã hoàn thành.

## Hiện tại — Now — Quý 1 năm 2027

- [x] Hoàn thiện bộ quy chế quản trị cộng đồng tại .github/GOVERNANCE.md, bao gồm bậc thang thăng tiến và trạng thái Emeritus.
- [ ] Hoàn tất kiểm chứng phân quyền Admin, Write, Triage và quy trình đóng góp qua fork.
- [x] Kiểm chứng workflow tiếp nhận Issue: bình luận chào mừng và gán nhãn status: needs-triage. Minh chứng: [Issue #1](https://github.com/OpenSource-DUT/governance-lab/issues/1), [workflow thành công](https://github.com/OpenSource-DUT/governance-lab/actions/runs/45146097320).
- [ ] Thiết lập kiểm thử CI/CD tự động đạt độ phủ mã nguồn tối thiểu 80% khi dự án có mã nguồn ứng dụng.
- [ ] Rà soát và xử lý các lỗ hổng P0 trong module xử lý chuỗi khi module được triển khai.

## Tiếp theo — Next — Quý 2 năm 2027

- [ ] Hoàn tất thảo luận, xử lý phản đối và phê duyệt RFC-0001 về Structured JSON Logging.
- [ ] Triển khai định dạng log JSON theo RFC-0001 sau khi RFC được chấp thuận; duy trì tương thích trong giai đoạn chuyển đổi đã thống nhất.
- [ ] Hỗ trợ đóng gói đa nền tảng: Linux, macOS và Windows ARM64.
- [ ] Bổ sung ít nhất 02 thành viên vào nhóm Reviewers/Triagers theo tiêu chuẩn GOVERNANCE.md.

## Tương lai — Later — Cuối năm 2027 trở đi

- [ ] Nghiên cứu biên dịch WebAssembly cho phiên bản chạy trên trình duyệt.
- [ ] Đánh giá mức độ sẵn sàng và chuẩn bị hồ sơ gia nhập CNCF Sandbox.

## Theo dõi tiến độ

- Core Maintainer @tphus-810 theo dõi các Issue/PR liên quan; Project Lead @dhtphu05 điều phối việc rà soát.
- Chỉ đánh dấu hoàn thành khi có minh chứng tương ứng từ tài liệu, Issue, PR hoặc workflow run.
- Khi thay đổi ưu tiên hoặc thời hạn, mở PR cập nhật roadmap và ghi rõ lý do.
