- Sắp xếp chèn (Insertion Sort):
Ý tưởng: Thuật toán này lấy cảm hứng từ việc chơi bài, khi người chơi “chèn” thêm một quân bài mới vào bộ bài đã được sắp xếp trên tay.
Cách hoạt động: Tại bước thứ k, đưa phần tử thứ k trong mảng vào đúng vị trí trong dãy gồm k phần tử đầu tiên.
Đánh giá:
Trường hợp tốt nhất: 0 hoán đổi, n-1 so sánh (khi dãy đầu vào đã được sắp).
Trường hợp xấu nhất: n^2/2 hoán đổi và so sánh (khi dãy đầu vào có thứ tự ngược lại với thứ tự cần sắp xếp).
```cpp
void insertionSort(int arr[], int n) {
    for (int i = 1; i < n; i++) {
        int key = arr[i];
        int j = i - 1;
        while (j >= 0 && arr[j] > key) {
            arr[j + 1] = arr[j];
            j--;
        }
        arr[j + 1] = key;
    }
}
```
- Sắp xếp lựa chọn (Selection Sort):
Ý tưởng: Tìm từng phần tử cho mỗi vị trí của mảng hoán vị A’.
Cách hoạt động: Tìm phần tử nhỏ nhất và đưa vào vị trí thích hợp.
Đánh giá:
Trường hợp tốt nhất: 0 đổi chỗ (n-1 so sánh).
Trường hợp xấu nhất: n-1 đổi chỗ và n^2/2 so sánh.
- Sắp xếp nổi bọt (Bubble Sort):
Ý tưởng: Đẩy phần tử lớn nhất xuống cuối dãy, dịch chuyển phần tử nhỏ hơn về đầu dãy.
Đánh giá:
Trường hợp tốt nhất: O(n) đổi chỗ và n^2/2 so sánh.
Trường hợp xấu nhất: O(n^2) đổi chỗ và so sánh.
- Merge Sort (Sắp xếp trộn):
Ý tưởng: Merge Sort là thuật toán chia để trị dựa trên việc chia một danh sách thành các danh sách con cho đến khi mỗi danh sách con chỉ chứa một phần tử. Sau đó, chúng ta sẽ gộp các danh sách con này sao cho danh sách kết quả được sắp xếp.
Cách hoạt động:
Chia danh sách thành các danh sách con chứa từng phần tử.
Gộp các cặp danh sách con “đơn” (chỉ chứa một phần tử) để tạo danh sách có 2 phần tử.
Lặp lại các bước trên cho đến khi có danh sách hoàn toàn đã sắp xếp.
Đánh giá:
Trường hợp tốt nhất, trung bình và xấu nhất: O(n log n), không phụ thuộc vào phân phối dữ liệu.
```python
def selection_sort(arr):
    n = len(arr)
    for i in range(n - 1):
        min_index = i
        for j in range(i + 1, n):
            if arr[j] < arr[min_index]:
                min_index = j
        arr[i], arr[min_index] = arr[min_index], arr[i]

# Ví dụ sử dụng
my_array = [64, 25, 12, 22, 11]
selection_sort(my_array)
print("Mảng sau khi sắp xếp theo thứ tự tăng dần:")
print(my_array)  # Kết quả: [11, 12, 22, 25, 64]

```
- Quick Sort (Sắp xếp nhanh):
Ý tưởng: Quick Sort sử dụng phân chia và sắp xếp các phần tử trong mảng dựa trên một pivot được chọn.
Cách hoạt động:
Phân chia mảng thành các phần tử nhỏ hơn và lớn hơn pivot.
Đệ quy sắp xếp các phần tử nhỏ hơn và lớn hơn pivot.
Kết hợp các phần tử đã sắp xếp để tạo mảng hoàn chỉnh.
Đánh giá:
Thời gian tốt nhất, trung bình và xấu nhất: O(n log n) với lựa chọn ngẫu nhiên của pivot.
```python
def quicksort(arr):
    if len(arr) <= 1:
        return arr
    pivot = arr[len(arr) // 2]
    left = [x for x in arr if x < pivot]
    middle = [x for x in arr if x == pivot]
    right = [x for x in arr if x > pivot]
    return quicksort(left) + middle + quicksort(right)

myArray = [3, 7, 2, 5, 1, 4, 6, 8]
sortedArray = quicksort(myArray)
print(sortedArray)  # Output: [1, 2, 3, 4, 5, 6, 7, 8]

```
- Heap Sort (Sắp xếp Heap):
Ý tưởng: Heap Sort sử dụng cây heap (max-heap hoặc min-heap) để sắp xếp dãy số.
Cách hoạt động:
Xây dựng max-heap hoặc min-heap từ dãy số.
Lấy phần tử gốc (max hoặc min) ra khỏi heap và thêm vào danh sách kết quả.
Lặp lại bước trên cho đến khi heap trống.
Đánh giá:
Thời gian tốt nhất, trung bình và xấu nhất: O(n log n), không phụ thuộc vào phân phối dữ liệu