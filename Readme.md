# Tiếng Việt

Hướng dẫn cách bỏ Dual Clock dành cho các dòng máy LG Hàn (V30, V40, V50, V60 Thinq, G8, LG Velvet...)

LƯU Ý : TỪ BẢN ANDROID 10 TRỞ LÊN KHI XÓA DUAL CLOCK, ĐỒNG HỒ KHÔNG CĂN GIỮA MÀN HÌNH VÀ TỪ BẢN ANDROID 10 TRỞ XUỐNG ĐỒNG HỒ TỰ ĐỘNG CĂN GIỮA MÀN HÌNH.

## Các bước để bỏ Dual Clock

### 1. Cài đặt các phần mềm cần thiết

Trên điện thoại các bạn tải cho mình [SetEdit (Settings Database Editor)](https://play.google.com/store/apps/details?id=by4a.setedit22&hl=en)

Trên máy tính các bạn tải File `LGMobileDriver_WHQL_Ver_4.2.0.exe` và `adb-setup-1.4.3.exe`
Sau đó cài đặt lên trên máy tính 2 File này

### 2. Kết nối điện thoại với máy tính

Sau khi cài đặt các phần mềm ở trên xong, hãy kết nối điện thoại vào máy tính
Trên máy tính, chạy CMD với quyền quản trị sau đó gõ lệnh "cd/" và gõ tiếp "cd adb".
(ADB sau khi cài đặt, thư mục mặc định ở ổ C:. Nếu các bạn để chỗ khác, hãy trỏ cmd sang chỗ các bạn cài ADB)
Sau khi làm và trỏ CMD đến ADB, gõ lệnh
```bash
adb devices
```

B4.1 : Đầu tiên các bạn gõ là  thì nó sẽ hiện là :
      VD : "LGMG600K1de67c62        unauthorized"
          tức là chưa cấp phép ADB trên điện thoại, bạn vào điện thoại bấm cho phép
          nhé.
Sau khi bấm xong các bạn gõ tiếp : "adb devices", nó hiện là :
           "LGMG600K1de67c62        device"
           tức là máy đã được cấp phép rồi nhé, đến bước tiếp theo thôi.
