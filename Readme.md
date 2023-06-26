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

# English

Instructions on how to remove Dual Clock for LG Korean models (V30, V40, V50, V60 Thinq, G8, LG Velvet...)

NOTE : FROM ANDROID 10 AND UP WHEN CLEARING DUAL CLOCK, THE CLOCK DOESN'T align the middle of the screen and from ANDROID 10 AND LOW THE CLOCK AUTOMATICALLY centered on the screen.

## Steps to remove Dual Clock

### 1. Install the necessary software

On your phone, download [SetEdit (Settings Database Editor)](https://play.google.com/store/apps/details?id=by4a.setedit22&hl=en)

On your computer, download the File `LGMobileDriver_WHQL_Ver_4.2.0.exe` and `adb-setup-1.4.3.exe`

Then install these 2 files on your computer

### 2. Connect phone to computer

After installing the above software, connect your phone to the computer.

On the computer, run CMD with administrative privileges then type "cd/" and then type "cd adb".

(ADB after installation, the default folder is in C: drive. If you put it somewhere else, please point cmd to the place where you installed ADB).

After doing and pointing CMD to ADB, type command
```bash
adb devices
```
It will show your device model
```bash
LGMG600K1de67c62 unauthorized
```
If it is displayed like this, it means that ADB has not been authorized on the phone, on the phone, click allow.
After clicking, please continue to type
```bash
adb devices
```
And it will appear like this and done, go to the next step
```bash
LGMG600K1de67c62 device
```
If it doesn't show up, type `adb devices` again.

### 3. Enter the command into ADB on the computer

In the ADB window you just did above, enter this command to grant the Set Edit permission that you have installed on your phone.
```bash
adb shell pm grant by4a.setedit22 android.permission.WRITE_SECURE_SETTINGS
```

### 4. Open App Set Edit on your phone

Open the Set Edit app on the phone, pay attention to the line `System Table`

Click and go to `Secure table`, then find the line that says `roaming_dualclock`

Click on that line, select `Edit Value` then change the value to `1` and save.

### 5. Done, enjoy the results.

That's it, now try to turn off the screen and turn it back on to see the results.

I tested it on LG G6 KT Telecom and it's running Android 9 so it will automatically center the clock.

### Article source: https://lgviet.info/threads/tat-dong-ho-doi-lg-v50-remove-dual-clock.2254/
