- Degree: Số Child Node của một Node cho trước
- Level: Khoảng cách giữa một Node và Root Node
- Size: Tổng số Node trong một Tree

- Tree "add": Thêm Node theo một Path đã xác định (Node chưa tồn tại trên Path sẽ được tạo thêm)
- Tree "remove": Xóa Node (bao gồm toàn bộ Sub Tree, Child,...) theo một Path đã xác định (Node chưa tồn tại trên Path sẽ báo lỗi)
- Tree "find": Depth-First hoặc Breath-First

- Depth-First: Duyệt hết độ sâu của một Path rồi mới tới Sibling
- Breath-First: Duyệt hết Sibling ở từng Level

- Depth-First hay Breath-First: Tùy thuộc vào cách tổ chức dữ liệu, loại dữ liệu Tree đại diện và tình huống cụ thể mà một trong hai giải thuật có thể trả về kết quả tìm kiếm sớm hơn giải thuật còn lại

- Binary Search Tree (A Tree for Sorted Data): Mỗi Node có tối đa 2 Child; Left Child Node nhỏ hơn Parent Node, Right Child Node lớn hơn Parent Node

- Binary Search Tree "add": Giá trị của Node cần chèn nhỏ hơn Parent Node => Left Child Node. Giá trị của Node cần chèn lớn hơn Parent Node => Right Child Node. Giá trị của Node cần chèn bằng Parent Node => Do Nothing
- Binary Search Tree "find": Giá trị cần tìm nhỏ hơn Value của Node hiện tại => Tìm kiếm trong Left Sub Tree. Giá trị cần tìm lớn hơn Value của Node hiện tại => Tìm kiếm trong Right Sub Tree. Lặp lại cho tới khi tìm thấy Node mang giá trị cần tìm hoặc khi đã lặp qua tất cả Node
- Binary Search Tree "remove" (Leaf Node): Xóa bỏ liên kết giữa Parent Node và Leaf Node cần xóa
- Binary Search Tree "remove" ("One-Child" Node): Thay thế Node cần xóa bằng Child Node của nó (Left Child Node hoặc Right Child Node)
- Binary Search Tree "remove" ("Multi-Child" Node): Nếu tồn tại Left Child Node trong Right Sub Tree, thay thế Node cần xóa. Nếu không tồn tại, thay thế Node cần xóa bằng Right Child Node trong Right Sub Tree

- AVL (Georgy Adelson-Velsky Evgenii Landis) Tree: Binary Search Tree có chêch lệch độ sâu lớn nhất giữa các Sub Tree nhỏ hơn hoặc tối đa bằng 1 (AVL fix Binary Search Tree Worst Case thông qua Balancing)

- Cân bằng AVL Tree (4 trường hợp): Left Rotation, Right Rotation, Left-Right Rotation, Right-Left Rotation

- Balance Factor: Chênh lệch độ sâu Sub Tree (left - right)

- Nếu Binary Search Tree có cấu trúc lệch (Worst Case), sử dụng AVL Tree là lựa chọn hợp lý (giảm độ phức tạp thời gian từ O(n) xuống O(log n)). Nếu dữ liệu phân bố đều, dùng AVL Tree có thể tiêu tốn tài nguyên hơn

- Trie: Root Node mang giá trị rỗng. Root Node bao gồm Slot cho các Child Node (mang giá trị rỗng) đại diện cho các kí tự trong bảng chữ cái (sắp xếp theo thứ tự bảng chữ cái). Mỗi Child Node lại có cấu trúc tương tự như Root Node. Đến một độ sâu nhất định nào đó Child Node sẽ mang một giá trị (chỉ các Node cần thiết trên Path tới Node lưu trữ giá trị mới thực sự được tạo)
- Trie được sử dụng để lưu trữ các cặp Key-Value trong Tree (tương tự Hash Table)

- Trie "insert": Lặp qua hết các kí tự của Key và tạo Node tương ứng với mỗi kí tự (nếu Node chứa kí tự ở chính xác vị trí đó chưa tồn tại). Lưu giá trị ở Node tương ứng với kí tự cuối cùng

- Trie "find": Lặp qua hết các kí tự của Key cho tới Node tương ứng với kí tự cuối cùng. Giá trị của Node đó chính là Value của Key

- Trie "remove": Không xóa tất cả các Node tương ứng với tất cả kí tự mà chỉ loại bỏ giá trị của Node tương ứng với kí tự cuối cùng của Key cần xóa Value. Nếu lựa chọn xóa Node tương ứng với kí tự cuối cùng, cần xem xét Child của Node đó vì chỉ nên xóa Leaf Node

- Sử dụng Trie khi cần sự đơn giản
- Có thể ứng dụng Trie vào gợi ý kết quả tìm kiếm
- Trie có độ phức tạp không gian lớn hơn Hash Table
