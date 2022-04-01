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

In the previous example, suppose we want to assign `value` an integer `0` if `y` in `null`, so we need to check for `y` if it's `null`, one way to do this is to use the ternary operator:

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

This works, but we have a much shorter way to do the same job for us:

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

What this does, is to assign `0` if `y` is `null`.
