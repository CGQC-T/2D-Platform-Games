1.สร้าง Script สำหรับ Player:
  คลิกขวาที่โฟลเดอร์ Assets → Create → C# Script → ตั้งชื่อว่า PlayerController.
  ดับเบิลคลิกเปิดใน Code Editor (เช่น Visual Studio).

2.เขียนโค้ดใน PlayerController.cs:

3.เพิ่ม Script ให้ Player:
  ลาก Script PlayerController ไปที่ GameObject Player ใน Hierarchy.
  ตั้งค่า Speed และ Jump Force ใน Inspector (เช่น Speed = 5, Jump Force = 10).

4.กำหนด Tag ให้ Ground:
  เลือก GameObject Ground. 
  ใน Inspector → Add Tag → สร้าง Tag ชื่อ "Ground".
  กลับมาที่ Ground → Assign Tag "Ground".
