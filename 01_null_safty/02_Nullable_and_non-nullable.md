### Types are non-nullable by default

```dart
void main() {
    int x = null; // you can't assign a null value to an `int` value
}
```

If we want to assign `null` to this variable, we have to declare it as nullable, and we do that by adding `?` after the type name:

```dart
void main() {
    int? x = null;
}
```

We can remove the initializer, and `x` will be set to `null` by default:

```dart
void main() {
    int? x;
}
```

If we declare another variable and we add it to x, we will get an error at compile time, and that's one of the useful usages of Dart being `null` safe language.

```dart
void main() {
    int? x;
    int y = 2;
    print(x + y);
}
```
