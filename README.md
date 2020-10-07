# iubenda
Cookie Solution for Magento 2.X.X
=====================

(A work in progress)

[iubenda](https://www.iubenda.com/) is a easy to use privacy and cookie policy service. This is a module which lets you use their JavaScript to embed your privacy policy into your Magento website.WordPress website.

**Important** - you will not need to use iubenda's [paid Pro service](https://www.iubenda.com/en/pricing) to use this module. This module will default to the JavaScript embedding method.

The module requests the policy using Iubenda's API, then caches the policy for 24 hours to make things speedier. The policy is then displayed whereever the tag is placed in the theme.

If the policy is a pro version, then the fallback is Iubenda's API embed.

To do
-----
Install Package from github pasticcinformatici.com

- Download the latest version https://github.com/ciratt/Ciratt_Iubenda/archive/main.zip of the module;

- Extract the module in your Magento directory:
```
unzip Ciratt_Iubenda-main.zip
```

- create the Ciratt folder, and the Iubenda subfolder, in app/code:
```
cd app/code
mkdir Ciratt
cd Ciratt
mkdir Iubenda
cd Iubenda
mv  -v ~/Ciratt_Iubenda-main/* ~/Iubenda/
```

- Run the following command in Magento 2 root folder:
```
rm -rf var/di/* var/generation/* var/cache/* var/page_cache/* var/view_preprocessed/* var/composer_home/cache/* pub/static/* generated/code/*
php bin/magento setup:upgrade
php bin/magento setup:di:compile
php bin/magento setup:static-content:deploy -f
php bin/magento indexer:reindex
php bin/magento cache:clean
php bin/magento cache:flush
```

Disclaimer
----------
And, of course, this module is in no way affiliated or endorsed by Iubenda, Magento, or Automattic.

Contact
----------
For info, questions, collaborations or support:
- email: info@pasticcinformatici.com
- telephone: +39 041 5352646
