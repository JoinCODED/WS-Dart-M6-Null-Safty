To start, we need to know about the `null value:

```dart
void main () {
    const person = {
        'name': 'salem'
    };
    print(person['age']);
}
```

If we have a map and we try to access a key that doesn't exist:

Output

```
null
```

And `null` means `no value`. We can check for a value to know if it's `null` or not using an if statement:

```dart
void main () {
    const person = {
        'name': 'salem'
    };
    if (person['age'] == null){
        print('no such key');
    } else {
        print(person['age']);
    }
}
```

There are cases were `null` can be useful, however, sometimes `null` values are **unwanted**.

Dart and some other languages, have a feature called **Null Safety**, as they can decide at compile time if a variable can be `null` or not.

But what does that all mean for us?

Here's the main takeaways:
