- List: Collection of Value (Array, Set, LinkedList). Tối ưu để lưu trữ những giá trị được lấy bằng position và lặp
- Table: Collection of Key-Value Pair (Object, Map). Tối ưu để lưu trữ những giá trị được lấy bằng Key và không tập trung vào lặp

- Stack: LIFO - Last In First Out
- Stack "push": Thêm phần tử vào đỉnh Stack
- Stack "pop": Xóa phần tử ở đỉnh Stack
- Stack "isEmpty": Kiểm tra số phần tử trong Stack có bằng 0 hay không
- Stack "toArray": Trả về các phần tử có trong Stack dưới dạng Array

- Sử dụng Stack để giới hạn thao tác với Array (chỉ có thể push và pop)

- Queue: FIFO - First in First Out
- Queue "enqueue": Thêm phần tử vào đầu Queue
- Queue "dequeue": Xóa phần tử ở cuối Queue
- Queue "isEmpty": Kiểm tra số phần tử trong Queue có bằng 0 hay không
- Queue "toArray": Trả về các phần tử có trong Queue dưới dạng Array

- Sử dụng Queue để giới hạn thao tác với Array (chỉ có thể enqueue và dequeue). Nếu được triển khai đúng cách, Queue tối ưu hơn Array trong chèn dữ liệu vào đầu danh sách

- JS 'object' bản chất là một Hash Table
- Bản chất của Hash Table trong JS là một Array
- Với mỗi Input (Key Name), Hash Function luôn trả về một Output (Index)

- Thuật toán tìm kí tự lặp lại đầu tiên với Hash Table

- Không sử dụng String làm Key vì:

* Đa phần các ngôn ngữ lập trình chỉ cho phép sử dụng Integer làm Index cho Array
* Sử dụng String do User khởi tạo làm Key dẫn tới phân bố dữ liệu không đồng đều, không tận dụng được tối đa tài nguyên, thậm chí gây lãng phí tài nguyên => Không hiệu quả

- Collision: Khi nhiều hơn 1 Key được Hash thành cùng 1 Index

- Hash Table "set": Thêm cặp Key-Value vào Hash Table
- Hash Table "get": Lấy ra cặp Key-Value từ Hash Table

- Giải quyết Collision với Chaining: Lưu trữ nhiều Value (và Key tương ứng) tại cùng Index được Hash từ các Key khác nhau
- Giải quyết Collision với Open Addressing: Nếu nhiều hơn 1 Key được Hash thành cùng 1 Index, Value của các Key tiếp theo sẽ được lưu trữ tại Index trống tiếp theo (có nhiều cách tìm Index trống tiếp theo: tăng Index 1 đơn vị cho tới khi tìm thấy Index trống,...). Có thể thất bại nếu không đủ không gian lưu trữ Value, cần không gian lưu trữ lớn và giải phóng lưu trữ đối với những Value không được sử dụng

- Không nên dùng Object trong mọi trường hợp, thay thế Array,...
