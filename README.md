# React + TypeScript + Vite

This template provides a minimal setup to get React working in Vite with HMR and some ESLint rules.

Currently, two official plugins are available:

- [@vitejs/plugin-react](https://github.com/vitejs/vite-plugin-react/blob/main/packages/plugin-react) uses [Babel](https://babeljs.io/) for Fast Refresh
- [@vitejs/plugin-react-swc](https://github.com/vitejs/vite-plugin-react/blob/main/packages/plugin-react-swc) uses [SWC](https://swc.rs/) for Fast Refresh

## React Compiler

The React Compiler is enabled on this template. See [this documentation](https://react.dev/learn/react-compiler) for more information.

Note: This will impact Vite dev & build performances.

## Expanding the ESLint configuration

If you are developing a production application, we recommend updating the configuration to enable type-aware lint rules:

```js
export default defineConfig([
  globalIgnores(['dist']),
  {
    files: ['**/*.{ts,tsx}'],
    extends: [
      // Other configs...

      // Remove tseslint.configs.recommended and replace with this
      tseslint.configs.recommendedTypeChecked,
      // Alternatively, use this for stricter rules
      tseslint.configs.strictTypeChecked,
      // Optionally, add this for stylistic rules
      tseslint.configs.stylisticTypeChecked,

      // Other configs...
    ],
    languageOptions: {
      parserOptions: {
        project: ['./tsconfig.node.json', './tsconfig.app.json'],
        tsconfigRootDir: import.meta.dirname,
      },
      // other options...
    },
  },
])
```

You can also install [eslint-plugin-react-x](https://github.com/Rel1cx/eslint-react/tree/main/packages/plugins/eslint-plugin-react-x) and [eslint-plugin-react-dom](https://github.com/Rel1cx/eslint-react/tree/main/packages/plugins/eslint-plugin-react-dom) for React-specific lint rules:

```js
// eslint.config.js
import reactX from 'eslint-plugin-react-x'
import reactDom from 'eslint-plugin-react-dom'

export default defineConfig([
  globalIgnores(['dist']),
  {
    files: ['**/*.{ts,tsx}'],
    extends: [
      // Other configs...
      // Enable lint rules for React
      reactX.configs['recommended-typescript'],
      // Enable lint rules for React DOM
      reactDom.configs.recommended,
    ],
    languageOptions: {
      parserOptions: {
        project: ['./tsconfig.node.json', './tsconfig.app.json'],
        tsconfigRootDir: import.meta.dirname,
      },
      // other options...
    },
  },
])
```

# ABApp
React App for the UofSC ABA club.
The casual slack app for orgs.


## Stack for ABApp
**Frontend**
    - React Native + Expo
**Backend**
    - Firebase
**Extras**
    - Push notifications (Expo + Firebase)
    - Calendar API for Google Calendar.


## **Features**
- **Users** --> Different Account Types
    - Owner (Club Leader)
    - Admin (Club Exec Board)
    - Member (Club Member)

- **Push Notifications for Event Syncing**
    - Automatically Add to Everyones Calendar
    - Send a reminder (Options for Morning of, Hour before, 30 minutes before, custom)
    - WhenToMeet availability feature per user (Can change whenever)
    - Event signup
        - Headcount vs "signup" (everyone expected to attend vs who wants to do the event)
        - fill out form ( Who has car, extra information )

- **Announcments and Messages**
    - Announce to the group
        - Pinned at top of GC
    - Pinned messages like GroupME
        - Grouped pins of messages
    - Exec only GC

- **No direct messages between members**

- **Big feature: Making it feel casual**
    - not professional like Slack
    - not too casual like instagram
    - make messages feel iMessage
    - Emojis instead of yes or no for polls and stuff

## Problems
- Multiple GC's (Too many people for 1)
    - Create large groupchat
    - Instagram feels too professional



## User Discovery
    - Streaks for meetings attended? 
        - Could be trophies
        - Only admin can see?

    - Message reactions
        - Emojis for yes or no
        - iMessage vs Insta vs discord style

    - What features theyd want as members vs as exec