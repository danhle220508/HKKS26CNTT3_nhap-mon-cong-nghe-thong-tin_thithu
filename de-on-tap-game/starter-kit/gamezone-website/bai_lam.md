# BÀI LÀM – THI THỬ HACKATHON 02 (GAMEZONE)

- **Họ tên: Lê Đức Anh** 
- **Lớp: CNTT3** 
- **Link repository:** 
- **Hệ điều hành (Windows/macOS):windows** 

## 4.2. Thao tác CLI

### Các lệnh đã chạy

```powershell
pwd
ls -Force
mv .\cap_nhat.txt .\docs\
mv .\logo_gamezone.png .\media\
cp .\media\logo_gamezone.png .\backup\
rm .\temp_207.tmp
cd .\logs\
ls -force
cd..
```

### Kết quả liệt kê toàn bộ dự án

```text
   Directory: C:\Users\AD\OneDrive\Documents\Downloads\New folder\de-on-tap-game\starter-kit\gamezone-website


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
d-----        10/26/2026   1:25 PM                backup
d-----        10/26/2026   1:23 PM                data
d-----        10/26/2026   1:25 PM                docs
d-----        10/26/2026   1:23 PM                logs
d-----        10/26/2026   1:25 PM                media
-a----        10/26/2026   1:10 PM             70 .env
-a----        10/26/2026   1:10 PM           1437 bai_lam.md

```

## 4.3. Lọc log thủ công

### Lệnh đã chạy

```powershell
Get-Content .\logs\game.log | Select-String "ERROR" > .\logs\daily_report.txt

```

### 2 dòng lỗi đầu tiên trong daily_report.txt

```text
2025-11-05 08:03:15 [ERROR] Mat ket noi may chu game
2025-11-05 08:09:15 [ERROR] Mat ket noi may chu game
```

## 4.4. README.md

> Chấm trực tiếp trên `README.md` ở gốc dự án.

- [x] Heading 1
- [x] Mô tả in đậm + in nghiêng
- [x] Bảng `Thư mục | Nội dung` (≥3 dòng)
- [x] Code block lệnh liệt kê
- [x] Task list (≥2 việc, ≥1 đã xong)
- [ ] Blockquote nhắc không upload `.env`

## 4.5. Chạy script auto_report

### Lệnh chạy

```shell
.\auto_report.ps1
```

### Nội dung file logs/auto_report.txt

```text
=== BAO CAO LOI GAMEZONE ===

2025-11-05 08:03:15 [ERROR] Mat ket noi may chu game
2025-11-05 08:09:15 [ERROR] Mat ket noi may chu game
2025-11-05 08:12:15 [ERROR] Mat ket noi may chu game
2025-11-05 08:39:15 [ERROR] Mat ket noi may chu game
2025-11-05 08:42:15 [ERROR] Mat ket noi may chu game
2025-11-05 08:51:15 [ERROR] Loi luu tien trinh choi


```

## 4.6. Đếm số dòng lỗi

### Lệnh

```powershell
(Get-Content .\logs\game.log | Select-String "ERROR").count

```

### Kết quả đếm

```text
6

```

## 4.7. Báo cáo tổng hợp

### Các lệnh đã chạy

```shell
 "=== TONG HOP LOG GAMEZONE ===" > .\logs\tong_hop.txt
 Get-Content .\logs\game.log | Select-String "WARNING"
  (Get-Content .\logs\game.log | Select-String "WARNING").Count >> .\logs\tong_hop.txt

```

### Nội dung file logs/tong_hop.txt

```text
=== TONG HOP LOG GAMEZONE ===
2025-11-05 08:54:15 [WARNING] May chu qua tai CPU 90%


1


```

## 4.8. Excel

> Chấm trực tiếp trên file `data/giao_dich_thang_11.xlsx`.

