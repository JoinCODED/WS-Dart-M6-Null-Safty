```dart
void main() {
    int x = -5;
    int? y;

    if (x > 0){
        y = x;
    }

    int value = y!;

    print(value);
}
```

In the previous example, suppose we want to assign an integer `0` to `value` if `y` is `null`. To do that, we use the ternary operator:

```dart
void main() {
    int x = -5;
    int? y;

    if (x > 0){
        y = x;
    }

    int value = y == null ? 0 : y;

    print(value);
}
```

That works, but we have a much shorter way that gets the same job done:

```dart
void main() {
    int x = -5;
    int? y;

    if (x > 0){
        y = x;
    }

    int value = y ?? 0;

    print(value);
}
```

It assigns `0` to `value` if `y` is `null`.
