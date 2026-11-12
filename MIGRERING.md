# Migreringsplan

1. Opprett GitHub-repo og push dette prosjektet.
2. Cloudflare Dashboard → Workers & Pages → Create → Pages → Connect to Git. Velg repoet, la build command stå tom, output directory `/`.
3. Test på `*.pages.dev`-adressen og sammenlign med dagens side.
4. **E-post først:** sjekk MX/TXT-poster hos dagens DNS-leverandør. Hvis e-post ligger på domenet (ikke bare Gmail), må postene kopieres uendret til ny DNS.
5. Legg til `gartnermarianne.no` og `www` som Custom domain i Pages. Enten:
   - flytt hele DNS til Cloudflare (bytt nameservere hos domeneregistrar), eller
   - behold DNS der den er og pek A/CNAME mot Pages (apex krever CNAME-flattening/ALIAS).
6. Senk TTL på gamle poster 24 timer før bytte. Vent på at SSL-sertifikatet blir aktivt.
7. La WordPress-hosten stå i noen uker som backup, og si den opp etterpå.
8. Redirects fra gamle WordPress-URL-er (`/feed/`, `/wp-json/`) trengs ikke, siden siden bare har én side.
