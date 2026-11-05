# Công cụ giải bóng bàn

Hai công cụ miễn phí, chạy ngay trên trình duyệt, không cần cài đặt, không cần tài khoản. Không có dữ liệu người chơi nào được lưu trên mạng: mọi thứ nằm trong máy của bạn.

| Công cụ | Dùng để làm gì | Mở bằng |
|---|---|---|
| **Ghi điểm + phụ đề** (`index.html`) | Bấm điểm từng trận trên điện thoại, sau đó tạo file phụ đề `.srt` khớp với video quay bằng máy quay cố định | Điện thoại và máy tính |
| **Giải bóng bàn** (`GiaiBongBan.html`) | Nhập danh sách người chơi, chia bảng, in danh sách trận, bảng xếp hạng, sơ đồ nhánh (giấy hoặc Word) | Máy tính |

Link dùng: https://friendzoner49.github.io/tt-giai-dau/ (ghi điểm) và https://friendzoner49.github.io/tt-giai-dau/GiaiBongBan.html (tổ chức giải).

---

## 1. Tổ chức giải và in giấy (máy tính)

1. Mở `GiaiBongBan.html`.
2. Tab **Người chơi**: dán tên từng hạng (mỗi dòng một người, xếp theo thứ tự mạnh đến yếu), bấm **Cập nhật**.
3. Tab **Chia bảng**: máy chia bảng theo "số người kỳ vọng mỗi bảng". Có thể chia tay.
4. Tab **Giải đôi**: ghép đôi bằng tay.
5. Tab **In giấy**: bấm **Tải file Word (.docx)** để chỉnh tay và gửi cho người khác in, hoặc **In thẳng từ trang này** (bỏ tích "Đầu trang và chân trang" trong hộp thoại in).
6. Bấm **Sao chép danh sách trận cho điện thoại** nếu sẽ ghi điểm bằng điện thoại (mục 2).

Lưu ý: đổi danh sách người (kể cả người đến muộn) thì mã đánh số lại, hãy in lại tất cả các tờ cùng lúc. Dữ liệu lưu trong trình duyệt; dùng **Lưu file sao lưu** / **Mở file sao lưu** để sao lưu.

## 2. Ghi điểm trên điện thoại

Mở link ghi điểm trên điện thoại (iPhone: Safari, rồi **Chia sẻ → Thêm vào Màn hình chính** để dùng như ứng dụng, mở lại không cần mạng).

1. Tab **Ghi điểm**: dán danh sách trận đã sao chép ở mục 1, bấm **Nạp danh sách**.
2. Gõ mã trận vào ô tìm kiếm (ví dụ `NH1`), bấm vào trận.
3. Bấm **▶ Bắt đầu** khi trận bắt đầu. Bấm tên người thắng điểm: mỗi lần bấm là +1.
4. Máy tự nhận hết set, hết trận, và tự đổi bên sau mỗi set (ở set quyết định, đổi bên khi người đầu tiên chạm 5 điểm). Bấm **Đổi bên** nếu cần chỉnh.
5. Bấm **↶ Hoàn tác** nếu bấm nhầm.
6. **Chế độ nhẹ (chỉ bấm khi hết set)**: đỡ mỏi tay. Có thể chọn trận 5 hoặc 3 set.
7. Mỗi lần bấm được lưu ngay trong điện thoại. Tải lại trang không mất. Cuối ngày bấm **Lưu file ghi điểm** để gửi file ghi điểm sang máy tính.

### Tab Đồng hồ

Hiện giờ có phần mười giây. **Đầu mỗi clip, quay vào màn hình này khoảng 3 giây.** Có hình đồng hồ trong video thì máy tính biết chính xác clip bắt đầu lúc nào, không phụ thuộc đồng hồ máy quay.

## 3. Tạo phụ đề cho video (máy tính)

1. Mở link ghi điểm trên máy tính, chọn tab **Phụ đề (máy tính)**.
2. Chọn file ghi điểm (JSON) từ điện thoại, rồi chọn các clip video.
3. Máy tự đọc giờ bắt đầu từ tên file DJI (ví dụ `DJI_20261031200203_0155_D.MP4` là 20:02:03) và giờ trong file.
4. Nếu giờ đồng hồ máy quay lệch: mở mục "khớp chính xác", gõ giờ nhìn thấy trên đồng hồ quay và giây tương ứng trong video, bấm **Tính giờ bắt đầu**.
5. Bấm **Tạo phụ đề (.srt)**: ra file `.srt` cùng tên clip, mỗi lần đổi tỉ số là một dòng.
6. DaVinci Resolve: kéo file `.srt` vào dòng thời gian (hoặc Media Pool, rồi vào track phụ đề).

Chỉ trận có trong khoảng clip mới ra phụ đề. Nếu báo "Không có lần bấm nào rơi vào clip", kiểm tra lại giờ bắt đầu hoặc múi giờ.

## Đã kiểm và chưa kiểm

- Đã kiểm: bấm điểm, hoàn tác, đổi bên tự động, lưu và nạp lại, tạo `.srt`, đọc giờ từ tên file và từ file mp4 của máy DJI Osmo Pocket 3 thật (giờ trong tên file là giờ địa phương của máy quay, giờ trong header mp4 là UTC; máy quay mẫu lệch UTC+3 và máy đọc ra đúng 20:02:03 cả hai cách). Máy tính nên đặt cùng múi giờ với máy quay.
- Chưa kiểm: điện thoại iPhone thật (giữ sáng màn hình, chia sẻ file), nhập `.srt` vào DaVinci, in A4 thật.

## Mã nguồn

Bản công khai chỉ chứa công cụ đã đóng gói. Không chứa tên hay dữ liệu người chơi.
