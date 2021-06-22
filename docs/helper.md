# Хелпер для IPGeobase

При установке библиотеки она создает две таблицы: #__lib_ipgeobase_cities и #__lib_ipgeobase_regions. Там хранятся спарсенные города и регионы из библиотеки, для более эффективного доступа к названиям.

### Требуется
Чтобы работал код, который ниже будет применяться, вам требуется загрузить класс хелпера.
Как загрузить
```php
JLoader::register('JIpgeobase', JPATH_ROOT . '/libraries/ipgeobase/ipgeobase.php');
```


### Получение названия города и региона из IP
```php
$ip = '0.0.0.0';
$address = JIpgeobase::get($ip);
echo $address['city'];
echo $address['region'];
```


### Получение названия города из ID
```php
$id = 1;
$city = JIpgeobase::getCityFromId($id);
```


### Получение города и региона из ip
```php
$id = 1;
$city = JIpgeobase::getRegionFromId($id);
```


### Получение ID города из названия
```php
$title = 'москва';
$id = JIpgeobase::getIdFromCity($title);
```


### Получение ID региона из названия
```php
$region = 'московская область';
$id = JIpgeobase::getIdFromRegion($region);
```