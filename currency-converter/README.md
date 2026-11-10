# Currency Converter

A small web app for converting between your favorite currencies.

- Pick currencies from the full list (search by code or name) and they stay saved as your favorites.
- Type an amount in any favorite and all the others are converted as you type.
- Favorites, the last amount and the latest rates are kept in the browser's `localStorage`.

## Run it

It is plain HTML, CSS and JavaScript with no build step. Open `index.html` in a browser, or serve the folder:

```sh
python3 -m http.server --directory currency-converter 8000
```

Then open <http://localhost:8000>.

To host it, enable GitHub Pages for this repository (Settings → Pages → deploy from the `main` branch). The app is then served at `/currency-converter/` of the Pages site.

## Exchange rates

Rates come from [ExchangeRate-API](https://www.exchangerate-api.com) (free, no key, updated daily). If that is unreachable, the app falls back to [fawazahmed0/exchange-api](https://github.com/fawazahmed0/exchange-api). Rates are cached for an hour and the saved copy keeps working offline.
