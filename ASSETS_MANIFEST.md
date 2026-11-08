# DANH MỤC TÀI NGUYÊN HÌNH ẢNH, SƠ ĐỒ TIKZ & BẢNG BIỂU CHO POSTER KHKT

> **Thư mục lưu trữ:** `D:\KHKT\poster\assets\`  
> **Quy định bắt buộc (Thông tư 84/2026/TT-BGDĐT & Hướng dẫn chuẩn bị Poster 2026–2027):**
> 1. **Mọi hình ảnh, sơ đồ, biểu đồ, đồ thị và bảng số liệu trên Poster ĐỀU PHẢI CÓ CHÚ THÍCH VÀ NGUỒN RÕ RÀNG ngay bên dưới.**
> 2. **Tuyệt đối KHÔNG đưa lên Poster:** Tên học sinh, lớp, trường, tên giáo viên hướng dẫn, ảnh chụp rõ mặt người, mã QR, hoặc đường dẫn URL bên ngoài.

---

## I. SƠ ĐỒ VECTOR / TIKZ (CÓ MÃ NGUỒN `.tex`, BẢN VECTOR `.pdf` / `.svg` VÀ ẢNH `.png` 600 DPI)

### 1. Sơ đồ 1: Kiến trúc luồng xử lý dữ liệu và vòng lặp điều khiển khép kín 1 Hz
* **Tệp nguồn chỉnh sửa:** `01_tikz_architecture_closed_loop.tex`
* **Tệp Vector (Illustrator / CorelDRAW / Inkscape / Canva / Figma):** `01_tikz_architecture_closed_loop.pdf`, `01_tikz_architecture_closed_loop.svg`
* **Tệp ảnh độ phân giải cao (600 DPI):** `01_tikz_architecture_closed_loop.png`
* **Vị trí đặt trên Poster:** Cột Giữa (Phần *Thiết kế và Phương pháp nghiên cứu* – mục Kiến trúc tổng thể hệ thống).
* **Chú thích & Nguồn bắt buộc ghi dưới hình:**
  > **Hình 1:** Sơ đồ khối luồng xử lý dữ liệu và vòng lặp điều khiển khép kín của hệ thống (tần số quét $1\text{ Hz}$).  
  > *Nguồn: Sơ đồ được thiết kế bằng công cụ TikZ (LaTeX) và do học sinh tự thực hiện.*

### 2. Sơ đồ 2: Máy trạng thái hữu hạn (FSM) điều khiển lai Dual-Mode & 4 kịch bản thích ứng
* **Tệp nguồn chỉnh sửa:** `02_tikz_fsm_dual_mode.tex`
* **Tệp Vector (Illustrator / CorelDRAW / Inkscape / Canva / Figma):** `02_tikz_fsm_dual_mode.pdf`, `02_tikz_fsm_dual_mode.svg`
* **Tệp ảnh độ phân giải cao (600 DPI):** `02_tikz_fsm_dual_mode.png`
* **Vị trí đặt trên Poster:** Cột Giữa (Phần *Thiết kế và Phương pháp nghiên cứu* – mục Thuật toán điều khiển chuyển pha FSM).
* **Chú thích & Nguồn bắt buộc ghi dưới hình:**
  > **Hình 3:** Sơ đồ máy trạng thái hữu hạn (FSM) điều khiển chu kỳ chuyển pha kết hợp 4 kịch bản thích ứng (TH1 – TH4).  
  > *Nguồn: Sơ đồ được thiết kế bằng công cụ TikZ (LaTeX) và do học sinh tự thực hiện.*

---

## II. HÌNH ẢNH THỰC NGHIỆM & BIỂU ĐỒ ĐỊNH LƯỢNG CHÍNH THỨC (TRONG BÁO CÁO CHÍNH)

### 3. Hình nhận diện thực tế YOLOv12m và giao diện HUD chỉ số áp suất $S_{\text{congestion}}$
* **Tên tệp:** `03_detection_sample_hud.png`
* **Nội dung:** Minh họa trực quan khung hình thực nghiệm 15 phương tiện (10 xe máy $K_1=0,3$; 2 ô tô con $K_2=1,0$; 3 xe tải/buýt $K_3=2,5$), tính toán $S_{\text{xe}} = 12,50$, độ chiếm dụng mặt đường $6,8\% \rightarrow S_{\text{mặt đường}} = 0,68$, tổng áp suất $S_{\text{congestion}} = 13,18$, độ trễ $22,14\text{ ms}$ ($45,2\text{ FPS}$).
* **Vị trí đặt trên Poster:** Cột Giữa (Liên kết trực tiếp giữa *Mô hình nhận thức thị giác YOLOv12m* và *Công thức toán học $S_{\text{congestion}}$*).
* **Chú thích & Nguồn bắt buộc ghi dưới hình:**
  > **Hình 2:** Giao diện quan sát nhận thức thời gian thực của mô hình YOLOv12m: phân loại 7 nhóm phương tiện, đo lường độ che phủ mặt đường và hiển thị các thành phần của chỉ số áp suất $S_{\text{congestion}}$.  
  > *Nguồn: Hình ảnh được trích xuất từ chương trình thực nghiệm trên tệp Yolov12m.ipynb (thư viện Ultralytics, OpenCV) và do học sinh tự thực hiện.*

### 4. Biểu đồ đối chứng định lượng trước và sau khi tinh chỉnh (Fine-tune) YOLOv12m
* **Tên tệp:** `04_chart_before_vs_after_finetune.png`
* **Nội dung:** Đối chứng 4 chỉ số trên tập kiểm định 120 ảnh ngã tư mật độ cao (1.971 đối tượng): Precision tăng từ $39,84\%$ lên $80,19\%$ ($+40,35\%$), Recall tăng từ $48,75\%$ lên $80,37\%$ ($+31,62\%$), $mAP@0.50$ tăng từ $34,12\%$ lên $74,53\%$ ($+40,41\%$), $mAP@0.50:0.95$ tăng từ $18,48\%$ lên $47,15\%$ ($+28,67\%$).
* **Vị trí đặt trên Poster:** Cột Giữa (Phần *Thực hiện và Kết quả kiểm chứng tầng thị giác AI*).
* **Chú thích & Nguồn bắt buộc ghi dưới hình:**
  > **Hình 4:** Biểu đồ so sánh định lượng các chỉ số đánh giá của mô hình YOLOv12m trước và sau khi tinh chỉnh trên tập dữ liệu kiểm định 120 ảnh ngã tư mật độ cao.  
  > *Nguồn: Biểu đồ được tạo bằng thư viện Matplotlib từ tệp Yolov12m.ipynb và do học sinh tự thực hiện.*

### 5. Đồ thị phân rã độ trễ (Latency) và tốc độ khung hình (FPS) trên luồng video liên tục
* **Tên tệp:** `05_chart_video_stream_latency_fps.png`
* **Nội dung:** Đo lường qua 150 khung hình video liên tiếp: Tổng độ trễ toàn phần trung bình $23,41 \pm 1,47\text{ ms}$/khung hình (Suy luận mạng $21,02\text{ ms}$, Tiền xử lý $1,10\text{ ms}$, NMS $1,29\text{ ms}$), tốc độ trung bình $42,9\text{ FPS}$ (vượt ngưỡng chuẩn thời gian thực $30\text{ FPS}$), chỉ chiếm $2,34\%$ chu kỳ điều khiển $1\text{s}$.
* **Vị trí đặt trên Poster:** Cột Giữa hoặc đầu Cột Phải (Phần *Kiểm chứng hiệu năng đáp ứng thời gian thực*).
* **Chú thích & Nguồn bắt buộc ghi dưới hình:**
  > **Hình 5:** Đồ thị phân rã độ trễ từng khâu xử lý và biến thiên tốc độ khung hình của mô hình YOLOv12m trên chuỗi 150 khung hình video giao thông liên tục.  
  > *Nguồn: Biểu đồ được tạo bằng thư viện Matplotlib từ tệp Yolov12m.ipynb và do học sinh tự thực hiện.*

### 6. Giao diện mô phỏng vi mô nút giao và giản đồ pha tín hiệu trên SUMO-GUI
* **Tên tệp:** `06_sumo_simulation_interface.png`
* **Nội dung:** Mô hình nút giao đồng mức 4 nhánh ($300\text{m}$/nhánh, 2 làn/chiều) trên SUMO v1.27.1 kết nối Python 3.12 qua giao thức TraCI, hiển thị dòng phương tiện hỗn hợp và cửa sổ theo dõi giản đồ chuyển pha đèn tín hiệu thời gian thực (Phase Tracker).
* **Vị trí đặt trên Poster:** Cột Giữa – góc dưới bên phải hoặc đầu Cột Phải (Phần *Mô phỏng kiểm chứng vi mô trên SUMO*).
* **Chú thích & Nguồn bắt buộc ghi dưới hình:**
  > **Hình 6:** Giao diện mô phỏng vi mô nút giao trên phần mềm SUMO-GUI: hiển thị dòng phương tiện hỗn hợp và cửa sổ theo dõi giản đồ chuyển pha đèn tín hiệu thời gian thực.  
  > *Nguồn: Ảnh chụp màn hình từ phần mềm mô phỏng SUMO v1.27.1 và do học sinh tự thực hiện.*

---

## III. TÀI NGUYÊN BỔ TRỢ CHuyên SÂU (TÙY CHỌN ĐƯA VÀO CỤM MINH CHỨNG QUÁ TRÌNH)

* `07_confusion_matrix_normalized.png`: Ma trận nhầm lẫn chuẩn hóa 7 lớp phương tiện Việt Nam.  
  *(Nguồn: Biểu đồ được trích xuất từ quá trình đánh giá mô hình trên tệp Yolov12m.ipynb và do học sinh tự thực hiện.)*
* `08_training_curves_20epochs.png`: Đồ thị hội tụ hàm mất mát và các chỉ số mAP qua 20 chu kỳ huấn luyện tinh chỉnh.  
  *(Nguồn: Đồ thị được xuất từ thư viện Ultralytics trên tệp Yolov12m.ipynb và do học sinh tự thực hiện.)*
* `09_BoxPR_curve_after_finetune.png`: Đường cong Precision–Recall của 7 nhóm phương tiện sau tinh chỉnh ($mAP@0.50 = 74,5\%$).  
  *(Nguồn: Đồ thị được xuất từ thư viện Ultralytics trên tệp Yolov12m.ipynb và do học sinh tự thực hiện.)*
* `10_val_batch0_pred_grid.jpg`: Lưới ảnh kết quả nhận diện thực tế trên tập kiểm định mật độ cao.  
  *(Nguồn: Hình ảnh kết quả kiểm thử trích xuất từ tệp Yolov12m.ipynb và do học sinh tự thực hiện.)*

---

## IV. DỮ LIỆU BẢNG BIỂU CHUẨN HÓA ĐỂ THIẾT KẾ TRỰC TIẾP TRÊN POSTER (`tables_data/`)

### Bảng 1: Quy chuẩn 7 nhóm phương tiện nhận diện của mô hình YOLOv12m và hệ số diện tích ($K_i$)
| ID | Lớp nhận diện | Hệ số $K_i$ | Chủng loại phương tiện thực tế | Vai trò giải thuật |
| :---: | :--- | :---: | :--- | :--- |
| 0 | `bicycle` | $K_1 = 0,3$ | Xe đạp, xe thô sơ, xe đạp điện | Tính toán $S_{\text{xe}}$ |
| 1 | `motorcycle` | $K_1 = 0,3$ | Xe máy, xe gắn máy 2 bánh ($70\text{--}85\%$) | Tính toán $S_{\text{xe}}$ |
| 2 | `car` | $K_2 = 1,0$ | Ô tô con, taxi, xe du lịch dưới 9 chỗ | Chuẩn hóa áp suất |
| 3 | `bus` | $K_3 = 2,5$ | Xe buýt công cộng, xe khách liên tỉnh | Tính toán $S_{\text{xe}}$ |
| 4 | `truck` | $K_3 = 2,5$ | Xe tải chở hàng, xe tải trung và nặng | Tính toán $S_{\text{xe}}$ |
| 5 | `container` | $K_3 = 2,5$ | Xe đầu kéo rơ-moóc, xe container lớn | Tính toán $S_{\text{xe}}$ |
| 6 | `emergency` | -- | Xe cứu thương, chữa cháy, công vụ | Bật cờ `has_emer` (TH1) |

> *Nguồn ghi dưới bảng:* **Bảng 1:** Quy chuẩn 7 nhóm phương tiện nhận diện của mô hình YOLOv12m và thông số ánh xạ hệ số diện tích ($K_i$). *Nguồn: Bảng tham số phân loại do học sinh tự thiết lập và tích hợp vào mô hình.*

### Bảng 2: Thông số kỹ thuật đo lường hiệu năng thời gian thực trên chuỗi 150 khung hình video
| Thông số kỹ thuật đo lường trên luồng video (150 khung hình) | Kết quả thực nghiệm |
| :--- | :---: |
| Thời gian tiền xử lý (Pre-process) / Lọc trùng lặp (NMS) | $1,10\text{ ms}$ / $1,29\text{ ms}$ |
| Độ trễ suy luận mạng trung bình (Inference Latency) | $\mathbf{21,02\text{ ms}}$ |
| **Tổng độ trễ xử lý toàn phần (Total Latency)** | $\mathbf{23,41 \pm 1,47\text{ ms/khung hình}}$ |
| **Tốc độ xử lý khung hình trung bình (FPS)** | $\mathbf{42,9\text{ FPS}}$ (Chuẩn yêu cầu $\ge 30\text{ FPS}$) |
| **Tỷ lệ chiếm dụng chu kỳ điều khiển $1\text{s}$ ($1000\text{ ms}$)** | $\mathbf{2,34\%}$ ($< 3\%$ chu kỳ điều khiển) |
| Độ tin cậy nhận diện trung bình (Mean Confidence) | $71,70\%$ |

> *Nguồn ghi dưới bảng:* **Bảng 2:** Thông số kỹ thuật đo lường hiệu năng thời gian thực của mô hình YOLOv12m trên chuỗi 150 khung hình video giao thông liên tục. *Nguồn: Bảng số liệu được trích xuất từ kết quả thực nghiệm trên tệp Yolov12m.ipynb và do học sinh tự thực hiện.*

### Bảng 3: Kết quả thực nghiệm đối chứng giữa Chu kỳ cố định và Hệ thống AI-ITS trên SUMO v1.27.1
| Kịch bản thử nghiệm và chỉ số đo lường | Chu kỳ cố định ($47\text{s}-3\text{s}-50\text{s}$) | Hệ thống AI-ITS (Đề xuất) | Mức cải thiện |
| :--- | :---: | :---: | :---: |
| **TH1: Ưu tiên phương tiện khẩn cấp** — Thời gian xe ưu tiên qua nút (giây) | $42,0\text{ s}$ | $\mathbf{16,0\text{ s}}$ | **Giảm 61,9%** |
| **TH2: Cắt pha xanh sớm khi hết dòng** — Thời gian chờ trung bình (giây/xe) | $13,2\text{ s}$ | $\mathbf{6,6\text{ s}}$ | **Giảm 50,0%** |
| **TH3: Điều tiết pha theo áp lực dòng** — Thời gian chờ trung bình (giây/xe) | $20,8\text{ s}$ | $\mathbf{17,8\text{ s}}$ | **Giảm 14,4%** |
| **TH4: Đồng bộ đón đoàn xe liên nút** — Chiều dài hàng đợi cực đại (mét) | $42,9\text{ m}$ | $\mathbf{38,1\text{ m}}$ | **Giảm 11,2%** |

> *Nguồn ghi dưới bảng:* **Bảng 3:** Kết quả thực nghiệm đối chứng giữa chu kỳ cố định và thuật toán AI-ITS trên phần mềm SUMO v1.27.1 theo 4 kịch bản thích ứng. *Nguồn: Bảng số liệu kết quả mô phỏng trên phần mềm SUMO v1.27.1 và do học sinh tự thực hiện.*
