
CODE BẰNG PYTHON, DB LƯU TRỮ TRÊN SQLITE
1.3. Mục tiêu và phạm vi đề tài
1.3.1. Mục tiêu
1.3.1.1. Mục tiêu chức năng
Hệ thống hướng đến việc cung cấp đầy đủ các chức năng đáp ứng nhu cầu của ba nhóm người dùng chính: sinh viên, ban quản trị CLB, và quản trị viên (Admin).
 Cụ thể:
-	Đối với sinh viên:
o	Đăng ký tài khoản và cập nhật thông tin cá nhân.
o	Tìm kiếm, xem thông tin CLB, sự kiện và sản phẩm.
o	Nộp đơn tham gia CLB, đơn ứng tuyển vị trí hoặc tham gia sự kiện.
o	Thêm sản phẩm vào giỏ hàng, đặt hàng và theo dõi đơn hàng.
o	Theo dõi tình trạng đơn ứng tuyển, đơn đặt hàng và hoạt động CLB đã tham gia.
-	Đối với Ban quản trị CLB:
o	Quản lý thông tin CLB, thành viên và các hoạt động nội bộ.
o	Duyệt đơn tham gia, đơn ứng tuyển và đơn thành lập CLB mới.
o	Tạo, chỉnh sửa, xóa sự kiện và sản phẩm của CLB.
o	Quản lý đơn hàng, báo cáo doanh thu và thống kê hoạt động.
o	Gửi thông báo, cập nhật tin tức và kết nối với thành viên.
-	Đối với Quản trị viên (Admin):
o	Quản lý toàn bộ CLB, sinh viên
o	Phê duyệt các hoạt động, sản phẩm và sự kiện của CLB.
o	Theo dõi và tổng hợp báo cáo chung cho toàn hệ thống.
1.3.1.2. Mục tiêu phi chức năng
Bên cạnh các chức năng nghiệp vụ, hệ thống còn hướng tới đáp ứng các yêu cầu phi chức năng sau:
-	Tính hiệu quả: Giao diện thân thiện, thao tác đơn giản, phản hồi nhanh chóng.
-	Tính bảo mật: Bảo vệ thông tin tài khoản, dữ liệu cá nhân và hoạt động của CLB bằng cơ chế xác thực và phân quyền người dùng.
-	Tính ổn định và tin cậy: Hệ thống hoạt động liên tục, hạn chế lỗi phát sinh và đảm bảo tính toàn vẹn dữ liệu.
-	Tính mở rộng: Dễ dàng nâng cấp, tích hợp thêm các mô-đun chức năng hoặc mở rộng phạm vi cho toàn trường.
-	Tính tương thích: Có thể truy cập trên nhiều thiết bị (máy tính, điện thoại, máy tính bảng) và trình duyệt khác nhau.
-	Tính thẩm mỹ: Giao diện trực quan, hiện đại, phù hợp với đối tượng sinh viên và phong cách của trường.
1.3.2. Phạm vi
Hệ thống “Quản lý và Kết nối CLB – Sinh viên NEU” được thiết kế hướng tới phạm vi triển khai trong toàn bộ môi trường sinh viên và các Câu lạc bộ tại Đại học Kinh tế Quốc dân.
Cụ thể, phạm vi của hệ thống bao gồm:
-	Quản lý CLB: Lưu trữ và quản lý thông tin chi tiết của các CLB (tên, mô tả, lĩnh vực hoạt động, thành viên, sự kiện, sản phẩm, báo cáo…).
-	Quản lý sinh viên: Hỗ trợ sinh viên tạo tài khoản, cập nhật thông tin cá nhân, theo dõi và tham gia các CLB, sự kiện hoặc hoạt động ngoại khóa.
-	Quản lý sự kiện & bài viết: Cho phép CLB tạo, chỉnh sửa và công khai các sự kiện; sinh viên có thể đăng ký, theo dõi và tham gia.
-	Quản lý sản phẩm: Các CLB có thể đăng bán sản phẩm, sinh viên có thể xem thông tin, đặt hàng và thanh toán.
-	Quản lý đơn và báo cáo: Quản trị viên và Ban quản trị CLB có thể duyệt đơn, tổng hợp dữ liệu và thống kê báo cáo hoạt động định kỳ.
-	Kết nối thông tin: Xây dựng kênh giao tiếp trực tuyến giữa CLB – sinh viên – quản trị viên, giúp chia sẻ thông báo, tin tức và phản hồi nhanh chóng.
Hệ thống tập trung vào việc số hóa và tự động hóa các quy trình quản lý và truyền thông của CLB, nhưng không bao gồm các hoạt động thanh toán trực tuyến hoặc xử lý giao dịch tài chính thực tế. Ngoài ra, hệ thống không can thiệp sâu vào các hoạt động nội bộ chi tiết của từng CLB như phân công công việc hoặc tổ chức họp nội bộ. Trong giai đoạn hiện tại, phạm vi triển khai của hệ thống giới hạn trong khối sinh viên và các CLB trực thuộc Đại học Kinh tế Quốc dân.
1.4. Phương pháp nghiên cứu
Đề tài “Quản lý và Kết nối CLB – Sinh viên NEU” được phân tích và thiết kế theo phương pháp hướng đối tượng (OOAD), giúp mô hình hóa hệ thống thông qua các đối tượng (object) có đặc tính (thuộc tính) và hành vi (phương thức) riêng biệt.
Phương pháp hướng đối tượng nổi bật với nhiều ưu điểm như:
-	Tăng tính tái sử dụng và mở rộng nhờ cơ chế kế thừa và đóng gói.
-	Dễ bảo trì, cập nhật và phát triển chức năng mới mà không ảnh hưởng đến toàn hệ thống.
-	Giúp mô hình hóa hệ thống sát thực tế, dễ hiểu, rõ ràng về quan hệ giữa các thành phần.
Trong quá trình phân tích và thiết kế, nhóm sử dụng ngôn ngữ mô hình hóa UML (Unified Modeling Language) để thể hiện cấu trúc và hành vi hệ thống thông qua các biểu đồ sau:
-	Biểu đồ ca sử dụng (Use Case Diagram) – mô tả chức năng tổng quát và mối quan hệ giữa người dùng và hệ thống.
-	Biểu đồ lớp (Class Diagram) – biểu diễn cấu trúc dữ liệu, thuộc tính và mối quan hệ giữa các lớp.
-	Biểu đồ trình tự (Sequence Diagram) – mô tả quá trình tương tác giữa các đối tượng khi thực hiện chức năng cụ thể.
-	Biểu đồ hoạt động (Activity Diagram) – mô tả luồng xử lý nghiệp vụ của các chức năng chính.
-	Biểu đồ gói và thành phần (Package, Component Diagram) – biểu diễn sự tổ chức logic và cấu trúc thành phần phần mềm.
Phương pháp hướng đối tượng giúp hệ thống đạt được tính mô-đun hóa, dễ bảo trì và dễ mở rộng, đáp ứng tốt yêu cầu thay đổi trong tương lai.
CHƯƠNG 2. KHẢO SÁT HỆ THỐNG
2.2.1. Xác định các nhóm người dùng
Qua quá trình phân tích, hệ thống “Quản lý và kết nối CLB – sinh viên NEU” được thiết kế nhằm đáp ứng nhu cầu sử dụng của ba nhóm người dùng chính bao gồm: Sinh viên, Ban tổ chức CLB và Quản trị viên.
Sinh viên
	Là đối tượng trực tiếp tham gia vào các CLB, sự kiện, hoạt động ngoại khóa trong trường. Sinh viên có nhu cầu tìm kiếm, đăng ký, theo dõi và tham gia các hoạt động của CLB, đồng thời kết nối với các tổ chức trong trường.
Ban tổ chức CLB (Ban quản trị CLB)
Là nhóm người dùng chịu trách nhiệm điều hành, tổ chức và triển khai các hoạt động của CLB. Bao gồm Ban chủ nhiệm và các ban chức năng (Ban nhân sự, Ban truyền thông, Ban sự kiện, Ban tài chính…). Họ có nhu cầu tạo, quản lý sự kiện, tuyển thành viên, quản lý sản phẩm và tương tác với sinh viên.
Quản trị viên (Admin)
Là bộ phận phụ trách giám sát và điều hành toàn bộ hoạt động CLB trong trường, thường thuộc Phòng Công tác Sinh viên hoặc Đoàn – Hội cấp trường. Nhóm này có nhu cầu kiểm duyệt, phê duyệt các sự kiện, thống kê dữ liệu, xuất báo cáo, và đảm bảo hoạt động của hệ thống diễn ra ổn định, đúng quy định.
2.2.2. Phân tích nhu cầu và chức năng mong muốn của từng nhóm
Nhóm	Nhu cầu	Chức năng mong muốn
Sinh viên	1. Sinh viên cần có một nền tảng tập trung để tìm kiếm, xem thông tin về các Câu lạc bộ (CLB), sự kiện và sản phẩm do CLB tổ chức hoặc phát hành.
2. Có thể đăng ký tài khoản, đăng nhập và tham gia các hoạt động CLB dễ dàng, minh bạch.
3. Thực hiện các hoạt động như nộp đơn tham gia CLB, đăng ký tham gia sự kiện, mua sản phẩm của CLB.
4. Theo dõi tình trạng các đơn đăng ký, đơn hàng, điểm Đoàn, và thông tin cá nhân trên hệ thống.
	1. Đăng ký tài khoản và đăng nhập hệ thống.
2. Điền và gửi đơn đăng ký tham gia CLB.
3. Tìm kiếm và xem thông tin sự kiện.
4. Điền và gửi đơn đăng ký tham gia sự kiện.
5. Tìm kiếm và xem danh sách sản phẩm.
6. Cập nhật thông tin mua hàng và tạo đơn đặt mua sản phẩm.
7. Theo dõi lịch sử đơn đăng ký, đơn hàng.
CLB	1. Cần có công cụ để đăng ký thành lập CLB mới và gửi đơn xin duyệt lên hệ thống.
2. Quản lý toàn bộ thông tin CLB, bao gồm sự kiện, sản phẩm, đơn đăng ký, đơn hàng.
3. Có khả năng duyệt các đơn đăng ký tham gia CLB, sự kiện, sản phẩm, cũng như ghi nhận điểm Đoàn cho sinh viên tham gia.
4. Theo dõi, thống kê và báo cáo kết quả hoạt động CLB.	1. Đăng ký tài khoản và đăng nhập hệ thống.
2. Quản lý sản phẩm: thêm, sửa, xóa, xem danh sách sản phẩm.
3. Quản lý sự kiện: thêm, sửa, hủy, xem danh sách sự kiện.
4. Quản lý đăng ký tham gia sự kiện: duyệt đơn, xem danh sách tham gia, ghi nhận tham gia và điểm Đoàn.

Admin	1. Quản lý toàn bộ hệ thống, đảm bảo hoạt động ổn định và minh bạch.
2. Quản lý người dùng (sinh viên, CLB) và các thông tin liên quan.
3. Duyệt các đơn đăng ký thành lập CLB, các sự kiện và sản phẩm được CLB gửi lên hệ thống.
4. Theo dõi, tổng hợp báo cáo và thống kê toàn bộ dữ liệu hệ thống.	1. Quản lý tài khoản người dùng (sinh viên, CLB).
2. Quản lý thông tin CLB: thêm mới, duyệt đơn đăng ký, chỉnh sửa, xóa CLB.
3. Duyệt sự kiện và sản phẩm được CLB gửi lên.
4. Tổng hợp, thống kê và xuất báo cáo tổng quan toàn hệ thống.

