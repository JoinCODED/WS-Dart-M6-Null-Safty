### Types are non-nullable by default

```dart
void main() {
    int x = null; // you can't assign a null value to an `int` value
}
```

But if we really want to assign `null` to this variable, we have to declare it as nullable, and we do this by adding `?` after the name of the type:

```dart
void main() {
    int? x = null;
}
```

And we can remove the initializer and `x` will be set to `null` by default:

```dart
void main() {
    int? x;
}
```

And if we declare another variable and we add them together, we will get an error at compile time, and that's one useful use of dart being `null` safe language.

```dart
void main() {
    int? x;
    int y = 2;
    print(x + y);
}
```
