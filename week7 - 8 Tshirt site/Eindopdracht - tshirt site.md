# Projectopdracht — Laravel T‑Shirt Website

Je gaat een T‑shirt webshop bouwen met Laravel.  
Elke T‑shirt heeft:
- 1–2 tekstregels
- 1 afbeelding
- 1 kleur
- 1 categorie

Je ontwerpt eerst de database (ERD) en bouwt daarna de modellen, controllers, views en routes volgens Laravel‑best practices.

## Requirements

- Je gebruikt een layout (Blade layout)
- Je gebruikt Eloquent ORM
- Je maakt eerst een ERD
- Je maakt modellen, views en controllers
- Je gebruikt named routes
- Je gebruikt Blade components
- Je let op joins en eager loading
- Je maakt detailpagina’s
- Je maakt lijstpagina’s:
  - T‑shirts per categorie
  - T‑shirts per kleur
- Je zorgt dat alle pagina’s naar elkaar doorlinken

## Startcategorieën

- Funny
- Sports
- Gaming
- Animals
- Quotes

## Startkleuren

- Black
- White
- Red
- Blue
- Green

# Checklist (Takenlijst van begin tot eind)

## 1. Laravel Setup
- [ ] Laravel installeren
- [ ] `.env` configureren (database, app naam, etc.)
- [ ] git repo opzetten

## 2. ERD (Entity Relationship Diagram)
- [ ] Entiteiten bepalen:
  - Tshirt
  - Category
  - Color
- [ ] Relaties bepalen:
  - Tshirt behoort tot Category
  - Tshirt behoort tot Color
- [ ] Attributen bepalen:
  - Tshirt: id, text_line_1, text_line_2, image_path, color_id, category_id
  - Category: id, name
  - Color: id, name

## 3. Migrations
- [ ] Migration & Model voor categories tabel
- [ ] Migration & Model voor colors tabel
- [ ] Migration & Model voor tshirts tabel met foreign keys
- [ ] relaties voor in de migrations gemaakt
- [ ] `php artisan migrate` uitvoeren
- [ ] Factories maken met testdata (deels via faker, categorieen en colors moeten de startwaardes hebben)
- [ ] Test data in de seeder late aanmaken
- [ ] fresh migration met seed getest

## 4. Models
- [ ] Relaties toevoegen:
  - [ ] Tshirt -> category()
  - [ ] Tshirt -> color()
  - [ ] Category -> tshirts()
  - [ ] Color -> tshirts()

## 5. Controllers
- [ ] TshirtController maken
- [ ] CategoryController maken
- [ ] ColorController maken

## 6. Routes
- [ ] Named routes aanmaken voor:
  - [ ] Alle T‑shirts
  - [ ] Detailpagina T‑shirt
  - [ ] T‑shirts per categorie
  - [ ] T‑shirts per kleur

## 7. Views
- [ ] Layoutbestand maken (app.blade.php)
- [ ] Componenten maken (bijv. card, header, footer)
- [ ] Views maken:
  - [ ] Overzicht van alle T‑shirts
  - [ ] Detailpagina van één T‑shirt
  - [ ] Lijst per categorie
  - [ ] Lijst per kleur

## 8. Eager Loading en Joins
- [ ] In controllers `with('category', 'color')` gebruiken
- [ ] Controleren dat er geen N+1 queries ontstaan

## 9. Navigatie en Doorlinken
- [ ] Menu met links naar alle pagina’s
- [ ] Klikbare T‑shirt kaarten
- [ ] Klikbare categorie‑ en kleurfilters

## 10. Testen en Afronden
- [ ] Controleren of alle pagina’s werken
- [ ] Controleren of alle links kloppen
- [ ] Controleren of detailpagina’s correct laden
- [ ] Controleren of filters correct werken
