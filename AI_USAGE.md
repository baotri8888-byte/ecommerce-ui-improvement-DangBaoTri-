# AI Usage Log

## 1. Công cụ AI
Tên công cụ:
- Gemini: phân tích website (Prompt 1).
- Claude: đề xuất phương án thiết kế, hỗ trợ viết HTML/CSS, rà soát kết quả kiểm tra (Prompt 2, Prompt 3).

## 2. Mục đích sử dụng
- Phân tích giao diện Zara VN theo 5 khu vực.
- Đề xuất bố cục và phương án thiết kế thẻ sản phẩm.
- Hỗ trợ viết mã HTML/CSS và giải thích các thành phần.
- Hỗ trợ tìm và sửa lỗi sau khi tôi chạy thử.

## 3. Prompt đã sử dụng

**Prompt 1 – Phân tích website (Gemini)**
```
Bạn là chuyên gia phân tích nghiệp vụ và thiết kế trải nghiệm người dùng
cho website thương mại điện tử.

Tôi đang khảo sát website: Zara Việt Nam (https://www.zara.com/vn/).

Hãy giúp tôi lập bảng phân tích các khu vực:
1. Trang chủ. 2. Danh mục sản phẩm. 3. Chi tiết sản phẩm. 4. Tìm kiếm. 5. Giỏ hàng.

Với mỗi khu vực, hãy nêu:
- Mục đích của chức năng.
- Thành phần giao diện cần có.
- Điểm thuận tiện đối với khách hàng.
- Một vấn đề có thể phát sinh.
- Một đề xuất cải tiến.

Không khẳng định những tính năng chưa được kiểm chứng.
Phân biệt rõ nhận xét dựa trên quan sát và đề xuất của AI.
```

**Prompt 2 – Đề xuất phương án giao diện (Claude)**
```
Tôi đang thực hiện bài tập phát triển giao diện website thương mại điện tử
bằng HTML5 và CSS3.

Tôi muốn cải tiến khu vực: thẻ sản phẩm để hiển thị hình ảnh, tên, giá và nút mua hàng rõ ràng hơn.
Vấn đề quan sát được: (1) giá khuyến mãi chưa nổi bật; (2) % giảm dính liền với giá mới;
(3) tên sản phẩm bị cắt trên điện thoại; (4) nút thêm vào giỏ chỉ là dấu "+" nhỏ;
(5) ô chọn màu nhỏ, khó phân biệt, không có tên màu.

Đối tượng sử dụng: khách hàng mua sắm trực tuyến tại Việt Nam.

Hãy đề xuất: 1. Bố cục giao diện. 2. Các thành phần HTML cần sử dụng. 3. Cách tổ chức CSS.
4. Cách hiển thị trên máy tính và điện thoại. 5. Những điểm cần kiểm tra về khả năng sử dụng.

Trước tiên, hãy giải thích phương án thiết kế.
Chưa tạo toàn bộ mã nguồn cho đến khi tôi yêu cầu.
```

**Prompt 3 – Tạo mã nguồn (Claude)**
```
Dựa trên phương án đã thống nhất, hãy tạo một trang giao diện
thương mại điện tử bằng HTML5 và CSS3.

Yêu cầu:
- Giao diện có tiêu đề và khu vực sản phẩm.
- Có tối thiểu 4 sản phẩm mẫu.
- Mỗi sản phẩm có hình ảnh, tên, giá và nút thao tác.
- Bố cục phù hợp với màn hình máy tính và điện thoại.
- Mã HTML có cấu trúc rõ ràng.
- CSS được tách thành file riêng.
- Không sử dụng backend hoặc cơ sở dữ liệu.
- Không đưa thư viện hoặc thành phần không cần thiết vào dự án.

Giải thích cách chạy trang web và những phần tôi cần kiểm tra.
```

Các prompt phụ: nhờ AI nhận xét ảnh chụp màn hình Zara (máy tính và điện thoại) để xác định vấn đề; nhờ sửa tên màu hiển thị trên điện thoại; nhờ rà lỗi ảnh không hiện.

## 4. Kết quả AI đề xuất
- **Gemini:** bảng phân tích 5 khu vực kèm đề xuất như thanh điều hướng nhanh, Quick View, accordion thông tin sản phẩm, gợi ý tìm kiếm, thanh tiến trình freeship.
- **Claude:** phương án thẻ sản phẩm (ảnh tỷ lệ 3:4, nhãn % giảm ở góc ảnh, giá mới nổi bật, ô màu, nút "Thêm vào giỏ"), lưới 2/3/4 cột theo màn hình, và bản đầu của `index.html` và `css/style.css`.

## 5. Kiểm tra và điều chỉnh
Đã kiểm tra:
- [ ] Đối chiếu bảng của Gemini với website thật (ghi rõ mục đúng/sai: ...)
- [ ] Mở trang trên máy tính: 4 cột, ảnh hiện đủ
- [ ] Kiểm tra bằng Chrome DevTools ở 375px, 768px, 1280px
- [ ] Không có thanh cuộn ngang ở màn hình nhỏ
- [ ] Phím Tab hiện viền focus ở nút "Thêm vào giỏ"

Đã sửa:
- Tên màu chỉ hiện khi rê chuột nên điện thoại không thấy: thêm `<p class="swatch-names">` và CSS `.swatch-names`.
- Ảnh không hiện vì để trong `images/placeholder/` trong khi `src` trỏ `images/`: chuyển ảnh về `images/`.
- Ảnh sản phẩm thứ 4 của tôi là áo sơ mi, không khớp mô tả ban đầu của AI: sửa tên, `alt` và màu cho đúng ảnh.

Không sử dụng:
- Các đề xuất của Gemini mà tôi không thấy trên website thật: [liệt kê các ý đã loại bỏ].

## 6. Phần tôi hiểu và có thể giải thích
(Hãy viết lại bằng lời của bạn sau khi đã hiểu từng ý.)

- **`<article class="product-card">`**: mỗi sản phẩm là một khối nội dung độc lập, nằm trong `<li>` của danh sách `<ul class="product-grid">`.
- **`<del>`** cho giá gốc: thẻ ngữ nghĩa thể hiện nội dung bị gạch bỏ; kèm `.sr-only` để trình đọc màn hình đọc "Giá gốc", "Giá khuyến mãi".
- **`display: grid` và `grid-template-columns: repeat(2, 1fr)`**: chia lưới 2 cột đều nhau cho điện thoại; `@media (min-width: 600px)` đổi thành 3 cột, `@media (min-width: 1024px)` đổi thành 4 cột.
- **Mobile-first**: viết CSS cho điện thoại trước, rồi dùng `min-width` mở rộng cho màn hình lớn.
- **`aspect-ratio: 3 / 4` và `object-fit: cover`**: giữ khung ảnh cùng tỷ lệ và cắt ảnh vừa khung thay vì méo.
- **`line-clamp: 2` và `min-height`**: giới hạn tên 2 dòng và chừa sẵn chiều cao 2 dòng để các thẻ thẳng hàng.
- **`position: absolute` cho `.badge`** (đặt trong `.product-card__media` có `position: relative`): đặt nhãn % giảm ở góc ảnh.
- **`.btn` có `margin-top: auto`** trong thẻ `display: flex; flex-direction: column`: đẩy nút xuống đáy thẻ.
- **Biến CSS (`:root`)**: đổi màu, khoảng cách ở một chỗ.
- **`.swatch-names`**: tên màu hiển thị bằng chữ vì điện thoại không có hover.
