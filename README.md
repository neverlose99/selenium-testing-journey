# KIỂM THỬ TỰ ĐỘNG VỚI SELENIUM IDE

- **Học phần:** Đánh giá và kiểm định chất lượng phần mềm
- **Giảng viên hướng dẫn:** Trịnh Thanh Bình
- **Sinh viên thực hiện:** Bùi Minh Đức
- **Mã sinh viên:** 22014062

---

## I. Tổng quan về dự án & Công cụ

Dự án thực hiện kiểm thử tự động hộp đen (Black-box Automation Testing) áp dụng phương pháp **Record & Playback** nhằm đánh giá tính ổn định của luồng mua hàng tiêu chuẩn trên trang thương mại điện tử Swag Labs.

* **Công cụ sử dụng:** Selenium IDE (Web Extension v3.x)
* **Trình duyệt thực thi:** Google Chrome 
* **Phương pháp:** Xây dựng kịch bản độc lập (Atomic Tests)

---

## II. Danh sách kịch bản kiểm thử (Test Suite)

Bộ kiểm thử bao gồm **03 Test Case** mô phỏng hành vi của người dùng thực tế:

| Mã TC | Tên kịch bản | Các bước thực hiện (Steps) | Dữ liệu đầu vào (Input) | Kết quả mong đợi (Expected) | Trạng thái |
| :--- | :--- | :--- | :--- | :--- | :---: |
| **TC-01** | `TC01_Login` | 1. Mở trang chủ<br>2. Nhập Username<br>3. Nhập Password<br>4. Click nút *Login* | - User: `standard_user`<br>- Pass: `secret_sauce` | Chuyển hướng sang giao diện `/inventory.html`, hiển thị danh sách sản phẩm. | **PASSED** |
| **TC-02** | `TC02_Add_Cart`| 1. Tại trang Inventory, click *Add to cart* tại sản phẩm *Sauce Labs Backpack*<br>2. Click vào biểu tượng Giỏ hàng | Không có | Nút "Add to cart" chuyển thành "Remove", icon giỏ hàng hiển thị số `1`. | **PASSED** |
| **TC-03** | `TC03_Logout`| 1. Click mở *Hamburger Menu* (góc trái)<br>2. Click chọn *Logout* | Không có | Hủy phiên làm việc, đưa người dùng quay trở về trang Login. | **PASSED** |

---

## III. Hướng dẫn tái thực thi (Reproduction Steps)

1. Cài đặt extension **Selenium IDE** trên Chrome hoặc Edge.
2. Tải file `SauceDemo_Test.side` tại repository này.
3. Mở Selenium IDE -> Chọn **"Open an existing project"** -> Trỏ vào file `.side` vừa tải.
4. Nhấn nút **Run all tests** (biểu tượng 3 hình tam giác) để trình duyệt tự động chạy kiểm chứng.

---

## IV. Bằng chứng thực thi (Execution Evidence)

Toàn bộ 03 kịch bản thực thi thành công (0% Failure / 0% Error):

Login :

<img width="1913" height="1017" alt="image" src="https://github.com/user-attachments/assets/d592d523-b5f5-4aeb-a51f-463f8382df50" />

Add_Cart:

<img width="1918" height="1021" alt="image" src="https://github.com/user-attachments/assets/166f8a9f-6ff2-4257-903c-1a464c158ff8" />

Logout :

<img width="1918" height="801" alt="image" src="https://github.com/user-attachments/assets/cdee405d-41c1-4256-8c8f-73d1609b2bb1" />