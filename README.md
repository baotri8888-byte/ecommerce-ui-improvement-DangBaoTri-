# E-commerce UI Improvement

## 1. Giới thiệu
Bài tập cá nhân Chương 1 môn Phát triển ứng dụng WEB/TMĐT (UEH).

Mình khảo sát website thời trang **Zara Việt Nam** và cải tiến một khu vực giao diện nhỏ: **thẻ sản phẩm trong danh sách sản phẩm đang giảm giá**. Trang demo gồm 4 thẻ mẫu, làm bằng HTML5 và CSS3 thuần.

## 2. Website tham khảo
- Tên website: ZARA Việt Nam
- URL: https://www.zara.com/vn/
- Khu vực đã khảo sát: Trang chủ, Danh mục sản phẩm, Chi tiết sản phẩm, Tìm kiếm, Giỏ hàng (trọng tâm cải tiến: thẻ sản phẩm ở danh mục giảm giá)

## 3. Chức năng
- Hiển thị danh sách sản phẩm.
- Hiển thị tên và giá sản phẩm (giá khuyến mãi, giá gốc, % giảm).
- Hiển thị màu sắc có sẵn (ô màu và tên màu) và nút "Thêm vào giỏ".
- Bố cục hỗ trợ nhiều kích thước màn hình: 2 cột trên điện thoại, 3 cột trên máy tính bảng, 4 cột trên máy tính.

## 4. Công nghệ
- HTML5
- CSS3 (Grid, Flexbox, biến CSS, media query)

## 5. Cách chạy
Mở file `index.html` bằng trình duyệt.

- Mã nguồn (GitHub): https://github.com/baotri8888-byte/ecommerce-ui-improvement-DangBaoTri-
- Bản demo trực tuyến (GitHub Pages): https://baotri8888-byte.github.io/ecommerce-ui-improvement-DangBaoTri-/

## 6. Cải tiến đã thực hiện
**Vấn đề ban đầu** (quan sát trên Zara VN, máy tính và điện thoại):

| # | Vấn đề | Thay đổi đã thực hiện |
|---|---|---|
| 1 | Giá khuyến mãi không nổi bật: giá gốc, % giảm và giá mới cùng cỡ chữ nhỏ | Giá mới cỡ chữ lớn, đậm, màu đỏ; giá gốc nhỏ, xám, gạch ngang (`<del>`) |
| 2 | % giảm dính liền với giá mới trong cùng khối nền đen | Nhãn % giảm tách riêng, đặt ở góc ảnh |
| 3 | Tên sản phẩm bị cắt bằng "…" trên điện thoại | Cho tên hiển thị tối đa 2 dòng, chừa sẵn chiều cao 2 dòng để các thẻ thẳng hàng |
| 4 | Nút thêm vào giỏ chỉ là dấu "+" nhỏ | Nút "Thêm vào giỏ" có chữ, rộng bằng thẻ, cao tối thiểu 44px |
| 5 | Ô màu nhỏ, khó phân biệt, không có tên màu | Ô màu tròn 24px có viền và tên màu hiển thị bằng chữ |

**Điểm tự phát hiện và sửa khi kiểm tra:**
- Tên màu ban đầu chỉ hiện khi rê chuột (thuộc tính `title`), điện thoại không có hover nên không thấy. Đã thêm dòng chữ `.swatch-names` hiển thị trực tiếp.
- Ảnh không hiện do để sai thư mục (`images/placeholder/`), đã chuyển về `images/` cho khớp đường dẫn `src` trong HTML.

## 7. Hỗ trợ từ AI
- Công cụ: Gemini (phân tích website), Claude (đề xuất phương án và hỗ trợ viết mã HTML/CSS).
- AI hỗ trợ: lập bảng phân tích 5 khu vực, đề xuất bố cục, viết bản đầu của HTML/CSS.
- Phần tôi đã tự kiểm tra, điều chỉnh: đối chiếu kết quả AI với website thật, loại bỏ nhận xét chưa kiểm chứng, chạy thử trên máy tính và điện thoại, tự sửa lỗi tên màu và lỗi đường dẫn ảnh.
- Chi tiết xem file [AI_USAGE.md](AI_USAGE.md).

## 8. Cấu trúc thư mục
```
ecommerce-ui-improvement-DangBaoTri-/
├── index.html
├── css/
│   └── style.css
├── images/
│   ├── product-1.jpg
│   ├── product-2.jpg
│   ├── product-3.jpg
│   └── product-4.jpg
├── README.md
└── AI_USAGE.md
```

## 9. Nguồn ảnh
Ảnh minh họa sản phẩm chỉ dùng cho mục đích học tập. Nguồn: [ĐIỀN NGUỒN ẢNH CỦA BẠN, ví dụ: ảnh tham khảo từ zara.com/vn, hoặc Unsplash/Pexels kèm tên tác giả].
