"การเขียนโค้ดควบคุม Player"
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

"การเพิ่มระบบคะแนน (Score System)"
1.เพิ่ม Text สำหรับแสดงคะแนน:
    คลิกขวาที่ Hierarchy → UI → Text → ตั้งชื่อว่า ScoreText.
    ใน Inspector:
        - ตั้งค่า Text เริ่มต้นเป็น "Score: 0".
        - ปรับตำแหน่ง Text ให้อยู่มุมบนซ้ายของหน้าจอ.
2.สร้าง Script สำหรับ GameManager:
    คลิกขวาที่ Assets → Create → C# Script → ตั้งชื่อว่า GameManager.
3.เพิ่ม Script ให้ GameManager:
    ลาก Script GameManager ไปที่ GameObject Canvas.
    ใน Inspector ของ GameManager → Assign ScoreText.

"เพิ่ม Script สำหรับ Obstacle:"
    คลิกขวาที่ Assets → Create → C# Script → ตั้งชื่อว่า Obstacle.
    ลาก Script ไปที่ GameObject Obstacle.
