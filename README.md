# 📄 Kỹ Năng Xử Lý Văn Phòng (Office Automation Skill)

> **Kiến trúc 2 Chiều (Bi-directional Architecture)** – Tự động hóa tạo lập, chỉnh sửa và chuyển đổi tài liệu văn phòng (Word, Excel, PowerPoint, PDF) chuẩn hóa theo Brand Kit hoặc Nghị định 30.

---

> ⚠️ **LƯU Ý QUAN TRỌNG**  
> Kỹ năng AI hỗ trợ thiết kế và tái tạo tài liệu theo **Brand Kit**, tuy nhiên người dùng **cần kiểm tra tính chính xác của các số liệu kinh doanh** trước khi phát hành chính thức.

---

## 📌 Tổng Quan

**Kỹ năng Xử lý Văn phòng** áp dụng **Kiến trúc 2 Chiều (Bi-directional Architecture)** giúp AI xử lý toàn diện mọi thao tác văn phòng. 

Điểm khác biệt cốt lõi so với các công cụ thông thường là khả năng **bóc tách nhận diện thương hiệu (Brand Kit)** từ file mẫu có sẵn, từ đó "tái sinh" các văn bản, slide, báo cáo mới đạt chuẩn mực thẩm mỹ và quy chuẩn doanh nghiệp/hành chính.

```
       ┌───────────────────────────────┐
       │   FILE MẪU (Template/Draft)   │
       └──────────────┬────────────────┘
                      │
           [Chiều Đọc - Extraction]
                      │
                      ▼
 ┌──────────────────────────────────────────┐
 │ • Trích xuất Brand Kit (Color, Font, Logo)│
 │ • Phân tích Cấu trúc & Thể thức           │
 └────────────────────┬─────────────────────┘
                      │
           [Chiều Ghi - Generation]
                      │
                      ▼
       ┌───────────────────────────────┐
       │   TÀI LIỆU HOÀN THIỆN MỚI     │
       │   (Word / Excel / PPT / PDF)  │
       └───────────────────────────────┘
```

---

## 💡 Vì Sao Kỹ Năng Này Ra Đời?

Khi tạo lập tài liệu văn phòng qua AI, người dùng thường gặp phải **3 vấn đề lớn**:

| STT | Thách thức phổ biến | Giải pháp từ Kỹ năng 2.0 |
| :---: | :--- | :--- |
| **1** | **Mất bản sắc thương hiệu:** AI thường sinh văn bản thô hoặc dùng mẫu mặc định đơn điệu, lệch màu/font công ty. | **Tự động áp dụng Brand Kit:** Trích xuất bảng màu, font chữ, vị trí logo chuẩn xác từ tài liệu mẫu. |
| **2** | **Thiếu khả năng kế thừa:** Không đọc được file mẫu để tái sử dụng quy chuẩn thẩm mỹ cho tài liệu mới. | **Kiến trúc 2 chiều:** Đọc – Trích xuất – Tái tạo đồng bộ trên tài liệu mới. |
| **3** | **Không đáp ứng chuẩn hành chính:** Khó căn lề, chỉnh giãn dòng, trình trình bày thể thức văn bản nhà nước. | **Đạt chuẩn Nghị định 30:** Tự động áp dụng quy chuẩn hành chính Việt Nam nghiêm ngặt. |

---

## ✨ NHỮNG ĐIỂM MẤU CHỐT TRONG BỘ SKILL

* 🔄 **Kiến trúc 2 Chiều (Bi-directional):** Đọc trích xuất Brand Kit từ file mẫu và ghi tái tạo văn bản tự động.
* 🏛️ **Hỗ trợ song song 2 chuẩn xuất bản:** 
  * *Chuẩn Doanh nghiệp Hiện đại:* Linh hoạt, thẩm mỹ cao theo Brand Kit.
  * *Chuẩn Hành chính Nhà nước:* Chuẩn thể thức theo **Nghị định 30/2020/NĐ-CP**.
* 🖥️ **Tối ưu định dạng đa nền tảng:** Kết xuất đồng bộ cho Word (`.docx`), Excel (`.xlsx`), PowerPoint (`.pptx`) và xuất file PDF chất lượng cao.

---

## 🚀 Ví Dụ Thực Chiến

### **Tình huống**
Người dùng cung cấp một **file slide mẫu của công ty** (`mau_slide.pptx`) và một **bản ghi chú nội dung cuộc họp** (`dan_y.md`), yêu cầu tạo bộ slide thuyết trình tổng kết quý gồm 6 trang.

### **Kịch bản xử lý của Agent**

1. **Bước 1: Bóc tách (Chiều Đọc)**
   * Agent phân tích file mẫu để trích xuất bảng màu chủ đạo (*Primary, Secondary, Accent*), font chữ tiêu đề và vị trí đặt logo thương hiệu.
2. **Bước 2: Quy hoạch Cấu trúc Slide**
   * Agent xây dựng dàn ý chi tiết 6 trang slide theo mô hình trực quan, phân bổ nội dung và biểu tượng minh họa phù hợp.
3. **Bước 3: Thực thi (Chiều Ghi)**
   * Agent chạy pipeline lập trình sinh file PowerPoint hoàn chỉnh mang đúng thông số Brand Kit đã trích xuất từ Bước 1.

---

## ⚙️ Hướng Dẫn Cài Đặt & Sử Dụng

### 1. Cài đặt kỹ năng

1. Tải về và giải nén file `.zip`.
2. Sao chép thư mục `xu-ly-van-phong` vào thư mục `skills` của hệ thống:
   ```bash
   cp -r xu-ly-van-phong ~/.gemini/config/skills/
   ```
3. Khởi động lại phiên làm việc để hệ thống ghi nhận kỹ năng mới.

---

### 2. Công thức câu lệnh kích hoạt

```bash
/xu-ly-van-phong [File mẫu hoặc bản nháp] [Yêu cầu định dạng và phong cách]
```

---

### 3. Mẫu Prompt thực tế

#### 🎯 Mẫu 1: Thiết kế slide theo mẫu nhận diện thương hiệu
> `/xu-ly-van-phong từ file mau_slide.pptx và dan_y.md. Hãy bóc tách Brand Kit từ file mẫu để tạo bộ slide 6 trang giới thiệu dịch vụ mới.`

#### 🏛️ Mẫu 2: Soạn thảo văn bản theo chuẩn Nghị định 30
> `/xu-ly-van-phong từ nội dung thông báo.txt. Hãy tạo file Word công văn hành chính chuẩn Nghị định 30 với font Times New Roman và căn lề chính xác.`

#### 📊 Mẫu 3: Tạo báo cáo tài chính Word có bảng biểu chuyên nghiệp
> `/xu-ly-van-phong từ số liệu quý 2. Hãy soạn thảo báo cáo Word hoàn chỉnh với bảng biểu kẻ viền chỉn chu và biểu đồ minh họa.`

---

## 📝 License

Phát hành dưới giấy phép **MIT License**. Bạn có thể tự do chỉnh sửa và tích hợp vào hệ thống AI của mình.
