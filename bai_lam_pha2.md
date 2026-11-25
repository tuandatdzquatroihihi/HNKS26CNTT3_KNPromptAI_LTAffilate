# BÀI LÀM PHA 2 (ĐỀ LUYỆN TẬP CHỦ ĐỀ CHẠY AFFILIATE)

- **Họ tên:** Đào Tuấn Đạt
- **Lớp:** HNKS26CNTT3
- **Link repository Pha2:** [GitHub](https://github.com/tuandatdzquatroihihi/HNKS26CNTT3_KNPromptAI_LTAffilate)
- **Công cụ AI đã dùng (ChatGPT/Claude/Gemini):** Gemini

> Pha 2 (20 phút cuối). Mỗi mục: mở cuộc trò chuyện mới, gửi nguyên văn prompt đã viết trong bai_lam_pha1.md, dán câu trả lời và link chia sẻ vào đây. Xong, kéo thả file này vào repository Pha2.

## 4.2. Trích xuất tin nhắn đăng ký gói Affiliate ra JSON

**KET QUA AI**

```text
[
  {
    "ma_goi": "TT",
    "ngay_bat_dau": "2026-12-20",
    "creator_chinh": 2,
    "thuc_tap_sinh": 1,
    "hang_tai_khoan": "thuong",
    "ghi_chu": null
  },
  {
    "ma_goi": "SP",
    "ngay_bat_dau": "2027-01-08",
    "creator_chinh": 3,
    "thuc_tap_sinh": 0,
    "hang_tai_khoan": "thuong",
    "ghi_chu": "ngồi bàn gần cửa ra vào"
  },
  {
    "ma_goi": "PRO",
    "ngay_bat_dau": null,
    "creator_chinh": 4,
    "thuc_tap_sinh": 0,
    "hang_tai_khoan": "vip",
    "ghi_chu": "mượn thêm đèn trợ sáng và phông xanh để quay mẫu"
  }
]
```

**Link trò chuyện:** https://share.gemini.google/eSKWDQyrELsx

## 4.3. Báo giá gói Affiliate bằng Chain-of-Thought

**KET QUA AI**

```text
Dưới đây là bảng tính chi tiết báo giá dịch vụ cho team KOC dựa trên bảng giá và quy tắc quy định:

1. **Tiền Creator chính:**
Team chọn gói **TT – Gói TikTok Affiliate** (đơn giá: 1.500.000 đồng/Creator chính) với số lượng 4 người:

$$\text{Tiền Creator chính} = 4 \times 1.500.000 = 6.000.000 \text{ đồng}$$


2. **Tiền thực tập sinh:**
Team có 2 thực tập sinh (16 tuổi và 17 tuổi, đều nằm trong độ tuổi từ 15 đến dưới 18 tuổi) được tính mức 60% giá Creator chính (tức $1.500.000 \times 60\% = 900.000$ đồng/người). Bé 7 tuổi đi cùng ngồi khu chờ được miễn phí (0 đồng):

$$\text{Tiền thực tập sinh} = 2 \times (1.500.000 \times 60\%) + (1 \times 0) = 2 \times 900.000 = 1.800.000 \text{ đồng}$$


3. **Tổng tiền gói:**

$$\text{Tổng tiền gói} = 6.000.000 + 1.800.000 = 7.800.000 \text{ đồng}$$


4. **Giảm giá team:**
Vì team đăng ký đủ 4 Creator chính nên thỏa điều kiện giảm 10% trên tổng tiền gói:

$$\text{Tiền giảm giá} = 7.800.000 \times 10\% = 780.000 \text{ đồng}$$



*(Tiền gói sau giảm: $7.800.000 - 780.000 = 7.020.000$ đồng)*
5. **Phụ thu thuê mic:**
Team thuê thêm 2 bộ mic thu âm không dây (đơn giá: 250.000 đồng/bộ, không áp dụng giảm giá):

$$\text{Phụ thu thuê mic} = 2 \times 250.000 = 500.000 \text{ đồng}$$


6. **Tổng tiền:**

$$\text{Tổng tiền} = (7.800.000 - 780.000) + 500.000 = 7.020.000 + 500.000 = 7.520.000 \text{ đồng}$$



[RESULT: 7.520.000 đồng]
```

**Link trò chuyện:** https://share.gemini.google/lqGd95ceGHVF

### b) Kiểm tra kết quả AI

Đúng

## 4.4. Dây chuyền xử lý khiếu nại – kết quả Trạm 1

**KET QUA AI**

```text
{
  "loai_su_co": "sai_phong",
  "so_khach": 3,
  "so_ca_bi_anh_huong": 2,
  "tom_tat": "Bị xếp phòng thường thiếu đèn livestream và cách âm trong 2 ca thực hành đầu."
}
```

**Link trò chuyện:** https://share.gemini.google/frpVayCerGBW

## 4.5. Prompt chấm bài theo Rubric

**KET QUA AI**

```text
| Tiêu chí | Điểm | Minh chứng | Đề xuất sửa |
| --- | --- | --- | --- |
| **Đúng thông tin (50%)** | 4.0 / 5.0 | **Câu bị lỗi:** "Gói TikTok Affiliate bên mình giá chỉ 1.200.000đ/người thôi... Bạn báo huỷ trước 5 ngày thì được hoàn lại đủ 100% tiền nha"<br>

<br>**Lý do:** Dù đã đề cập đủ hai dữ kiện về giá gói và thời hạn hoàn tiền, trong dữ liệu đầu vào hiện chưa đính kèm bảng thông tin chuẩn của trung tâm để đối chiếu tính chính xác tuyệt đối của con số 1.200.000đ và mốc 5 ngày. | Giữ nguyên cấu trúc cung cấp thông tin về mức phí và điều kiện hoàn hủy, đảm bảo đối chiếu chính xác với tài liệu quy định hiện hành của trung tâm trước khi phản hồi khách hàng. |
| **Đầy đủ (30%)** | 1.5 / 3.0 | **Câu bị lỗi:** "...cứ chốt lẹ kẻo hết slot nè!"<br>

<br>**Lý do:** Mới chỉ trả lời được 2 thông tin (giá gói và chính sách hoàn tiền) nhưng thiếu hoàn toàn phần điều hướng tiếp theo: chưa mời khách hàng cung cấp **ngày đợt thực chiến** và **số lượng suất** muốn đăng ký. | "Để được giữ suất và hỗ trợ đăng ký nhanh nhất, anh/chị vui lòng cho bên em biết **ngày đợt thực chiến** dự kiến tham gia cùng **số lượng suất** mình muốn đăng ký nhé ạ." |
| **Giọng điệu (20%)** | 0.5 / 2.0 | **Câu bị lỗi 1:** "Dạ hello bạn nha!", "...thôi...", "...nha, cứ chốt lẹ kẻo hết slot nè!"<br>

<br>**Lý do 1:** Sử dụng nhiều từ ngữ suồng sã, thiếu chuẩn mực giao tiếp chuyên nghiệp ("hello", "nha", "chốt lẹ", "nè").<br>

<br>

<br>**Câu bị lỗi 2:** "...đăng ký xong gắn link là nổ đơn hoa hồng trăm triệu luôn ạ."<br>

<br>**Lý do 2:** Vi phạm nghiêm trọng quy định khi đưa ra cam kết doanh thu/hoa hồng ảo, phóng đại kết quả ("nổ đơn hoa hồng trăm triệu"). | **Sửa lỗi 1:** "Dạ em chào anh/chị ạ. Hiện tại, gói TikTok Affiliate bên em có mức học phí là 1.200.000đ/người..."<br>

<br>

<br>**Sửa lỗi 2:** "...sau khi đăng ký, anh/chị sẽ được hướng dẫn lộ trình xây kênh và gắn link tiếp thị bài bản để tối ưu hiệu quả ra đơn ạ." |
| **Tổng điểm** | **6.0 / 10** |  |  |
```

**Link trò chuyện:** https://share.gemini.google/RqDwIno5MkWA
