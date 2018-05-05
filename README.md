# Bài tập Trainee Colombo 2018

Thực hiện bởi [Nguyễn Phi Huy](https://github.com/huynhan147)
# ĐỀ BÀI : [Link !](https://docs.google.com/document/d/1yF6Mv-TInH2Ui79lAtJ8W9RWuOKpru-DhR1zUqYio68/edit)

# 1. Phân biệt array vs Object trong JS
- Mảng là một đối tượng đặc biệt với các chỉ mục được đánh số
- Mảng sử dụng các chỉ mục đánh số;
- Object sử dụng các chỉ mục được đặt tên
# 2. Khi nào nên dùng Object và khi nào nên dùng array?
- Sử dụng Object khi muốn tên các phần tử là một chuỗi
- Sử dụng Array khi muốn tên phần tử là một số
# 3. Associative Array là gì? phân biệt so với array thường?
- Associative Array là mảng với các chỉ mục được đặt tên
- Phân biệt so với Array thường 
	+> Mảng: các phần tử được lập chỉ mục bắt đầu bằng số nguyên.
	+> Associative Array : lập chỉ mục bằng các chuỗi  tùy ý. Associative Array có thể sử dụng như các mảng chung chỉ đơn giản bằng cách dử dụng số để lập chỉ mục chúng.
# 4. Có thể thay thế Object bằng Asscociative Array không?
- Có thể thay thế.Vì Object trong js là một Asscociative Array với vô số tính năng đặc biệt
# 5. Đáp án :
7
8
7
# 6 Viết 1 đoạn code nhỏ bằng JS lấy nội dung html  của trang https://www.w3schools.com/html/default.asp
``` 
const puppeteer = require('puppeteer');

puppeteer.launch().then(async browser => {
  const page = await browser.newPage();
  const response = await page.goto('https://www.w3schools.com/html/default.asp');
  console.log(await response.text());
  browser.close();
});
```
# 7.Phân biệt Object trong JS và Object trong PHP ?
- JS : Khởi tạo Object : ` let a = new Object();`
- PHP : Khỏi tạo Object : ```
			$obj1 = new \stdClass;
			$obj3 = (object)[];
			$obj2 = new class{};
			```
- JS : Duyệt OBJ bằng câu lệnh For(key in Object) - Lấy ra lần lượt theo key tăng dần nếu key là số hoặc chuỗi số;
- PHP : Duyệt OBJ bằng câu lệnh Foreach($Object as $key=>$value)- Lấy ra lần lượt theo thứ tự trong Object;
- JS : Object là một Asscociative Array với nhiều tính năng đặc biệt nên có thể truy xuất đến giá trị của thuộc tính trong Object như - truy xuất giá trị của một phần tử trong Asscociative Array : ví dụ : `user['name']; user{name : 'Tun'};`
- PHP : Không thể truy xuất thẳng đến phần tử có key là số .. ví dụ `$Object ->0 (fasle)--`
- JS : Vì js có kiểu dữ liệu underfined nên Khi gọi đến thuộc tính ko có trong Object sẽ trả về giá trị là underfined
- PHP : Lỗi nếu gọi đến thuộc tính ko có trong Object
- JS : `let a = {}; let b = {}  ; a==b (false)`
- PHP : `$a = new StdClass(); $b = new StdClass();   a==b(true)`
- JS : Truy cập thuộc tính đối tượng : `objectName.propertyName` or `objectName["propertyName"]`
- PHP : Truy cập thuộc tính đối tượng `$Object->propertyName`

# 8.PHP Associative Array là gì? phân biệt so với array thường? Cách duyệt Associative array và array thường khác nhau thế nào?
- Mảng  kết hợp (associative array): là loại mảng với chỉ mục là chuỗi, các phần tử trong mảng sẽ được lưu trữ dưới dạng key-value
- Phân biệt : Mảng thường : các chỉ mục là các số nguyên, liên tiếp
		Mảng kết hợp : Chỉ mục là chuỗi hoặc số nguyên do mình gán.
- Cách duyệt Associative array : Không kiểm soát các lần duyệt-- Array thường : có thể kiếm soát các lần duyệt
# 9.
```
<?php
$Object1 = (Object)[
    'age'=> 18,
    'name'=>'huy',
];
$Object2 = (Object)[
    'age'=> 16,
    'name'=>'nam',
];
$Object3 = (Object)[
    'age'=> 21,
    'name'=>'lan',
];
$arr = [
$Object1,$Object2,$Object3
];
usort($arr,function($first,$second){
    return $first->age > $second->age;
});
echo '<pre>';
print_r($arr);
 ?>
```
# 10.Phân biệt 3 loại link list? Nêu thử 1 ứng dụng của circula link list
- Danh sách liên kết đơn (Simple Linked List): chỉ duyệt các phần tử theo chiều về trước.
- Danh sách liên kết đôi (Doubly Linked List): các phần tử có thể được duyệt theo chiều về trước hoặc về sau.
- Danh sách liên kết vòng (Circular Linked List): phần tử cuối cùng chứa link của phần tử đầu tiên như là next và phần tử đầu tiên có link tới phần tử cuối cùng như là prev
- Ứng dụng : dùng danh sách liên kết vòng để theo dõi lượt của ai trong trò chơi theo lượt.
# 11.Phân biệt link list - array (nếu ưu của link list và array)
* Mảng : 
	  - Là tập hợp các phần tử có cùng kiểu dữ liệu với tên chung
	 - Trong mảng, các phần tử có thể được truy cập bằng cách sử dụng giá trị chỉ mục/chỉ số, tức là các phần tử có thể được truy cập ngẫu nhiên
	 - Trong mảng, các phần tử được lưu trữ liên tục trong bộ nhớ
	 - Chèn và xóa mất nhiều thời gian hơn vì các phần tử được lưu trữ trong các vị trí bộ nhớ liên tiếp
	 - Trong mảng, bộ nhớ được cấp phát tại thời gian biên dịch, tức là phân bổ bộ nhớ tĩnh 
	 - Mảng có thể là một chiều, hai chiều hoặc đa chiều
	 - Trong mảng, mỗi phần tử độc lập, không có kết nối với phần tử trước đó hoặc với vị trí của nó
	 - Trong mảng, không có con trỏ nào được sử dụng như danh sách liên kết, do đó không cần thêm bộ nhớ cho con trỏ
* Danh sách liên kết : 
	- Là tập hợp các phần tử được sắp xếp được kết nối bởi các liên kết/ con trỏ
	- Trong danh sách liên kết, các phần tử không thể được truy cập ngẫu nhiên nhưng có thể được truy cập chỉ theo tuần tự và phần tử truy cập mất O(n) lần
	- Các phần tử có thể được lưu trữ tại bất kỳ nơi nào có sẵn vì địa chỉ của nút được lưu trữ trong nút trước đó.
	- Chèn và xóa nhanh chóng và dễ dàng trong danh sách liên kết vì chỉ có giá trị của con trỏ là cần thiết để thay đổi
	- Bộ nhớ được cấp phát tại thời gian chạy tức là phần bổ bộ nhớ động
	- Danh sách liên kết có thể là danh sách liên kết đơn, đôi và vòng
	- Vị trí hoặc địa chỉ của các phần tử được lưu trữ trong phần liên kết của phần tử/ nút trước đó
	- Sự kề nhau giữa các phần tử được duy trì bằng cách sử dụng con trỏ hoặc các liên kết, do đó các con trỏ được sử dụng và cần thêm không gian bộ nhớ.
# 12. Khác nhau cơ bản giữa stack và queue? 1 ví dụ ứng dụng trong thực tế.
* Stack : 
	 - Các đối tượng được chèn vào và gỡ bỏ ở cùng một đầu
	 - Chỉ có 1 con trỏ được sử dụng. Nó chỉ lên trên cùng của ngăn xếp
	 - Thứ tự Last In First Out
	 - Các hoạt động trong ngăn xếp được gọi là push và pop
	 - Ngăn xếp được hiển thị dưới dạng dọc
	 - Ví dụ thực tế : Những cái đĩa khi được xếp vào nhau..
* Queue : 
         - Các đối tượng được chèn và loại bỏ khỏi các đầu khác nhau.ư
	 - Hai con trỏ khác nhau được sử dụng cho các đầu phía trước và phía sau
	 - Trong hàng đợi, đối tượng được chèn đầu tiên trước tiên sẽ bị xóa.
	 - Thứ tự First In First Out
	 - Các hoạt động trong ngăn xếp được gọi là enqueue và dequeue
	 - Hàng đợi được hiển thị dưới dạng ngang
	 - Ví dụ thực tế : Mọi người xếp hàng lên xe bus



