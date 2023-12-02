# Zusty

ZustyMiddleware is a middleware designed for Zusty, a Zustand Dev Tool, to facilitate the debugging of state management in your applications.

## Installation

Use the package manager to install zustymiddleware.

```bash
npm i zustymiddleware
```

## Usage

1. Import zustymiddleware at the top of your file
2. Wrap your store in the middleware
3. Before you export your store, add window.store = < your store name>

```javascript
import zustymiddleware from 'zustymiddleware';

const useStore = create(
  zustymiddleware((set) => ({
    bears: 0,
    increasePopulation: () => set((state) => ({ bears: state.bears + 1 })),
    removeAllBears: () => set({ bears: 0 }),
  }))
);

window.store = useStore;
export default useStore;
```

## Contributing

Pull requests are welcome. For major changes, please open an issue first
to discuss what you would like to change.

## License

[MIT](https://choosealicense.com/licenses/mit/)
