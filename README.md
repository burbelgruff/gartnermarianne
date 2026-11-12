# gartnermarianne.no

Statisk nettside for Marianne Holt, gartner på Øvre Romerike. Ingen byggesteg: `index.html`, `style.css` og `images/` blir servert som de er via GitHub Pages.

## Lokalt

```
npx serve .
```

eller åpne `index.html` direkte i nettleseren.

## Publisering

GitHub Pages publiserer `main` (rot) automatisk ved push. Domenet er satt i `CNAME`.

DNS ligger hos ProISP:

| Navn | Type | Innhold |
|---|---|---|
| `gartnermarianne.no` | A | `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153` |
| `gartnermarianne.no` | AAAA | `2606:50c0:8000::153`, `2606:50c0:8001::153`, `2606:50c0:8002::153`, `2606:50c0:8003::153` |
| `www` | CNAME | `burbelgruff.github.io` |
