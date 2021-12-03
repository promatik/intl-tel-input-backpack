# BackpackIntlTelInput

[![Latest Version on Packagist][ico-version]][link-packagist]
[![Total Downloads][ico-downloads]][link-downloads]
[![The Whole Fruit Manifesto](https://img.shields.io/badge/writing%20standard-the%20whole%20fruit-brightgreen)](https://github.com/the-whole-fruit/manifesto)

> **// TODO: customize this description and delete this line**

This package provides XXX functionality for projects that use the [Backpack for Laravel](https://backpackforlaravel.com/) administration panel. 

More exactly, it adds X and Y so that you can easily do Z.


## Screenshots

> **// TODO: add a screenshot and delete these lines;** 
> to add a screenshot to a github markdown file, the easiest way is to
> open an issue, upload the screenshot there with drag&drop, then close the issue;
> you now have that image hosted on Github's servers; so you can then right-click 
> the image to copy its URL, and use that URL wherever you want (for example... here)

![Backpack Toggle Field Addon](https://via.placeholder.com/600x250?text=screenshot+needed)


## Installation

Via Composer

``` bash
composer require mikey-be-like/backpack-intl-tel-input
```

## Usage

> **// TODO: explain to your users how to use the functionality** this package provides; 
> we've provided an example for a Backpack addon that provides a custom field

To use the field this package provides, inside your custom CrudController do:

```php
$this->crud->addField([
    'name' => 'agreed',
    'label' => 'I agree to the terms and conditions',
    'type' => 'new_field_name',
    'view_namespace' => 'mikey-be-like.backpack-intl-tel-input::fields',
]);
```

Notice the ```view_namespace``` attribute - make sure that is exactly as above, to tell Backpack to load the field from this _addon package_, instead of assuming it's inside the _Backpack\CRUD package_.


## Overwriting

> **// TODO: explain to your users how to overwrite the functionality this package provides;**
> we've provided an example for a custom field

If you need to change the field in any way, you can easily publish the file to your app, and modify that file any way you want. But please keep in mind that you will not be getting any updates.

**Step 1.** Copy-paste the blade file to your directory:
```bash
# create the fields directory if it's not already there
mkdir -p resources/views/vendor/backpack/crud/fields

# copy the blade file inside the folder we created above
cp -i vendor/mikey-be-like/backpack-intl-tel-input/src/resources/views/fields/field_name.blade.php resources/views/vendor/backpack/crud/fields/field_name.blade.php
```

**Step 2.** Remove the vendor namespace wherever you've used the field:
```diff
$this->crud->addField([
    'name' => 'agreed',
    'type' => 'toggle',
    'label' => 'I agree to the terms and conditions',
-   'view_namespace' => 'mikey-be-like.backpack-intl-tel-input::fields'
]);
```

**Step 3.** Uninstall this package. Since it only provides one file, and you're no longer using that file, it makes no sense to have the package installed:
```bash
composer remove mikey-be-like/backpack-intl-tel-input
```

## Change log

Changes are documented here on Github. Please see the [Releases tab](https://github.com/mikey-be-like/backpack-intl-tel-input/releases).

## Testing

``` bash
composer test
```

## Contributing

Please see [contributing.md](contributing.md) for a todolist and howtos.

## Security

If you discover any security related issues, please email hi@mikey.dev instead of using the issue tracker.

## Credits

- [Michael Olukoya][link-author]
- [All Contributors][link-contributors]

## License

This project was released under MIT, so you can install it on top of any Backpack & Laravel project. Please see the [license file](license.md) for more information. 

However, please note that you do need Backpack installed, so you need to also abide by its [YUMMY License](https://github.com/Laravel-Backpack/CRUD/blob/master/LICENSE.md). That means in production you'll need a Backpack license code. You can get a free one for non-commercial use (or a paid one for commercial use) on [backpackforlaravel.com](https://backpackforlaravel.com).


[ico-version]: https://img.shields.io/packagist/v/mikey-be-like/backpack-intl-tel-input.svg?style=flat-square
[ico-downloads]: https://img.shields.io/packagist/dt/mikey-be-like/backpack-intl-tel-input.svg?style=flat-square

[link-packagist]: https://packagist.org/packages/mikey-be-like/backpack-intl-tel-input
[link-downloads]: https://packagist.org/packages/mikey-be-like/backpack-intl-tel-input
[link-author]: https://github.com/mikey-be-like
[link-contributors]: ../../contributors
