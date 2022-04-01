The Assertion operator is used to assign nullable values to non-nullable variables, let me show you how it works:

```dart
void main() {
    int x = 50;
    int? y;

    if (x > 0){
        y = x;
    }
}
```

So here, `y` may be `null` if `x < 0`, let's continue:

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

Here, we got an error, we can't assign the value `y` which is of type `int?` aka `nullable` to the variable `value` which is `non-nullable` variable, unless we use the `assertion` operator:

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
