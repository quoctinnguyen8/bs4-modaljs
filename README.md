# Bootstrap4 Modal library

Thư viện hỗ trợ làm việc với modal trong BS4

## Sử dụng cơ bản

Nhúng thư viện, yêu cầu jQuery & Bootstrap 4.x

```xml
<script src="https://code.jquery.com/jquery-3.5.1.min.js"></script>
<script src="https://cdn.jsdelivr.net/npm/popper.js@1.16.1/dist/umd/popper.min.js"></script>
<script src="https://cdn.jsdelivr.net/npm/bootstrap@4.6.0/dist/js/bootstrap.min.js"></script>

<script src="modal.js"></script>
```

Tạo đối tượng modal

```javascript
// Tạo modal có id="myModal" và tiêu đề là 'Hello world'
var modal = new Modal('myModal','Hello world!');
```

Hiển thị modal

```javascript
modal.show();
```

Ẩn modal

```javascript
modal.hide();
```

## Các phương thức & thuộc tính

### Phương thức

#### 1. `show()`

Hiện modal đã được khởi tạo trước đó

#### 2. `hide()`

Ẩn modal đã được khởi tạo/hiện trước đó

#### 3. `setTitle(title)`

`title : string`

Đặt lại tiêu đề của modal

#### 4. `appendBody(args)`

`args : any`

**Thêm** nội dung cho modal body, tham số có thể là text, element hoặc jQuery element

#### 5. `clearBody()`

Xóa tất cả phần tử ra khỏi modal body

#### 6. `toggle()`

Ẩn/hiện modal tùy vào trạng thái của nó

#### 7. `setOption(backdrop, keyboard)`

`backdrop : string | boolean`

`keyboard : boolean`

Cài đặt tùy chỉnh cho modal,`backdrop` điều chỉnh background của modal, có thể là `true`/`false`/`'static'`;  `keyboard`cho phép nhấn phím **Esc** để ẩn modal, có thể là`true`/`false`

#### 8. `resetOptions()`

Reset cài đặt liên quan đến backdrop, keyboard về trạng thái mặc định ban đầu

#### 9. `useBoxShadow(status)`

`status : None | boolean`

Quy định việc sử dụng`box-shadow` trong trường hợp `backdrop` ở hàm `setOption` được đặt là `false`. Không truyền tham số hoặc tham số `true` đều có nghĩa là sử dụng `box-shadow`, `false` được hiểu là không dùng

#### 10. `useNormalSize()`

Sử dụng modal với kích thước mặc định

#### 11. `useSmallSize()`

Sử dụng modal với kích thước nhỏ

#### 12. `useLargeSize()`

Sử dụng modal với kích thước lớn

#### 13. `useFullScreenSize()`

Sử dụng modal với kích thước toàn màn hình

#### 14. `useButtonOnTheLeft()`

Đặt các button ở footer về phía bên trái modal

#### 15. `setFooterButton(args)`

`args : ModalButton | Array of ModalButton`

Thêm các button vào modal footer, bao gồm cả event của các button đó

#### 16. `setDefaultFooterButton(primaryText, secondaryText, primaryEvent)`

`primaryText : String`

`secondaryText : String`

`primaryEvent : Function | None`

Thêm **02** button vào modal footer với text chỉ định. Event của button phụ (secondary) luôn luôn là đóng modal

#### 17. `addPrimaryButtonEvent(evType, evCallback)` hoặc `addPrimaryButtonEvent(evCallback)`

`evType : String`

`evCallback : Function`

Chỉ định event cho button primary, dùng kèm với hàm **16. `setDefaultFooterButton(...)`** trong trường hợp event của button primary chưa được chỉ định

#### 18. `afterShow(callBack)`

Thêm sự kiện after-show cho modal, sự kiện được kích hoạt sau khi gọi hàm `show()`

#### 19. `afterHide(callBack)`

Thêm sự kiện after-hide cho modal, sự kiện được kích hoạt sau khi gọi hàm `hide()`

---

### Thuộc tính

#### 1. `name : String`

Tên modal, đồng thời cũng là id của modal

#### 2. `hideShowingModals : Boolean`

Cho phép ẩn tất cả modal khác đang show trên màn hình khi modal này được show ra, giá trị mặc định là `false`

#### 3. `modal : jQuery Element`

Modal gốc hiện tại

#### 4. `modalTitle : jQuery Element`

Thẻ chứa tiêu đề của modal

#### 5. `modalBody : jQuery Element`

Thẻ modal-body

#### 6. `modalFooter : jQuery Element`

Thẻ modal-footer

#### 7. `modalDialog : jQuery Element`

Thẻ modal-dialog

#### 8. `modalContent : jQuery Element`

Thẻ modal-content

#### 9. `hideModalAfterEndPrimaryEvent : Boolean`

Cho phép modal tự động ẩn sau khi thực hiện sự kiện của button primary, giá trị mặc định là `true`

---
