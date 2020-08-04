# Java

## Table of Content
1. [Java Core](#java-core)
2. [Design Patterns](#design-pattern)

#
## Java Core

### There are 4 main principles for OOP:
1. __Encapsulation__
    - Là trạng thái của đối tượng được bảo vệ không cho các truy cập từ code bên ngoài như thay đổi trong thái hay nhìn trực tiếp. Việc cho phép môi trường bên ngoài tác động lên các dữ liệu nội tại của một đối tượng theo cách nào là hoàn toàn tùy thuộc vào người viết mã.
2. __Inheritance__
    - Khả năng cho phép ta xây dựng một lớp mới dựa trên các định nghĩa của một lớp đã có.

3. __Polymorphism__
    - Khi một tác vụ được thực hiện theo nhiều cách khác nhau
    - Trong Java, chúng ta sử dụng nạp chồng phương thức (method overloading) và ghi đè phương thức (method overriding) để có tính đa hình:
        - __Nạp chồng (Overloading)__: Đây là khả năng cho phép một lớp có nhiều thuộc tính, phương thức cùng tên nhưng với các tham số khác nhau về loại cũng như về số lượng.
        - __Ghi đè (Overriding)__: là hai phương thức cùng tên, cùng tham số, cùng kiểu trả về nhưng thằng con viết lại và dùng theo cách của nó, và xuất hiện ở lớp cha và tiếp tục xuất hiện ở lớp con. 
4. __Abstraction__
    - Ẩn các chi tiết trình triển khai và chỉ hiển thị tính năng tới người dùng.
    - Trong Java, chúng là sử dụng __abstract class__ và __abstract interface__ để có tính trừu tượng.

#
## Design Patterns
Hiện tại có 23 mẫu được chia thành 3 nhóm:
1. [Creational Pattern](#creational-pattern): Cung cấp giải pháp để tạo ra object và che giấu đi logic của việc tạo object. Điều này giúp cho chương trình trở nên mềm dẻo trong việc quyết định object nào cần tạo ra trong những tình huống được đưa ra.

2. [Structural Pattern](#structural-pattern): Dùng để thiết lập, định nghĩa mối quan hệ giữa các object.

3. [Behavioral Pattern](#behavioral-pattern): Dùng trong thực hiện các hành vi của object và cách giao tiếp giữa các object.

### Creational Pattern
![](img/creational-patterns.png)

1. __Singleton__
    - Definition: Đảm bảo 1 class chỉ có 1 instance và cung cấp 1 điểm truy xuất toàn cục đến nó.
    ![](img/singleton-example.png)

2. __Factory Method__
    - Definition: Định nghĩa Interface để sinh ra đối tượng nhưng để cho lớp con quyết định lớp nào được dùng để sinh ra đối tượng.
    ![](img/factory-method-diagram.png)

3. __Abstract Factory__
    - Abstract factory như là một nhà máy lớn chứa nhiều nhà máy nhỏ.
    ![](img/abstract-factory-diagram.png)

4. __Builder__
    - Definition: Phân tách việc xây dựng một đối tượng phức tạp ra khỏi thể hiện của nó và sử dụng tiếp cận từng bước, do đó cùng một tiến trình xây dựng có thể tạo ra các biểu diễn khác nhau.

    ![](img/builder-diagram.png)


5. __Prototype__
    - Definition: dùng một đối tượng mẫu, tạo mới nhờ vào sao chép đối tượng mẫu này.

    ![](img/prototype-diagram.png)



### Structural Pattern
![](img/structural-patterns.png)

6. __Adapter__
    - Definition: Do vấn đề tương thích, thay đổi interface của một lớp thành một interface khác phù hợp với yêu cầu người sử dụng lớp.

7. __Bridge__
    - Definition: Tách tính trừu tượng (abstraction) ra khỏi tính hiện thực (implementation) của nó. Từ đó có thể dễ dàng chỉnh sửa hoặc thay thế mà không làm ảnh hưởng đến những nơi có sử dụng lớp ban đầu.
    - Adapter Pattern làm cho mọi thứ có thể hoạt động với nhau sau khi chúng đã được thiết kế (đã tồn tại). Bridge Pattern nên được thiết kế trước khi phát triển hệ thống để Abstraction và Implementation có thể thực hiện một cách độc lập.

    ![](img/bridge-example.png)

8. __Composite__
    - Definition: Tổ chức các đối tượng theo cấu trúc phân cấp dạng cây. Tất cả các đối tượng trong cấu trúc được thao tác theo một cách thuần nhất như nhau.
    - Tạo quan hệ thứ bậc bao gộp giữa các đối tượng. Client có thể xem đối tượng bao gộp và bị bao gộp như nhau -> khả năng tổng quát hoá trong code của client -> dễ phát triển, nâng cấp, bảo trì.

    ![](img/composite-example.png)

9. __Decorator__
    - Definition: Cho phép người dùng thêm chức năng mới vào đối tượng hiện tại mà không muốn ảnh hưởng đến các đối tượng khác.

    ![](img/decorator-example.png)

    - Component (EmployeeComponent): là một interface quy định chung cần có trong tất cả các thành phần tham gia
    - ConcreteComponent (EmployeeConcreteComponent): là lớp implements các phương thức của Component.
    - Decorator (EmployeeDecorator): là một abstract class dùng để duy trì tham chiếu của đối tượng Component và đồng thời implements các phương thức của Component.
    - ConcreteDecorator (TeamMember, TeamLeader, Manager): là lớp extends Decorator, implements các phương thức của Decorator và cài đặt thêm các tính năng mới cho Component.

10. __Facade__
    - Definition: Cung cấp một giao diện chung đơn giản thay cho một nhóm các giao diện có trong subsystem. Facade Pattern định nghĩa một giao diện ở một cấp độ cao cấp hơn để giúp con người dùng có thể dễ dàng sử dụng subsystem.

    ![](img/facade-diagram.png)

11. __Flyweight__
    - Definition: Sử dụng việc chia sẻ để thao tác hiệu quả trên một số lượng lớn đối tượng

12. __Proxy__
    - Definition: Cung cấp đối tượng đại diện cho đối tượng khác để kiểm soát quá trình truy cập đối tượng đó.

    ![](img/proxy-diagram.png)

### Behavioral Pattern
![](img/behavioral-patterns.png)

13. __Chain of Responsibility__
    - Definition: Khắc phục việc ghép cặp giữa bộ gởi và bộ nhận thông điệp. Các đối tượng nhận thông điệp được kết nối thành một chuỗi và thông điệp được chuyển dọc theo chuỗi này đến khi gặp được đối tượng xử lý nó. Tránh việc gắn kết cứng giữa phần tử gởi request với phần tử nhận và xử lý request bằng cách cho phép hơn 1 đối tượng có có cơ hội xử lý request.

    ![](img/chain-of-responsibility-diagram.png)
14. __Command__
    - Definition: Sử dụng Command Object như một class trung gian để lưu trữ các câu lệnh và trạng thái của object tại một thời điểm nào đó. Command Pattern cho phép tất cả những request gửi đến object được lưu trữ trong Command Object.

    ![](img/command-diagram.png)

15. __Iterator__
    - Denifition: Truy xuất các phần tử của đối tượng dạng tập hợp (list, array, ...) mà không phụ thuộc vào biểu diễn bên trong của các phần tử.
    - Cung cấp một cách thức truy cập tuần tự tới các phần tử của một đối tượng tổng hợp, mà không tiết lộ biển diễn bên trong.

    ![](img/iterator-example.png)

    - ConcreteAggregate (Menu): Nó cài đặt interface tạo Iterator để trả về một thể hiện của ConcreteIterator thích hợp.
    - Iterator (ItemIterator): là một interface hay abstract class, định nghĩa các phương thức để truy cập và duyệt qua các phần tử.
    - ConcreteIterator (MenuItemIterator): cài đặt các phương thức của Iterator, giữ index khi duyệt qua các phần tử.

16. __Mediator__
    - Definition: Định nghĩa một đối tượng để bao bọc việc giao tiếp giữa một - nhiều đối tượng với nhau.
    
    ![](img/mediator-example-chat-flow.png)

    ![](img/mediator-example.png)

17. __Memento__
    - Definition: Hiệu chỉnh và trả lại như cũ trạng thái bên trong của đối tượng mà vẫn không vi phạm việc bao bọc dữ liệu.

18. __Observer__
    - Definition: Định nghĩa sự phụ thuộc một hoặc nhiều chiều giữa các đối tượng sao cho khi một đối tượng thay đổi trạng thái thì tất cả các đối tượng phụ thuộc nó cũng thay đổi theo.
    - Observer có thể đăng ký với hệ thống. Khi hệ thống có sự thay đổi, hệ thống sẽ thông báo cho Observer biết. Khi không cần nữa, mẫu Observer sẽ được gỡ khỏi hệ thống.

    ![](img/observer-example.png)

    - Subject : cung cấp các phương thức để thêm, loại bỏ, thông báo observer.
    - AccountService : đóng vai trò là ConcreteSubject, sẽ thông báo tới tất cả các observers bất cứ khi nào có thao tác của người dùng liên quan đến đăng nhập, tài khoản hết hạn.
    - Observer : định nghĩa một phương thức update() cho các đối tượng sẽ được subject thông báo đến khi có sự thay đổi trạng thái.
    - Logger, Mailer và Protector là các ConcreteObserver. Sau khi nhận được thông báo rằng có thao tác với user và gọi tới phương thức update(), các ConcreteObserver sẽ sử dụng dữ liệu SubjectState để xử lý.

19. __State__
    - Definition: Cho phép một đối tượng thay đổi hành vi khi trạng thái bên trong của nó thay đổi.

    ![](img/state-example.png)

20. __Strategy__
    - Definition: Định nghĩa một họ các thuật toán, đóng gói từng thuật toán và hoán đổi sử dụng giữa chúng. Strategy cho phép thuật toán biến đổi độc lập với người dùng.

    ![](img/strategy-example.png)

    - Strategy: định nghĩa hành vi
    - ConcreteStrategy : cài đặt các hành vi cụ thể của Strategy.
    - Context (SortedList): chứa một tham chiếu đến đối tượng Strategy và nhận các yêu cầu từ Client, các yêu cầu này sau đó được ủy quyền cho Strategy thực hiện.

21. __Template method__
    - Definition: Định nghĩa phần khung của một thuật toán gọi đến một số phương thức chưa được cài đặt trong lớp cơ sở; việc cài đặt các phương thức được ủy nhiệm cho các lớp kế thừa.
    
    ![](img/template-method-example.png)

22. __Vistor__
    - Definition: Cho phép định nghĩa thêm phép toán mới tác động lên các phần tử của một cấu trúc đối tượng mà không cần thay đổi các lớp định nghĩa cấu trúc đó.
