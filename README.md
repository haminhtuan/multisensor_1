# multisensor_1

1. Bước 1: Hàn linh kiện vào board

+ Hàn linh kiện: dùng điện trở phù hợp với sức nặng của đệm, nhưng trở 47K Ohm tôi thấy dùng ổn
Nếu chỉ dùng cảm biến giường thì chỉ cần hàn chân ESP, chân cắm fsr, điện trở. Tuỳ theo nhu cầu, có thể hàn thêm các cảm biến CO2, ánh sáng, chân cắm led.




+ Hàn dây điện vào đầu dây FSR, lưu ý dùng kẹp cao su, và nhiệt hàn vừa phải, hàn nhanh để tránh làm hỏng dây FSR





2. Bước 2: Trải dây FSR đưới giường
Trải dây vào đươi vị trí hay nằm để cảm biến được lực

![image](https://github.com/haminhtuan/multisensor_1/assets/39614020/93490689-a8a5-4b4e-b4fb-b24e96e47b07)


  

3. Bước 3 Nạp code Esphome cho esp32 d1 mini





4. Bước 4:
- Cắm chip esp vào board,
- Cắm các dây FSR, dây led
- Cắm điện 5v vào board
- Chờ các cảm biến hiện lên
- Viết các automation theo nhu cầu




