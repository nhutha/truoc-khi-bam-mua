# Trước Khi Bấm Mua — trang sản phẩm theo từng video

Trang đích cho link bio TikTok của kênh [@truockhibammua](https://www.tiktok.com/@truockhibammua).
Xem tại **<https://nhutha.github.io/truoc-khi-bam-mua/>**.

## Đây là gì

Mỗi video giải thích một thông số bị hiểu sai khi mua đồ công nghệ. Trang này liệt kê, theo
từng video, **5 sản phẩm mà chính hãng có công bố đúng con số video đó nói tới** — kèm link
tới trang thông số của hãng để người xem tự kiểm.

Hai điều trang này cố ý làm khác:

- **Con số lấy từ trang hãng, không lấy từ mô tả người bán.** Mỗi dòng có link nguồn.
- **Không xếp hạng.** Kênh không cầm hàng nên không đo được cái nào tốt hơn.

## Không sửa `index.html` bằng tay

File này được sinh ra. Sửa dữ liệu rồi chạy lại generator:

```bash
python production/scripts/build-affiliate-landing-page.py
```

Nguồn dữ liệu là `production/affiliate/products.json` trong repo sản xuất (không công khai).
Generator **chặn** nếu một sản phẩm thiếu URL trang hãng, hoặc nếu URL nguồn lại trỏ về
Shopee — tức là không thể vô tình đăng một con số mà chỉ người bán khai.

Luật chọn hàng đầy đủ: `docs/gan-link-affiliate-shopee-vao-video.md` trong repo sản xuất.
