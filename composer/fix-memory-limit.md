# Fixing Memory limit issue of Composer

### Solution

- Append following text at the beginning of command

````
    COMPOSER_MEMORY_LIMIT=-1
````

### For example,

````
    COMPOSER_MEMORY_LIMIT=-1 composer require spatie/laravel-medialibrary
```` 
