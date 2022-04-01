Suppose we have this list:

```dart
void main() {
    List<String> countries = ['Kuwait','Oman','Egypt'];
}
```

Let's try to add a `null` value to this list:

```dart
void main() {
    List<String> countries = ['Kuwait','Oman','Egypt',null];
}
```

Dart will complain about a `null` value in a list of `String`.

To solve this, we can tell dart this is a list of `nullable` strings:

```dart
void main() {
    List<String?> countries = ['Kuwait','Oman','Egypt',null];
}
```

Let's try to iterate over this list and print an upperCase of all string:

```dart
void main() {
    List<String?> countries = ['Kuwait','Oman','Egypt',null];

    for (var country in countries){
        print(country.toUpperCase());
    }
}
```

As you see, we get an error because we can't use `toUpperCase()` which is a string method on null, to solve this we need to promote `country` to a non nullable variable:

```dart
void main() {
    List<String?> countries = ['Kuwait','Oman','Egypt',null];

    for (var country in countries){
        if(country != null){
        print(country.toUpperCase());
        }
    }
}
```

What about a shorter way? we can use `Conditional access operator`:

```dart
void main() {
    List<String?> countries = ['Kuwait','Oman','Egypt',null];

    for (var country in countries){
        print(country?.toUpperCase());
    }
}
```

By adding a `?` we are telling dart that do everything after the question mark, only if `country` is not `null`!
