# react-screentype-hook

> React hook to dynamically get current screen type

## Install

```sh
// with npm
npm install react-screentype-hook

// with yarn
yarn add react-screentype-hook
```

## How to use

## Without custom breakpoints

```javascript
import React from "react";
import useScreenType from "react-screentype-hook";

function App() {
  const screenType = useScreenType();

  return (
    <div style={{ height: "100vh", width: "100vw" }}>
      <img
        src={
          screenType.isMobile
            ? "https://picsum.photos/200/200"
            : "https://picsum.photos/400/400"
        }
      />
    </div>
  );
}

export default App;
```

## With custom breakpoints

```javascript
import React from "react";
import useScreenType from "react-screentype-hook";

function App() {
  const screenType = useScreenType({
    mobile: 400,
    tablet: 800,
    desktop: 1000
  });

  return (
    <div style={{ height: "100vh", width: "100vw" }}>
      <img
        src={
          screenType.isMobile
            ? "https://picsum.photos/200/200"
            : "https://picsum.photos/400/400"
        }
      />
    </div>
  );
}

export default App;
```

## License

[MIT](LICENSE)
