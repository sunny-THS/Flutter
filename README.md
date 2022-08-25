# Flutter

## Cách thức hoạt động của Consumer
- Consumer sẽ dùng method builder thay vì chỉ là object child. Builder cần chính xác 3 tham số là BuildContext,  category data và sau đó là một Widget.‌‌
- Consumer là generic type vì vậy chúng ta phải chỉ định loại dữ liệu nào chúng ta muốn sử dụng. Trong trường hợp của này, ta đang sử dụng dữ liệu từ CategoryProvider do đó chúng mình sẽ viết Consumer<CategoryProvider>(...).‌‌
- Bạn có thể so sánh điều này với Provider.of<...>(context) vì cả hai đều thiết lập active listener đối với provider và kích hoạt hàm build khi dữ liệu thay đổi.‌‌
Builder sẽ nhận BuildContext mà chúng ta cung cấp bằng cách sử dụng context có sẵn bên trong widget của chúng ta.‌‌
- Nó cũng nhận được instance dữ liệu. Giống như trong trường hợp trên, chúng ta nhận được snapshot dữ liệu mới nhất từ ​​CategoryProvider có tên biến là categoryData.‌‌

## The difference between stateFul widget and stateLess widget
| stateLessWidget | stateFulWidget |
| :-- | :-- |
| Stateless Widgets are static widgets. | Stateful Widgets are dynamic widgets.|
| They do not depend on any data change or any behavior change. | They can be updated during runtime based on user action or data change.|
| Stateless Widgets do not have a state, they will be rendered once and will not update themselves, but will only be updated when external data changes. | Stateful Widgets have an internal state and can re-render if the input data changes or if Widget’s state changes. |
| For Example: Text, Icon, RaisedButton are Stateless Widgets.  | For Example: Checkbox, Radio Button, Slider are Stateful Widgets |

## AppBar 
- Thanh menu được hiện thị trên cùng gồm các thanh công cụ và các tiện ích khác

<br />

![AppBar](app_bar.png "appbar")

### Properties
#### actions
- A list of Widgets to display in a row after the title widget.
#### title
- The primary widget displayed in the app bar.

<br />

```dart
AppBar(
    title: Text(widget.title),
    actions: <Widget>[
        IconButton(
            icon: const Icon(Icons.more_vert),
            tooltip: 'More',
            onPressed: () {
                // handle the press
            },
        ),
    ],
)
```
## Container
- The same ***div*** in HTML
### Properties
#### alignment
- Align the child within the container. 
#### child
- The child contained by the container.
#### decoration
- The decoration to paint behind the child
#### foreDecoration
- The decoration to paint in font of the child