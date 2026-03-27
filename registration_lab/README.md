# Lab 1: User Registration Form

A Flutter application demonstrating forms, input validation, and stateful widgets.

## Features
- Form validation for all input fields
- Email format validation
- Password strength check (minimum 6 characters)
- Password confirmation matching
- Success dialog on registration
- Responsive UI with Material Design

## How to Run

1. Navigate to this folder:
   ```bash
   cd lab1-registration-form
   ```

2. Get dependencies:
   ```bash
   flutter pub get
   ```

3. Run the app:
   ```bash
   flutter run -d chrome
   ```
   Or for Windows:
   ```bash
   flutter run -d windows
   ```

## What is a Widget Tree?

The **Widget Tree** is a hierarchical structure that shows how Flutter widgets are nested and organized in your app. Every Flutter app is built using a tree of widgets, where:
- Each widget can contain child widgets
- Parent widgets control the layout and behavior of their children
- The tree starts from the root widget (usually `MaterialApp`) and branches down

You can view the live widget tree in **Flutter DevTools** while your app is running.

### How to View Widget Tree in Flutter DevTools:

1. Run your app: `flutter run -d chrome`
2. When the app starts, you'll see a DevTools URL in the terminal
3. Open that URL in your browser
4. Click on the "Widget Inspector" tab
5. You'll see the interactive widget tree with all widgets highlighted

## Widget Tree Structure for This App

```
MaterialApp (Root)
│
└── RegistrationScreen (StatefulWidget)
    │
    └── Scaffold (Main layout structure)
        │
        ├── AppBar
        │   └── Text ('Register')
        │
        └── body: Padding (16px all sides)
            │
            └── Form (with GlobalKey for validation)
                │
                └── ListView (Scrollable list of children)
                    │
                    ├── TextFormField (Full Name input)
                    │   ├── InputDecoration (label, border)
                    │   └── validator function
                    │
                    ├── SizedBox (height: 16 - spacing)
                    │
                    ├── TextFormField (Email input)
                    │   ├── InputDecoration (label, border)
                    │   ├── keyboardType: emailAddress
                    │   └── validator function
                    │
                    ├── SizedBox (height: 16 - spacing)
                    │
                    ├── TextFormField (Password input)
                    │   ├── InputDecoration (label, border)
                    │   ├── obscureText: true
                    │   └── validator function
                    │
                    ├── SizedBox (height: 16 - spacing)
                    │
                    ├── TextFormField (Confirm Password)
                    │   ├── InputDecoration (label, border)
                    │   ├── obscureText: true
                    │   └── validator function
                    │
                    ├── SizedBox (height: 24 - spacing)
                    │
                    └── Center
                        │
                        └── SizedBox (width: 200, height: 45)
                            │
                            └── ElevatedButton
                                ├── onPressed: _submitForm
                                ├── style: rounded corners
                                └── child: Text ('Register')
```

### Widget Tree Explanation:

1. **MaterialApp**: Root widget that provides Material Design styling
2. **RegistrationScreen**: Custom StatefulWidget that manages form state
3. **Scaffold**: Provides basic app structure (AppBar, Body)
4. **Form**: Manages form validation state
5. **ListView**: Makes content scrollable
6. **TextFormField**: Input fields with built-in validation
7. **SizedBox**: Used for spacing between widgets
8. **ElevatedButton**: Submit button with custom styling

## Screenshots

### Running App
![App Screenshot](screenshots/app-screenshot.png)

### Widget Tree in DevTools
![Widget Tree](screenshots/widget-tree.png)

## Code Structure

- `lib/main.dart` - Main application code containing:
  - `RegistrationApp` - Root StatelessWidget
  - `RegistrationScreen` - StatefulWidget for the form
  - `_RegistrationScreenState` - State management and form logic

## Key Concepts Demonstrated

1. **StatefulWidget vs StatelessWidget**
   - `RegistrationApp` is stateless (doesn't change)
   - `RegistrationScreen` is stateful (manages form data)

2. **Form Validation**
   - Using `GlobalKey<FormState>` to manage form state
   - Individual validators for each field
   - Form-wide validation on submit

3. **TextEditingController**
   - Managing text input state
   - Accessing input values
   - Proper disposal to prevent memory leaks

4. **Material Design Widgets**
   - Scaffold, AppBar, TextFormField
   - ElevatedButton with custom styling
   - AlertDialog for success message

## Technologies Used

- Flutter SDK
- Dart programming language
- Material Design components
