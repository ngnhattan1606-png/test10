# Chuyến xe ban đêm — V4 Vercel-safe

Bản V4 đã chỉnh:

- tài xế luôn nằm **trên layer của khách**, kể cả khách 02;
- ở các step đón khách, nút **Trả khách** chỉ xuất hiện sau khi người dùng đã mở và đóng bài báo của đúng nhân vật đó;
- hover/focus vào vùng nhân vật sẽ hiện thẻ thông tin nhanh: **họ tên, tuổi, nghề nghiệp**;
- các trường họ tên/tuổi hiện để placeholder `[ ... ]` nhằm tránh tự bịa dữ liệu nhân vật; thay trực tiếp trong `profile` của Step 4, 7, 10 nếu có dữ liệu thật;
- giữ nguyên logic cùng địa điểm: tài xế không chạy lại nếu route không đổi;
- toàn bộ ảnh vẫn được nhúng trực tiếp trong `index.html`, không cần thư mục `assets/`, tránh lỗi mất hình trên Vercel.

## Deploy GitHub → Vercel

Repo chỉ cần:

- `index.html`
- `vercel.json`
- `README.md`

Framework Preset: **Other**. Không cần build command/output directory.
