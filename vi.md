# Lý do sử dụng thiết kế mẫu  
## Giới thiệu  
Nối tiếp những bài báo trước với tựa đề [Tại sao thiết kế là quan trọng để phát triển phần mềm](https://www.codeproject.com/Tips/806867/Why-Design-is-Critical-to-Software-Development), tôi muốn giải quyết một khía cạnh nâng cao hơn của thiết kế phần mềm gọi là `các mẫu thiết kế`. Như ở bài báo trước của tôi, ý tưởng xuất phát từ một cuộc thảo luận về mức độ quan trọng của thiết kế phần mềm với việc làm việc chung với đồng nghiệp. Nhân vật chính của cuộc thảo luận là quan điểm rằng `các mẫu thiết kế ` quá mất thời gian để sử dụng bên trong mảng phát triển phần mềm thương mại. Ý định của tôi ở đây là để chứng minh rằng tại sao tôi tin nó là sai.  
Tôi sẽ không đề cập đến bất cứ chi tiết nào cơ học hay việc thực hiện của bất cứ cụ thể nào của `các mẫu thiết kế` . Có quá nhiều nguồn đáng tin có sẵn ở khắp nơi.  

## Mẫu thiết kế là gì?  
Hãy bắt đầu với `mẫu thiết kế ` chính xác là gì? Ở đây có cặp định nghĩa cho thuật ngữ này:  
Trích từ [Wikipedia](https://en.wikipedia.org/wiki/Design_pattern):  
```
	"Mẫu thiết kế trong kiến trúc và khoa học máy tính là cách ghi chép chính thức cách giải quyết cho vấn đề thiết kế trong khía cạnh chuyên môn."
```  
Trích từ [Data & Object Factory](http://www.dofactory.com/net/design-patterns):  
```
	"Mẫu thiết kế là cách giải quyết định kì cho vấn đề thiết kế phần mềm mà bạn luôn tìm kiếm trong việc phát triển ứng dụng thực tế. Mẫu đề cập về thiết kế và sự tương tác đối tượng, cũng như cung cấp nền tảng giao tiếp liên quan đến sự trong sáng, những giải pháp có thể tái sử dụng để lập trình các vấn đề thường gặp."
```  

## Tài liệu tốt và dễ hiểu  
Giống như `mẫu thiết kế ` là một tài liệu tốt và dễ hiểu được viết bởi các kĩ sư phần mềm, nhà thiết kế và những nhà phát triển, thì ứng dụng của họ bên trong các cách giải quyết riêng sẽ cũng trở nên dễ hiểu.  
`mẫu thiết kế ` cho phép người phát triển phần mềm để thử và kiểm tra các cách giải quyết vấn đề chung, do vậy giảm bớt rủi ro kĩ thuật để các dự án không phải thử những thiết kế mới và chưa được kiểm thử.  

`mẫu thiết kế ` có thể ban đầu không giảm thời gian phát triển, vì vậy nó là đường vòng nếu nhóm không quen với nó. Tuy nhiên, nếu nhìn xuống sâu hơn luồng phát triển, sẽ trở nên quen thuộc hơn, thời gian phát triển sẽ dần dần được giảm.  

## Sự gần gũi với kĩ thuật phổ thông  
Để đưa ra sự tương đồng của `mẫu thiết kế ` từ lĩnh vực của kĩ thuật phổ thông (thứ mà tôi đã bắt đầu trong bài báo [Tại sao thiết kế là quan trọng để phát triển phần mềm](https://www.codeproject.com/Tips/806867/Why-Design-is-Critical-to-Software-Development) của tôi có nhiều điểm tương đồng với kĩ thuật phần mềm), sẽ là cách suy nghĩ cho giải quyết băng qua con sông. Nó là vấn đề định kì cho kĩ thuật phổ thông, là một cặp tài liệu tốt và cách giải quyết dễ hiểu. Kĩ thuật phổ thông có thể xây dựng một cây cầu hay đường hầm.  

Tại sao các kĩ sư phổ thông cố gắng để giải quyết vấn đề này khi mà những cách giải quyết thực tế có thể gọi tới? Có nhiều sự tương đồng giữa việc kĩ sư phổ thông giải quyết vấn đề dòng sông, và cách sắp xếp các vấn đề riêng của họ.  
* Các cách giải quyết (bắc cầu hay đường hầm) bao gồm cả việc dễ hiểu ngầm và dẫn chứng tốt.  
* Các cách giải quyết (bắc cầu hay đường hầm) giải quyết định kì vấn đề kĩ thuật phổ thông.  
* Các cách giải quyết (bắc cầu hay đường hầm xây dựng nguyên liệu để các ví dụ có thể được lựa chọn định hướng cụ thể)   

Cuộc tranh luận xoay quanh `mẫu thiết kế ` rằng chúng không thích hợp với mục đích thương mại do họ mất quá nhiều thời gian để phát triển nó là không giữ được. `mẫu thiết kế ` tiết kiệm thời gian (khi mà đã xem tổng quan vòng đời của ứng dụng) với việc giúp cho nhà phát triển những lựa chọn để thử và kiểm tra cách giải quyết những thứ mà họ có thể ghép với những thứ họ cần.  

Chỉ có một vấn đề tôi đã gặp với `mẫu thiết kế ` là họ mất quá nhiều thời gian để học. Một vài trong số đó có thể khó khăn để hiểu và nắm vững. Đó là một lời phế bình hợp lý, và vì vậy nó yêu cầu nhiều kĩ năng của người phát triển để sử dụng. Điều này có thể làm tăng chi phí ban đầu của dự án. Tuy nhiên, khi nhìn tổng quan về vòng đời của ứng dụng, tôi đã hết sức kì vọng rằng chi phí phát triển ban đầu sẽ được thu lại bằng chi phí duy trì do tính dễ bao quát và mở rộng hơn (giúp cho ứng dụng dễ phát triển hơn trong tương lai nếu có những cơ hội mới).  

`mẫu thiết kế ` giảm sự phức tạp, và do vậy cách giải quyết trở nên dễ hiểu hơn.  

`mẫu thiết kế ` là giải pháp đã được thử và kiểm tra, nhà phát triển không cần bắt đầu từ những lỗi nhỏ, có thể bắt đầu ngay với các cách giải quyết đã được kiểm chứng trong công việc (miễn là `mẫu thiết kế ` có thể được sử dụng để giải quyết vấn đề chung). It would be wrong to expect a bridge to solve the problem of crossing an ocean, where a bridge would simply be unsuitable.  

## Lợi ích của việc sử dụng các mẫu thiết kế  
`mẫu thiết kế ` cung cấp những lợi ích dưới đây:  
1. Nó mang lại cho các nhà phát triển sự lựa chọn các giải pháp thử nghiệm để làm việc.  
2. Nó là ngôn ngữ trung lập do vậy bạn có thể áp dụng vào bất cứ ngôn ngữ nào hộ trợ hướng đối tượng.  
3. Nó hỗ trợ giao tiếp tốt đến nỗi mà nó được tài liệu tốt và có thể được nghiên cứu nếu nó không phải trường hợp bạn cần.  
4. Nó có ghi lại cái theo dõi kiểm chứng khi được sử dụng rộng rãi và vì thế giảm thiểu rủi ro công nghệ trong dự án.  
5. Nó rất linh hoạt và có thể sư dụng thực tế trong bất kỳ loại ứng dụng hoặc tên miền nào  

## Kết luận  
`mẫu thiết kế `, mặc dù ban đầu họ học theo đường vòng, là một sự đầu tư rất đáng giá. Nó sẽ cho phép bạn triển khai các giải pháp đã được thử và kiểm tra cho vấn đề, do đó tiết kiệm thời gian và sự nỗ lực trong suốt thời gian phát triển phần mềm. Bằng việc sử dụng những giải pháp dễ hiểu và tài liệu tốt, sản phẩm cuối cùng sẽ có mức độ hiểu cao hơn. Nếu cách giải quyết dễ dàng để hiểu, sau đó bởi cách mở rộng, nó cũng sẽ dễ dàng để duy trì.  

## Thực hành  
* https://coderoncode.com/design-patterns/programming/php/coding/development/2014/01/19/design-patterns-php-factories.html  
* https://www.binpress.com/tutorial/the-factory-design-pattern-explained-by-example/142  
* https://www.codeproject.com/Articles/852232/PHP-Singleton-Pattern-A-Step-by-Step-And-Problem-s  
* http://www.fluffycat.com/PHP-Design-Patterns/  