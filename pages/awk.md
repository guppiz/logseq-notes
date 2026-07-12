- nguyên tắc hoạt động: đọc từng dòng - tách cột - kiểm tra điều kiện - thực hiện hành động
- cấu trúc cơ bản
  `awk 'điều kiện {hành động}' tên file`
- các biến đặc biệt
	- `$0`: toàn bộ dòng hiện tại
	- `$1`, `$2`, ...: cột 1, cột 2, ...
	- `NF` (nunber of fields): số lượng cột của dòng đó
	- `NR` (number of row): số thứ tự của dòng đang đọc
	- **in log theo dạng dễ nhìn**
	  `awk '{printf "%-22s | %-3s | %-5s | %-15s | %-15s\n", $1, $4, $7, $9, $12}' proxy-host-7_access.log | head -n 10`
	- **liệt kê các cột của dòng đầu tiên**
	  `awk 'NR==1 {for (i=1; i<=NF; i++) printf "Cột %-2d: %s\n", i, $i}' proxy-host-7_access.log`
	  **Giải thích lệnh:**
	  **`NR==1`**: Chỉ thực hiện với dòng đầu tiên (Number of Record = 1).
	  **`for (i=1; i<=NF; i++)`**: Chạy một vòng lặp từ cột thứ nhất đến cột cuối cùng (`NF` là biến chứa tổng số cột của dòng đó).
	  **`printf "Cột %-2d: %s\n", i, $i`**: In ra số thứ tự cột (`i`) và nội dung của cột đó (`$i`).