# UI / UX & Smooth App References (iOS + Android)

References for making the app feel polished, fast and pleasant on both platforms.

## High-quality open-source health / wellness apps (inspiration)

| Project | Stack | Why useful | Link |
|---------|-------|------------|------|
| Flexify | Flutter | Clean offline-first workout tracker, good charts, themes | https://github.com/brandonp2412/Flexify |
| State of Health | React Native | Polished fitness tracking UI | https://github.com/Kennygunderman/state-of-health-tracker |
| Menstrudel | Flutter | Simple, private cycle tracker with solid Material design | https://github.com/J-shw/Menstrudel |
| Bluma | React Native | Modern, calm, offline-first aesthetic | https://github.com/blumaHQ/bluma-app |

## Smooth animations & interaction libraries

### React Native (works on iOS + Android)
| Library / Collection | What it offers | Link |
|----------------------|----------------|------|
| **react-native-reanimated** | Industry standard for smooth, 60/120fps animations | https://github.com/software-mansion/react-native-reanimated |
| **react-native-gesture-handler** | Native gestures | https://github.com/software-mansion/react-native-gesture-handler |
| **@shopify/react-native-skia** | High-performance 2D graphics & shaders | https://github.com/Shopify/react-native-skia |
| Reactiive Demos | Large collection of production-quality Reanimated + Skia demos | https://github.com/enzomanuelmangano/demos |
| quattro4maggi | Monthly production-grade Skia / Reanimated demos | https://github.com/ImCitizen13/quattro4maggi |
| native-springs | Ready-to-copy animated components (carousels, liquid effects, etc.) | https://github.com/MatthewSRC/native-springs |
| rn-animated-components | Production-ready Skia components (liquid switch, loaders, etc.) | https://github.com/ogulcanbagatir/rn-animated-components |

### Flutter (works on iOS + Android)
| Library / Collection | What it offers | Link |
|----------------------|----------------|------|
| Flutter samples | Official high-quality examples (animations, Material 3, navigation) | https://github.com/flutter/samples |
| flutter-ui-designs | Large collection of polished, animated UI screens | https://github.com/hmziqrs/flutter-ui-designs |
| flutter-ui-nice | 130+ pages of UI examples | https://github.com/FlutterOpen/flutter-ui-nice |
| dashboard_reborn | Beautiful animated dashboard template | https://github.com/urmilshroff/dashboard_reborn |
| Flutter Shadcn UI | Clean, modern component library | https://github.com/nank1ro/flutter-shadcn-ui |

## Design principles for a smooth feel

1. **60/120 fps animations** — use Reanimated or Flutter’s implicit animations; avoid heavy JS-thread work.
2. **Haptic feedback** on important actions (period start, ovulation confirmation, mode switch).
3. **Skeleton loaders** instead of spinners for charts and lists.
4. **Calm color palette** — soft neutrals + one accent color. Avoid aggressive pink.
5. **Large tap targets** and clear visual hierarchy.
6. **Dark mode** from day one.
7. **Smooth charts** (BBT graph, cycle overview) — consider `fl_chart` (Flutter) or Victory Native / Skia-based charts (React Native).
8. **Accessible** — dynamic type, sufficient contrast, screen-reader labels.

## Recommended starting point

- If you choose **Flutter**: start with Menstrudel + Flexify for structure, then study `flutter/samples` and `flutter-ui-designs`.
- If you choose **React Native**: study Bluma + Menstrudel (for concept), then use Reanimated + Skia from the demo repos above.

These references help you avoid the “generic period app” look and build something that feels premium and trustworthy.
