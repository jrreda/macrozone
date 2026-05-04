# MacroZone

MacroZone is a React Native app for tracking daily calories and macronutrients (protein, carbs, fat). Log meals, see progress against your goals on the home dashboard, and optionally enable meal reminders.

![MacroZone home screen showing macro summary, meal reminders toggle, and recent meals](./assets/images/tabIcons/screen.png)

## Features

- **Dashboard** — Daily totals for calories, protein, carbs, and fat with color-coded progress against configurable goals.
- **Meals** — Add meals with macros; browse and manage the full list on a dedicated tab.
- **Local storage** — Meals persist on device with AsyncStorage.
- **Sharing & clipboard** — Share a summary or copy it for quick paste elsewhere.
- **Meal reminders** — Optional local notifications when enabled.

## Tech stack

- [Expo](https://expo.dev/) SDK 55
- [Expo Router](https://docs.expo.dev/router/introduction/) (file-based tabs)
- React 19 / React Native 0.83
- TypeScript
- `@react-native-async-storage/async-storage`, `expo-notifications`, `expo-clipboard`

## Requirements

- [Node.js](https://nodejs.org/) (LTS recommended)
- [npm](https://www.npmjs.com/) or another compatible package manager
- For device builds: [Expo Go](https://expo.dev/go) or a dev client; for store builds, [EAS Build](https://docs.expo.dev/build/introduction/) (see `eas.json`)

## Getting started

Clone the repository, install dependencies, and start the dev server:

```bash
npm install
npm start
```

Then press `i` for iOS simulator, `a` for Android emulator, or scan the QR code with Expo Go on a physical device.

### Scripts

| Command        | Description                    |
| -------------- | ------------------------------ |
| `npm start`    | Start Expo dev server          |
| `npm run ios`  | Start with iOS target          |
| `npm run android` | Start with Android target   |
| `npm run web`  | Start web target               |
| `npm run lint` | Run Expo lint                  |

## Project layout

- `src/app/` — Expo Router routes and layouts (`(tabs)` for Home, Add Meal, All Meals).
- `src/components/` — UI pieces (macro grid, meal rows, header, toggles, share/copy).
- `src/storage/` — AsyncStorage helpers for meals.
- `src/utils/` — Notifications and related utilities.
- `assets/` — Images, icons, and splash assets.

## License

Private project (`"private": true` in `package.json`). Adjust licensing if you open-source the repo.
