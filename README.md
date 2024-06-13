# elputocarnicero.com

[![elputocarnicero.com](/assets/media/logo.png)](https://elputocarnicero.com/)


## STEPS


### Local

- If new project (not fork):
  - Copy [elputocarnicero.com project files](https://github.com/elputocarnicero/elputocarnicero.com)
  - `git submodule add https://github.com/lorensansol/sansoul.git themes/sansoul`
- Else if fork:
  - Download submódule theme files: `git submodule update --init --recursive`
- If you want use svg emojies:
  - `git submodule add https://github.com/lorensansol/sansoul-emojis.git layouts/partials/svg/emojis`
- Now you can see the run project in the browser with the `do server` comand
- `README.md` ⏩ edit baseURL ("elputocarnicero.com") + delete steps bit by bit
- Design
  - You can edit any file with the same structure of theme sansoul
  - GENERAL
    - `config.yml`
    - `data/*.{yml,md}`
  - REDIRECTS
    - `assets/redirects.md`
  - Try in Safari and Firefox
  - Check in [W3 Validator](https://validator.w3.org/)
  - Check in [PageSpeed Insights](https://pagespeed.web.dev/)


### After client validate web


#### Domain

- If Netlify
  - [`Domain Management / settings`](https://app.netlify.com/sites/elputocarnicero/settings/domain)
  - `Add custom domain`
  - `Check DNS configuration` Copy
  - Add `DNS Records` copied from Netlify to Domain gestor:
    - From: `elputocarnicero.com`
      DNS Record: `ALIAS`, `ANAME` or `flattened CNAME`
      To: `apex-loadbalancer.netlify.com`
    - From: `elputocarnicero.com`
      DNS Record: `A`
      To: `75.2.60.5`
    - From: `www`
      DNS Record: `CNAME`
      To: `elputocarnicero.netlify.app.`
    - Maybe you need to eliminate the previous records with similar names
  - `Verify DNS configuration`
  - If it does not work after a while, try `Set as main domain` in the `www` version and also in te `nowww` version


#### Forms

- If Netlify Form
  - Don't need configure nothing! Build like you want in local or with CMS
  - [`Netlify ⏩ Site ⏩ Forms ⏩ Form Notifications`](https://app.netlify.com/sites/elputocarnicero/settings/forms#form-notifications) ⏩ `Add notification ⏩ Email notification ⏩ Email to Notify`
    - `Email to notify` = Emails of collaborators that want receive submissions
    - `Custom email subject line` = `Formulario de contacto de elputocarnicero.com`
    - `Save`
  - Submissions: [`Netlify site ⏩ Forms`](https://app.netlify.com/sites/elputocarnicero/forms)


#### [Google Search Console](https://search.google.com/search-console)

- Add property
- Verify versions ⏩ `data/config.yml`
  - `google_analytics`
  - `google_site_verification`
  - `google_file_verification`
  - DNS:
    From: `@`
    DNS Record: `TXT`
    To: `google-site-verification=[google_site_verification]`
- Link with Analytics
- Add sitemap.xml


##### Delivery

Send to all collaborators next:

```
*ENTREGA WEB elputocarnicero.com:* https://seacomoseo.com/entrega/
```
