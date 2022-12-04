
# Card Banner
It is simple to add a banner to any widget using card banner.

## Features

- Highly customizable.
- Multi-platform support.


## Getting started

Add this line to your pubspec.yaml under the dependencies:
```dart
dependencies:
    card_banner: ^0.0.1
```
alternatively, you can use this command:
```dart
flutter pub add card_banner
```
Import statement
```dart
import 'package:card_banner/card_banner.dart'
```

## Usage

`Simple example:` Cover the card widget with the card banner and provide the required text. It's done

```dart
class MyBanner extends StatelessWidget {
  const MyBanner({super.key});

  @override
  Widget build(BuildContext context) {
    return Scaffold(
      backgroundColor: const Color.fromARGB(255, 221, 222, 245),
      body: ListView.builder(
        padding: const EdgeInsets.symmetric(horizontal: 10),
        itemCount: 8,
        itemBuilder: (context, index) {
          return CardBanner(
            text: "50% Off",
            child: foodCard(),
          );
        },
      ),
    );
  }

  Card foodCard() {
    return Card(
      child: ListTile(
        contentPadding: EdgeInsets.zero,
        title: Image.network(
          "https://images.pexels.com/photos/461198/pexels-photo-461198.jpeg",
          fit: BoxFit.cover,
        ),
        subtitle: const Padding(
          padding: EdgeInsets.all(12.0),
          child: Text(
            "Nulla cillum qui elit adipisicing culpa ad laboris amet laboris velit. Pariatur sit tempor nostrud non duis commodo laboris. Consequat incididunt laborum qui dolore in velit consequat mollit amet. Proident eu et sint veniam sunt fugiat quis fugiat sunt pariatur do enim in.",
            overflow: TextOverflow.ellipsis,
            maxLines: 3,
          ),
        ),
      ),
    );
  }
}

```

## Additional information

Check the [example project](https://github.com/abhishek-900/card_banner/example) on github for advanced usage.
