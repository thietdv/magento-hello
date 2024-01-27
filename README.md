
<p align="center">
<a href="https://magento.com/products/magento-open-source">
<img alt="Adobe logo" height="50px" src="https://www.adobe.com/content/dam/cc/icons/Adobe_Corporate_Horizontal_Red_HEX.svg"/>
</a>
</p>

<h1 align="center">Magento Sample extension</h1>

## Installation guide

- Add repositories to composer.json under Magento root foler
```
    "repositories": [
        {
            "type": "composer",
            "url": "https://repo.magento.com/"
        },
        {
            "type": "git",
            "url": "https://github.com/{your-company}/{your-project}.git"
        }
    ],
```
- Rename auth.json.sample to auth.json
- Fill in "username" and "password" with Magento authentication keys
- Run command `composer require {your-company}/{your-project}:dev-master`<br/>
  (eg: `composer require thietdv/hello:dev-master`)
- Enable your extension `php bin/magento module:enable Thietdv_Hello`<br/><br/>
- Upgrade your Magento store `php bin/magento setup:upgrade`
- Compile dependencies `php bin/magento setup:di:compile`
- Deploy static content: `php bin/magento setup:static-content:deploy -f`

## To get [Magento authentication keys](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/prerequisites/authentication-keys.html):

- Log in to the [Commerce Marketplace](https://commercemarketplace.adobe.com/). If you don’t have an account, click <b>Register</b>.
- Click your account name in the top right of the page and select <b>My Profile</b>.
- Click <b>Access Keys</b> in the <b>Marketplace</b> tab.
