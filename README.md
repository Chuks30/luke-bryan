# Luke Bryan — Official Site

A fully self-contained artist website with security gate and theme settings.

## Quick Start

Open `index.html` in any modern browser. No server required.

## Security

- **Default PIN:** `1234`
- To change the PIN, open `index.html` and find this line near the top of the `<script>` block:
  ```js
  const CORRECT_PIN = '1234';
  ```
  Replace `'1234'` with your desired 4-digit PIN.

## Settings Panel

Click the ⚙ gear button (bottom-right) or "⚙ Settings" in the nav to open the settings panel.

### Themes
| Name        | Description              |
|-------------|--------------------------|
| Gold        | Midnight Gold (default)  |
| Steel       | Steel Blue               |
| Crimson     | Crimson Night            |
| Forest      | Forest Sage              |
| Light       | Pure Light (day mode)    |

### Other Settings
- **Animations** — toggle page animations on/off
- **Star Field** — toggle hero star background
- **Horizon Glow** — toggle the horizon line effect
- **Text Size** — scale text from 80% to 120%

## Security Features
- 4-digit PIN gate on every visit
- 3-attempt brute-force lockout (30-second cooldown)
- 10-minute auto-expiring session with progress bar
- 60-second warning toast before session ends
- "Lock Site Now" button in Settings
- In-memory audit log of all auth events

## Session Config (in index.html)
```js
const MAX_ATTEMPTS  = 3;    // wrong attempts before lockout
const LOCKOUT_SECS  = 30;   // lockout duration in seconds
const SESSION_SECS  = 600;  // session length (10 min)
const WARN_AT_SECS  = 60;   // warn before expiry
```

## Files
```
luke-bryan-site/
├── index.html       ← Main site (all-in-one)
├── README.md        ← This file
├── css/             ← Reserved for custom stylesheets
├── js/              ← Reserved for custom scripts
└── images/          ← Add artist photos here
```

## Browser Support
Chrome 105+, Firefox 103+, Safari 15.4+, Edge 105+
(uses CSS `color-mix()` — not supported in older browsers)

---
© 2026 Luke Bryan · MCA Nashville
