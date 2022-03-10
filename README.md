# SampleFlutterCode
```dart
return Scaffold(
      body: AnnotatedRegion<SystemUiOverlayStyle>(
        value: SystemUiOverlayStyle.light,
        child: Container(
          decoration: BoxDecoration(
            gradient: LinearGradient(
              begin: Alignment.topCenter,
              end: Alignment.bottomCenter,
              stops: [0.1, 0.4, 0.7, 0.9],
              colors: [
                Color(0xFF3594DD),
                Color(0xFF4563DB),
                Color(0xFF5036D5),
                Color(0xFF5B16D0),
              ]
            )
          ),
        ),
      ),
    );
```

<img width="341" alt="Screenshot 2022-02-27 at 18 47 37" src="https://user-images.githubusercontent.com/863760/155881147-71875fc5-c8fe-4e90-a955-9ceece28ff64.png">


```dart

Card(
elevation: 8.0,
shape: RoundedRectangleBorder(
borderRadius: const BorderRadius.all(40),
),
child: Icon(Icons.home)

```
<img width="477" alt="Screenshot 2022-03-10 at 11 12 13" src="https://user-images.githubusercontent.com/863760/157587247-674034bb-3d8b-40a3-b7fd-a89db9a1ffcf.png">

