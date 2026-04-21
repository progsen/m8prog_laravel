# Laravel Routing – Worksheet

## 1. Route naar een Blade-view

### Uitleg
Een route kan direct een Blade-view tonen.  
De URL komt tussen de aanhalingstekens achter `Route::get()`.  
De view-naam (zonder `.blade.php`) komt in `view('...')`.

### Voorbeeld
URL: /timetable  
View: timetable.blade.php → dus invullen: about
```php

    Route::get('/timetable', function () {
        return view('timetable');
    });
```
### Opdracht
Vul in met de URL /about.  
Vul in met de view-naam about.
```php
    Route::get('________________________', function () {
        return view('________________________');
    });
```

## 2. Route naar een andere Blade-view

### Instructie
Maak een route die de URL /introduction opent en de view introduction.blade.php toont.  
Vul de juiste URL en view-naam in.
```php
    Route::get('________________________', function () {
        return view('________________________');
    });
```

## 3. Route naar een controller

### Uitleg
Een route kan ook naar een controller gaan.  
De URL komt in de eerste aanhalingstekens.  
De controller-methode komt in de tweede aanhalingstekens.
> bijvoorbeeld, url /timetable, controller TimeTableController en method (function) getTimeTable
```php
    Route::get('/timetable', [TimeTableController::class, 'getTimeTable']);
```
### Opdracht
Maak een route voor de URL /directions die de methode index van DirectionsController gebruikt.
```php
    Route::get('________________________',
    [DirectionsController::class, '________________________']);
```


## 4. Route met parameter

### Uitleg
Een parameter in de URL ziet er zo uit: `{iets}`.  
Bijvoorbeeld: /customer/12  
De controller krijgt automatisch de waarde binnen.

### Opdracht
Maak een route voor /customer/{customerId} die naar CustomerController gaat en de methode show gebruikt.
```php
    Route::get('/customer/________________________', 
    [CustomerController::class, '________________________']);
```

## 5. Named route

### Uitleg
Een named route krijgt een naam met `->name('...')`.  
Die naam kun je later gebruiken in links.

### Opdracht
Maak een route voor de URL /profile die naar `ProfileController@index` gaat en de naam `profile` krijgt.
```php
    Route::get('________________________', 
    [ProfileController::class, '________________________'])
    ->name('________________________');
```

## 6. Link naar een named route

### Uitleg
In Blade kun je linken naar een named route met `route('naam')`.

### Opdracht
Maak een link naar de named route `profile`.
```html
<a href="{{ route('________________________') }}">Ga naar profiel</a>
```

# Doe-het-zelf opdrachten

## DIY 1 – Route naar een view
Maak een route /faq die een Blade-view toont.

```
_____________________________________________________________________________________  _____________________________________________________________________________________  _____________________________________________________________________________________  _____________________________________________________________________________________ 
```
## DIY 2 – Controller-route
Maak een route /products die naar `ProductController@index` verwijst.
```
_____________________________________________________________________________________  _____________________________________________________________________________________  _____________________________________________________________________________________  _____________________________________________________________________________________ 
```
## DIY 3 – Route met meerdere parameters
Maak een route /shop/{category}/{productId}.
```
_____________________________________________________________________________________  _____________________________________________________________________________________  _____________________________________________________________________________________  _____________________________________________________________________________________ 
```
## DIY 4 – Named route + link
Maak een named route `settings.account` en een Blade-link die ernaar verwijst.
```
_____________________________________________________________________________________  _____________________________________________________________________________________  _____________________________________________________________________________________  _____________________________________________________________________________________ 
```
