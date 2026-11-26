# Xưởng Đấu Dây

Bàn thực hành điện ảo chạy trên trình duyệt: đấu dây tủ điện công nghiệp, đi dây điện nhà và chạy thử sơ đồ nguyên lý.

## Tính năng
- 3 chế độ: **Đấu dây công nghiệp**, **Điện dân dụng**, **Sơ đồ nguyên lý** (ký hiệu IEC chạy mô phỏng được)
- 174 linh kiện: aptomat, RCBO, cầu chì, contactor, rơ le nhiệt, timer, biến tần, SSR, động cơ 3 pha / 6 đầu / 2 tốc độ / DC, điện trở nhiệt 3 pha, đèn huỳnh quang, công tơ, ampe kế, vôn kế, biến dòng 3 pha, đồng hồ đa năng…
- Đủ loại cảm biến: tiệm cận cảm ứng / điện dung, quang khuếch tán / gương / thu-phát, sợi quang, màu, laser, siêu âm, cảm biến từ xi lanh, màn chắn an toàn, PT100, can nhiệt K, cảm biến 4–20 mA, báo khói, gas, mưa, rung, dòng chảy, từ cửa…
- **PLC nhiều model**: Siemens S7-1200 (SCL), S7-200 SMART (STL), Mitsubishi FX3U (IL), Delta DVP (IL), Omron CP1E (Mnemonic), LS XBC (IL) và PLC chuẩn IEC (ST / biểu thức) – đúng địa chỉ và chân đấu từng hãng, đổi model tự chuyển chương trình, sơ đồ thang chạy trực tiếp
- **Trình soạn LAD chạm-để-vẽ**: không cần gõ lệnh – chạm để thêm tiếp điểm thường mở/thường đóng, nhánh song song, so sánh analog, cuộn dây, SET/RESET, TON/TOF, CTU; chọn địa chỉ từ danh sách. Sơ đồ vẽ đúng ký hiệu từng hãng (khối TON của TIA Portal, `( T0 K50 )` của GX Works, khối TIM của CX-Programmer, `[TMR]` của Delta, `[TON]` của XG5000, T37 của S7-200 SMART) và tự sinh mã lệnh tương đương (SCL / STL / IL / Mnemonic)
- Bộ điều khiển nhiệt độ, lò sấy mô phỏng nhiệt độ tăng giảm theo điện trở
- Mô phỏng thật: contactor hút, tự giữ, khóa chéo, sao – tam giác, đảo chiều, timer, mất pha, ngắn mạch, cấp sai điện áp
- Hiệu ứng sự cố tại đúng vị trí: nổ khi chập, cháy thiết bị, khói và cảnh báo khi mất pha
- **Vi điều khiển, vi xử lý**: bàn làm việc mới với 5 bo Arduino Uno, ESP32, 8051 (AT89S52), PIC16F877A, STM32 Blue Pill; viết chương trình C ngay trong app (Arduino, Keil C51, CCS C / XC8, STM32 HAL) và chạy mô phỏng có Serial Monitor; hơn 20 linh kiện: điện trở, LED, LED RGB, nút nhấn, biến trở, transistor, còi, rơ le 5V, servo SG90, LED 7 đoạn, LCD 16x2 I2C, động cơ DC + L298N, HC-SR04, DHT11, quang trở, hồng ngoại, PIR, LM35, nguồn 5V/9V/12V, 7805; 13 bài mẫu
- **Robot gắp thả khí nén điều khiển bằng PLC**: mô hình robot 2 trục có 3 van 5/2, cảm biến vị trí a0 a1 b0 b1 và cảm biến phôi; bài mẫu PLC S7-1200 chạy tuần tự 8 bước bằng LAD, có Start/Stop và dừng khẩn cắt nguồn van
- **Màu dây tự động theo tiêu chuẩn**: chọn IEC 60445 + IEC 60204-1, kiểu dễ học, kiểu cũ ở Việt Nam, Mỹ NEC/NFPA 79 hoặc Trung Quốc GB; app tự nhận ra dây pha, trung tính, tiếp địa, điều khiển AC, +24 V, 0 V, tín hiệu, analog để tô màu, có nút tô lại toàn bộ dây
- **Biến tần cài thông số như máy thật**: chọn hãng (Mitsubishi FR-D700, Siemens V20, Delta VFD-M, LS iG5A, Yaskawa V1000 hoặc chuẩn chung), bàn phím mô phỏng và bảng thông số theo mã của từng hãng; mô phỏng tăng/giảm tốc, đảo chiều, biến trở 0–10 V, 3 cấp tốc độ, relay lỗi và các lỗi quá dòng, quá áp, quá tải
- **Cẩm nang biến tần**: nguyên lý, chọn biến tần, đấu dây động lực và điều khiển, thứ tự cài thông số, cách cài trên bàn phím từng hãng, 5 bài thực hành, bảng lỗi, an toàn và câu hỏi tự kiểm tra
- **Cẩm nang PLC cho người mới**: PLC là gì, chu kỳ quét, đấu dây ngõ vào PNP/NPN và ngõ ra Relay/Transistor, bảng địa chỉ và phần mềm từng hãng, 12 bài sơ đồ thang (tiếp điểm, tự giữ, nút Stop thường đóng, SET/RESET, khóa chéo, TON, TOF, bộ đếm, xung nhấp nháy, sao – tam giác, analog 4–20 mA) có bàn thực hành đấu sẵn, bảng lỗi thường gặp, an toàn và câu hỏi tự kiểm tra
- 21 bài mẫu có hướng dẫn từng bước (có PLC, lò sấy, bơm theo mức 4–20 mA)
- Màu dây theo IEC 60445 / IEC 60204-1, có màu tùy chỉnh
- Đồng hồ đo điện áp và thông mạch
- Cẩm nang linh kiện, bảng ký hiệu điện
- Tự lưu dự án trong trình duyệt, xuất/nhập mã dự án

## Chạy
Chỉ cần mở `index.html` bằng trình duyệt (Chrome, Safari, Edge). Không cần cài đặt, không cần máy chủ.

## Cài lên điện thoại
Bật GitHub Pages cho repo này, mở đường link trên Safari (iPhone) → nút Chia sẻ → **Thêm vào MH chính**. Trên Android dùng Chrome → **Cài đặt ứng dụng**.

> Công cụ học tập mô phỏng. Khi thi công thật luôn cắt điện, đo kiểm và tuân thủ quy chuẩn an toàn điện.
