# SampleFlutterCode


<img width="341" alt="Screenshot 2022-02-27 at 18 47 37" src="https://user-images.githubusercontent.com/863760/155881147-71875fc5-c8fe-4e90-a955-9ceece28ff64.png">
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



<img width="477" alt="Screenshot 2022-03-10 at 11 12 13" src="https://user-images.githubusercontent.com/863760/157587247-674034bb-3d8b-40a3-b7fd-a89db9a1ffcf.png">

```dart

Card(
elevation: 8.0,
shape: RoundedRectangleBorder(
borderRadius: const BorderRadius.all(40),
),
child: Icon(Icons.home)

```




<img width="344" alt="Screenshot 2022-06-05 at 16 15 34" src="https://user-images.githubusercontent.com/863760/172043782-ec11ce15-70c2-4bff-958b-524c787f06d6.png">

```dart
import 'package:flutter/material.dart';

class NumericPad extends StatelessWidget {
  final Function(int) onNumberSelected;

  NumericPad({required this.onNumberSelected});

  @override
  Widget build(BuildContext context) {
    return Container(
      color: Color(0xFFF5F4F9),
      child: Column(
        crossAxisAlignment: CrossAxisAlignment.stretch,
        mainAxisAlignment: MainAxisAlignment.spaceEvenly,
        children: <Widget>[
          Container(
            height: MediaQuery.of(context).size.height * 0.1,
            child: Row(
              mainAxisAlignment: MainAxisAlignment.spaceEvenly,
              crossAxisAlignment: CrossAxisAlignment.start,
              children: <Widget>[
                buildNumber(1),
                buildNumber(2),
                buildNumber(3),
              ],
            ),
          ),
          Container(
            height: MediaQuery.of(context).size.height * 0.1,
            child: Row(
              mainAxisAlignment: MainAxisAlignment.spaceEvenly,
              crossAxisAlignment: CrossAxisAlignment.start,
              children: <Widget>[
                buildNumber(4),
                buildNumber(5),
                buildNumber(6),
              ],
            ),
          ),
          Container(
            height: MediaQuery.of(context).size.height * 0.1,
            child: Row(
              mainAxisAlignment: MainAxisAlignment.spaceEvenly,
              crossAxisAlignment: CrossAxisAlignment.start,
              children: <Widget>[
                buildNumber(7),
                buildNumber(8),
                buildNumber(9),
              ],
            ),
          ),
          Container(
            height: MediaQuery.of(context).size.height * 0.1,
            child: Row(
              mainAxisAlignment: MainAxisAlignment.spaceEvenly,
              crossAxisAlignment: CrossAxisAlignment.start,
              children: <Widget>[
                buildEmptySpace(),
                buildNumber(0),
                buildBackspace(),
              ],
            ),
          ),
        ],
      ),
    );
  }

  Widget buildNumber(int number) {
    return Expanded(
      child: GestureDetector(
        onTap: () {
          onNumberSelected(number);
        },
        child: Padding(
          padding: EdgeInsets.all(7),
          child: Container(
            decoration: BoxDecoration(
              color: Colors.white,
              borderRadius: BorderRadius.all(
                Radius.circular(15),
              ),
            ),
            child: Center(
              child: Text(
                number.toString(),
                style: TextStyle(
                  fontSize: 28,
                  fontWeight: FontWeight.bold,
                  color: Color(0xFF1F1F1F),
                ),
              ),
            ),
          ),
        ),
      ),
    );
  }

  Widget buildBackspace() {
    return Expanded(
      child: GestureDetector(
        onTap: () {
          onNumberSelected(-1);
        },
        child: Padding(
          padding: EdgeInsets.all(10),
          child: Container(
            decoration: BoxDecoration(
              color: Colors.white,
              borderRadius: BorderRadius.all(
                Radius.circular(15),
              ),
            ),
            child: Center(
              child: Icon(
                Icons.backspace,
                size: 28,
                color: Color(0xFF1F1F1F),
              ),
            ),
          ),
        ),
      ),
    );
  }

  Widget buildEmptySpace() {
    return Expanded(
      child: Container(),
    );
  }

}

````



