# laminas sendgrid integration

This is a small package that simplifies integrating Twilio into Laminas and Mezzio projects.

## Installation

Install this package using Composer:

```bash
composer require settermjd/laminas-twilio-integration
```

During installation, the default configuration file, _config/autoload/twilio.global.php_, will be copied to _config/autoload_, if used within a Mezzio project.
Otherwise, you will need to copy the default configuration file to the applicable directory in your project.

## Configuration

In the configuration file, replace `<<TWILIO_ACCOUNT_SID>>` and `<<TWILIO_AUTH_TOKEN>>` with your Twilio [Account SID and Auth Token](https://www.twilio.com/blog/better-twilio-authentication-csharp-twilio-api-keys) respectively.
I recommend using an [environment variable](https://www.twilio.com/blog/working-with-environment-variables-in-php), as in the following example, perhaps set using [PHP Dotenv](https://github.com/vlucas/phpdotenv).

```php
<?php

return [
    'twilio' => [
        'account_sid' => $_SERVER['TWILIO_ACCOUNT_SID'],
        'auth_token' => $_SERVER['TWILIO_AUTH_TOKEN'],
    ]
];
```