PepoCampaigns PHP client
========================

PHP client for PepoCampaigns REST API. For details about the API, documentation and examples please visit: [https://know.pepocampaigns.com/categories/api/](https://know.pepocampaigns.com/categories/api/)

## Requirements

* PHP 5.4 or higher
* openssl 1.0.1
* TLS 1.2 protocol is recommended

## Usage

### Initiation 
	
```php	
require ("PepoCampaigns.class.php");

// key and secret to be passed while initiation
$pepo_campaigns = new PepoCampaigns(array(
	'key' => '3gd68b470d1205bd57fd4dbfa1208ab1',
    'secret' => 'e74c748409db3fae8add716fbeb315a2'
));
```    

### Example API Calls

[Creating a new list](https://know.pepocampaigns.com/articles/managing-lists-api/#creating-a-new-list)

```php	
$pepo_campaigns->create_list(array(
	'name' => 'test list2', 
	'source' => 'My Pepo Campaigns Test List2'
));
```

[Adding a contact to a List](https://know.pepocampaigns.com/articles/managing-lists-api/#adding-a-contact-to-a-list)

```php	
$pepo_campaigns->add_contact_to_list(419,
	array(
    	'email' => 'vpuui.skbbx21@gmail.com', 
    	'first_name' => 'Test2', 
    	'last_name' => 'Test2'
	)
);
```

[Removing a contact from a list](https://know.pepocampaigns.com/articles/managing-lists-api/#removing-a-contact-from-a-list)

```php
$pepo_campaigns->remove_contact_from_list(419,
	array(
		'email' => 'lcoqw.rymyo10@gmail.com'
	)
);
```

[Changing User Status](https://know.pepocampaigns.com/articles/managing-contacts-api/#changing-user-status)

```php
$pepo_campaigns->change_user_status(array(
	'email' => 'vpuui.skbbx21@gmail.com', 
	'type' => 'unsubscribe'
));
```

## License

[MIT License](LICENSE)
