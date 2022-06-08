## Hãy viết một đoạn mã Javascript xử lý sự kiện: Khi click vào button nào thì xóa luôn hàng chứa button đó.

## Ý tưởng giải như sau:

Để gán sự kiện cho button nào thì ta thêm đoạn onclick="func_name()" vào button đó. Tuy nhiên, gán kiểu này sẽ không hay lắm, mà ta phải sử dụng DOM Element để lấy danh sách các button, sau đó sử dụng vòng lặp for để lặp qua từng button và sử dụng hàm addEventListener() để thêm sự kiện click.

Vì cấu trúc thẻ HTML là tr -> td -> button nên để xóa hàng chứa button thì ta chỉ việc xóa thẻ cha tr ngoài cùng là được. Để xác định thẻ cha thì ta sử dụng parentElement. Như vậy trong trường hợp này ta phải tìm thẻ cha tr qua hai lần tìm button.parentElement.parentElement.

Cuối cùng chúng ta sử dụng hàm remove() để xóa.