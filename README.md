# expense_manager

A personal expense tracker built with Flutter. Record expenses, organize them by category and tag, view spending by date or category, and manage your own categories and tags. Data is persisted locally on the device.

## Features

- **Add expenses** — amount, payee, note, date, category, and tag
- **View by date** — chronological list of all expenses with swipe-to-delete
- **View by category** — expenses grouped by category with per-category totals
- **Manage categories** — add or delete custom categories (defaults include Food, Transport, Entertainment, Office, Gym)
- **Manage tags** — add or delete tags (defaults include Breakfast, Lunch, Dinner, Train, Vacation, and more)
- **Edit expenses** — update existing expense records
- **Local storage** — all data persisted on device via `localstorage` (no backend required)

## Screens

| Screen | Description |
|--------|-------------|
| Home | Two tabs: "By Date" (chronological list) and "By Category" (grouped with totals) |
| Add Expense | Form to record a new expense or edit an existing one |
| Manage Categories | Add/delete expense categories |
| Manage Tags | Add/delete expense tags |

## Tech Stack

- **Flutter** (Dart SDK ^3.5.1)
- **State management**: `provider`
- **Local persistence**: `localstorage`
- **Date formatting**: `intl`
- **Collections**: `collection`

## Getting Started

### Prerequisites

- [Flutter SDK](https://docs.flutter.dev/get-started/install) installed
- An editor (Android Studio, VS Code, etc.)

### Run the app

```bash
cd expense_manager
flutter pub get
flutter run
```

This will launch the app on your connected device/emulator. Supported platforms include Android, iOS, web, Windows, macOS, and Linux.

## Project Structure

```
lib/
├── main.dart              # App entry point and routing
├── models/
│   ├── expense.dart       # Expense data model
│   ├── expense_category.dart
│   └── tag.dart
├── providers/
│   └── expense_provider.dart  # State management + local storage
├── screens/
│   ├── home_screen.dart           # Home with By Date / By Category tabs
│   ├── add_expense_screen.dart    # Add/edit expense form
│   ├── category_management_screen.dart
│   └── tag_management_screen.dart
└── widgets/
    ├── add_category_dialog.dart
    └── add_tag_dialog.dart
```

## Default Data

The app ships with built-in default categories and tags:

**Categories:** Food, Transport, Entertainment, Office, Gym  
**Tags:** Breakfast, Lunch, Dinner, Treat, Cafe, Restaurant, Train, Vacation, Birthday, Diet, MovieNight, Tech, CarStuff, SelfCare, Streaming

You can add your own categories and tags from the respective management screens.

## License

This is a starter Flutter project. Feel free to modify and extend it as needed.
