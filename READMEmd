Vietnam Jobs Dataset — Data Cleaning & EX4
Dự án thực hiện làm sạch và đánh giá chất lượng bộ dữ liệu tuyển dụng việc làm tại Việt Nam gồm 85.470 bản ghi.
Files
Datacleansing.ipynb — Quá trình kiểm tra và làm sạch dữ liệu.
EX4.ipynb — Phân tích Outliers, Noise và Consistency.
jobs.csv — Dataset gốc.
jobs_cleaned.csv — Dataset sau khi làm sạch.
Original/ — Các file gốc được lưu lại trong quá trình thực hiện.
Data Cleaning
Các bước chính:
Kiểm tra cấu trúc và missing values.
Chuẩn hóa tên thành phố: 466 → 88 giá trị khác nhau.
Làm sạch và chuẩn hóa salary.
Tạo các trường salary_min, salary_max, salary_currency, salary_type và salary_quality.
Chuẩn hóa format của job_type.
Giữ lại missing values khi không có đủ thông tin để thay thế đáng tin cậy.
EX4
Outlier Detection
Phân tích salary_max bằng:
IQR: 5.511 outliers
Z-score: 1.056 outliers
Các outliers lớn nhất được kiểm tra lại với dataset gốc trước khi quyết định giữ lại.
Consistency
So sánh dữ liệu trước và sau khi cleaning, tập trung vào city và job_type.
Cleaning Decisions
Các giá trị bất thường không bị xóa tự động. Quyết định xử lý dựa trên dữ liệu nguồn và khả năng xác định rõ giá trị có thực sự sai hay không.
Main Principle
Không phải mọi giá trị bất thường đều là dữ liệu sai.
Mục tiêu của quá trình cleaning là cải thiện tính nhất quán và khả năng phân tích của dữ liệu mà không đưa ra các giả định không có cơ sở.


Data Cleaning Report
1. Mục tiêu
Thực hiện kiểm tra và làm sạch bộ dữ liệu tuyển dụng việc làm tại Việt Nam gồm 85.470 bản ghi, tập trung vào dữ liệu thiếu, tính nhất quán của văn bản và thông tin lương.
2. Các bước đã thực hiện
Kiểm tra dữ liệu
Kiểm tra số dòng, số cột, kiểu dữ liệu và các giá trị khác nhau.
Kiểm tra số lượng dữ liệu thiếu trong từng cột.
Chuẩn hóa thành phố
Chuẩn hóa các tên thành phố có cách viết khác nhau bằng mapping.
Số lượng thành phố khác nhau giảm từ 466 xuống 88.
Làm sạch thông tin lương
Phân tích nhiều định dạng lương khác nhau.
Trích xuất mức lương tối thiểu và tối đa.
Xác định loại tiền tệ.
Tạo các cột salary_min và salary_max.
Tạo các cột salary_currency, salary_type và salary_quality để hỗ trợ phân tích.
Chuẩn hóa văn bản
Chuẩn hóa job_type bằng cách:
Xóa khoảng trắng thừa.
Chuyển về chữ thường.
Chuẩn hóa nhiều khoảng trắng liên tiếp.
Số lượng category vẫn là 27, nhưng có 1 dòng được thay đổi.
Dữ liệu thiếu
Các giá trị thiếu được xác định và giữ lại khi không có đủ thông tin để suy ra giá trị chính xác.
Các cột có nhiều missing nhất là:
skills: 11.294
job_fields: 7.625
salary_max: 3.278
salary_min: 2.338
Kiểm tra cuối
Sau khi làm sạch, dataset được kiểm tra lại về:
Kích thước dữ liệu.
Missing values.
Số lượng category.
Chất lượng dữ liệu lương.
Dataset sau khi làm sạch được lưu thành jobs_cleaned.csv.
3. Nguyên tắc xử lý
Không tự động xóa các giá trị bất thường hoặc thiếu nếu không có đủ bằng chứng để xác định chúng là sai. Mục tiêu là cải thiện tính nhất quán và khả năng phân tích mà vẫn giữ thông tin từ dữ liệu gốc.


EX4 — Outliers, Noise and Consistency
1. Mục tiêu
Phân tích các giá trị ngoại lệ, kiểm tra tính nhất quán và đánh giá một số vấn đề về chất lượng dữ liệu sau khi làm sạch.
2. EX4.1 — Phát hiện Outlier
Sử dụng cột salary_max_vnd và áp dụng hai phương pháp:
IQR: phát hiện 5.511 outliers.
Z-score: phát hiện 1.056 outliers.
Trong đó:
1.056 giá trị được phát hiện bởi cả hai phương pháp.
4.455 giá trị chỉ được phát hiện bằng IQR.
Không có giá trị nào chỉ được phát hiện bằng Z-score.
Hai phương pháp cho kết quả khác nhau vì sử dụng các tiêu chí thống kê khác nhau.
3. EX4.2 — Kiểm tra Outlier
Kiểm tra 5 giá trị salary_max_vnd lớn nhất và truy ngược về dữ liệu gốc.
Một số giá trị lớn nhất gồm:
36 - 600 triệu
100 tr - 500 tr vnd
15,000 - 20,000 usd
Các giá trị này đều được tìm thấy trong dữ liệu gốc và được chuyển đổi đúng trong quá trình cleaning.
Do đó, các giá trị này được giữ lại thay vì tự động xóa.
Một số bản ghi trùng lặp cũng được quan sát trong quá trình kiểm tra.
4. EX4.3 — Kiểm tra tính nhất quán
So sánh số lượng giá trị khác nhau trước và sau khi làm sạch:
CộtTrướcSaujob_title23.57623.576job_type2727position_level2626city46688experience181181skills20.48420.484job_fields7.4917.491
Trong đó:
city có sự thay đổi rõ rệt do chuẩn hóa tên thành phố.
job_type giữ nguyên số category nhưng có 1 dòng được chuẩn hóa về format.
5. Missing Values
Các missing values chính vẫn còn trong:
skills
job_fields
salary_min
salary_max
city
job_title
Các giá trị này được giữ lại khi không có cơ sở đáng tin cậy để thay thế.
6. EX4.4 — Cleaning Decision
Các quyết định chính:
Chuẩn hóa city để xử lý các tên không nhất quán.
Chuẩn hóa format của job_type.
Chuyển đổi và chuẩn hóa salary để phục vụ phân tích.
Giữ missing values khi không thể suy ra đáng tin cậy.
Điều tra outliers thay vì tự động xóa.
Giữ experience ở dạng text vì chuyển sang số cần thêm các giả định.
7. Kết luận
Quá trình EX4 cho thấy không phải mọi giá trị bất thường đều là dữ liệu sai. Các quyết định xử lý được dựa trên dữ liệu nguồn và khả năng xác định rõ giá trị cần thay đổi.
