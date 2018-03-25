# Magento 2 Store Switcher URL Fix

Fixes the URL used for switching to a specific store view page for which a URL rewrite exists. The issue can be observed
for URLs which have an even number of segments greater than 3 - excluding the store code segment if present
(e.g. `http://example.com/en/shop/with/multilevel/categories.html` would throw a 404 error when switching to a different
store view).

## Installation steps

1. Get the module via composer
   ```
   composer require "vladflonta/magento2-store-switcher-url-fix":"~1.0"
   ```

   or via git
   ```
   git clone https://github.com/vladflonta/magento2-store-switcher-url-fix app/code/VladFlonta/StoreSwitcherUrlFix
   ```

2. Enable module

```
bin/magento module:enable VladFlonta_StoreSwitcherUrlFix
bin/magento setup:upgrade
```

## License

This project is licensed under the [Open Software License (OSL 3.0)](http://opensource.org/licenses/osl-3.0.php)
