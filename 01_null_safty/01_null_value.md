Let's run the following code to get to know what the null value is:

```dart
void main () {
    const person = {
        'name': 'Salem'
    };
    print(person['age']);
}
```

If we have a map and we try to access a key that doesn't exist, the output will be:

```
null
```

`null` means `no value`. We can check to know if a value is `null` or not using an `if` statement:

```dart
void main () {
    const person = {
        'name': 'Salem'
    };
    if (person['age'] == null){
        print('no such key');
    } else {
        print(person['age']);
    }
}
```

There are some cases where `null` can be useful. However, sometimes `null` values are **unwanted**.

Dart and some other languages have a feature called **Null Safety**, as they can decide at compile time if a variable can be `null` or not.

What does that mean for us?

Here are the main takeaways: <!-- Where are the main takeaways? do u mean in the next section? -->
