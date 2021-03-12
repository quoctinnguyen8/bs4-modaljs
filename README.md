# Bootstrap4 Modal library

Thư viện hỗ trợ làm việc với modal trong BS4

### Khởi tạo

```
<script src="https://code.jquery.com/jquery-3.5.1.min.js"></script>
<script src="https://cdn.jsdelivr.net/npm/popper.js@1.16.1/dist/umd/popper.min.js"></script>
<script src="https://cdn.jsdelivr.net/npm/bootstrap@4.6.0/dist/js/bootstrap.min.js"></script>

<script src="modal.js"></script>
```


### Sử dụng

```
	var modal = new Modal('Tiêu đề');
	modal.appendBody('<b>Nội dung</b>');
	modal.show();
```

Tham số cũng có thể là Element/jQuery Element

```
	var mBody = $('<b>').text('Nội dung');
	var modal = new Modal('Tiêu đề');
	modal.appendBody(mBody);
	modal.show();
```
