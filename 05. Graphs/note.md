- Graph: Một Node (Đỉnh) có thể được kết nối (thông qua Cạnh) với nhiều Node khác. Kết nối 2 chiều, vòng lặp là khả dụng. Không tồn tại khái niệm "Level", "Nesting", "Child/Parent"
- 2 loại Graph: Directed Graph (Cạnh giữa các Node là 1 chiều) và Undirected Graph (Cạnh giữa các Node là 2 chiều)
- Ví dụ: Social Network Contact (Undirected Graph), Dependency (Directed Graph),...

- Biểu diễn Graph trong Code: Adjacency Matrix (Ma trận kề), Adjacency List (Danh sách kề)

- Adjacency Matrix và Adjacency List chỉ thể hiện liên kết giữa các Node. Giá trị của các Node có thể được lưu trữ riêng biệt

- Graph "addNode": Thêm Value và Identifier tương ứng cho Node mới
- Graph "addEdge": Thêm Start Node và End Node tương ứng cho liên kết mới
- Graph "removeNode": Xóa Node và loại bỏ các liên kết tương ứng
- Graph "removeEdge": Loại bỏ các liên kết giữa 2 Node xác định (nếu tồn tại)
- Graph "hasEdge": Kiểm tra liên kết giữa 2 Node xác định có tồn tại không
- Graph "getAllEdges": Trả về tất cả liên kết giữa 2 Node xác định
