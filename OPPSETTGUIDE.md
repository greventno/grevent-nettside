# Grevent nettside — Oppsettguide

## Slik får du nettsiden på nett med redigerbart admin-panel

### Steg 1: Lag en GitHub-konto (gratis)
1. Gå til **github.com** og klikk "Sign up"
2. Følg stegene for å lage en konto

### Steg 2: Last opp filene til GitHub
1. Logg inn på GitHub
2. Klikk **"New repository"** (den grønne knappen)
3. Gi den navnet `grevent-nettside`
4. Velg **Public**
5. Klikk **"Create repository"**
6. Klikk **"uploading an existing file"**
7. Dra hele innholdet av `grevent-nettside`-mappen hit (alle filer og mapper)
8. Klikk **"Commit changes"**

### Steg 3: Lag en Netlify-konto og koble til GitHub
1. Gå til **app.netlify.com** og klikk "Sign up"
2. Velg **"Sign up with GitHub"** (enklest)
3. Når du er innlogget, klikk **"Add new site"** → **"Import an existing project"**
4. Velg **GitHub** og finn repositoryet `grevent-nettside`
5. La alle innstillinger stå som standard
6. Klikk **"Deploy site"**
7. Netlify gir deg en midlertidig URL (f.eks. `random-name.netlify.app`)

### Steg 4: Aktiver admin-panelet (Decap CMS)
1. I Netlify-dashboardet, gå til **Site settings** → **Identity**
2. Klikk **"Enable Identity"**
3. Under **Registration**, velg **"Invite only"**
4. Gå til **Identity** → **"Invite users"** og legg inn din e-postadresse
5. Gå til **Site settings** → **Identity** → **Services** → **Git Gateway**
6. Klikk **"Enable Git Gateway"**
7. Du får en e-post med invitasjonslenke — klikk på den og sett et passord

### Steg 5: Logg inn i admin-panelet
1. Gå til `din-side.netlify.app/admin/`
2. Logg inn med e-postadressen og passordet du satte
3. Du ser nå admin-panelet der du kan redigere alt innhold!

---

## Slik redigerer du innhold

Når du er logget inn på `/admin/`:

- **Klikk på "Rediger nettside"** for å se alle seksjoner
- Endre tekst, priser, beskrivelser direkte i feltene
- **Last opp bilder** ved å klikke på bildefeltene
- **Legg til/fjern utstyr eller pakker** med + og – knappene
- Klikk **"Publish"** (øverst) for å lagre endringene
- Endringene vises på nettsiden innen ca. 30 sekunder

---

## Valgfritt: Eget domene (grevent.no)

Hvis du vil bruke grevent.no:
1. I Netlify → **Domain settings** → **Add custom domain**
2. Skriv inn `grevent.no`
3. Oppdater DNS-innstillingene hos domeneregistraren din (f.eks. Domeneshop)
4. Netlify viser deg nøyaktig hvilke DNS-endringer du må gjøre
5. SSL-sertifikat (https) settes opp automatisk av Netlify

---

## Filstruktur

```
grevent-nettside/
├── index.html              ← Selve nettsiden
├── logo.png                ← Din logo (legg til manuelt)
├── admin/
│   ├── index.html          ← Admin-panelet
│   └── config.yml          ← CMS-konfigurasjon
├── content/
│   └── site.json           ← Alt redigerbart innhold
└── bilder/                 ← Mappe for bilder (last opp via admin)
```

## Trenger du hjelp?

Kontakt Vegard eller se Netlify sin dokumentasjon på docs.netlify.com.
