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

Cài đặt tùy chỉnh cho modal,`backdrop` điều chỉnh background của modal, có thể là `true`/`false`/`'static'`;  `keyboard`cho phép nhấn phím**Esc** để ẩn modal, có thể là`true`/`false`

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

#### 13. `setFooterButton(args)`

`args : ModalButton | Array of ModalButton`

Thêm các button vào modal footer, hỗ trợ thêm kèm event

#### 14. `setDefaultFooterButton(_primaryText, _secondaryText, _primaryEvent)`

`_primaryText : String`

`_secondaryText : String`

`_primaryEvent : Callback | None`

Thêm 02 button vào modal footer với text chỉ định. Event của button phụ (secondary) luôn luôn là đóng modal

#### 15. `addPrimaryButtonEvent(_evType, _evCallback)` hoặc `addPrimaryButtonEvent(_evCallback)`

`_evType : String`

`_evCallback : Callback`

Chỉ định event cho button primary, dùng kèm với hàm **14. `setDefaultFooterButton(...)`** trong trường hợp event chưa được chỉ định

#### 16. Các event liên quan

_Sắp ra mắt_
