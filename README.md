# PTJ (UAT) — ElectroVerde Go-To-Market Kit

Acest folder conține materiale “ready-to-ship” pentru oportunitatea PTJ (UAT): landing page + one-pagers + checklist REA + instrucțiuni de publicare și export PDF.

## Conținut recomandat în repo

```text
ptj/
  README.md
  landing/
    index.html
  pdf-src/
    one-pager-ultra.md
    one-pager-executive.md
    checklist-rea.md
  assets/
    electroverde-ptj-one-pager.pdf
    electroverde-ptj-checklist-rea.pdf
```

> Notă: `assets/` conține PDF-urile finale folosite de landing page. `pdf-src/` conține sursele în Markdown.

---

## Cum exportăm Markdown → PDF (rapid și “curat”)

### Varianta A (cea mai simplă): Google Docs / Word
1. Copiază conținutul din fișierul `.md` (ex: `pdf-src/checklist-rea.md`).
2. Paste în Google Docs / Word.
3. Ajustează minimal:
   - Font: Inter/Calibri/Arial
   - H1: 18–20, H2: 14–16, text: 11–12
   - Spațiere: 1.1–1.15
4. Export:
   - **File → Download → PDF (.pdf)**

### Varianta B (dev-friendly): Markdown → PDF cu tool
- Poți folosi `pandoc` sau un generator (ex: md-to-pdf).
- Recomandare: păstrează PDF-ul sub **1–2 MB**.

---

## Landing page: publicare & configurare

### Path recomandat
- `electroverde.ro/ptj` **sau**
- `ptj.electroverde.ro` (ideal pentru separare)

### Fișiere
- Landing: `ptj/landing/index.html`
- PDF-uri: `ptj/assets/*.pdf`

### Setare linkuri PDF în landing
În `index.html` caută secțiunea `#downloads` și actualizează:
- `/assets/electroverde-ptj-one-pager.pdf`
- `/assets/electroverde-ptj-checklist-rea.pdf`

> Dacă host-ul folosește alt folder public (ex: `/public/assets/`), ajustează linkurile.

---

## Formular lead-uri (fără mailto)

Landing page-ul este pregătit pentru **Netlify Forms** (default).

### Netlify Forms (recomandat)
1. Publică landing page-ul pe Netlify.
2. Asigură-te că form-ul are:
   - `data-netlify="true"`
   - `name="ptj-leads"`
   - `<input type="hidden" name="form-name" value="ptj-leads" />`
3. În Netlify Dashboard:
   - Site → **Forms** → vei vedea `ptj-leads`
4. Setează notificări:
   - Email notifications (sau Slack/Zapier dacă folosești)

### Redirect după submit
Form-ul are `action="/thanks/"`.
Opțiuni:
- Creezi o pagină `thanks/index.html` (simplă)  
sau
- elimini `action` și folosești JS pentru mesaj de success inline.

### Alternative rapide
#### Formspree
Înlocuiești atributul `action`:
- `action="https://formspree.io/f/XXXXYYYY"`
și păstrezi `method="POST"`.

#### HubSpot / Zoho
- Generezi embed code din CRM și îl pui în locul form-ului din landing.
- Beneficiu: lead-ul intră direct în pipeline, scoring și automatizări.

---

## Checklist REA — cum îl folosiți în proces

### Workflow recomandat
1. UAT completează `Checklist REA` (1 pagină) + atașează:
   - poze acoperiș / tablouri / contor
   - consum (ideal 12 luni)
2. ElectroVerde livrează în 5 zile:
   - 2 scenarii (minim / optim)
   - buget orientativ (interval)
   - timeline implementare
   - riscuri și pași următori
3. Se programează un call de 15 minute pentru clarificări și next steps.

### “Definition of Done” pentru REA
- minim 2 clădiri definite
- consum (sau estimare) inclus
- existența/absența camerei tehnice menționată
- riscuri notate explicit (acoperiș / umbre / racordare)

---

## Update policy (ca să nu vă încurcați în versiuni)

### Convenție versiuni
- one-pagers: `v1.0`, `v1.1` etc.
- landing: `v2`, `v2.1` etc.

### Când actualizăm
- la schimbări oficiale de ghid / calendar
- la feedback din teren (UAT întreabă același lucru de 3 ori → îl adăugăm în copy)

---

## Checklist final înainte de publicare

- [ ] Linkurile PDF funcționează pe mobil
- [ ] Formularul trimite lead-uri (test cu 2 submit-uri)
- [ ] Butoanele sunt tap-friendly (min 44px)
- [ ] Pagina se vede ok pe iPhone + Android (Chrome/Safari)
- [ ] Titlu + description sunt relevante (SEO basic)
- [ ] Contactele sunt reale (telefon/email)

---

## Owner & responsabilități (intern)
- Owner GTM (vânzare UAT): ______________________
- Owner tehnic (REA + dimensionare): ______________________
- Owner marketing (landing + PDF): ______________________
- Owner bid/procurement (SEAP + oferte): ______________________

---

## Note
Acest kit este conceput pentru a păstra comunicarea:
- clară (executive-friendly)
- trasabilă (audit-friendly)
- eficientă (time-to-first-assessment în 5 zile)