# Tiimin käytännöt – AI Smarties

---

## Yleiset periaatteet

- Koodi kirjoitetaan englanniksi (muuttujat, funktiot, kommentit)
- Kommentit voi kirjoittaa suomeksi jos selkeyttää
- Nimeä kuvaavasti → koodi on dokumentaatiota
- Koodi läpäisee lintterin tarkistuksen

---

## Definition of Done

User Story on valmis kun:

- [ ] Kaikki storyn hyväksymiskriteerit täyttyvät
- [ ] Toiminnallisuus testattu staging-ympäristössä
- [ ] Koodikatselmus tehty (1 henkilö)
- [ ] Yksikkötestit kirjoitettu uudelle koodille
- [ ] Kriittiset/Virhe alttiit toiminnot testattu
- [ ] Kaikki testit menevät läpi
- [ ] Testikattavuus ≥60%

---

## Haarakäytännöt

| Haara | Tarkoitus | Säännöt |
|-------|-----------|---------|
| `main` | Tuotantokelpoinen koodi | CI vihreä, ei suoraa pushia |
| `dev` | Integraatiohaara | Kaikki feature-haarat mergetään tänne |
| `feature/*` | Uusi ominaisuus | Mergetään dev:iin PR:llä |
| `fix/*` | Bugikorjaus | Mergetään dev:iin PR:llä |

### Flow

1. Luo feature-haara: `git checkout -b feature/bluetooth-pairing`
2. Koodaa & committaa
3. Push & luo PR → `dev`
4. Code review (1 hlö)
5. Merge `dev`:iin
6. Kun `dev` toimii → merge `main`:iin

---

## Git commit -viestit

```bash
feat: add bluetooth connection
fix: resolve memory leak
test: add embedding service tests
docs: update README
```
---
