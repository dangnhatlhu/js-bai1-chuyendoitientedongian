# Nhật ký prompt và giải thích

## Nhật ký prompt

**Yêu cầu:** Bạn là một lập trình viên Javascipt. Hãy Viết mã JavaScript cho phép nhập số lượng USD và tính ra số tiền VND tương ứng với tỷ giá giả định 25.000 VND/USD. Kết quả hiển thị trong console. Đặt toàn bộ mã trong `index.html`, giải thích các dòng code và lưu nhật ký prompt vào `nhatky_promt.md`.

## Giải thích mã trong `index.html`

- `<!DOCTYPE html>` khai báo tài liệu sử dụng chuẩn HTML5.
- `<html lang="vi">` bắt đầu trang HTML và khai báo ngôn ngữ là tiếng Việt.
- `<head>` chứa thông tin cấu hình và tiêu đề trang.
- `<meta charset="UTF-8">` giúp hiển thị chính xác tiếng Việt.
- `<meta name="viewport" content="width=device-width, initial-scale=1.0">` giúp trang hiển thị phù hợp trên thiết bị di động.
- `<title>Chuyển đổi USD sang VND</title>` đặt tiêu đề hiển thị trên tab trình duyệt.
- `<body>` chứa nội dung người dùng nhìn thấy trên trang.
- `<h1>` hiển thị tiêu đề chức năng.
- `<p>` hướng dẫn mở Developer Tools và tab Console để xem kết quả.
- `<script>` bắt đầu phần mã JavaScript chạy trong trình duyệt.
- `const exchangeRate = 25000;` khai báo tỷ giá cố định: 1 USD bằng 25.000 VND.
- `const input = prompt(...)` mở hộp thoại để người dùng nhập số tiền USD; nếu nhấn Cancel, giá trị nhận được là `null`.
- `if (input === null)` kiểm tra trường hợp người dùng hủy nhập và ghi thông báo vào console.
- `else` chỉ xử lý tiếp khi người dùng không hủy hộp thoại.
- `const usd = Number(input);` chuyển nội dung nhập thành kiểu số để có thể tính toán.
- `if (input.trim() === "" || !Number.isFinite(usd) || usd < 0)` từ chối nội dung rỗng, giá trị không phải số hữu hạn và số tiền âm.
- `console.log(...)` trong nhánh nhập sai hiển thị hướng dẫn nhập số USD hợp lệ.
- `const vnd = usd * exchangeRate;` nhân số USD với tỷ giá để tính số VND.
- ``console.log(`${usd} USD = ${vnd.toLocaleString("vi-VN")} VND`);`` hiển thị phép quy đổi trong console; `toLocaleString("vi-VN")` định dạng số theo cách đọc quen thuộc tại Việt Nam.
- `</script>`, `</body>` và `</html>` lần lượt đóng phần JavaScript, nội dung trang và tài liệu HTML.

## Cách chạy

1. Mở `index.html` bằng trình duyệt.
2. Nhập số USD trong hộp thoại rồi nhấn OK.
3. Nhấn F12, mở tab **Console** để xem kết quả hoặc thông báo lỗi nhập liệu.
