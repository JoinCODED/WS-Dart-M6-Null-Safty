Let's add an `if` statement to check if `x` is null. If so, execute the print statement. Otherwise, add `x` and `y` only if `x` is not null:

```dart
void main() {
    int? x;
    int y = 2;
    if(x == null){
        print('x is null');
    } else {
      print(x + y);
    }
}
```

As you can see, the error went away, because Dart has a feature called `flow analysis: promotion` which makes it smart enough to know that `x` can't be null here.

It's called `promotion` because `x` was promoted from being nullable to a non-nullable variable.
