### BIÊN BẢN TỔNG KẾT & KẾT QUẢ THỐNG NHẤT CUỐI CÙNG
**(MASTER SUMMARY & RESOLUTION REPORT)**

**CẨM NANG HƯỚNG DẪN BÀN GIAO THIẾT KẾ POSTER KHKT CẤP QUỐC GIA**  
*(HANDOVER SPECIFICATION DOCUMENT)*

* **Tên dự án:** Hệ thống Quản lý Giao thông Thông minh Tích hợp Trí tuệ Nhân tạo (AI-ITS)
* **Lĩnh vực KHKT:** Máy tính (Khoa học Máy tính & Hệ thống Phần mềm)
* **Đơn vị ban hành:** Hội đồng Thẩm định & Kiến trúc sư Thiết kế Poster Khoa học Quốc tế
* **Ủy viên Hội đồng:** Giáo sư Josef (Thụy Sĩ), Tiến sĩ Edward (Hoa Kỳ), Kỹ sư Trưởng Klaus (Đức), Giám đốc Nghệ thuật Kenji (Nhật Bản).

---

### PHẦN I: TUYÊN BỐ THỐNG NHẤT CỐT LÕI (CORE STRATEGIC DECISIONS)

Hội đồng Thẩm định 4 Chuyên gia chính thức ký duyệt **4 Quyết định Chiến lược Toàn diện** giải quyết dứt điểm các bất hợp lý về mặt vật lý, thị giác và pháp lý của các bản nháp trước:

1. **Tái quy hoạch Sơ đồ Kiến trúc `01_tikz` & Cấu trúc Cánh Trái:**
   * **Đồng thuận:** Đưa sơ đồ luồng `01_tikz` lên đỉnh **Thân Chính Giữa** (chiều rộng \\(94\text{cm}\\)) và dàn thành **luồng ngang 5 bước khép kín** (tần số quét 1 Hz / \\(\Delta t = 1\text{s}\\)).
   * **Lý do:** Khung rộng \\(94\text{cm}\\) giúp các hộp quy trình đạt kích thước \\(16.5\text{cm}\\), đảm bảo font chữ 18–22pt đọc rõ ở cự ly 2m mà không bị chèn ép.
   * **Trả Cánh Trái (\\(44\text{cm}\\)) về vai trò Nền tảng Kỹ thuật:** Trình bày 3 khối độc lập: (1) Bối cảnh & 3 Bất cập giao thông, (2) 4 Tiêu chí kỹ thuật định lượng (Real-time \\(\ge 30\text{ FPS}\\), Latency \\(<30\text{ms}\\), áp suất \\(S_{congestion}\\)), và (3) 4 Ràng buộc an toàn bắt buộc (\\(G_{min}=10\text{s}\\), \\(T_{wait}=2\text{s}\\) toàn đỏ, \\(T_{red\_max} \le 100\text{s}\\), đồng bộ trục).

2. **Cân đối Stat Callouts Lưới \\(2 \times 2\\) (Font 68pt Extra-Bold):**
   * **Đồng thuận:** Giảm cỡ chữ Callouts từ 96pt xuống **68pt Extra-Bold** (chiều cao in thực tế \\(24\text{mm}\\)) và sắp xếp dạng **lưới \\(2 \times 2\\)** ở đỉnh Cánh Phải.
   * **Lý do:** Tối ưu tải nhận thức (Cognitive Load), vượt qua *5-Second Glance Test* với 4 con số ngôi sao chiếu sáng trọn vẹn 4 khâu đột phá của đề tài: **`-61.9%`** (Xe ưu tiên qua nút), **`-50.0%`** (Thời gian chờ khi lưu lượng thấp), **`+40.41%`** (mAP@0.50 fine-tune YOLOv12m), và **`42.9 FPS`** (Latency \\(23.41\text{ms}\\)).

3. **Bảo toàn Tính liên tục 100% của Hình 1 \\(\rightarrow\\) Hình 6 và Bảng 1 \\(\rightarrow\\) Bảng 3:**
   * **Đồng thuận:** Giữ nguyên đồ thị đôi `05_chart` tại Cánh Phải (thu gọn chiều cao còn \\(18\text{cm}\\) theo phong cách Tufte Dual-Panel), đồng thời tích hợp trực tiếp số liệu `table_video_stream_benchmark` (Bảng 2) ngay bên dưới đồ thị.
   * **Lý do:** Đảm bảo thứ tự hiển thị trên poster trùng khớp 100% với danh mục minh chứng trong cuốn Báo cáo KHKT gửi Giám khảo.

4. **Quy cách Bình trang In bạt cuộn \\(1,2\text{m} \times 2,4\text{m}\\) Khít 100%:**
   * **Đồng thuận:** Sắp xếp 4 tấm vật lý trên cuộn bạt in công nghiệp rộng \\(1,2\text{m}\\) \\(\times\\) dài \\(2,4\text{m}\\) theo thứ tự: **Thân Giữa (1.0m) + Cánh Trái (0.5m) + Cánh Phải (0.5m) + Bảng Tên xoay dọc \\(90^\circ\\) (0.4m)**.
   * **Lý do:** Tổng chiều dài cuộn bạt đúng bằng \\(100\text{cm} + 50\text{cm} + 50\text{cm} + 40\text{cm} = 240\text{cm}\\) (\\(2,4\text{m}\\)), không dư thừa hay tốn chi phí bù hao bạt.

---

### PHẦN II: BẢNG THÔNG SỐ KỸ THUẬT CHUẨN VÀNG (THE MASTER DESIGN SPECS)

#### 1. Kích thước Vật lý 4 Tấm & Tọa độ Bình trang:

```
========================================================================================================
                          SƠ ĐỒ BÌNH TRANG IN BẠT CUỘN (1.2m x 2.4m)
========================================================================================================
0.0m                                 1.0m               1.5m               2.0m               2.4m
+------------------------------------+------------------+------------------+------------------+
|                                    |                  |                  |                  |
|                                    |                  |                  | BẢNG TÊN HEADER  |
|          THÂN CHÍNH GIỮA           |    CÁNH TRÁI     |    CÁNH PHẢI     |  (XOAY DỌC 90°)  |
|           (1.0m x 1.2m)            |  (0.5m x 1.2m)   |  (0.5m x 1.2m)   |  (0.4m x 1.2m)   |
|                                    |                  |                  |                  |
|                                    |                  |                  |                  |
+------------------------------------+------------------+------------------+------------------+
|<------------- 100cm -------------->|<------ 50cm ---->|<------ 50cm ---->|<------ 40cm ---->|
|<--------------------------------- CHIỀU DÀI CUỘN 240cm (2.4m) ----------------------------->|
========================================================================================================
```

* **Tấm 1 (Bảng tên Header Panel):** Rộng \\(120\text{cm}\\) \\(\times\\) Cao \\(40\text{cm}\\). Lề ngoài (Margin): Trên/Dưới \\(40\text{mm}\\), Trái/Phải \\(50\text{mm}\\).
* **Tấm 2 (Cánh Trái):** Rộng \\(50\text{cm}\\) \\(\times\\) Cao \\(120\text{cm}\\). Lề ngoài: Trái \\(40\text{mm}\\), Phải \\(20\text{mm}\\). Cột nội dung rộng \\(440\text{mm}\\).
* **Tấm 3 (Thân Chính Giữa):** Rộng \\(100\text{cm}\\) \\(\times\\) Cao \\(120\text{cm}\\). Lề ngoài: Trái/Phải \\(30\text{mm}\\). 2 Cột con (\\(450\text{mm}\\) mỗi cột) + Rãnh Gutter \\(40\text{mm}\\).
* **Tấm 4 (Cánh Phải):** Rộng \\(50\text{cm}\\) \\(\times\\) Cao \\(120\text{cm}\\). Lề ngoài: Trái \\(20\text{mm}\\), Phải \\(40\text{mm}\\). Cột nội dung rộng \\(440\text{mm}\\).

#### 2. Bảng mã màu Semantic Palette (Quy tắc 60–30–10):

| Nhóm Màu | Tên Gọi Học Thuật | Mã Hex | Thông số CMYK | Vai trò & Ứng dụng |
| :--- | :--- | :--- | :--- | :--- |
| **60% Dominant** | Trắng Tuyết Học thuật | `#FAFAFC` | `2 - 2 - 0 - 0` | Nền chính poster, WCAG AAA, chống lóa ánh đèn hội trường. |
| **30% Structure**| Xám Băng Card | `#F0F4F8` | `6 - 3 - 2 - 0` | Khối Card chứa nội dung, phân vùng không cần viền đậm. |
| **Text / Borders**| Slate Dark / Medium | `#1E293B` / `#334155` | `80-70-50-50` | Văn bản nội dung, tiêu đề khối và đường viền khung. |
| **10% Accent 1** | Cyan Blue | `#0284C7` | `85 - 35 - 0 - 0` | Accent Tầng Nhận thức AI YOLOv12m & Mô hình hóa. |
| **10% Accent 2** | Emerald Green | `#059669` | `85 - 10 - 70 - 10` | Accent Tầng Điều khiển FSM, Pha Xanh & Tín hiệu SUMO. |
| **10% Accent 3** | Amber Gold | `#D97706` | `10 - 55 - 100 - 0` | Highlight Chỉ số Ngôi sao Callouts & Cảnh báo An toàn. |

#### 3. Thang đo Typography Chuẩn Quốc tế (7 Cấp độ):

| Cấp độ Typography | Cỡ chữ (pt) | Chiều cao in thực tế | Độ đậm (Weight) | Distance Readability | Font Family khuyên dùng |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **1. Tên đề tài** | `84 pt` | \\(29.6\text{mm}\\) | Bold (700) | Cự ly 5m | Montserrat Bold |
| **2. Mã số đề tài** | `44 pt` | \\(15.5\text{mm}\\) | Semi-Bold (600) | Cự ly 5m | Montserrat Semi-Bold |
| **3. Tiêu đề mục (H1)** | `38 pt` | \\(13.4\text{mm}\\) | Bold (700) | Cự ly 2m | Montserrat Bold |
| **4. Tiêu đề phụ (H2)** | `26 pt` | \\(9.2\text{mm}\\) | Semi-Bold (600) | Cự ly 2m | Montserrat Semi-Bold |
| **5. Nội dung (Body Text)**| `22 pt` | \\(7.8\text{mm}\\) | Regular (400) | Cự ly 1m | Inter / Arial Regular |
| **6. Stat Callout Khổng lồ**| `68 pt` | \\(24.0\text{mm}\\) | Extra-Bold (800) | Cự ly 5m | Montserrat Extra-Bold |
| **7. Caption, Nguồn & AI** | `14 pt` | \\(4.9\text{mm}\\) | Italic / Medium | Cự ly 1m | Inter / Arial Italic |

---

### PHẦN III: DANH MỤC TÀI NGUYÊN SẴN SÀNG THỰC THI (READY-TO-USE ASSETS MANIFEST)

Bảng phán quyết vị trí cố định và chuẩn hóa kỹ thuật cho 13 tài nguyên gốc cùng các tệp đồ họa Vector xuất bản:

| Tên Asset / Tệp gốc | Loại định dạng | Vị trí đặt cố định trên Poster | Trạng thái kỹ thuật & Phán quyết |
| :--- | :--- | :--- | :--- |
| **01_tikz_architecture_closed_loop** | LaTeX TikZ Vector (`.pdf`) | **Tấm 3 (Thân Giữa)** - Block M-1 (Đỉnh) | **GIỮ LẠI (Hình 1)** - Dàn ngang 5 bước khép kín tần số 1 Hz. |
| **03_detection_sample_hud.png** | Image HUD (Cropped) | **Tấm 3 (Thân Giữa)** - Block M-2 (Trái) | **GIỮ LẠI (Hình 2)** - Trích xuất HUD YOLOv12m + Badges \\(K_i\\). |
| **02_tikz_fsm_dual_mode** | LaTeX TikZ Vector (`.pdf`) | **Tấm 3 (Thân Giữa)** - Block M-3 | **GIỮ LẠI (Hình 3)** - Sơ đồ FSM Dual-Mode 4 kịch bản TH1–TH4. |
| **04_chart_before_vs_after_finetune** | Vector PDF/SVG (Python) | **Tấm 3 (Thân Giữa)** - Block M-4 | **GIỮ LẠI (Hình 4)** - Biểu đồ đối chứng mAP (+40.41%) Tufte. |
| **05_chart_video_stream_latency_fps**| Vector PDF/SVG (Python) | **Tấm 4 (Cánh Phải)** - Block R-2 | **GIỮ LẠI (Hình 5)** - Biểu đồ độ trễ 18cm & tích hợp Bảng 2. |
| **06_sumo_simulation_interface.png** | Image GUI (Cropped) | **Tấm 4 (Cánh Phải)** - Block R-3 (Góc) | **GIỮ LẠI (Hình 6)** - Ảnh mô phỏng giao lộ J1 trên SUMO-GUI. |
| **table_01_vehicle_classes_Ki** | Vector Text Badges | **Tấm 3 (Thân Giữa)** - Block M-2 | **HỢP NHẤT (Bảng 1)** - Dải Badges \\(K_1=0.3, K_2=1.0, K_3=2.5\\). |
| **table_video_stream_benchmark** | Vector Text Table | **Tấm 4 (Cánh Phải)** - Block R-2 | **HỢP NHẤT (Bảng 2)** - Bảng đo phân rã độ trễ 23.41ms / 42.9 FPS. |
| **table_03_sumo_benchmark_comparison**| Vector Text Table | **Tấm 4 (Cánh Phải)** - Block R-3 | **GIỮ LẠI (Bảng 3)** - Bảng đối chứng SUMO chuẩn Tufte 3 dòng kẻ. |
| **07_confusion_matrix_normalized.png**| Bitmap Image | **Sổ tay Nghiên cứu Kỹ thuật** | **TRỤC XUẤT** - Chuyển xuống tài liệu đặt tại bàn demo. |
| **08_training_curves_20epochs.png** | Bitmap Image | **Sổ tay Nghiên cứu Kỹ thuật** | **TRỤC XUẤT** - Chuyển xuống tài liệu đặt tại bàn demo. |
| **09_BoxPR_curve_after_finetune.png** | Bitmap Image | **Sổ tay Nghiên cứu Kỹ thuật** | **TRỤC XUẤT** - Chuyển xuống tài liệu đặt tại bàn demo. |
| **10_val_batch0_pred_grid.jpg** | Bitmap Image | **Laptop Demo / Phụ lục** | **TRỤC XUẤT** - Chuyển sang trình chiếu trên máy tính demo. |

---

### PHẦN IV: CAM KẾT PHÁP LÝ & LIÊM CHÍNH KHKT (LEGAL & COMPLIANCE STATEMENT)

Poster tuân thủ 100% quy định của **Thông tư 84/2026/TT-BGDĐT** và Quy chế Cuộc thi KHKT Quốc gia:

1. **Vô danh hóa 100% (Anonymization):** 
   * Tuyệt đối không xuất hiện tên thí sinh, tên giáo viên hướng dẫn, tên trường, tên lớp hoặc logo đơn vị trên cả 4 tấm poster.

2. **Tuân thủ Tuyệt đối Cấm đoán Mã QR & Đường dẫn Web:**
   * Loại bỏ 100% mã QR Code và đường dẫn URL (bác bỏ tính năng QR của BetterPoster gốc) để tránh nguy cơ vi phạm quy chế bảo mật thông tin trực tuyến.

3. **Quy chuẩn Micro-Captioning Tích hợp:**
   * Tất cả 6 Hình và 3 Bảng đều có câu chú thích (Caption) và Nguồn gốc in ngay bên dưới (Font Inter/Arial Italic `14 pt`, màu Slate Light `#64748B`, ép chân hình đúng `3 mm`).
   * Cú pháp chuẩn: `Hình X: [Tên chú thích ngắn gọn] | Nguồn: [Mô tả nguồn gốc do học sinh tự thực hiện].`

4. **Khối Khai báo Sử dụng AI (Điều 15 TT 84/2026/TT-BGDĐT):**
   * Đặt cố định tại chân Cánh Phải (Kích thước \\(44\text{cm} \times 14\text{cm}\\)), đóng khung Legal Card mỏng 5% xám nhạt (`#F4F6F8`), trình bày 4 gạch đầu dòng minh bạch:
     1. **Mô hình AI & Huấn luyện:** Dự án sử dụng mạng YOLOv12m Area Attention trên Google Colab (Ultralytics, PyTorch, OpenCV). Học sinh tái cấu trúc tầng phân loại từ 80 lớp sang 7 nhóm phương tiện Việt Nam và fine-tune 20 epochs trên tệp `Yolov12m.ipynb`.
     2. **Phần mềm Mô phỏng:** Dùng SUMO v1.27.1 và giao thức TraCI Python 3.12 để mô hình hóa ngã tư (`map.net.xml`) và chạy 4 kịch bản đối chứng gốc (`th1.rou.xml` – `th4.rou.xml`).
     3. **Công cụ Trợ lý AI Kỹ thuật:** Trợ lý AI hỗ trợ rà soát cú pháp Python TraCI, gỡ lỗi kết nối FSM khép kín, và định dạng mã nguồn vẽ biểu đồ Matplotlib / LaTeX.
     4. **Cam kết Nguyên gốc:** 100% ý tưởng thực tiễn, thuật toán FSM Dual-Mode, công thức áp suất \\(S_{congestion}\\), hệ số \\(K_i\\) và dữ liệu đo đạc thực nghiệm gốc do học sinh tự thực hiện, không giả mạo dữ liệu.

---

### BÀN GIAO & NẠP DỮ LIỆU VÀO PHẦN MỀM ĐỒ HỌA
Bản Biên bản này đóng vai trò là **Cẩm nang Hướng dẫn Bàn giao (Handover Specification Document)** chính thức. Tác giả hoặc Kỹ sư đồ họa có thể sử dụng trực tiếp các thông số kỹ thuật, quy hoạch tọa độ, bảng mã màu và các tệp đồ họa Vector đã được xuất bản (`04_chart_before_vs_after_finetune.pdf` và `05_chart_video_stream_latency_fps.pdf` có sẵn trong Studio Panel) để thao tác dán thẳng vào Figma / Adobe Illustrator / LaTeX mà không cần tranh cãi hay hiệu chỉnh lại từ đầu.

*Biên bản được ký duyệt đồng thuận bởi 4 Ủy viên Hội đồng Thẩm định.*