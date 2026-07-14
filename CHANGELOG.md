# Changelog
## 2.0.2
### Fixed
- `Import::create()` sent its multipart payload as JSON instead of multipart form data, causing every import (e.g. bulk table sync) to fail with `json_encode error: Type is not supported` as soon as a file was included.
## 1.0.4
### What's Changed
- Caching the authorization token for 14 minutes (15 minutes is the default Actito validity)
## 1.0.3
### Added
- When creating the profile, you can now add the subscriptions
```php
$data = [
    'attributes' => [ ... ],
    'subscriptions' => [
        'Newsletter' => true,
        'Retargeting' => false,
    ],
];

Actito::profile()->updateOrCreate($data);
```
## 1.0.0 - 2022-06-03
### What's Changed
- Initial release
### Features
#### CRUD
- Profile
- Table
- Webhook
- Action

#### Others
- Send transactional email
- Send user email
- See form participation
- Import data to profile or table
