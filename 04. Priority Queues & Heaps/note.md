- Priority Queue: Ưu tiên Item trong Queue, thay vì xử lí lần lượt (với độ ưu tiên ngang nhau) (phần tử có độ ưu tiên cao hơn sẽ được xử lý trước)

- Priority Queue "insert": Phần tử mới được chèn vào vị trí có độ ưu tiên tương ứng
- Priority Queue "process": Loại bỏ phần tử có độ ưu tiên cao nhất

- Heap: Array mô tả cấu trúc của một Binary Tree, các phần tử sau là Child của phần tử trước (Binary Heap). Các phần tử Child luôn nhỏ hơn (hoặc lớn hơn phần tử Parent, tùy thuộc vào Max Heap hay Min Heap). Index của Parent và Child liên hệ với nhau qua công thức parentIndex = Math.floor((childIndex + 1) / 2) - 1, leftChildIndex = 2 _ parentIndex + 1, rightChildIndex = 2 _ parentIndex + 2

- Heap "insert": So sánh giá trị của phần tử cần chèn với giá trị của Parent để tìm vị trí phù hợp (swap với Parent) (đảm bảo luôn nhỏ hơn (hoặc lớn hơn) Parent và lớn hơn (hoặc nhỏ hơn) Child)

- Heap "process": Loại bỏ phần tử đầu tiên trong Array (phân tử lớn nhất hoặc nhỏ nhất, tùy thuộc vào Max Heap hay Min Heap). Chọn 1 phần tử ngẫu nhiên làm phần tử đầu tiên. So sánh giá trị của Parent với giá trị của Child để tìm vị trí phù hợp (swap với Child) cho tới khi Heap thỏa mãn điều kiện của Max Heap hoặc Min Heap

- Heap tối ưu khi muốn truy cập phần tử lớn nhất hoặc nhỏ nhất, không quan tâm thứ tự của các phần tử còn lại
- Priority Queue triển khai bằng Heap tối ưu hơn
