1.สร้าง Script สำหรับ Player:
  คลิกขวาที่โฟลเดอร์ Assets → Create → C# Script → ตั้งชื่อว่า PlayerController.
  ดับเบิลคลิกเปิดใน Code Editor (เช่น Visual Studio).

2.เขียนโค้ดใน PlayerController.cs:

using UnityEngine;

public class PlayerController : MonoBehaviour
{
    public float speed = 5f; // ความเร็วในการเดิน
    public float jumpForce = 10f; // แรงกระโดด
    private Rigidbody2D rb;
    private bool isGrounded = true;

    void Start()
    {
        rb = GetComponent<Rigidbody2D>();
    }

    void Update()
    {
        // การเดินซ้าย-ขวา
        float moveX = Input.GetAxis("Horizontal");
        rb.velocity = new Vector2(moveX * speed, rb.velocity.y);

        // การกระโดด
        if (Input.GetKeyDown(KeyCode.Space) && isGrounded)
        {
            rb.velocity = new Vector2(rb.velocity.x, jumpForce);
            isGrounded = false; // กระโดดแล้ว
        }
    }

    private void OnCollisionEnter2D(Collision2D collision)
    {
        // ตรวจจับการแตะพื้น
        if (collision.gameObject.CompareTag("Ground"))
        {
            isGrounded = true;
        }
    }
}


3.เพิ่ม Script ให้ Player:
  ลาก Script PlayerController ไปที่ GameObject Player ใน Hierarchy.
  ตั้งค่า Speed และ Jump Force ใน Inspector (เช่น Speed = 5, Jump Force = 10).

4.กำหนด Tag ให้ Ground:
  เลือก GameObject Ground. ใน Inspector → Add Tag → สร้าง Tag ชื่อ "Ground".
  กลับมาที่ Ground → Assign Tag "Ground".
