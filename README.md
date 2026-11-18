# [Bài thực hành 7] Xây dựng kế hoạch tổ chức sự kiện công nghệ AI Innovation Day

## 1. Bộ Prompt hoàn chỉnh (Kết hợp 3 kỹ thuật)

Hệ thống được thiết kế kết hợp đồng thời **Chain-of-Thought** (suy luận từng bước), **Prompt Chaining** (chuỗi prompt nối tiếp đầu ra – đầu vào) và **Context Management** (quản lý & đóng gói ngữ cảnh khi chuyển hội thoại).

### Giai đoạn 1: Phân tích tính khả thi (Chain-of-Thought + Prompt Chaining)
> **Prompt 1:**
> "Đóng vai Trưởng ban Tổ chức sự kiện công nghệ sinh viên. Sự kiện **'AI Innovation Day'** có các thông số cố định: quy mô **150 sinh viên**, thời gian **1 ngày**, ngân sách tối đa **15.000.000 VNĐ**, nhân sự **10 người**, mục tiêu giúp sinh viên hiểu và trải nghiệm ứng dụng AI trong học tập và công việc.
> Hãy suy nghĩ từng bước (Chain-of-Thought) để phân tích tính khả thi:
> 1. Đánh giá sự tương quan giữa quy mô 150 người và 10 nhân sự vận hành.
> 2. Tính toán mức chi bình quân đầu người dựa trên trần ngân sách 15 triệu đồng.
> 3. Xác định 3 rủi ro lớn nhất về vận hành/tài chính và đề xuất giải pháp phòng ngừa."

### Giai đoạn 2: Xây dựng Lịch trình, Dự toán & Nhân sự (Prompt Chaining)
> **Prompt 2:**
> "Dựa trên kết quả phân tích khả thi và các giải pháp phòng ngừa rủi ro ở [Output 1], hãy xây dựng kế hoạch vận hành chi tiết gồm 3 phần liên kết chặt chẽ với nhau:
> 1. **Lịch trình sự kiện 1 ngày** (từ 07:30 đến 17:00) chia rõ khung giờ, hoạt động và địa điểm giả định (hội trường trường).
> 2. **Bảng dự toán ngân sách** khớp với các hoạt động trong lịch trình, tổng chi phí bắt buộc **<= 15.000.000 VNĐ** (có quỹ dự phòng).
> 3. **Bảng phân công nhiệm vụ cho đủ 10 nhân sự** bao phủ toàn bộ các đầu việc trong lịch trình và quản lý các hạng mục ngân sách."

### Giai đoạn 3: Đóng gói ngữ cảnh & Chuyển hội thoại (Context Management)
> **Prompt 3 (Tạo bản tóm tắt ngữ cảnh):**
> "Hãy tổng hợp toàn bộ thông số cốt lõi, lịch trình khung, tổng ngân sách đã chốt và cơ cấu 10 nhân sự từ [Output 1] và [Output 2] thành một **Bản tóm tắt ngữ cảnh (Context Summary)** ngắn gọn dưới 250 từ để tôi chuyển sang phiên làm việc mới mà không làm sai lệch dữ liệu."

> **Prompt 4 (Tại phiên hội thoại mới – Lập kế hoạch truyền thông):**
> "Dưới đây là ngữ cảnh dự án đã được phê duyệt: `[Dán Context Summary từ Output 3]`.
> Dựa trên ngữ cảnh này, hãy lập **Kế hoạch truyền thông trước sự kiện (14 ngày)** nhằm thu hút đủ 150 sinh viên đăng ký tham gia, đảm bảo chi phí truyền thông nằm đúng trong khoản mục ngân sách đã duyệt."

### Giai đoạn 4: Kiểm tra chéo & Hiệu chỉnh (Chain-of-Thought + Prompt Chaining)
> **Prompt 5:**
> "Đóng vai Kiểm toán viên & Điều phối viên sự kiện. Hãy đối chiếu toàn bộ kế hoạch gồm: Phân tích khả thi, Lịch trình, Dự toán ngân sách, Phân công 10 nhân sự và Kế hoạch truyền thông với các ràng buộc gốc (150 SV, 1 ngày, <= 15 triệu đồng, 10 nhân sự). Phân tích từng bước các mâu thuẫn tiềm ẩn giữa các hạng mục và đưa ra phương án hiệu chỉnh."

---

## 2. Bản phân tích tính khả thi (Output 1)

* **Bước 1 – Đánh giá tương quan nhân sự & quy mô (10 nhân sự / 150 sinh viên):**
  * Tỷ lệ phục vụ là **1 nhân sự hỗ trợ 15 sinh viên**. Đây là tỷ lệ khả thi nếu tổ chức tập trung tại 1 hội trường lớn của trường và ứng dụng công nghệ (check-in bằng QR Code, tài liệu số hóa) để giảm tải khâu thủ công.
* **Bước 2 – Phân tích bài toán ngân sách (15.000.000 VNĐ / 150 sinh viên):**
  * Mức chi trung bình tối đa là **100.000 VNĐ/sinh viên** cho cả ngày.
  * *Kết luận khả thi:* Hoàn toàn khả thi nếu tận dụng cơ sở vật chất sẵn có của nhà trường (miễn phí thuê hội trường, âm thanh, máy chiếu) và mời diễn giả là giảng viên/cựu sinh viên hoặc đối tác công nghệ hỗ trợ theo hình thức tài trợ chuyên môn. Ngân sách sẽ tập trung vào tea-break, in ấn, quà tặng minigame và truyền thông.
* **Bước 3 – Đánh giá rủi ro & Giải pháp:**
  1. *Rủi ro quá tải check-in và đường truyền mạng khi 150 người cùng thực hành AI:* Giải pháp là chia 2 luồng check-in QR Code và chuẩn bị sẵn 2 bộ phát Wi-Fi 4G dự phòng.
  2. *Rủi ro phát sinh chi phí ăn uống/in ấn vượt trần 15 triệu:* Giải pháp là chốt danh sách tham dự trước 48 giờ và trích lập quỹ dự phòng 10% (1.500.000 VNĐ).
  3. *Rủi ro sinh viên bỏ về giữa chừng buổi chiều:* Giải pháp là thiết kế workshop thực hành buổi chiều có phần thi thực chiến và trao thưởng cuối giờ.

---

## 3. Lịch trình sự kiện theo khung giờ (Output 2.1)

* **Địa điểm:** Hội trường A (Sức chứa 200 chỗ – Mượn miễn phí từ Nhà trường).
* **Thời gian:** 1 ngày (07:30 – 17:00).

| Khung giờ | Thời lượng | Nội dung hoạt động | Chi tiết triển khai |
| :--- | :---: | :--- | :--- |
| **07:30 – 08:15** | 45 phút | Đón khách & Check-in | Quét mã QR điểm danh, phát thẻ tên + tờ rơi hướng dẫn truy cập công cụ AI. |
| **08:15 – 08:45** | 30 phút | Khai mạc sự kiện | Tuyên bố lý do, giới thiệu Ban tổ chức, diễn giả và thể lệ thử thách trong ngày. |
| **08:45 – 10:15** | 90 phút | **Phiên 1 (Talkshow):** Toàn cảnh AI & Ứng dụng trong học tập | Diễn giả chia sẻ cách dùng AI nghiên cứu tài liệu, tóm tắt bài giảng, học ngoại ngữ hiệu quả. |
| **10:15 – 10:35** | 20 phút | Tea-break & Giao lưu | Phục vụ bánh ngọt, nước uống; sinh viên tham quan góc trải nghiệm demo công cụ AI. |
| **10:35 – 11:45** | 70 phút | **Phiên 2 (Panel):** AI trong công việc & Kỹ năng tương lai | Tọa đàm hỏi đáp (Q&A) giữa diễn giả và sinh viên về cơ hội nghề nghiệp thời đại AI. |
| **11:45 – 13:30** | 105 phút | Nghỉ trưa tự túc | Sinh viên tự túc ăn trưa (BTC chuẩn bị sẵn 12 suất ăn trưa cho BTC & Diễn giả). |
| **13:30 – 15:30** | 120 phút | **Phiên 3 (Workshop Thực hành):** Thực chiến giải quyết bài toán bằng AI | Chia nhóm thực hành viết Prompt, tạo slide thuyết trình, xử lý dữ liệu và tạo sản phẩm mẫu. |
| **15:30 – 16:30** | 60 phút | Mini-Contest: Trình bày sản phẩm nhanh | Top 5 nhóm xuất sắc nhất thuyết trình sản phẩm (5 phút/nhóm) trước Ban giám khảo. |
| **16:30 – 17:00** | 30 phút | Trao giải, Tổng kết & Bế mạc | Công bố giải thưởng, chụp ảnh lưu niệm, gửi form khảo sát nhận E-Certificate. |

---

## 4. Bảng dự toán ngân sách (Output 2.2)

| STT | Hạng mục chi phí | Diễn giải chi tiết | Số lượng | Đơn giá (VNĐ) | Thành tiền (VNĐ) |
| :---: | :--- | :--- | :---: | :---: | :---: |
| 1 | **Truyền thông & In ấn** | In standee (2 chiếc), backdrop chính, thẻ đeo BTC & phiếu tham dự | 1 gói | 2.200.000 | 2.200.000 |
| 2 | **Chạy quảng cáo truyền thông** | Hỗ trợ đẩy bài đăng trên Fanpage CLB để thu hút đủ 150 SV | 1 gói | 800.000 | 800.000 |
| 3 | **Tea-break buổi sáng** | Bánh ngọt, trái cây, nước suối cho 150 SV + khách mời | 160 suất | 25.000 | 4.000.000 |
| 4 | **Ăn trưa nội bộ** | Cơm trưa cho 10 nhân sự BTC và 2 diễn giả/khách mời | 12 suất | 50.000 | 600.000 |
| 5 | **Quà tặng & Cảm ơn diễn giả** | Kỷ niệm chương / Quà tặng tri ân 2 diễn giả chuyên môn | 2 suất | 1.000.000 | 2.000.000 |
| 6 | **Giải thưởng Mini-Contest** | 1 Giải Nhất (1.2tr), 1 Giải Nhì (800k), 1 Giải Ba (500k) + Quà minigame | 1 gói | 3.000.000 | 3.000.000 |
| 7 | **Vật tư kỹ thuật & Văn phòng phẩm** | Thuê 2 cục phát Wi-Fi 4G tốc độ cao, dây cáp, bút, giấy note | 1 gói | 900.000 | 900.000 |
| 8 | **Quỹ dự phòng phát sinh** | Dự phòng 10% cho các chi phí đột xuất trong ngày tổ chức | 1 gói | 1.500.000 | 1.500.000 |
| | **TỔNG CỘNG** | **Đảm bảo không vượt trần 15.000.000 VNĐ** | | | **15.000.000** |

---

## 5. Bảng phân công 10 nhân sự (Output 2.3)

| STT | Vị trí / Vai trò | Số lượng | Nhiệm vụ cụ thể trước & trong sự kiện |
| :---: | :--- | :---: | :--- |
| 1 | **Trưởng ban Tổ chức (Project Leader)** | 1 | Điều phối chung toàn bộ tiến độ, làm việc với nhà trường mượn hội trường và xử lý sự cố khẩn cấp. |
| 2 | **Điều phối viên Chương trình & MC** | 1 | Quản lý kịch bản timeline từng khung giờ, dẫn dắt chương trình, kết nối diễn giả và sinh viên. |
| 3 | **Phụ trách Đối ngoại & Diễn giả** | 1 | Mời diễn giả, thu thập slide bài giảng trước sự kiện, đón tiếp và chuẩn bị quà tri ân diễn giả. |
| 4 | **Trưởng nhóm Truyền thông & Thiết kế** | 2 | Lên kế hoạch truyền thông 14 ngày, thiết kế ấn phẩm (poster, backdrop, thẻ đeo), quản lý form đăng ký. |
| 5 | **Phụ trách Kỹ thuật & Hạ tầng mạng** | 2 | Vận hành âm thanh, máy chiếu, thiết lập 2 bộ phát Wi-Fi 4G dự phòng, hỗ trợ kỹ thuật lúc thực hành AI. |
| 6 | **Phụ trách Hậu cần & Tài chính** | 2 | Quản lý thu chi đúng 15 triệu đồng, đặt in ấn, chuẩn bị tea-break, cơm trưa và vật tư văn phòng phẩm. |
| 7 | **Phụ trách Check-in & Hỗ trợ khán giả** | 1 | Quản lý bàn check-in QR Code đầu giờ, điều phối chỗ ngồi hội trường và hỗ trợ chia nhóm workshop. |
| | **TỔNG NHÂN SỰ** | **10** | **Phủ kín 100% các đầu việc vận hành sự kiện** |

---

## 6. Bản tóm tắt ngữ cảnh dự án (Output 3 – Context Management)

> **[CONTEXT SUMMARY – DỰ ÁN AI INNOVATION DAY]**
> * **Thông số cố định:** Quy mô 150 sinh viên; Thời gian 1 ngày (07:30–17:00 tại Hội trường trường miễn phí); Ngân sách trần 15.000.000 VNĐ; Nhân sự 10 người.
> * **Cấu trúc chương trình:** Sáng gồm 2 phiên Talkshow & Panel về ứng dụng AI trong học tập và nghề nghiệp (có Tea-break); Chiều gồm Workshop thực hành viết Prompt/tạo sản phẩm AI và thi Mini-Contest trao thưởng.
> * **Phân bổ ngân sách trọng tâm:** Truyền thông & In ấn (3.000.000 VNĐ, trong đó 800.000 VNĐ chạy quảng cáo), Tea-break & Ăn trưa nội bộ (4.600.000 VNĐ), Quà diễn giả & Giải thưởng (5.000.000 VNĐ), Kỹ thuật (900.000 VNĐ), Dự phòng (1.500.000 VNĐ).
> * **Nhân sự phụ trách truyền thông:** 2 thành viên thuộc nhóm Truyền thông & Thiết kế chịu trách nhiệm thu hút đủ 150 lượt đăng ký tham gia.

---

## 7. Kế hoạch truyền thông trước sự kiện (Output 4)

* **Thời gian triển khai:** 14 ngày trước sự kiện.
* **Ngân sách sử dụng:** 800.000 VNĐ (chạy quảng cáo bài viết chính) + tận dụng kênh miễn phí của CLB và Đoàn/Hội trường.
* **Mục tiêu:** Đạt 180–200 đơn đăng ký trực tuyến (dự phòng tỷ lệ vắng mặt 15–20% để đảm bảo thực tế có mặt 150 sinh viên).

| Giai đoạn | Thời gian | Hoạt động truyền thông chính | Kênh triển khai | KPI mục tiêu |
| :--- | :--- | :--- | :--- | :--- |
