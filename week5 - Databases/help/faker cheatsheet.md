# Faker Cheatsheet (Laravel / FakerPHP)

## Basic Text
- $faker->word()
- $faker->words(3, true)
- $faker->sentence()
- $faker->sentences(3, true)
- $faker->paragraph()
- $faker->paragraphs(3, true)
- $faker->text(200)

## Names (people)
- $faker->name()
- $faker->firstName()
- $faker->lastName()

## Addresses
- $faker->address()
- $faker->streetAddress()
- $faker->city()
- $faker->country()
- $faker->postcode()

## Contact
- $faker->email()
- $faker->safeEmail()
- $faker->phoneNumber()
- $faker->url()

## Numbers
- $faker->randomDigit()
- $faker->randomDigitNotNull()
- $faker->numberBetween(1, 100)
- $faker->randomFloat(2, 0, 9999)

## Dates & Times
- $faker->date()
- $faker->time()
- $faker->dateTime()
- $faker->dateTimeBetween('-1 year', 'now')

## Commerce / Money
- $faker->randomFloat(2, 1, 999)
- $faker->currencyCode()

## Company / Business
- $faker->company()
- $faker->companySuffix()
- $faker->jobTitle()

## Internet
- $faker->userName()
- $faker->domainName()
- $faker->ipv4()
- $faker->ipv6()
- $faker->macAddress()

## Text Utilities
- $faker->lexify('??????')        // random letters
- $faker->numerify('###-###')     // random numbers
- $faker->bothify('??##??')       // letters + numbers
- $faker->unique()->lexify('????')

## Brand‑Style Names (useful for commercial projects)
- ucfirst($faker->unique()->lexify('??????'))
- ucfirst($faker->word()) . ' ' . ucfirst($faker->word())
- $faker->company()

## Boolean
- $faker->boolean()
- $faker->boolean(80)   // 80% true

## from array
 - $faker->randomElement(['Apple', 'Samsung', 'Sony']);

## Misc
- $faker->uuid()
- $faker->slug()
- $faker->colorName()
- $faker->hexColor()
- $faker->rgbColor()
