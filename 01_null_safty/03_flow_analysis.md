Let's add an if statement to check if `x` is null and add `x` and `y` only if `x` is not null:

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

as you see, the error went away, because dart has a feature called `flow analysis: promotion` that makes it smart enough to know that `x` can't be null here.

And it's called `promotion` because `x` was promoted from being a nullable to non-nullable variable.
