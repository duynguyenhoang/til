# Chia sẻ hành trình của bản thân chuyển từ Fullstack sang Data Engineering

Vài người bạn của mình đề nghị chia sẻ về hành trình chuyển từ Fullstack dev sang Data Engineer, nên mình chia sẻ hành trình của mình cùng mọi người.

Phần này chỉ mang mục đích chia sẻ kinh nghiệm và ý kiến cá nhân của bản thân.

## Lý do tôi chuyển sang Data Engineer.

Nhắc đến việc này, thì nên trở về cách đây hơn 2 năm. Lúc đầu mình gia nhập công ty hiện tại với vị trí là Fullstack, phát triển một ứng dụng trên kiến trúc serverless dựa trên nền AWS cloud. Công việc cũng tiến triển được tầm 4-6 tháng gì đó mình không nhớ chính xác, một anh trong team Data Engineer có việc gia đình nên trở về lại Pháp.

Do lúc đó team Data chỉ có 2 thành viên, anh Data Engineer kia rời team thì chỉ còn 1. Cho nên sếp bên mình cũng có ý định thêm 1 người từ team Fullstack gia nhập với team Data.

Không cần nói thêm thì các bạn cũng biết ai đã tình nguyện gia nhập vào team Data rồi.

Lý do gia nhập là:

* Mình cũng đã từng làm việc qua với team Data, thấy cũng hứng thú một phần với stack của nó.
* Chính bản thân mình cũng là một người thích tìm hiểu rộng về nhiều thứ. Cơ hội để học hỏi một công việc hoàn toàn mới, không lý do gì để từ bỏ cơ hội này.
* Data Engineer và Machine Learning về mặt nào đó có sự liên kết rất chặt chẽ, và Machine Learning đang bùng nổ trong thời gian đó.

## Thử thách và khó khăn

Cũng may mắn lúc đầu mọi thứ nền tảng của hệ thống đã được xây dựng sẵn. Đó cũng là một tài nguyên tốt cho bản thân tự học hỏi dựa vào những gì đang được xây dựng.

Nhưng không phải là không có khó khăn, ngược lại nó có khá nhiều khó khăn về lượng kiến thức để làm việc với Big Data.

* Học và tìm hiểu về Big Data, ứng dụng và kiến thức cơ bản về nó. Bạn đang có những gì đang hoạt động, nhưng muốn đi sâu và làm tốt, nhất định bạn phải hiểu nó rõ.
* Phải học rất nhiều về data processing, data visualization, những lý thuyết và framework liên quan tới data: Distributed Processing, thiết kế data schema, data wareshouse, data lake, batch, streaming,...
* Tiên quyết là phải hiểu về các frameworks đang được sử dụng: Apache Spark, Hadoop, Pandas,...
* Tìm hiểu nhiều hơn về AWS ứng dụng cho Big Data: S3, Redshift, RDS, Kinesis, DynamoDB.
* Bạn phải viết và bảo trì rất nhiều tài liệu mô tả dữ liệu cũng như cách hoạt động của hệ thống. Thật sự thừa nhận là trước kia mình rất lười và rất ít khi viết nhiều tài liệu như thế. Cảm ơn người bạn đồng nghiệp của mình, mình đã học được nhiều lợi ích từ việc này, mặc dù lúc đầu cũng khá phản đối nó.
* Làm việc với team không quá mạnh về coding. Mình không biết vấn đề này là chung chung hay nó chỉ riêng với từng công ty. Team có thể hoàn thành code cho chạy, nhưng code dư thừa rất nhiều, không có Unit Test, và coding convention thì tuỳ tiện. Bên cạnh đó cũng rất khó thuyết phục mọi người tuân theo chuẩn, vì nhiều lý do khách quan.

## Lợi thế của bạn

Nhắc tới khó khăn thử thách thì chúng ta cũng không thể bỏ qua lợi thế của mình từ Fullstack qua.

* Mạnh về Software Engineering, mình dám chắc kỹ năng về phát triển phần mềm của các bạn Fullstack sẽ hơn các bạn bắt đầu từ Data Engineer.
* Bạn từ Fullstack, bạn hiểu rõ được web/api và dữ liệu được phát sinh thế nào, giờ bạn làm Data Engineer bạn càng hiểu rõ hơn về dòng đi của dữ liệu, từ lúc xuất hiện tới việc sử dụng sau này và giá trị của chúng.
* Data Engineer không chỉ xây dựng kiến trúc, xử lý lưu trữ dữ liệu mà còn ghi dữ liệu ra nhiều nơi khác nhau. Database/Streaming/Elasticsearch là những nơi thường thấy nhất, bạn sẽ có lợi thế kinh nghiệm về những việc này. Với kinh nghiệm về Fullstack, bạn có thể ước lượng được, đoán được dữ liệu được ghi và quản lý thế nào là tốt nhất khi nó được đọc ra.
* Đôi khi bạn cũng sẽ phải xây dựng và quản lý API để hỗ trợ team khác đọc dữ liệu, đây chắc chắc là lợi thế về kinh nghiệm của bạn.

## Tôi đã làm được gì cho tới hiện tại?

Thật sự tới hiện tại mình đã đầu tư nhiều thời gian tìm hiểu về Big Data, hệ sinh thái Hadoop, các dự án Opensouce về Big Data, hiểu và sử dụng hiệu quả các dịch vụ AWS chuyên về Data

Tận dụng kinh nghiệm về phát triển phần mềm, giúp việc phát triển và bảo trì các ứng dụng xử lý dữ liệu ngày tốt hơn. Áp dụng UnitTest vào tương lai gần, khuyến khích và dần bắt buộc mọi người viết UnitTest. 

Hỗ trợ thành viên mới, và cả Data Science team về vấn đề coding, turning. Bên cạnh đó hỗ trợ team để deploy và bảo trì Machine Learning Pipelines

Áp dụng Apache Spark vào một số xử lý Machine Learning, đặc biệt trong các bước xử lý và tổng hợp dữ liệu. Việc này giúp Data Science team rất nhiều, họ chỉ cần sử dụng những câu truy vấn SQL để trích lọc tổng hợp dữ liệu, không cần quan tâm nhiều đến vấn đề khác

## Tương lai sẽ như thế nào?

Tới hiện tại, mình vẫn thấy hạnh phúc đi tiếp con đường Data Engineer, một mặt thì dã quen thuộc với nó mặt khác thì Data Engineer là một trong những vị trí được nhiều công ty săn đón với chế độ khá cao 💴

Mình sẽ tiếp tục học và tìm hiểu thêm về Data Engineer, học và thi vài chứng chỉ liên quan Big Data. Hiện tại sẽ bắt đầu tập chung vào `AWS Certified Big Data – Specialty` do mình quen thuộc với AWS nhất. Ngoài ra chứng chỉ của Google Cloud Platform - GCP cũng là một chứng chỉ có giá trị, mình đánh giá nó cao hơn AWS 

## Kết bài

![Big Data Quote](https://www.azquotes.com/picture-quotes/quote-big-data-is-like-teenage-sex-everyone-talks-about-it-nobody-really-knows-how-to-do-it-dan-ariely-66-19-39.jpg)

Hành trình tìm hiểu về Data Engineer của mình cũng không quá dài, chỉ hơn 2 năm làm việc thật tế, ngoài việc tự cố gắng từ phía bản thân thì sự may mắn khi làm việc tại công ty cũng không phải là yếu tố nhỏ.

Nếu các bạn muốn mở rộng kiến thức, có ý định thử thách ở một khía cạch khác của IT, hãy mạnh dạn, chủ động tìm kiếm và nắm bắt cơ hội, bạn sẽ ít nhiều học và trải nghiệm thêm nhiều thứ.

