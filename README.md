# useScrollDirection

This is a custom React Hook that allows you to track the direction of the user's scroll on a webpage. It provides two directions: `up` and `down`. The scroll direction is updated only when there is a significant scroll movement (at least 10 pixels).

## Installation

This package is distributed via npm. You can add it to your project using:

```shell
npm install use-scroll-direction
```

Or if you're using Yarn:

```shell
yarn add use-scroll-direction
```

## Usage

Here's a simple usage example:

```tsx
import React from "react";
import useScrollDirection from "use-scroll-direction";

const MyComponent = () => {
  const scrollDirection = useScrollDirection();

  return (
    <div>
      <p>Current scroll direction: {scrollDirection}</p>
    </div>
  );
};

export default MyComponent;
```

By default, the initial direction is set to `"up"`. However, you can specify a different initial direction (`"up"` or `"down"`) if needed:

```tsx
const scrollDirection = useScrollDirection({ initialDirection: "down" });
```

## API

### `useScrollDirection({ initialDirection }: { initialDirection?: 'up' | 'down' })`

This function is the default export of the `use-scroll-direction` package. It accepts an optional configuration object and returns the current scroll direction.

#### Arguments

- `initialDirection` (optional): This optional field lets you set the initial scroll direction. It can be either `"up"` or `"down"`. Defaults to `"up"`.

#### Returns

- `(string)`: Returns a string representing the current scroll direction, either `"up"` or `"down"`.

## Browser Support

This hook relies on the `window.pageYOffset` property which is supported in all modern browsers and Internet Explorer 9+. If you need to support older browsers, you may need to include a polyfill for `window.pageYOffset`.

## License

MIT
