Datamolino Client Bundle
========================

[![Latest Stable Version](https://poser.pugx.org/cwd/datamolino-bundle/v/stable)](https://packagist.org/packages/cwd/datamolino-bundle) 
[![Total Downloads](https://poser.pugx.org/cwd/datamolino-bundle/downloads)](https://packagist.org/packages/cwd/datamolino-bundle) 
[![Latest Unstable Version](https://poser.pugx.org/cwd/datamolino-bundle/v/unstable)](https://packagist.org/packages/cwd/datamolino-bundle) 
[![License](https://poser.pugx.org/cwd/datamolino-bundle/license)](https://packagist.org/packages/cwd/datamolino-bundle)


This is a Symfony Bridge for the Datamolino Client. 

Installation:
------------
`composer require cwd/datamolino-bundle`

Usage:
------

#### Configuration
Enable the bundle in bundles.php:

```
return [
 // ...
 Cwd\DatamolinoBundle\CwdDatamolinoBundle::class => ['all' => true],
]
```

Create config/packages/cwd_datamolino.yaml:
```
cwd_datamolino:
  client_id: your_client_id
  client_secret: you_client_secret
  datamolino_host: beta.datamolino.com or app.datamolino.com
  username: your_username
  password: your_password
```


#### Authentication
```php
$datamolino = $this->get(Cwd\Datamolino\DatamolinoClient::class);

// Get a Token via password authentication
$token = $datamolino->getClient()->authenticate();

```

See client for an example of all api methods: https://github.com/cwd/datamolino-client/blob/master/README.md     
