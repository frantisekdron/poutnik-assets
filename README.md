# poutnik-assets

Statické těžké soubory webu autapoutnik.cz (hero videa, fotogalerie vozů, PDF dokumenty), servírované přes GitHub Pages:
`https://frantisekdron.github.io/poutnik-assets/<cesta>`.

Důvod: build webu v Lovable měl 56 MB a publish padal na nahrávání na CDN. Web se na tyto soubory odkazuje přes `src/lib/assets.ts` (konstanta `ASSET_BASE`).

- `video/` — hero videa (3 střihy × AV1/VP9/H.264) + WebP postery
- `galerie/<slug>/` — fotky vozů 4:3, 1400 a 700 px
- `dokumenty/` — PDF ke stažení (VOP, řády, návody…) — generují se v repu `poutnik` z `docs/dokumenty/*.html`

Nasazení: `git add -A && git commit -m "…" && git push` (Pages z větve `main`, kořen).
