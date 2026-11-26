# BÀI LÀM PHA 2 – HACKATHON 02

- **Mã đề:** 07
- **Họ tên:** thi_thanh_dat
- **Lớp:** CNTT2
- **Link repository Pha2:**
- **Công cụ AI đã dùng (ChatGPT/Claude/Gemini):** Gemini

> Pha 2 (20 phút cuối). Mỗi mục: mở cuộc trò chuyện mới, gửi nguyên văn prompt đã viết trong bai_lam_pha1.md, dán câu trả lời và link chia sẻ vào đây. Xong, kéo thả file này vào repository Pha2.

## 4.2. Trích xuất tin nhắn đặt vé vào cổng ra JSON

**KET QUA AI**

```text
[
  {
    "loai_ve": "VECH",
    "ngay_choi": "2026-12-20",
    "nguoi_lon": 2,
    "tre_em": 1,
    "loai_tu": "nho",
    "ghi_chu": null
  },
  {
    "loai_ve": "VECN",
    "ngay_choi": "2027-01-03",
    "nguoi_lon": 3,
    "tre_em": 0,
    "loai_tu": null,
    "ghi_chu": "Một người đang bó bột tay"
  },
  {
    "loai_ve": "VEVIP",
    "ngay_choi": null,
    "nguoi_lon": 4,
    "tre_em": 0,
    "loai_tu": "lon",
    "ghi_chu": "một bạn đi xe lăn"
  }
]
```

**Link trò chuyện:** https://share.gemini.google/HIftxbvWjY2k

## 4.3. Báo giá bằng Chain-of-Thought

**KET QUA AI**

```text
Dựa trên dữ liệu bảng giá và quy tắc tính giá của Công viên Sóng Xanh, dưới đây là bản hạch toán chi tiết báo giá cho đoàn trường sử dụng gói **Vé cả ngày (VECN)**:

**Tóm tắt thông tin đầu vào:**

* **Loại vé áp dụng:** Vé cả ngày (VECN) — đơn giá người lớn $250.000\text{ đồng/vé}$.
* **Cơ cấu đoàn:** $8$ người lớn; $4$ trẻ em cao từ $1\text{ m}$ đến $1,4\text{ m}$ ($1,05\text{ m}$; $1,15\text{ m}$; $1,2\text{ m}$; $1,3\text{ m}$); $2$ bé cao dưới $1\text{ m}$.
* **Dịch vụ đi kèm:** Thuê $6$ áo phao — đơn giá $40.000\text{ đồng/chiếc}$.

---

**Bước 1: Tiền người lớn**

* Đoàn có $8$ người lớn mua vé VECN với đơn giá $250.000\text{ đồng/vé}$:

$$8 \times 250.000 = 2.000.000\text{ đồng}$$



**Bước 2: Tiền trẻ em**

* **Nhóm trẻ cao từ $1\text{ m}$ đến $1,4\text{ m}$:** Cả $4$ trẻ em ($1,05\text{ m}$; $1,15\text{ m}$; $1,2\text{ m}$ và $1,3\text{ m}$) đều thuộc khung chiều cao tính $60\%$ giá vé người lớn.
* Đơn giá vé trẻ em: $250.000 \times 60\% = 150.000\text{ đồng/vé}$.
* Thành tiền cho $4$ trẻ em: $4 \times 150.000 = 600.000\text{ đồng}$.


* **Nhóm trẻ cao dưới $1\text{ m}$:** $2$ bé được miễn phí hoàn toàn ($0\text{ đồng}$).
* **Tổng tiền vé trẻ em:**

$$600.000 + 0 = 600.000\text{ đồng}$$



**Bước 3: Tiền vé (tiền người lớn + trẻ em)**

* Cộng tiền vé người lớn (Bước 1) và tiền vé trẻ em (Bước 2):

$$2.000.000 + 600.000 = 2.600.000\text{ đồng}$$



**Bước 4: Giảm giá nhóm (tính ra vé sau khi giảm)**

* Do đoàn có $8$ người lớn (đạt điều kiện đoàn từ $8$ người lớn trở lên), đoàn được hưởng mức chiết khấu $10\%$ tính trên tổng tiền vé:
* Số tiền giảm giá nhóm: $2.600.000 \times 10\% = 260.000\text{ đồng}$.
* Tiền vé sau khi giảm:

$$2.600.000 - 260.000 = 2.340.000\text{ đồng}$$





**Bước 5: Phụ thu**

* Đoàn thuê $6$ chiếc áo phao với đơn giá $40.000\text{ đồng/chiếc}$ (theo quy định, khoản phụ thu không áp dụng giảm giá):

$$6 \times 40.000 = 240.000\text{ đồng}$$



**Bước 6: Tổng tiền**

* Tổng số tiền đoàn cần thanh toán bằng tiền vé sau giảm (Bước 4) cộng phụ thu (Bước 5):

$$2.340.000 + 240.000 = 2.580.000\text{ đồng}$$


* *Đối chiếu kiểm tra:* $(2.600.000 \times 90\%) + (6 \times 40.000) = 2.340.000 + 240.000 = 2.580.000\text{ đồng}$ (khớp số liệu).

---

Để bản báo giá sát hơn nữa với quy trình nghiệp vụ thực tế, bạn có muốn tôi điều chỉnh giọng văn theo thư chào giá gửi Ban Giám hiệu nhà trường, trình bày thêm bảng kê đối soát kế toán, hay bổ sung quy tắc xử lý khi sĩ số thực tế tại cổng thay đổi hoặc khách hỏi các chi phí ngoài dữ liệu không?

[RESULT: 2.580.000 đồng]
```

**Link trò chuyện:** https://share.gemini.google/b1jo5bcUNGsU

### b) Kiểm tra kết quả AI

(Ghi kết luận AI đúng hay sai; nếu sai, ghi bước sai đầu tiên và kết quả đúng của bước đó – xoá dòng này)

## 4.4. Dây chuyền xử lý khiếu nại – kết quả Trạm 1

**KET QUA AI**

```text
{
  "loai_su_co": "dong_khu_choi",
  "so_khach": 4,
  "so_khu_bi_dong": 2,
  "tom_tat": "Khách đi 4 người khiếu nại hai khu chơi lớn đóng cửa cả ngày không thông báo trước."
}
```

**Link trò chuyện:** https://share.gemini.google/JMGICznLbFCv

## 4.5. Prompt chấm bài theo Rubric

**KET QUA AI**

```text
Dạ chào quý khách, Trợ lý Sóng Xanh xin phản hồi thắc mắc của mình ạ:

* **Vé buổi chiều (VECH):** Hệ thống hiện chưa được cập nhật bảng giá niêm yết chi tiết theo ngày đi và đối tượng khách (người lớn/trẻ em).

Về trường hợp công viên đóng cửa sớm do mưa lớn, hiện em chưa có dữ liệu quy định hỗ trợ hay đền bù chính thức nên xin phép xác minh lại với bộ phận quản lý để phản hồi chính xác nhất. Quý khách dự định tham quan vào ngày nào và đi đoàn mấy người để em hỗ trợ kiểm tra giúp mình ạ?

---

*Để kịch bản tư vấn vận hành trơn tru và ra kết quả trọn vẹn hơn, bạn có muốn bổ sung thêm các thông tin còn thiếu sau không:*

1. **Dữ liệu gốc:** Bảng giá niêm yết của 3 hạng vé (`VECN`, `VECH`, `VEVIP`) và quy định xử lý/bảo lưu vé khi gặp thời tiết xấu?
2. **Hoàn thiện mục Xử lý ngoại lệ (đang để trống):** Quy định rõ câu mẫu từ chối khi khách hỏi ngoài phạm vi (ví dụ: hỏi vé trò chơi lẻ, dịch vụ bên ngoài, hoặc chính sách chưa ban hành) và cách hỏi lại khi khách cung cấp thiếu thông tin đặt vé (ngày đi, số lượng người lớn/trẻ em)?
```

**Link trò chuyện:** https://share.gemini.google/I3ZJY0EUprIt
