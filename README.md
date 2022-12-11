# responsive-img-material-ui ![Weekly downloads](https://img.shields.io/npm/dw/responsive-img-material-ui 'Weekly downloads')

A material-ui component which displays an image from different sources based on the page's current width (based on material-ui defined breakpoints).

The order of breakpoints: xs, sm, md, lg, xl. You can find [here](https://material-ui.com/layout/breakpoints) the values defined currently by material-ui for these breakpoints.

---

## Demo

You can access the storybook for this component [here](https://iulian-radu-at.github.io/responsive-img-material-ui/).

## Props

The component accepts the props defined bellow in the table.

### Props accepted by ResponsiveImgMaterialUi

| Name  | Type          | Required | Default   | Description                                                                         |
| ----- | ------------- | -------- | --------- | ----------------------------------------------------------------------------------- |
| id    | string        | no       | undefined | The id of the field                                                                 |
| lg    | string        | no\*     | undefined | Source used for the lg breakpoint and wider screens (if not overridden)             |
| md    | string        | no\*     | undefined | Source used for the md breakpoint and wider screens (if not overridden)             |
| sm    | string        | no\*     | undefined | Source used for the sm breakpoint and wider screens (if not overridden)             |
| xl    | string        | no\*     | undefined | Source used for the xl breakpoint and wider screens (if not overridden)             |
| xs    | string        | no\*     | undefined | Source used for the xs breakpoint and bellow, and wider screens (if not overridden) |
| style | CSSProperties | no       | undefined | The style applied to the field                                                      |

no\* means that at least one of them should be defined or an exception is triggered.

---

## Versions

| ResponsiveImgMaterialUi _uses_ | Material-ui |      React       |
| -----------------------------: | :---------: | :--------------: |
|                          1.0.x |    3.9.3    |      16.8.6      |
|                          2.0.x |    4.0.2    |      16.8.6      |
|                          2.1.x |    4.2.0    |      16.8.6      |
|                          2.2.x |    4.3.3    |      16.9.0      |
|                          2.3.x |    4.9.0    |      16.9.0      |
|                          2.4.x |    4.9.7    |      16.9.0      |
|                          2.5.x |   4.10.2    |      16.9.0      |
|                          2.6.x |   4.11.0    |      16.9.0      |
|                          2.7.x |   4.11.3    | 16.9.0 or 17.0.0 |
|                          3.0.x |   5.10.17   |     >=18.0.0     |

### About versioning schema used for ResponsiveImgMaterialUi

- Major - it will be increased if the major version of the dependat package changes or there are breaking changes in the code of ResponsiveImgMaterialUi
- Minor - it will be increased if no major version of the dependat package changes, but there are changes of the minor or patch versions of it
- Patch - it will be increased if there are no changes of the dependat packages, but there are non breaking changes in the code of ResponsiveImgMaterialUi

---

## Example

Displaying an image in three sizes based on the current window size:

```js
import * as React from 'react';
import ResponsiveImgMaterialUi from 'responsive-img-material-ui';

class App extends React.Component {
  render() {
    return (
      <div className="App">
        <ResponsiveImgMaterialUi
          xs="/img/logo-small.jpg"
          md="/img/logo-medium.jpg"
          lg="/img/logo-large.jpg"
        />
      </div>
    );
  }
}

export default App;
```

---

## Changelog

### 1.0.1

- responsive-img-material-ui is made publicly available

### 1.0.2

- Corrected the way we decide which provided src is used

### 2.0.0

- Updated packages

### 2.1.0

- Updated packages

### 2.2.0

- Updated packages

### 2.3.0

- Updated packages

### 2.4.0

- Updated packages
- Moved from npm to yarn

### 2.5.0

- Updated packages

### 2.6.0

- Updated packages

### 2.6.1

- Fixed crash produced by "export \* from"

### 2.7.0

- Accepting React 17 as peerDependencies
- Fixed security warnings

### 3.0.0

- Migrated to material-ui 5
- Supports minimum React 18
