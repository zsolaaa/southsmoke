# SouthSmoke — Projekt kontextus

Egyetlen fájl: `index.html`. Nincs build tool, nincs framework. Statikus HTML/CSS/JS, GitHub Pages-en fut (`master` branch, gyökér).

**GitHub repo:** https://github.com/zsolaaa/southsmoke.git  
**Deploy:** git push origin master → automatikusan él

---

## Fájl struktúra (`index.html`)

| Sor | Tartalom |
|-----|----------|
| 1–7 | HTML head, Google Fonts (Anton + Montserrat 500/600/700) |
| 8–330 | `<style>` — összes CSS |
| 334–345 | `<nav id="nav">` — navbar |
| 347–368 | `<header class="hero">` — hero szekció |
| 370–398 | `<section id="services">` — szolgáltatások |
| 400–425 | `<section id="why">` — USP (Miért minket?) |
| 427–437 | `<section id="gallery">` — galéria |
| 439–476 | `<section id="contact">` — kapcsolat + form |
| 478–489 | `<footer>` |
| 491–598 | `<script>` — füst animáció, navbar scroll, hamburger JS, reveal, form |

---

## CSS token-ek (`:root`)

```css
--bg:          oklch(12% 0.008 30)   /* fő háttér, majdnem fekete */
--surface:     oklch(17% 0.010 28)   /* section-alt háttér */
--surface-low: oklch(14% 0.009 29)   /* section-dark háttér */
--ember:       oklch(60% 0.20 34)    /* narancs — fő akcentus */
--ember-dim:   oklch(50% 0.18 32)    /* halványabb narancs */
--coal:        oklch(45% 0.22 22)    /* sötét vörös */
--ash:         oklch(78% 0.005 32)   /* szöveg szín */
--ash-bright:  oklch(96% 0.004 32)   /* fehér közeli */
--smoke:       oklch(52% 0.008 30)   /* másodlagos szöveg */
--outline:     oklch(28% 0.012 29)   /* border szín */
--ease-out:    cubic-bezier(0.23, 1, 0.32, 1)
```

---

## Tipográfia

**Fontok:** Anton (display/heading, uppercase), Montserrat (min. 500 weight, body/label)

**Skála osztályok** (`.f-display`-jel kombinálva):
- `.f-xl` — `clamp(4.5rem, 12vw, 10rem)`
- `.f-lg` — `clamp(2.75rem, 5.5vw, 5.5rem)`
- `.f-md` — `clamp(1.75rem, 3vw, 2.75rem)`
- `.f-sm` — `clamp(1.25rem, 2vw, 1.75rem)`
- `.f-label` — Montserrat 700, 0.75rem, 0.12em tracking, uppercase
- `.f-display` — Anton, uppercase, `line-height: 0.93`, `letter-spacing: 0.01em`

---

## Navbar

**Fontos:** A nav CSS szelektora `#nav` (ID), NEM `nav` tag — mert a footer is `<nav>` és a tag selector mindkettőre vonatkozott volna.

```html
<nav id="nav">
  <a href="#" class="nav-logo">South Smoke Barbecue</a>
  <div class="nav-links" id="navLinks">
    <a href="#services">Szolgáltatások</a>
    <a href="#gallery">Galéria</a>
    <a href="#contact">Kapcsolat</a>
  </div>
  <button class="nav-burger" id="burger">...</button>
</nav>
```

- Asztali: logo bal, linkek jobb (`margin-left: auto` a `.nav-links`-en)
- Mobil (`max-width: 860px`): `.nav-links { display: none }`, `.nav-burger { display: flex }`
- Hamburger JS: `navLinks.classList.toggle('open')` + `burger.classList.toggle('open')`

---

## Szekció-szintű konvenciók

- `.section` — `padding: clamp(5rem, 10vw, 9rem) clamp(1.5rem, 5vw, 4rem)` (vízszintes padding = nav padding = hero padding)
- `.section-alt` → `background: var(--surface)` (USP szekció)
- `.section-dark` → `background: var(--surface-low)` (contact szekció)
- `.reveal` + `.reveal.in` — IntersectionObserver fade-in animáció

---

## Képek

| Fájl | Hol |
|------|-----|
| `hero.png` | Hero desktop háttér |
| `mobilhero.png` | Hero mobil (`<source media="(max-width: 860px)">`) |
| `szószok.png` | 02 szolgáltatás (BBQ szószok) |
| `722384697_...jpg` | Galéria g1 (nagy bal) |
| `723197065_...jpg` | Galéria g2 (nagy jobb) |
| `158635465_...jpg` | Galéria g3 |
| `159475287_...jpg` | Galéria g4 |
| `hambi.jpg` | Galéria g5 |
| `720010473_...jpg` | 01 szolgáltatás (rendezvény) |

---

## Design korlátok (DESIGN.md-ből)

- Lekerekített sarkak tilosak (`border-radius: 0` mindenütt)
- Montserrat min. 500 weight (400 tilos, "vékony" hatás)
- `border-left` > 1px mint dekoráció tilos
- Gradient szöveg tilos (`background-clip: text`)
- Minden szín OKLCH

---

## Preview szerver

`.claude/launch.json` konfigurálva: `python -m http.server 8765` a projekt gyökerében.
