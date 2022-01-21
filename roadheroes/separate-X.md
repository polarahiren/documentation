###Steps to separate system(X)

#####File related changes
- Go through each functions of `helpers.php` file and identify the functions which is using `contact_type` attribute.

- Refacor or remove all identified functions (using contact_type or identifying X) and also refactor all files accordingly where those function are used.

- `getContactType()` function is used in for class in blade files,
so, remove `getContactType()` and '-' from `'system-'.getContactType()` and update class name in the _navbar.scss : `system-carerocket` to `system` and remove other `system-` classes for other contact types.

- Copy content of `roadheroes.php` config file and move content to the system.php file. 

- Update all config values in `system.php` used from `roadheroes.php` file.
    - old value: `config('roadheroes.test')`
      new value: `config('system.test')`  
    - old value: `'road_heroes_vip_service' => 594`, `'care_rockets_vip_service' => 1260`
      new value: `'vip_service' => [1260, 594]`
    - old key: `dummy_carerocket_id`
      new key: `dummy_id`
    - old key: `dummy_driver_id`
      new key: `default_dummy_id`

- Add page related function values in `system.php` file.

- Remove all other X config values from `contacts.php`, and just unwrap X config values from X array. Update every files where this config values are used ( use new updated config string ).

- Remove all functions that is used to identify X ( isRoadheroes(), etc) and remove its usage and dependent code from whole system.

- Remove blade files for other X.

- Move all X files to its parent folder and use/update the new updated file path throughout the whole system and check wether all views are loading properly or not.
    - old files: contacts/carerocket/test/index.blade.php
      new files: contacts/test/index.blade.php

- Remove all lang files for other X.

- Update lang files values in the resources/lang folder as sp ecified in the X lang files. And then, remove X lang folder as well. Remove `contact_lang` function from the all files of the lang folder. and remove `contact_lang` function from the helpers.php file.
    - example

- Remove other X translation from `meta.php` file for each locale, and unwrap particular X meta translation from array. 

- And update meta lang path throughout the system.

- Remove sass files for other contact types, located in `resources\sass\` and `resources\sass\new-landing-page` and move X related files to its parent folder. And don't forget to remove and change sass files path in `webpack.mix.js`

- Find and remove contact type constant used in whole system.
  - eg. CONTACT_CAREROCKET, CONTACT_DRIVER, etc.

- Search for `contact_type` keyword and replace or remove code block from whole system.




#####Run Seeder to remove other contact type data from database
- Make copy of existing roadheroes database.

- Set new cloned database name in the env of project.

- Run below command
  - `php artisan db:seed --class=SeparateXSystemSeeder`
  - next, you will be asked to input `contact type` for which you want to `make separate system`.




#####Final Step, Check your system
