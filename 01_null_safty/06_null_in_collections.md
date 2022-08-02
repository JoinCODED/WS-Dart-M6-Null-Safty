Suppose we have the following list:

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

To solve that, we can tell Dart that this is a list of `nullable` strings:

```dart
void main() {
    List<String?> countries = ['Kuwait','Oman','Egypt',null];
}
```

Let's try to iterate over this list and print an upperCase of all strings:

```dart
void main() {
    List<String?> countries = ['Kuwait','Oman','Egypt',null];

    for (var country in countries){
        print(country.toUpperCase());
    }
}
```

As you can see, we got an error because `.toUpperCase()` is a string method and we can't use it on null. To solve that, we need to promote `country` to a non-nullable variable:

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

What about a shorter way? we can use `Conditional Access Operator`:

```dart
void main() {
    List<String?> countries = ['Kuwait','Oman','Egypt',null];

    for (var country in countries){
        print(country?.toUpperCase());
    }
}
```

By adding a `?`, we are telling Dart to do what's required after the question mark, only if `country` is not `null`.
