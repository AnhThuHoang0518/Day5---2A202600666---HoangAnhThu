# Evidence Pack — Moni Tài Chính (Ví MoMo AI Spending Insight)

## 1. Nhóm và Track
* **Tên nhóm:** Nhóm Moniii
* **Track:** D — Personal Finance (Tài chính cá nhân)
* **Product/app đã chọn:** Ví MoMo
* **Build slice đang nghĩ:** AI Action Layer trên Lịch sử giao dịch MoMo giúp phân tích chi tiêu tháng, phân loại giao dịch mập mờ/chưa rõ mục đích, cảnh báo rủi ro và gợi ý nhắc lịch thanh toán hóa đơn.

---

## 2. Nhật Ký Tự Trải Nghiệm (Self-Use Evidence)
Nhóm tự mở app MoMo thực tế, thực hiện các giao dịch hằng ngày và ghi nhận lại các điểm gãy (pain points):

| Observation | Screenshot/link | Path liên quan | Điều học được |
|---|---|---|---|
| Giao dịch chuyển tiền cho cá nhân bị bỏ trống danh mục và ghi nhận nhãn "Chưa phân loại". | [Screenshot](./2aoboqavvntn0jxydbta2iyldgevif4oknbdqk5i12.jpg) | Low-confidence Path | User lười tự tay tìm danh mục để gán. AI cần chủ động hỏi lại kèm các phương án trả lời nhanh thay vì bắt user chọn thủ công. |
| Giao dịch thanh toán Google Services bị AI tự động phân loại vào "Giải trí" dù thực tế là mua Workspace để làm việc. | [Screenshot](./2aoboqavvntpr8uliollt3tlel9flczf47cwekau8.jpg) | Failure / Correction Path | AI tự quyết dễ dẫn đến sai lệch dữ liệu. Cần hiển thị nhãn tin cậy (Medium Confidence) và cung cấp nút sửa nhanh (Correction Flow). |
| Trang chủ chứa quá nhiều banner dịch vụ phụ và quảng cáo, đẩy phần lịch sử chi tiêu xuống rất sâu. | [Screenshot](./2aoboqavvnkxbkbvmvlcj7azddrnpjjddhzpjzcs5.jpg) | Happy Path | Thông tin chi tiêu quan trọng bị phân tán. Cần thiết kế một Finance Card tinh gọn tập trung số liệu và có lối tắt truy cập AI. |
| Chatbot Moni gốc trên MoMo báo "Không tìm thấy" khi người dùng hỏi các câu hỏi tự nhiên về chi tiêu lẩu/ăn uống. | [Screenshot](./2aoboqavvnl02z7thidozsvtgdhe84wdggsnukcs1.jpg) | Happy Path | Ô nhập liệu tự do (free-text) dễ làm AI bối rối. Cần bổ sung các gợi ý dạng chip bấm nhanh (Suggested Prompt Chips) để định hướng. |

---

## 3. Khảo Sát & Bằng Chứng Xã Hội (User / Review / Social Evidence)
Nhóm đã tiến hành phỏng vấn chéo nhanh 5 người dùng MoMo thuộc phân khúc sinh viên và người mới đi làm:

| Quote / review / observation | Nguồn | User là ai? | Pain/failure mode |
|---|---|---|---|
| *"Cuối tháng chả bao giờ biết tiền đi đâu. Mở lịch sử giao dịch thì một đống tên người chuyển khoản chia tiền ăn, app không tự gán nhãn nên biểu đồ cuối tháng sai bét."* | Phỏng vấn trực tiếp | Khánh, 21 tuổi, Sinh viên năm 3 | Thiếu tính năng gợi ý phân loại tự động cho giao dịch cá nhân. |
| *"Nhiều lúc tài khoản bị trừ tiền Google mới nhớ ra là đến hạn dịch vụ. Muốn hủy đăng ký thì lười tra cứu, giá mà app tự nhắc trước."* | Phỏng vấn trực tiếp | Nam, 20 tuổi, Sinh viên | Không phát hiện được các giao dịch định kỳ để nhắc nhở người dùng. |
| *"Tôi không thích AI tự động đổi tiền bạc của mình mà không hỏi trước. Nhiều lúc nó đoán sai nhóm chi tiêu thì rất khó chịu."* | Phỏng vấn trực tiếp | Vy, 23 tuổi, Nhân viên bán hàng | Sợ rủi ro tự động hóa hoàn toàn (automation). Ủng hộ cơ chế AI gợi ý - người dùng quyết định (augmentation). |
| *"Tôi muốn biết chính xác tại sao tháng này chi tiêu của tôi lại tăng vọt chứ không chỉ muốn nhìn cái biểu đồ tròn vô hồn."* | Phỏng vấn trực tiếp | Trang, 22 tuổi, Designer | Thiếu lớp giải thích (explainable AI) bằng ngôn ngữ tự nhiên về xu hướng tài chính. |

> **Ghi chú về kiểm chứng:** Đây là khảo sát thực tế được nhóm thực hiện nhanh qua Google Meet/tin nhắn trước checkpoint M1 của Day 06 để củng cố giả định.

---

## 4. Phân Tích Đối Thủ (Competitor / Analog Evidence)

| App / mô hình tham khảo | Họ xử lý task này thế nào? | Pattern học được | Có áp dụng trong 1 ngày không? |
|---|---|---|---|
| **Money Lover** | Bắt người dùng nhập tay từng giao dịch rồi tự chọn danh mục. | Phân loại chi tiêu rất chi tiết nhưng trải nghiệm nhập liệu quá cực đoan. | **Không.** Chọn giải pháp đọc tự động giao dịch, chỉ hỏi lại user khi AI không chắc. |
| **Timo (Ngân hàng số)** | Tự động gán danh mục cho các giao dịch trong hệ thống. | Tự động phân loại nhanh nhưng thiếu phần giải thích xu hướng tài chính. | **Có.** Áp dụng cơ chế gán nhãn tự động kết hợp với conversational UI để giải thích ngữ cảnh chi tiết. |

---

## 5. Từ Bằng Chứng Đến Thấu Hiểu (Evidence -> Insight)
```text
Bằng chứng nổi bật nhất:
User cảm thấy bực bội khi các giao dịch như chuyển khoản cá nhân bị bỏ trống ("Chưa phân loại")
hoặc các giao dịch Google bị xếp sai nhóm mà không có cách chỉnh sửa nhanh chóng.

Insight:
Người dùng không chỉ gặp vấn đề ở việc nhìn số liệu. Thật ra họ cần cảm giác kiểm soát (control)
và sự chính xác trong báo cáo tài chính thông qua việc dễ dàng chỉnh sửa lại phân loại của AI
khi AI dự đoán sai lệch.

Opportunity:
AI có thể giúp bằng cách tự động gán nhãn nháp kèm mức độ tự tin (confidence level), sau đó
chủ động đưa ra các nút hành động chỉnh sửa nhanh (1-click correction) trên chatbot.
```

---

## 6. Bằng Chứng Làm Thay Đổi Thiết Kế (Evidence-Driven SPEC Changes)
* [ ] Đổi user chính.
* [ ] Đổi pain statement.
* [x] Đổi build slice.
* [x] Đổi Auto/Aug decision.
* [x] Đổi 4 paths.
* [ ] Đổi failure mode.
* [ ] Đổi owner/test plan.

**Ghi rõ các thay đổi quan trọng:**
```text
Trước evidence:
Nhóm định làm một chatbot tài chính hỏi đáp tự do (free-text chat), AI tự động gán danh mục
cho mọi giao dịch một cách im lặng (automation).

Sau evidence:
Nhóm đổi thành mô hình AI Action Layer trên màn hình lịch sử giao dịch. Bổ sung các Suggested Chips
để tránh chatbot báo "Không tìm thấy" và chuyển từ Automation sang Augmentation (AI chỉ gắn nhãn nháp
cảnh báo và hiển thị nút hành động để user xác nhận hoặc sửa lại).

Lý do:
Bằng chứng tự dùng và phỏng vấn người dùng cho thấy user sợ AI tự quyết định sai về tài chính của họ,
đồng thời chatbot tự do rất dễ bị gãy (fail) khi nhận câu hỏi tự nhiên mập mờ.
```
