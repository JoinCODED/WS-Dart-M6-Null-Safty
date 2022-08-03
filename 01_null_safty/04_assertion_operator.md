The assertion operator is used to assign nullable values to non-nullable variables. Let me show you how it works:

```dart
void main() {
    int x = 50;
    int? y;

    if (x > 0){
        y = x;
    }
}
```

Here, `y` might be `null` if `x < 0`. Let's continue:

```dart
void main() {
    int x = 50;
    int? y;

    if (x > 0){
        y = x;
    }

    int value = y;

    print(value);
}
```

We got an error because we can't assign the value `y` which is of type `int?` aka `nullable` to the variable `value`, which is a `non-nullable` variable, unless we use the `assertion` operator:

```dart
void main() {
    int x = 50;
    int? y;

    if (x > 0){
        y = x;
    }

    int value = y!;

    print(value);
}
```
