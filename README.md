# Flutter
## AppBar 
- Thanh menu được hiện thị trên cùng gồm các thanh công cụ và các tiện ích khác

<br />

![AppBar](app_bar.png "appbar")

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