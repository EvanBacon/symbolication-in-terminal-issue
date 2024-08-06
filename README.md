# Repro of Metro not symbolicating

- `bun install` (or whatever)
- `npx expo`
- Press I to open in the iOS Simulator
- The terminal will print broken stack traces like this:

```
 ERROR  STACK THING
    at App
    at withDevTools(App) (http://192.168.1.174:8081/node_modules/expo/AppEntry.bundle//&platform=ios&dev=true&hot=false&transform.engine=hermes&transform.bytecode=true&transform.routerRoot=app:129910:27)
    at RCTView
    at View (http://192.168.1.174:8081/node_modules/expo/AppEntry.bundle//&platform=ios&dev=true&hot=false&transform.engine=hermes&transform.bytecode=true&transform.routerRoot=app:74550:43)
    at RCTView
    at View (http://192.168.1.174:8081/node_modules/expo/AppEntry.bundle//&platform=ios&dev=true&hot=false&transform.engine=hermes&transform.bytecode=true&transform.routerRoot=app:74550:43)
    at AppContainer (http://192.168.1.174:8081/node_modules/expo/AppEntry.bundle//&platform=ios&dev=true&hot=false&transform.engine=hermes&transform.bytecode=true&transform.routerRoot=app:74393:25)
    at main(RootComponent) (http://192.168.1.174:8081/node_modules/expo/AppEntry.bundle//&platform=ios&dev=true&hot=false&transform.engine=hermes&transform.bytecode=true&transform.routerRoot=app:117823:28)
```
