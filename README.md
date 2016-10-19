# intercom-laravel
Laravel 5.x Wrapper for Intercom API forked from Alex Slaughter repo https://github.com/slaughter550/intercom-laravel

## Installation

Using Composer:
```json
{
    "repositories": [
        {
            "type": "vcs",
            "url": "https://github.com/massreuy/intercom-laravel"
        }
    ],
    "require": {
        "massreuy/intercom-laravel": "~1.1"
    }
}
```

## Configuration
config/app.php
```php
'providers' => [
    'Shadow\IntercomLaravel\ServiceProvider',
],
'aliases' => [
    'Intercom' => 'Shadow\IntercomLaravel\Facade',
],
```

config/services.php
```php
'intercom' => [
    'app_id' => 'appIdGoesHere',
    'api_key' => 'apiKeyGoesHere',
],
```

## Usage
```php
// Create/update a user
Intercom::users()->create([
    'email' => 'test@intercom.io'
]);
```
