---
title: "Event 1"
date: "2025-09-18"
weight: 1
chapter: false
pre: " <b> 4.1. </b> "
---


# Bài thu hoạch “Migration & Modernization”

### Mục Đích Của Sự Kiện

- Hoàn thành quá trình di chuyển và hiện đại hóa quy mô lớn với AWS
- Hiện đại hóa ứng dụng bằng các công cụ hỗ trợ AI tạo sinh
- Thảo luận nhóm: Hiện đại hóa ứng dụng: Đẩy nhanh quá trình chuyển đổi kinh doanh
- Chuyển đổi VMware với công nghệ hiện đại hóa đám mây dựa trên AI
- Bảo mật AWS ở quy mô lớn: Từ phát triển đến sản xuất

### Danh Sách Diễn Giả

- **Nguyen Van Hai** - Director of Software Engineering, Techcombank
- **Nguyen The Vinh** - Co-Founder & CTO, Ninety Eight
- **Nguyen Minh Nganh** - AI Specialist, OCB
- **Nguyen Manh Tuyen** - Head of Data Application, LPBank Securities

### Nội Dung Nổi Bật

#### 1. Tìm hiểu về các chiến lược di chuyển và hiện đại hóa quy mô lớn với AWS thông qua các nghiên cứu điển hình thực tế từ Techcombank.
- Chiến lược di chuyển và hiện đại hóa của Techcombank
  + **Assess**: Đánh giá được môi trường kiểm kê, và xác định được khoảng trống. 
  + **Mobilize**: Thiết lập CCoE, xác định hàng rào, xây dựng sự lưu loát của điện toán đám mây. 
  + **Migrate & Modernize**: Ưu tiên khối lượng công việc có tác động cao
  + **Reinvent**: AI, tự động hóa, sản phẩm dữ liệu, mô hình doanh mới. 

- Generative trong hiện đại hóa quy mô. 
  + **Code Transformation:** Java 8 -> 21, .NET -> .NET 8
  + **Dependency Mapping:** Lập bản đồ phụ thuộc để phân tích tự động các mối quan hệ của hệ thống. 
  + **Environment Assessment:** Amazon có hàng ngàn dịch vụ hiện tại hóa với AI có thể đáp ứng được cho doanh nghiệp. 

- Giải pháp và chiến lược mà Techcombank đã ứng dụng trong việc dùng các dịch vụ của AWS. 
  + Amazon EKS
  + Amazon Aurora MySQL
  + Amazon MSK 
  + Amazon ElastiCache for Redis OSS. 

- Tổng quan về chiến lược Modernization Strategy Blueprint.
        
      Align: Tài trợ việc triển khai và động lực doanh nghiệp.
      |
      Assess: Hiểu rõ về con người, quy trình, và công nghệ
      |
      Mobilize: CoE, quản trị, đào tạo
      |
      Modernize: Replatform, refactor, rebuild
      |
      Reinvent: Data, AI và hiện đại hóa các ứng dụng cho sự đổi mới

#### 2. Tìm hiểu về việc hiện đại hóa ứng dụng bằng các công cụ Generative AI, với những hiểu biết thực tế từ VPBank

- Hiện đại hóa là quá trình chuyển đổi dần dần các ứng dụng để đạt được lợi ích về tính khả dụng, khả năng mở rộng, tính linh hoạt trong kinh doanh và tối ưu hóa chi phí khi chạy trên nền tảng đám mây

***Top 4 trường hợp sử dụng hàng đầu - Hiện đại hóa ứng dụng với Generative AI.***

**Use case 1: Streamline VMware Migration with AWS Transform for VMware**

*Đẩy nhanh quá trình di chuyển và hiện đại hóa cơ sở hạ tầng với khám phá thông minh và thực thi tự động*

- Rút ngắn thời gian di chuyển VMware với tính năng tự động hóa thông minh của AWS Transform.
  
- Chuyển đổi các cấu hình mạng phức tạp chỉ trong vài giờ thay vì vài tuần nhờ tính năng khám phá, ánh xạ phụ thuộc và lập kế hoạch làn sóng tự động do AWS cung cấp.
  
- Mở rộng quy trình di chuyển của bạn với tính năng tạo nhóm bảo mật tự động, lựa chọn phiên bản EC2 thông minh và các tùy chọn triển khai linh hoạt, bao gồm cấu hình VPC dạng hub-and-spoke hoặc cấu hình VPC riêng biệt.
  
- Cải thiện thời gian thực hiện lên đến 90%, đồng thời giảm 80% công sức thủ công.

**Use case 2: GenAl Development with AWS Serverless and Container Solutions**

*Xây dựng các ứng dụng GenAl sẵn sàng cho doanh nghiệp trên nền tảng AWS Serverless và Container*

- AWS cung cấp hai giải pháp mạnh mẽ cho việc phát triển và triển khai ứng dụng GenAl:

  + Không máy chủ với AWS Bedrock: Phát triển và triển khai nhanh chóng các ứng dụng GenAl bằng AWS Lambda, ECS với Fargate, Step Functions và EventBridge. Lý tưởng cho chatbot, tạo tài liệu và xử lý nội dung thông minh. Tận dụng các bản cập nhật và kiến ​​trúc tham chiếu mới nhất của AWS Bedrock.

  + Dựa trên container với Amazon EKS: Xây dựng, đào tạo và chạy các ứng dụng GenAl trên Kubernetes, tận dụng khả năng điều phối mạnh mẽ của nó. Sử dụng các công cụ nguồn mở và dịch vụ đám mây gốc cho khối lượng công việc GenAl có khả năng mở rộng. Triển khai linh hoạt trên cả môi trường đám mây và tại chỗ với sự đổi mới liên tục từ cộng đồng OSS.

- Chọn một trong hai cách tiếp cận hoặc kết hợp cả hai để phù hợp nhất với yêu cầu ứng dụng GenAl cụ thể của bạn và đẩy nhanh hành trình AI của bạn.

**Use case 3: Revolutionize NET Modernization with AWS Transform for NET**

*Chuyển đổi các ứng dụng Windown cũ sang Cloud-native với tự động hóa được hỗ trợ bởi AI-powered.*

- Hiện đại hóa các ứng dụng chạy trên Windows nhanh hơn tới 4 lần với AWS Transform for NET.
- Tận dụng khả năng tự động hóa của AI để phân tích các phụ thuộc, tái cấu trúc mã và tối ưu hóa cho việc triển khai Linux, đồng thời cắt giảm chi phí cấp phép tới 40%.
- Chuyển đổi hàng trăm ứng dụng song song với khả năng kiểm tra và xác thực tự động - từ các ứng dụng MVC cũ sang các dịch vụ WCF.
- Các tính năng nâng cao bao gồm hiện đại hóa Ul tự động, xử lý gói riêng và lập kế hoạch sóng thông minh, mang lại khả năng hiện đại hóa toàn diện với tốc độ vượt trội.

**Use case 4: Nâng cao Kỹ thuật Nền tảng với Gen Al & IDP**

*Tận dụng sức mạnh của các trợ lý thông minh như AWS Transform Developer với Nền tảng phát triển nội bộ.*

- Việc mở rộng quy mô hiện đại hóa ở cấp độ doanh nghiệp đòi hỏi thời gian và đầu tư để phát triển Nền tảng Phát triển Nội bộ (IDP). Gartner dự đoán rằng đến năm 2026, 80% các tổ chức kỹ thuật phần mềm sẽ thành lập các nhóm nền tảng với tư cách là nhà cung cấp nội bộ các dịch vụ, thành phần và công cụ có thể tái sử dụng để triển khai ứng dụng.

- Khai thác sức mạnh của các trợ lý thông minh như AWS Transform Developer với IDP để:

  1. Tạo quy trình làm việc và tự động hóa các tác vụ lặp lại.

  2. Tìm hiểu các phương pháp hay nhất của IDP từ các tổ chức hàng đầu, chẳng hạn như Adobe, Expedia, JPMC và Goldman Sachs.

  3. Hiểu rõ các bản thiết kế container và kiến ​​trúc tham chiếu của AWS để mang lại tốc độ và khả năng mở rộng nhanh chóng cho sáng kiến ​​hiện đại hóa quy mô doanh nghiệp.

**Các động lực hiện đại hóa phổ biến**

- Giảm chi phí
  + Giảm/loại bỏ chi phí bản quyền Windows & SQL Server
  + Xây dựng kiến trúc khớp với tải thực tế để tối ưu chi phí
  + Tận dụng kiến trúc ARM64 để có hiệu năng/giá thành tốt hơn

- Tăng tốc độ đổi mới

  + Tách monolith thành các dịch vụ nhỏ hơn / microservices
  + Tận dụng công nghệ mới và các tính năng ngôn ngữ C#
  + Tự động hóa các quy trình thủ công

- Cải thiện khả năng mở rộng

  + Mở rộng từng thành phần / dịch vụ riêng lẻ
  + Mở rộng chi tiết với containers / serverless

- Thu hút và giữ chân nhân tài

#### 3. Nhận thông tin chuyên sâu từ các chuyên gia hàng đầu trong ngành thông qua các buổi thảo luận chuyên đề về hiện đại hóa ứng dụng
**.NET Framework so với đa nền tảng .NET** 
- **.NET Framework**: 
  + Chỉ hệ điều hành Windows
  + Phiên bản 1.0 được phát hành vào năm 2002
  + Phiên bản cuối cùng là 4.8*, phát hành năm 2019
  + Cài đặt nguyên khối - Số lượng lớn các thư viện được cài đặt cùng một lúc. 
  + EC2, Elastic Beanstalk, ECS và EKS. 

- **.NET (trước đây là .NET Core)**
  + Đa nền tảng (Windows, Linux, MacOS)
  + Phiên bản 1.0 được phát hành năm 2016
  + Phiên bản GA hiện tại là 8.0, được phát hành vào năm 2023
  + Hỗ trợ nhiều phiên bản để cài đặt
  + Hầu hết các thư viện được phân phối riêng lẻ 
  + EC2, Elastic Beanstalk, ECS, EKS, Lambda
  + Fargate

**AWS Transform: Trí thông minh được phối hợp**

  + Trải nghiệm web thống nhất -> Tự động hóa đầu cuối -> Cơ quan chuyên trách -> Định hướng mục tiêu -> Con người trong vòng lặp -> Hợp tác được đơn giản hóa

**AWS Transform cho .NET** 

- **Lợi ích khách hàng**
  + Giảm chi phí vận hành lên đến 40%
  + Loại bỏ thương mại giấy phép hệ điều hành 
  + Tiếp cận nhóm nhà phát triển lớn hơn
  + Quy mô đám mây và hiệu suất. 

- **Lợi ích kỹ thuật**
  + Hỗ trợ khắc phục lỗ hổng bảo mật
  + Hỗ trợ đa nền tảng: Windows, macOS, Linux (x86-64, arm64)
  + Tương thích với x86-64 và arm64
  + LightweightContainer
  + Kiến trúc Lambda Serverless

**Hoàn thành nâng cấp ngôn ngữ trong vài phút thông qua Amazon Q**
- Đẩy nhanh hiện đại hóa ứng dụng
Nâng cấp Ngôn ngữ Tự động (Java, .NET)
- Giảm Nợ Kỹ thuật
- Tiết kiệm Chi phí và Hiệu quả Vận hành
- Nâng cao Lợi thế Cạnh tranh

**Ứng dụng Kiro**: Giải pháp cho việc phát triển theo thông số kĩ thuật

- Kiro giúp các nhà phát triển và nhóm kỹ thuật vận chuyển phần mềm chất lượng cao với các tác nhân AI.
- Kiro biến lời nhắc của bạn thành các yêu cầu rõ ràng, thiết kế hệ thống và các nhiệm vụ riêng biệt
- Lặp lại với Kiro trên thông số kỹ thuật và kiến ​​trúc của bạn
- Các tác nhân Kiro triển khai thông số kỹ thuật trong khi vẫn giúp bạn kiểm soát.

**Agent hook**

- Phân quyền các tác vụ cho các tác nhân Al được kích hoạt khi có sự kiện như 'lưu tệp'
- Các tác nhân tự động thực thi ở chế độ nền dựa trên các lời nhắc được xác định trước của bạn
- Các hook tác nhân giúp bạn mở rộng quy mô công việc bằng cách tạo tài liệu, kiểm tra đơn vị hoặc tối ưu hóa hiệu suất mã

**Quản lí ngữ cảnh nâng cao**

- Kết nối với tài liệu, cơ sở dữ liệu, API và nhiều hơn nữa với tích hợp MCP gốc
- Cấu hình cách bạn muốn các tác nhân Kiro tương tác với từng dự án thông qua các tệp chỉ đạo
- Thả một hình ảnh về thiết kế Ul của bạn hoặc một bức ảnh về buổi thảo luận kiến ​​trúc của bạn và Kiro có thể sử dụng nó để hướng dẫn việc triển khai

**Sức mạnh, tính linh hoạt và bảo mật**
- Tương thích với VS code
  + Kiro hỗ trợ plugin, theme và cài đặt VS Code Open VSX trong môi trường Al-ready được sắp xếp hợp lý

- Các mô hình Claude tiên tiến
  + Lựa chọn giữa các mô hình Claude Sonnet 3.7 hoặc Sonnet 4, với nhiều tùy chọn hơn sẽ sớm được bổ sung

- Bảo mật cấp doanh nghiệp
  + Kiro được xây dựng và vận hành bởi AWS

**Các trường hợp sử dụng**

- Xây dựng ứng dụng mới
  + Nhanh chóng chuyển từ nguyên mẫu sang mã sản xuất và triển khai, với các phương pháp hay nhất được tích hợp sẵn, bao gồm thiết kế có cấu trúc, tài liệu hướng dẫn hoặc phạm vi kiểm thử

- Xây dựng trên các ứng dụng hiện có
  + Với thông số kỹ thuật và quản lý ngữ cảnh thông minh, Kiro giúp bạn dễ dàng tích hợp và xây dựng trên các ứng dụng hiện có mà vẫn duy trì tính nhất quán

- Tái cấu trúc và hiện đại hóa
  + Kiro hiểu rõ cơ sở mã của bạn và có thể hướng dẫn bạn chính xác trong việc tái cấu trúc hơn một triệu cơ sở mã LOC
  
#### 4. Tìm hiểu về hiện đại hóa đám mây dựa trên AI dành riêng cho môi trường VMware

**Trạng thái tương lai của khối lượng công việc VMware của bạn**
   
    RELOCATE: Amazon EVS
    |
    REHOST: Amazon EC2
    |
    REPLATFORM TO CONTAINERS: Amazon ECS or Amazon EKS
    |
    REPLATFORM TO MANAGED SERVICES: Amazon RDS, Amazon FSx, Amazon WorkSpaces, and more
    |
    REFACTOR: Modern Application

    => Áp dụng nhanh chóng, nền tảng của lợi ích đám mây và ROI nhanh....................---->....................Tất cả các lợi ích gốc của đám mây và ROl cao

**Chuyển đổi AWS cho VMware**

- Hiện đại hóa khối lượng công việc VMware lên Amazon EC2 với các tác nhân AI được thiết kế riêng
- Tự động hóa và đơn giản hóa các tác vụ chuyển đổi
- Giảm chi phí và phí cấp phép với Amazon EC2
- Nâng cao bảo mật, khả năng mở rộng và phục hồi
- Thúc đẩy đổi mới với hơn 200 dịch vụ gốc của AWS

**Lập bản đồ công nghệ gốc từ VMware sang AWS**

![VMware to AWS native technology mapping](https://github.com/DazielNguyen/AWS_FCJ_FA25_VAD_NOTES_LESSON/blob/main/fcj_web_local/static/images/4-EventParticipated/VMware%20to%20AWS%20native%20technology%20mapping.jpg)

**Một cách tiếp cận dựa trên AI của agentic để hiện đại hóa VMware**

    1. Kết nối với môi trường VMware của bạn
    |
    2. Phân tích khối lượng công việc, sự phụ thuộc và mức độ sẵn sàng
    |
    3. Chuyển đổi cấu hình mạng VMware sang các cấu trúc AWS gốc
    |
    4. Tạo các kế hoạch sóng thông minh dựa trên sự phụ thuộc của ứng dụng
    |
    5. Xác thực với nhóm của bạn, sau đó thực hiện

    => Chuyển đổi từng bước với xác thực human-in-the-loop

**Lí do AWS Transform dành cho việc di chuyển sang VMware?**
- **Chi phí thấp hơn**
  + Loại bỏ phí cấp phép VMware
  + Tối ưu hóa chi phí cơ sở hạ tầng với khả năng điều chỉnh kích thước phiên bản do AI điều khiển

- **Di chuyển nhanh hơn**
  + Tăng tốc chuyển đổi mạng lên đến 80 lần
Giảm thiểu gián đoạn, bảo toàn tính toàn vẹn của ứng dụng và đẩy nhanh quá trình chuyển đổi

- **Cải thiện bảo mật**
  + Tăng cường bảo mật với nền tảng đám mây gốc
  + Di chuyển an toàn với quy trình xác thực human-in-the-loop

- **Đổi mới ở quy mô lớn**
  + Giảm nợ kỹ thuật và xây dựng các ứng dụng hiện đại, có khả năng mở rộng
  + Tích hợp liền mạch với hơn 200 dịch vụ gốc của AWS như data lakes, phân tích nâng cao và AI/ML

#### 5. Kết nối và học hỏi trực tiếp từ các Kiến trúc sư Giải pháp AWS và các chuyên gia trong ngành

- 
### Những Gì Học Được

#### Tư Duy Thiết Kế

- **Business-first approach**: Luôn bắt đầu từ business domain, không phải technology
- **Ubiquitous language**: Importance của common vocabulary giữa business và tech teams
- **Bounded contexts**: Cách identify và manage complexity trong large systems

#### Kiến Trúc Kỹ Thuật

- **Event storming technique**: Phương pháp thực tế để mô hình hóa quy trình kinh doanh
- Sử dụng **Event-driven communication** thay vì synchronous calls
- **Integration patterns**: Hiểu khi nào dùng sync, async, pub/sub, streaming
- **Compute spectrum**: Criteria chọn từ VM → containers → serverless

#### Chiến Lược Hiện Đại Hóa

- **Phased approach**: Không rush, phải có roadmap rõ ràng
- **7Rs framework**: Nhiều con đường khác nhau tùy thuộc vào đặc điểm của mỗi ứng dụng
- **ROI measurement**: Cost reduction + business agility

### Ứng Dụng Vào Công Việc

- **Áp dụng DDD** cho project hiện tại: Event storming sessions với business team
- **Refactor microservices**: Sử dụng bounded contexts để identify service boundaries
- **Implement event-driven patterns**: Thay thế một số sync calls bằng async messaging
- **Serverless adoption**: Pilot AWS Lambda cho một số use cases phù hợp
- **Try Amazon Q Developer**: Integrate vào development workflow để boost productivity

### Trải nghiệm trong event

Tham gia workshop **“GenAI-powered App-DB Modernization”** là một trải nghiệm rất bổ ích, giúp tôi có cái nhìn toàn diện về cách hiện đại hóa ứng dụng và cơ sở dữ liệu bằng các phương pháp và công cụ hiện đại. Một số trải nghiệm nổi bật:

#### Học hỏi từ các diễn giả có chuyên môn cao

- Các diễn giả đến từ AWS và các tổ chức công nghệ lớn đã chia sẻ **best practices** trong thiết kế ứng dụng hiện đại.
- Qua các case study thực tế, tôi hiểu rõ hơn cách áp dụng **Domain-Driven Design (DDD)** và **Event-Driven Architecture** vào các project lớn.

#### Trải nghiệm kỹ thuật thực tế

- Tham gia các phiên trình bày về **event storming** giúp tôi hình dung cách **mô hình hóa quy trình kinh doanh** thành các domain events.
- Học cách **phân tách microservices** và xác định **bounded contexts** để quản lý sự phức tạp của hệ thống lớn.
- Hiểu rõ trade-offs giữa **synchronous và asynchronous communication** cũng như các pattern tích hợp như **pub/sub, point-to-point, streaming**.

#### Ứng dụng công cụ hiện đại

- Trực tiếp tìm hiểu về **Amazon Q Developer**, công cụ AI hỗ trợ SDLC từ lập kế hoạch đến maintenance.
- Học cách **tự động hóa code transformation** và pilot serverless với **AWS Lambda**, từ đó nâng cao năng suất phát triển.

#### Kết nối và trao đổi

- Workshop tạo cơ hội trao đổi trực tiếp với các chuyên gia, đồng nghiệp và team business, giúp **nâng cao ngôn ngữ chung (ubiquitous language)** giữa business và tech.
- Qua các ví dụ thực tế, tôi nhận ra tầm quan trọng của **business-first approach**, luôn bắt đầu từ nhu cầu kinh doanh thay vì chỉ tập trung vào công nghệ.

#### Bài học rút ra

- Việc áp dụng DDD và event-driven patterns giúp giảm **coupling**, tăng **scalability** và **resilience** cho hệ thống.
- Chiến lược hiện đại hóa cần **phased approach** và đo lường **ROI**, không nên vội vàng chuyển đổi toàn bộ hệ thống.
- Các công cụ AI như Amazon Q Developer có thể **boost productivity** nếu được tích hợp vào workflow phát triển hiện tại.

#### Một số hình ảnh khi tham gia sự kiện

- Thêm các hình ảnh của các bạn tại đây
  > Tổng thể, sự kiện không chỉ cung cấp kiến thức kỹ thuật mà còn giúp tôi thay đổi cách tư duy về thiết kế ứng dụng, hiện đại hóa hệ thống và phối hợp hiệu quả hơn giữa các team.

