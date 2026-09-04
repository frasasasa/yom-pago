# Yom · Landing de pago

Página estática con branding Yom que redirige al checkout de dLocal Go (sin iframe).

## Configurar el link

Editá `config.js` y reemplazá `REPLACE_ME` por el link completo de pago:

```js
window.YOM_PAYMENT = {
  url: "https://checkout.dlocalgo.com/checkout/payment?..."
};
```

## Publicar en GitHub Pages

1. Creá un repo público (o usá este).
2. Subí `index.html`, `config.js`, `logo-yom.png` y `favicon.png`.
3. Settings → Pages → Source: Deploy from a branch → `main` / `/ (root)`.
4. La URL queda como `https://<user>.github.io/<repo>/`.

## Por qué no iframe

dLocal no soporta embeber el checkout en iframe. El botón hace redirect top-level, que es el flujo soportado.
