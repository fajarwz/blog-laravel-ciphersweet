# Search and Encrypt Data in Laravel with CipherSweet
This is an implementation of Encryption in Laravel with CipherSweet. A blog about this can be found here: [Search and Encrypt Data in Laravel with CipherSweet | Fajarwz](https://fajarwz.com/blog/search-and-encrypt-data-in-laravel-with-ciphersweet/).

## Installation

### Composer Packages 
```
composer install
```

## Configuration

### Create `.env` file from `.env.example`
Create `.env` from `.env.example` and customize it based on your environment.
```
cp .env.example .env
```

### Generate Laravel App Key
```
php artisan key:generate
```

### Generate an Encryption Key
```
php artisan ciphersweet:generate-key
```

### Migrate the Database Migration
```
php artisan migrate --seed
```

## Search For An Encrypted Value
Run the following script in the tinker (`php artisan tinker`):
```php
User::whereBlind('id_card_number', 'id_card_number_index', 'asdajsdjfhjfihwe')->first()
```
