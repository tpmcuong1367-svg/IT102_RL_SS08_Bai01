Phân tích lỗi và Test Cases

Nguyên nhân lỗi:
Dùng pop() lấy nhầm xe cuối mảng thay vì xe đầu mảng. Sửa thành shift() để đúng nguyên tắc vào trước ra trước (FIFO).
Vòng lặp duyệt i <= length làm truy cập phần tử undefined, khi cộng dồn làm biến totalKwh thành NaN. Sửa thành i < length.
Bảng Test Cases:
STT	Trường hợp kiểm thử	Dữ liệu đầu vào	Kết quả sai thực tế	Kết quả đúng mong đợi
1	Mảng chuẩn nhiều xe	queue = ['29A-112.33', '30E-889.12', '51K-678.99'], kwh = [45.2, 30.5, 62.8, 28.0]	Xe: 51K-678.99, Kwh: NaN, Doanh thu: NaN	Xe: 29A-112.33, Kwh: 166.5, Doanh thu: 749250
2	Mảng 1 phần tử	queue = ['43A-999.99'], kwh = [20.0]	Xe: 43A-999.99, Kwh: NaN, Doanh thu: NaN	Xe: 43A-999.99, Kwh: 20, Doanh thu: 90000
3	Mảng rỗng	queue = [], kwh = []	Xe: undefined, Kwh: NaN, Doanh thu: NaN	Xe: undefined, Kwh: 0, Doanh thu: 0
