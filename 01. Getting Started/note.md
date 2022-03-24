- Ordered: Không có nghĩa là các phần tử được sắp xếp theo giá trị tăng dần hay giảm dần, mà nghĩa là thứ tự chèn (vị trí của phần tử) được lưu trữ

- JS cho phép mix kiểu dữ liệu trong Array
- Xóa và tìm kiếm phần tử có thể yêu cầu "extra work"

- Iterable (có thể sử dụng for-of loop)

- Thứ tự chèn trong Set không được đảm bảo
- Có thể truyền Array làm tham số khởi tạo cho Set: new Set([1, 2, 3])
- JS cho phép mix kiểu dữ liệu trong Set

- Nếu có nhiều hơn cùng một Key trong Object, Value của Key đó sẽ bị ghi đè
- Có thể tạo Property mới "on the fly" (object.newProp = 'new Property')

- Key của Map có thể nhận bất kì giá trị nào (bao gồm những giá trị tham chiếu như Object, Array,...)
- Map lưu trữ dữ liệu thuần túy (có thể lưu Function trong Map, nhưng không thể thực thi như với Object), tối ưu hóa cho truy cập dữ liệu
- Mỗi cặp Key-Value trong Map được lưu trữ dưới dạng Array ([Key, Value])

- Set và Map được tối ưu hóa cho lưu trữ và truy cập dữ liệu

- WeakSet & WeakMap: Biến thể của Set và Map. Value và Key chỉ được "weakly referenced" (Key và Value có thể bị xóa nếu không được sử dụng)

- Linked List: Hiệu quả với re-sizing và chèn ở đầu và cuối List

- Linked List "append": Tail trỏ sang giá trị mới được chèn
- Linked List "prepend": Head trỏ sang giá trị mới được chèn, Next của giá trị mới được chèn trỏ sang Head (cũ)
- Linked List "toArray": "Loop" qua tất cả các Node và đưa giá trị của mỗi Node vào Array
- Linked List "delete": Next tại Node trước Node mang giá trị cần xóa trỏ sang Node sau Node mang giá trị cần xóa
- Linked List "find": "Loop" qua tất cả các Node cho tới khi tìm thấy Node đầu tiên chứa giá trị cần tìm
- Linked List "insertAfter": Tail của Node trước Node cần chèn trỏ tới Node cần chèn; Tail của Node cần chèn trỏ tới Node sau Node cần chèn

- Linked List có ưu thế trong quản lý bộ nhớ và chèn dữ liệu vào đầu danh sách
