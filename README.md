Connect to Jira via Curl

### Usage

#### Composer
First add the following to your `composer.json` file:
```json
"require": {
  "srag/jiracurl": ">=0.1.0"
},
```

If your plugin should support ILIAS 5.2 or earlier you need to require `ilCurlConnection` like follow in your `composer.json` file:
```json
"autoload": {
    "classmap": [
      "../../../../../../../Services/WebServices/Curl/classes/class.ilCurlConnection.php",
```
May you need to adjust the relative `ilCurlConnection` path

And run a `composer install`.

If you deliver your plugin, the plugin has it's own copy of this library and the user doesn't need to install the library.

Tip: Because of multiple autoloaders of plugins, it could be, that different versions of this library exists and suddenly your plugin use an older or a newer version of an other plugin!

So I recommand to use [srag/librariesnamespacechanger](https://packagist.org/packages/srag/librariesnamespacechanger)

### Dependencies
* PHP >=7.0
* [composer](https://getcomposer.org)
* [srag/dic](https://packagist.org/packages/srag/dic)

Please use it for further development!

### Adjustment suggestions
* Adjustment suggestions by pull requests on https://git.studer-raimann.ch/ILIAS/Plugins/JiraCurl/tree/develop
* Adjustment suggestions which are not yet worked out in detail by Jira tasks under https://jira.studer-raimann.ch/projects/LJIRACURL
* Bug reports under https://jira.studer-raimann.ch/projects/LJIRACURL
* For external users please send an email to support-custom1@studer-raimann.ch

### Development
If you want development in this library you should install this library like follow:

Start at your ILIAS root directory
```bash
mkdir -p Customizing/global/libraries
cd Customizing/global/libraries
git clone -b develop git@git.studer-raimann.ch:ILIAS/Plugins/JiraCurl.git JiraCurl
```
