# multisensor_1

0. Chuẩn bị các linh kiện
- Module board sensor và các linh kiện nhỏ
![image](https://github.com/haminhtuan/multisensor_1/assets/39614020/37bd3b80-266f-4990-89a8-85c0686112c5)
hoặc
![image](https://github.com/haminhtuan/multisensor_1/assets/39614020/a82652c0-50b3-4c1c-8205-a2c328048b74)

- Nguồn DC 5v ( cung cấp kèm board hoặc mua thêm tuỳ bộ kit)
- Chip ESP 32 D1 mini ( mua thêm)
- Dây cảm biến lực FSR600 (mua thêm) tối đa 2 dây
- Dây led 2812b(mua thêm) : không quá 3m (phải thay nguồn 5v 4a)
- Cảm biến CO2 SCD40/41: mua thêm
- Cảm biến ánh sáng BH1750: mua thêm
- Cảm biến chuyển động LD2410c hoặc 2420 ( cần chỉnh jumper để set điện thế cấp): mua thêm

1. Bước 1: Hàn linh kiện vào board

+ Hàn linh kiện: dùng điện trở phù hợp với sức nặng của đệm, nhưng trở 47K Ohm tôi thấy dùng ổn
Nếu chỉ dùng cảm biến giường thì chỉ cần hàn chân ESP, chân cắm fsr, điện trở. Tuỳ theo nhu cầu, có thể hàn thêm các cảm biến CO2, ánh sáng, chân cắm led.

![image](https://github.com/haminhtuan/multisensor_1/assets/39614020/92f9f0cf-266a-416d-ab1a-b89695d606be)

+ Hàn dây điện vào đầu dây FSR, lưu ý dùng kẹp cao su, và nhiệt hàn vừa phải, hàn nhanh để tránh làm hỏng dây FSR

![image](https://github.com/haminhtuan/multisensor_1/assets/39614020/d3a9b425-3b7b-43df-960f-19bc2ae48583)


2. Bước 2: Trải dây FSR đưới giường
Trải dây vào đươi vị trí hay nằm để cảm biến được lực

![(https://github.com/haminhtuan/multisensor_1/assets/39614020/93490689-a8a5-4b4e-b4fb-b24e96e47b07)

![image](https://github.com/haminhtuan/multisensor_1/assets/39614020/b11c2e57-725e-41ef-a3e5-aaeaea724490)


3. Bước 3 Nạp code Esphome cho esp32 d1 mini

- Nạp ESP cho Hass: Cái này trên mạng nhiều, các bác google để tìm hiểu và cài
- Kết nối esphome cho chip ESP: cắm dây cáp usb giữa máy tính và esp và chọn New Device trong tab ESPHome, và làm theo hướng dẫn của máy
![image](https://github.com/haminhtuan/multisensor_1/assets/39614020/bb05229d-b2b8-4ca8-9236-90cb65f3ed95)
- Thêm code tại file Esphome code trong device đã có các thiết lập cơ bản esphome

4. Bước 4:
- Cắm chip esp vào board,
- Cắm các dây FSR, dây led
- Cắm điện 5v vào board
![image](https://github.com/haminhtuan/multisensor_1/assets/39614020/d8ddbb8e-d101-437b-88b3-d9032c3820aa)
- Chờ các cảm biến hiện lên
![image](https://github.com/haminhtuan/multisensor_1/assets/39614020/df277933-1a47-4671-88d0-b393b2d2038e)

- Viết các automation theo nhu cầu



Tôi tham khảo từ đây để làm fsr https://community.home-assistant.io/t/fsr-the-best-bed-occupancy-sensor/365795
