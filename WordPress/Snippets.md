# Snippets

## CSS

```json
	// WordPress
	"WordPress Theme Stylesheet Header": {
		"prefix": "wp theme header",
		"body": [
			"/**",
			" * Theme Name: ${1:Theme Name}",
			" * Description: ${1:Theme Name} ${2:Enter theme description here.}",
			" * Version: ${3:0.0.1}",
			" * Author: ${4:Author Name}",
			" * Author URI: https://${6:www.dsthedev.com}/}${11:",
			" * Theme URI: https://${6:www.dsthedev.com}/themes/${5:themename}}",
			" * }License: ${7:GNU General Public License v2 or later}",
			" * License URI: ${8:http://www.gnu.org/licenses/gpl-2.0.html}",
			" * Text Domain: ${5:themename}${12:",
			" * Tags: ${9:layouts, features, styles, etc}}",
			" *",
			" * ${10:Witty tagline that only developers will see.}",
			" *",
			" * @about https://developer.wordpress.org/themes/basics/main-stylesheet-style-css/",
			" */"
		],
		"description": "Main stylesheet for a WordPress theme."
	}
```

## PHP

```php
	// WordPress
	"Better WP Debug": {
		"prefix": "wp debug",
		"body": [
			"define('WP_DEBUG', true);",
			"define('WP_DEBUG_DISPLAY', false);",
			"ini_set('log_errors', 1);",
			"ini_set('error_log', ${2:ABSPATH . '/${1:debug-wp.log}}');",
		],
		"description": "Log WordPress errors to a custom file and location."
	},

	"WP Config Options": {
		"prefix": "wp options",
		"body": [
			"define('DISALLOW_FILE_EDIT', true);",
			"// define('DISALLOW_FILE_MODS',true);",
		],
		"description": "Customization options via the wp config file."
	},
```
