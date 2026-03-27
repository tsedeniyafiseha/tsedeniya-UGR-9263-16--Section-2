# flutter_project

A Flutter profile card application.

## Widget Tree Structure

```
MaterialApp
└── ProfileCardPage (Scaffold)
    ├── AppBar
    │   └── Text ("My Profile")
    └── Body (Center)
        └── Card
            └── Container
                └── Column
                    ├── CircleAvatar (with profile image)
                    ├── SizedBox (spacing)
                    ├── Text ("Alex Johnson")
                    ├── SizedBox (spacing)
                    ├── Text ("Flutter Developer")
                    ├── SizedBox (spacing)
                    └── Row (action buttons)
                        ├── IconButton (phone)
                        ├── IconButton (message)
                        └── IconButton (share)
```
<img width="1366" height="768" alt="image" src="https://github.com/user-attachments/assets/0e309847-ac38-474e-b320-074291e64895" />

## Getting Started

This project is a starting point for a Flutter application.

A few resources to get you started if this is your first Flutter project:

- [Learn Flutter](https://docs.flutter.dev/get-started/learn-flutter)
- [Write your first Flutter app](https://docs.flutter.dev/get-started/codelab)
- [Flutter learning resources](https://docs.flutter.dev/reference/learning-resources)

For help getting started with Flutter development, view the
[online documentation](https://docs.flutter.dev/), which offers tutorials,
samples, guidance on mobile development, and a full API reference.
