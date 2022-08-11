### welcome to dart Programming 

sample start:
---Practice.dart---
### SAMPLE 1
```dart
void main(List<String> arguments) {
  print('hello dart');
}
```
>dart run Practice.dart

### S2
```dart
void main(List<String> arguments) {
  String myString = 'Hello World';
  print(myString);
  print(myString.contains('Hello'));

  int myInteger = 5;
  print(myInteger.toString());
  print(myInteger.isEven);
  double myDouble = 5.5;

  num myNumber = 5.5;
  bool myBool = false;
  dynamic mySomething = 5;
  mySomething = 'Hello';
  mySomething = true;
}
```
### S3
```dart
void main(List<String> arguments) {
  var myString = 'Hello World';
  print(myString);
  myString = 'Update!';
  print("test" + myString);
}

void main(List<String> argumnts) {
  String? possible = 'abc'; // Warning: Operand of null-aware operation '?.' has type 'String' which excludes null.
  print(possible?.length);
}

void main(List<String> arguments) {
  String? possible = 'abc';
  print(possible.length);
}

void main(List<String> arguments) {
  int result;
  double resultDouble = 5 / 5;
  result = 5 ~/ 5; //using truncate operator
  int x = 5;
  x++;
  x--;
  x = x + 5;
  x += 5;
  x -= 5;
  x *= 5;
  x ~/= 5;
  bool isEqual = 5 == 10;
  String myString = 'Hello ' + isEqual.toString();
  print(myString);
}

void main(List<String> arguments) {
  String returnsStringNested() {
    return 'hello';
  }

  returnsStringNested();
  returnsString();
}

String returnsString() {
  return 'hello';
}

void otherFunction() {
  returnsString();
}

void positionalParams(int x, double y, String greeting) {
  positionalParams(5, 3.5, 'hi');
}

void optionalPositionalParams(int x, double y, [String greeting = 'hi']) {
  optionalPositionalParams(5, 3.5);
}

void optionalPositionalParam(int x, double y, [String? greeting]) {
  optionalPositionalParams(5, 3.5);
  optionalPositionalParams(5, 3.5, 'hi');
}

/*named parameter */
void nameOptionalParams({
  int? x,
  double? y,
  String? greeting,
}) {
  nameOptionalParams(x: 5, greeting: 'hi');
}

void nameOptionalParam({
  required int x,
  required double y,
  required String greeting,
}) {
  nameOptionalParam(x: 5, y: 3.5, greeting: 'hi');
}

void main(List<String> arguments) {
  final twicePlusFive = twice((x) => x + 5);
  final result = twicePlusFive(3);
  print(result);
}

int Function(int) twice(int Function(int) f) {
  return (int x) {
    return f(f(x));
  };
}
/* o/p: 13  */

void main(List<String> arguments) {
  List<int> myList = [1, 2, 3];
  final firstElement = myList[0];

  Map<String, dynamic> myMap = {
    'name': 'john Doe',
    'age': 42,
    'registered': true,
  };
  final name = myMap['name'];
  print(name);
  Set<int> mySet = {1, 2, 3, 2};
  print(mySet.length);
}
void main(List<String> arguments) {
  final names = ['John', 'Jane', 'Matthew'];
  final nameLength = names.map((name) => name.length).toList();
  print(nameLength[0]);
}

void main(List<String> arguments) {
  final names = ['John', 'Jane', 'Matthew'];
  final namesFilter = names.where((name) => name.length==4).toList();
  print(namesFilter);
}

void main(List<String> arguments) {
  final names = ['John', 'Jane', 'Matthew'];
  final namesFilter = names.map((name) => name).toList();
  print(namesFilter[0]);
}

void main(List<String> arguments) {
  final names = ['John', 'Jane', 'Matthew'];
  final namesFilter = names.map((name) => name).toList();
  print("test=>" + namesFilter[0]);
  for (final name in namesFilter) {
    print("test=>1" + name);
  }
  names.forEach((element) => {print("test=>2" + element)});
}

void main(List<String> arguments) {
  bool isSignedIn = true;
  <String>[
    "this is a fake content",
    if (isSignedIn) 'SignOut' else 'Sign In',
  ];

  final x = <String>[
    for (int i = 0; i < 5; i++) i.toString(),
    for (final number in [1, 2, 3]) number.toString(),
  ];
  print(x);

  final list1 = ['hello', 'there'];
  final List2 = ['what', 'up'];
  <String>[
    ...list1,
    ...List2,
  ];
}

/*
enum AccountType { free, premium, vip }
void main(List<String> arguments) {
  // final accountType = 'premium';
  final userAccountType = AccountType.premium;
  print(userAccountType.index);
  AccountType.values[1];

  switch (userAccountType) {
    case AccountType.free:
      print('0 USD');
      break;
    case AccountType.premium:
      print('30 USD');
      break;
    default:
      break;
  }
}
*/
void main(List<String> arguments) {}

class User {
  final String firstName;
  final String lastName;

  User({required this.firstName, required this.lastName});

  String getFullName() => '$firstName $lastName';
}

void main(List<String> arguments) {
  final user = User(firstName: 'john', lastName: 'Doe');
  user.fullName;
  user.firstName;
}

class User {
  final String firstName;
  final String lastName;

  User({required this.firstName, required this.lastName});

  String get fullName => '$firstName $lastName';
}

```
