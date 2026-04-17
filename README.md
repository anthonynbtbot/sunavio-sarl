# SUNAVIO — Site web

Site vitrine de SUNAVIO SARL, bureau d'ingenierie solaire base a Marrakech.

- **Production** : https://sunavio.ma
- **Hebergement** : Cloudflare Pages (CDN mondial)
- **Back-office** : https://sunavio.odoo.com (CRM, factures, projets)

## Stack

Site statique HTML/CSS mono-page. Aucune dependance, aucun build.

- `index.html` — page unique avec toutes les sections
- `_headers` — headers de securite + cache Cloudflare Pages
- `_redirects` — redirection www vers apex
- `robots.txt` / `sitemap.xml` — SEO
- `favicon.svg` — favicon S or sur fond noir

## Deploiement

Cloudflare Pages deploie automatiquement a chaque push sur `main`.

```bash
git add .
git commit -m "feat: update content"
git push origin main
```

## Developpement local

Aucun build necessaire. Ouvrir `index.html` dans un navigateur :

```bash
python3 -m http.server 8000
# puis http://localhost:8000
```

## Domaine

- `sunavio.ma` (apex)
- `www.sunavio.ma` -> redirige vers apex

Les DNS sont geres via Cloudflare. Le certificat SSL est emis et renouvele automatiquement.

## Contacts

- Anthony NEBOUT (direction technique) : sunavio.contact@gmail.com
- Imane ZNIN (commercial) : contact.sunavio@gmail.com
