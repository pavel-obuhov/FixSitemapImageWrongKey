# Magento 2 patch, fix sitemap image key

## Main Functionalities
Sometimes sitemap image url is brocken or not correct. Patch fix it.

## Installation
Before instalation need plugin cweagans/composer-patches
Add into composer.json
"extra": {
   "magento-force": "override",
   "composer-exit-on-patch-failure": true,
   "patches": {
      "magento/module-sitemap": {
         "Fix sitemap image on sitemap": "patches/imagesSitemapFixer.patch"
      }
   }
}

after that copy file imagesSitemapFixer.patch into patches/imagesSitemapFixer.patch
and 
composer.phar install

Sometimes need remove vendor directory, and 
composer.phar install
again
