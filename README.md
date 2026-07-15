# Thiết Kế, Tối Ưu Và So Sánh Hiệu Năng Cổng MUX 4-1 (2-Bit) 

Đồ án này tập trung nghiên cứu, thiết kế chi tiết ở mức vật lý (Physical Level) và so sánh hiệu năng của bộ chọn dữ liệu **MUX 4-1 (2-bit)** sử dụng hai cấu trúc logic khác nhau: **Static CMOS** và **Transmission Gate (TG)** trên công nghệ bán dẫn **90nm**.

* **Môn học:** CE222.Q22 – Thiết kế vi mạch số (Trường Đại học Công nghệ thông tin - ĐHQG-HCM)
* **Thành viên thực hiện:** Lê Đăng Khôi & Võ Nguyễn Anh Khôi

---

## 📂 Tài liệu Đồ án (Tải trực tiếp tại đây)
* 📄 **[Tải Báo Cáo Đồ Án Chi Tiết (PDF)](Report_MUX41_2bit_CMOS_TG.pdf)** 
* 📊 **[Tải Slide Thuyết Trình Đồ Án (PowerPoint)](Slides_MUX41_2bit_CMOS_TG.pptx)**

*(Lưu ý: Bạn có thể click trực tiếp vào các đường dẫn trên để xem hoặc tải về).*

---

## 📊 Kết quả Thực nghiệm & So sánh tiêu biểu (Post-Layout Simulation)
Dưới đây là bảng số liệu đối chứng đo đạc thực tế sau khi đã trích xuất ký sinh (PEX) với tải FO4 (Fan-Out of 4) từ công cụ Synopsys:

| Thông số so sánh | Cấu trúc Static CMOS | Cấu trúc Transmission Gate (TG) | Nhận xét nhanh |
| :--- | :---: | :---: | :--- |
| **Diện tích Layout** | **$125.97 \mu m^2$** | **$93.03 \mu m^2$** | **TG tiết kiệm ~26.1% diện tích** nhờ tối ưu hóa liên kết và chia sẻ vùng khuếch tán. |
| **Độ trễ tệ nhất ($t_{p}$)** | $t_{pLH} = 143\text{ ps}$<br>$t_{pHL} = 145\text{ ps}$ | $t_{pLH} = 45.9\text{ ps}$<br>$t_{pHL} = 60.4\text{ ps}$ | Độ trễ đường găng của cấu trúc TG thấp hơn rất nhiều. |
| **Tần số cực đại ($F_{max}$)** | **$3.47\text{ GHz}$** | **$9.4\text{ GHz}$** | **TG hoạt động nhanh hơn gấp ~2.7 lần** so với Static CMOS. |

---

## 🛠️ Công cụ & Công nghệ sử dụng
* **Môi trường thiết kế:** Synopsys Custom Compiler
* **Mô phỏng & Đo đạc:** Custom WaveView
* **Trích xuất ký sinh:** PEX (StarRC)
* **Công nghệ:** CMOS 90nm GP (General Purpose)
