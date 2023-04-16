# C-i-t-ADB-Debugging-GPU-Debug-Layer

- Hướng Dẫn Cài Đặt Trình Gỡ Lỗi ADB Bằng USB && Bật Tính Năng Lớp Gỡ Lỗi GPU Layer® 

# Fllow Me { FaceBook }
 
- https://facebook.com/truongthach.info

# Hotline Support ( 7H00 - 23H00 )

- 0354073192 

# USB && WIFI ADB Debugging 

- Cầu Gỡ lỗi ADB Không Dây 

Qualcomm Snapdragon && Mediatek 

Hisilicon Kirin && Dimensity 

- Arm Cortex v7a && v8a 64Bit

Android Developers™

Android Studio

Trương Văn Thạch ^⁠_⁠_⁠_⁠_⁠_⁠_⁠_⁠_⁠_⁠^

Copyright to Truong Van Thach (⁠人⁠ ⁠•͈⁠ᴗ⁠•͈⁠)


# Cầu gỡ lỗi Android (adb) là một công cụ dòng lệnh linh hoạt cho phép bạn giao tiếp với thiết bị.

Lệnh adb hỗ trợ nhiều thao tác trên thiết bị, chẳng hạn như cài đặt và gỡ lỗi ứng dụng. adb cung cấp quyền truy cập vào một shell Unix mà bạn có thể dùng để chạy nhiều lệnh trên thiết bị. Đây là một chương trình ứng dụng-máy chủ bao gồm ba thành phần:

Ứng dụng: sẽ gửi lệnh. Ứng dụng chạy trên máy phát triển của bạn. Bạn có thể gọi ứng dụng qua một dòng lệnh bằng cách phát ra lệnh adb.
Một trình nền (adbd) chạy lệnh trên thiết bị. daemon chạy dưới dạng quy trình trong nền trên từng thiết bị.
Máy chủ (server) quản lý việc giao tiếp giữa ứng dụng và trình nền. Máy chủ chạy dưới dạng quy trình nền trên máy phát triển của bạn.

#Cách Cài Đặt Công Cụ SDK Android Trên Windows 10 Pro 64Bit

adb nằm trong gói Công cụ nền tảng Android SDK. 

Hãy tải gói này xuống bằng Trình quản lý SDK rồi cài đặt gói này tại " android_sdk/platform-tools/." 

Nếu bạn muốn có gói Công cụ nền tảng Android SDK độc lập

- Bấm Vào Liên Kết Bên Dưới Tại Trang Developer Android ™

https://developer.android.com/studio/releases/platform-tools

# Lệnh Khởi Động Gỡ Lỗi Không Dây Trên Android 2.x >> Android 10

- adb thường giao tiếp với thiết bị qua USB

nhưng bạn cũng có thể sử dụng adb qua Wi-Fi. 

Để kết nối một thiết bị chạy Android 10 (API cấp 29) trở xuống

hãy làm theo các bước ban đầu sau đây qua USB:

1 :  Kết nối thiết bị Android và máy tính lưu trữ adb với mạng Wi-Fi chung.

2 : Kết nối thiết bị với máy tính lưu trữ bằng cáp USB.

3 : Đặt thiết bị đích để nghe kết nối TCP/IP trên cổng 5555:

- adb tcpip 5555

4 : Rút cáp USB khỏi thiết bị đích.

5 : Tìm địa chỉ IP của thiết bị Android. Hãy vào cài đặt WIFI để tìm điều này !

6 : Kết nối với thiết bị theo địa chỉ IP của thiết bị.

- adb connect device_ip_address:5555

7 : Xác nhận rằng máy tính lưu trữ của bạn đã kết nối với thiết bị đích.
 
- adb devices

< List of devices attached
device_ip_address:5555 device > 

8 : Nếu bạn thấy số seri thiết bị của bạn xuất hiện trên trình giả lập ADB ( Chúc Mừng Bạn Đã Kết Nối Thành Công ) 

 - Trên là các bước giúp bạn kết nối thiết bị của mình với Trình giả lập ADB trên PC ( Android 2.1 >> Android 10 { API 29 trở xuống } ). Còn các thiết bị Chạy Android 11 trở lên hãy bật gỡ lỗi ADB Qua WIFI trong phần ( Tùy Chọn Dành Cho Nhà Phát Triển )

# Các lệnh ADB Tăng Hiệu Suất Android ( Không Khuyến Cáo Vì Có Thể Ảnh Hưởng Đến Pin Và Ứng Suất Nhiệt Của CPU )

 - Lớp GLES

bookmark_border

Trên các thiết bị chạy Android 10 (API cấp 29) trở lên, bạn có thể sử dụng tính năng phân lớp OpenGL ES (GLES). 

Một ứng dụng có thể gỡ lỗi có thể tải các lớp GLES từ APK của ứng dụng đó, từ thư mục cơ sở của ứng dụng hoặc từ một APK lớp đã chọn.

Cách sử dụng lớp GLES tương tự như cách sử dụng lớp xác thực Vulkan.

- Yêu cầu

Lớp GLES chỉ được hỗ trợ trên các phiên bản GLES 2.0 trở lên.

- Đặt lớp

LayerLoader của GLES tìm kiếm các lớp ở những vị trí sau theo thứ tự ưu tiên:

1. Vị trí hệ thống cho thư mục gốc

Vị trí này yêu cầu quyền truy cập thư mục gốc

- adb root

- adb disable-verity

- adb reboot

- adb root

- adb shell setenforce 0

- adb shell mkdir -p /data/local/debug/gles

- adb push <layer>.so /data/local/debug/gles/

2. Thư mục cơ sở của ứng dụng

Ứng dụng mục tiêu phải là ứng dụng có thể gỡ lỗi hoặc bạn phải có quyền truy cập thư mục gốc:

- adb push libGLTrace.so /data/local/tmp

- adb shell run-as com.android.gl2jni cp /data/local/tmp/libGLTrace.so .

- adb shell run-as com.android.gl2jni ls | grep libGLTrace
libGLTrace.so

3. APK bên ngoài

Xác định ABI của ứng dụng mục tiêu, sau đó cài đặt APK chứa các lớp bạn muốn tải:

- adb install --abi armeabi-v7a layers.apk

4. Trong APK của ứng dụng mục tiêu

Ví dụ sau đây cho thấy cách đặt lớp vào APK của ứng dụng:

- jar tf GLES_layers.apk
lib/arm64-v8a/libGLES_glesLayer1.so
lib/arm64-v8a/libGLES_glesLayer2.so
lib/arm64-v8a/libGLES_glesLayer3.so
lib/armeabi-v7a/libGLES_glesLayer1.so
lib/armeabi-v7a/libGLES_glesLayer2.so
lib/armeabi-v7a/libGLES_glesLayer3.so
resources.arsc
AndroidManifest.xml
META-INF/CERT.SF
META-INF/CERT.RSA
META-INF/MANIFEST.MF

# Bật Lớp Cho Từng Ứng Dụng 

- hoặc trên toàn cục. Các chế độ cài đặt theo từng ứng dụng vẫn tồn tại sau những lần khởi động lại, trong khi các thuộc tính toàn cục sẽ bị xoá khi bạn khởi động lại.

# Enable layers

- adb shell settings put global enable_gpu_debug_layers 1

# Specify target application

- adb shell settings put global gpu_debug_app <Pack_Name>

# Specify layer list (from top to bottom)

# Layers are identified by their filenames, such as "libGLLayer.so"

- adb shell settings put global gpu_debug_layers_gles <layer1:layer2:layerN>

# Specify packages to search for layers

- adb shell settings put global gpu_debug_layer_app <package1:package2:packageN>

# Cách Tắt Lớp Trên Ứng Dụng

# Delete the global setting that enables layers

- adb shell settings delete global enable_gpu_debug_layers

# Delete the global setting that selects target application

- adb shell settings delete global gpu_debug_app

# Delete the global setting that specifies layer list

- adb shell settings delete global gpu_debug_layers_gles

# Delete the global setting that specifies layer packages

- adb shell settings delete global gpu_debug_layer_app
# Cách Bật Lớp Toàn Ứng Dụng 

- adb shell setprop debug.gles.layers <layer1:layer2:layerN>

# Nội dung và mã mẫu trên trang này phải tuân thủ các giấy phép như mô tả trong phần Giấy phép nội dung Github. 

Java và OpenJDK là nhãn hiệu hoặc nhãn hiệu đã đăng ký của Developer Android hoặc đơn vị liên kết của Trương Văn Thạch ✓. 


