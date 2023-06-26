# Tiếng Việt

Hướng dẫn cách bỏ Dual Clock dành cho các dòng máy LG Hàn (V30, V40, V50, V60 Thinq, G8, LG Velvet...)

LƯU Ý : TỪ BẢN ANDROID 10 TRỞ LÊN KHI XÓA DUAL CLOCK, ĐỒNG HỒ KHÔNG CĂN GIỮA MÀN HÌNH VÀ TỪ BẢN ANDROID 10 TRỞ XUỐNG ĐỒNG HỒ TỰ ĐỘNG CĂN GIỮA MÀN HÌNH.

## Các bước để bỏ Dual Clock

### 1. Cài đặt các phần mềm cần thiết

Trên điện thoại các bạn tải cho mình [SetEdit (Settings Database Editor)](https://play.google.com/store/apps/details?id=by4a.setedit22&hl=en)

Trên máy tính các bạn tải File `LGMobileDriver_WHQL_Ver_4.2.0.exe` và `adb-setup-1.4.3.exe`

Sau đó cài đặt lên trên máy tính 2 File này

### 2. Kết nối điện thoại với máy tính

Sau khi cài đặt các phần mềm ở trên xong, hãy kết nối điện thoại vào máy tính.

Trên máy tính, chạy CMD với quyền quản trị sau đó gõ lệnh "cd/" và gõ tiếp "cd adb".

(ADB sau khi cài đặt, thư mục mặc định ở ổ C:. Nếu các bạn để chỗ khác, hãy trỏ cmd sang chỗ các bạn cài ADB).

Sau khi làm và trỏ CMD đến ADB, gõ lệnh
```bash
adb devices
```
Nó sẽ hiển thị model máy bạn
```bash
LGMG600K1de67c62        unauthorized
```
Nếu hiển thị như này tức là chưa cấp phép ADB trên điện thoại, trên điện thoại hãy bấm cho phép.
Sau khi bấm xong các bạn gõ tiếp 
```bash
adb devices
```
Và nó sẽ hiện như này là xong, đến bước tiếp theo
```bash
LGMG600K1de67c62        device
```
Nếu như không hiển thị như vậy, hãy nhập lại `adb devices` một lần nữa.

### 3. Nhập lệnh vào ADB trên máy tính

Ở cửa sổ ADB bạn vừa làm ở trên, hãy nhập vào dòng lệnh này để cấp quyền cho Set Edit mà các bạn cài ở trên điện thoại
```bash
adb shell pm grant by4a.setedit22 android.permission.WRITE_SECURE_SETTINGS
```

### 4. Mở App Set Edit trên điện thoại

Mở app Set Edit ở trên điện thoại, chú ý vào dòng `System Table`

Bấm vào và chuyển qua `Secure table`, rồi tìm dòng ghi là `roaming_dualclock`

Bấm vào dòng đó, chọn `Edit Value` rồi chuyển giá trị thành `1` và lưu lại.

### 5. Xong, thưởng thức thành quả.

Vậy là xong, giờ các bạn thử tắt màn hình bật lại để xem thành quả nhé.

Mình đã test thử trên LG G6 KT Telecom và đang chạy Android 9 nên nó sẽ tự động căn đồng hồ ra giữa nhé.

### Nguồn bài viết : https://lgviet.info/threads/tat-dong-ho-doi-lg-v50-remove-dual-clock.2254/

