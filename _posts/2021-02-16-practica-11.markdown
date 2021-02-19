---
layout: post
title:  "practica11"
date:   2021-02-16 11:54:38 -0600
categories: practica
---
# Resultado 1:
### Para obtener la lista de plugins instalados en nuestro sitio WordPress podemos ejecutar:

* PS C:\Users\jesus> docker run -it --rm wpscanteam/wpscan --url http://3.236.92.160/  --enumerate p

```
_______________________________________________________________
         __          _______   _____
         \ \        / /  __ \ / ____|
          \ \  /\  / /| |__) | (___   ___  __ _ _ __ ®
           \ \/  \/ / |  ___/ \___ \ / __|/ _` | '_ \
            \  /\  /  | |     ____) | (__| (_| | | | |
             \/  \/   |_|    |_____/ \___|\__,_|_| |_|

         WordPress Security Scanner by the WPScan Team
                         Version 3.8.13
       Sponsored by Automattic - https://automattic.com/
       @_WPScan_, @ethicalhack3r, @erwan_lr, @firefart
_______________________________________________________________

[+] URL: http://3.236.92.160/ [3.236.92.160]
[+] Started: Thu Jan 14 21:56:04 2021

Interesting Finding(s):

[+] Headers
 | Interesting Entries:
 |  - Server: Apache
 |  - X-Powered-By: PHP/7.4.13
 |  - X-Mod-Pagespeed: 1.13.35.2-0
 | Found By: Headers (Passive Detection)
 | Confidence: 100%

[+] robots.txt found: http://3.236.92.160/robots.txt
 | Interesting Entries:
 |  - /wp-admin/
 |  - /wp-admin/admin-ajax.php
 | Found By: Robots Txt (Aggressive Detection)
 | Confidence: 100%

[+] XML-RPC seems to be enabled: http://3.236.92.160/xmlrpc.php
 | Found By: Direct Access (Aggressive Detection)
 | Confidence: 100%
 | References:
 |  - http://codex.wordpress.org/XML-RPC_Pingback_API
 |  - https://www.rapid7.com/db/modules/auxiliary/scanner/http/wordpress_ghost_scanner
 |  - https://www.rapid7.com/db/modules/auxiliary/dos/http/wordpress_xmlrpc_dos
 |  - https://www.rapid7.com/db/modules/auxiliary/scanner/http/wordpress_xmlrpc_login
 |  - https://www.rapid7.com/db/modules/auxiliary/scanner/http/wordpress_pingback_access

[+] WordPress readme found: http://3.236.92.160/readme.html
 | Found By: Direct Access (Aggressive Detection)
 | Confidence: 100%

[+] The external WP-Cron seems to be enabled: http://3.236.92.160/wp-cron.php
 | Found By: Direct Access (Aggressive Detection)
 | Confidence: 60%
 | References:
 |  - https://www.iplocation.net/defend-wordpress-from-ddos
 |  - https://github.com/wpscanteam/wpscan/issues/1299

[+] WordPress version 5.6 identified (Latest, released on 2020-12-08).
 | Found By: Rss Generator (Passive Detection)
 |  - http://3.236.92.160/feed/, <generator>https://wordpress.org/?v=5.6</generator>
 |  - http://3.236.92.160/comments/feed/, <generator>https://wordpress.org/?v=5.6</generator>

[+] WordPress theme in use: twentytwentyone
 | Location: http://3.236.92.160/wp-content/themes/twentytwentyone/
 | Last Updated: 2020-12-22T00:00:00.000Z
 | Readme: http://3.236.92.160/wp-content/themes/twentytwentyone/readme.txt
 | [!] The version is out of date, the latest version is 1.1
 | Style URL: http://3.236.92.160/wp-content/themes/twentytwentyone/style.css?ver=1.0
 | Style Name: Twenty Twenty-One
 | Style URI: https://wordpress.org/themes/twentytwentyone/
 | Description: Twenty Twenty-One is a blank canvas for your ideas and it makes the block editor your best brush. Wi...
 | Author: the WordPress team
 | Author URI: https://wordpress.org/
 |
 | Found By: Css Style In Homepage (Passive Detection)
 | Confirmed By: Css Style In 404 Page (Passive Detection)
 |
 | Version: 1.0 (80% confidence)
 | Found By: Style (Passive Detection)
 |  - http://3.236.92.160/wp-content/themes/twentytwentyone/style.css?ver=1.0, Match: 'Version: 1.0'

[+] Enumerating Most Popular Plugins (via Passive Methods)

[i] No plugins Found.

[!] No WPScan API Token given, as a result vulnerability data has not been output.
[!] You can get a free API token with 50 daily requests by registering at https://wpscan.com/register

[+] Finished: Thu Jan 14 21:56:12 2021
[+] Requests Done: 31
[+] Cached Requests: 7
[+] Data Sent: 7.384 KB
[+] Data Received: 213.459 KB
[+] Memory used: 241.055 MB
[+] Elapsed time: 00:00:07
```
 
# Resultado 2:
### En este ejemplo haremos uso de la API de WPScan que nos permite detectar vulnerabilidades haciendo uso de su base de datos de vulnerabilidades.
### Para poder hacer uso del servicio de la API de WPScan,es necesario registrarse en su web y obtener un TOKEN.

* PS C:\Users\jesus> docker run -it --rm wpscanteam/wpscan --url http://3.236.92.160/  --api-token 7aUhTRe0G0WB5M0R7HZLJdY4Sg4EZN7ScIZU2b6hiDI

```
_______________________________________________________________
         __          _______   _____
         \ \        / /  __ \ / ____|
          \ \  /\  / /| |__) | (___   ___  __ _ _ __ ®
           \ \/  \/ / |  ___/ \___ \ / __|/ _` | '_ \
            \  /\  /  | |     ____) | (__| (_| | | | |
             \/  \/   |_|    |_____/ \___|\__,_|_| |_|

         WordPress Security Scanner by the WPScan Team
                         Version 3.8.13
       Sponsored by Automattic - https://automattic.com/
       @_WPScan_, @ethicalhack3r, @erwan_lr, @firefart
_______________________________________________________________

[+] URL: http://3.236.92.160/ [3.236.92.160]
[+] Started: Thu Jan 14 21:57:31 2021

Interesting Finding(s):

[+] Headers
 | Interesting Entries:
 |  - Server: Apache
 |  - X-Powered-By: PHP/7.4.13
 |  - X-Mod-Pagespeed: 1.13.35.2-0
 | Found By: Headers (Passive Detection)
 | Confidence: 100%

[+] robots.txt found: http://3.236.92.160/robots.txt
 | Interesting Entries:
 |  - /wp-admin/
 |  - /wp-admin/admin-ajax.php
 | Found By: Robots Txt (Aggressive Detection)
 | Confidence: 100%

[+] XML-RPC seems to be enabled: http://3.236.92.160/xmlrpc.php
 | Found By: Direct Access (Aggressive Detection)
 | Confidence: 100%
 | References:
 |  - http://codex.wordpress.org/XML-RPC_Pingback_API
 |  - https://www.rapid7.com/db/modules/auxiliary/scanner/http/wordpress_ghost_scanner
 |  - https://www.rapid7.com/db/modules/auxiliary/dos/http/wordpress_xmlrpc_dos
 |  - https://www.rapid7.com/db/modules/auxiliary/scanner/http/wordpress_xmlrpc_login
 |  - https://www.rapid7.com/db/modules/auxiliary/scanner/http/wordpress_pingback_access

[+] WordPress readme found: http://3.236.92.160/readme.html
 | Found By: Direct Access (Aggressive Detection)
 | Confidence: 100%

[+] The external WP-Cron seems to be enabled: http://3.236.92.160/wp-cron.php
 | Found By: Direct Access (Aggressive Detection)
 | Confidence: 60%
 | References:
 |  - https://www.iplocation.net/defend-wordpress-from-ddos
 |  - https://github.com/wpscanteam/wpscan/issues/1299

[+] WordPress version 5.6 identified (Latest, released on 2020-12-08).
 | Found By: Rss Generator (Passive Detection)
 |  - http://3.236.92.160/feed/, <generator>https://wordpress.org/?v=5.6</generator>
 |  - http://3.236.92.160/comments/feed/, <generator>https://wordpress.org/?v=5.6</generator>

[+] WordPress theme in use: twentytwentyone
 | Location: http://3.236.92.160/wp-content/themes/twentytwentyone/
 | Last Updated: 2020-12-22T00:00:00.000Z
 | Readme: http://3.236.92.160/wp-content/themes/twentytwentyone/readme.txt
 | [!] The version is out of date, the latest version is 1.1
 | Style URL: http://3.236.92.160/wp-content/themes/twentytwentyone/style.css?ver=1.0
 | Style Name: Twenty Twenty-One
 | Style URI: https://wordpress.org/themes/twentytwentyone/
 | Description: Twenty Twenty-One is a blank canvas for your ideas and it makes the block editor your best brush. Wi...
 | Author: the WordPress team
 | Author URI: https://wordpress.org/
 |
 | Found By: Css Style In Homepage (Passive Detection)
 | Confirmed By: Css Style In 404 Page (Passive Detection)
 |
 | Version: 1.0 (80% confidence)
 | Found By: Style (Passive Detection)
 |  - http://3.236.92.160/wp-content/themes/twentytwentyone/style.css?ver=1.0, Match: 'Version: 1.0'

[+] Enumerating All Plugins (via Passive Methods)

[i] No plugins Found.

[+] Enumerating Config Backups (via Passive and Aggressive Methods)
 Checking Config Backups - Time: 00:00:01 <===========================================> (22 / 22) 100.00% Time: 00:00:01

[i] No Config Backups Found.

[+] WPScan DB API OK
 | Plan: free
 | Requests Done (during the scan): 2
 | Requests Remaining: 38

[+] Finished: Thu Jan 14 21:57:39 2021
[+] Requests Done: 57
[+] Cached Requests: 7
[+] Data Sent: 13.792 KB
[+] Data Received: 225.136 KB
[+] Memory used: 207.516 MB
[+] Elapsed time: 00:00:08
```

# Resultado 3:
### Para realizar un escaneo completo de un sitio WordPress podemos ejecutar:
### docker run -it --rm wpscanteam/wpscan --url http://51.77.242.168

```
_______________________________________________________________
         __          _______   _____
         \ \        / /  __ \ / ____|
          \ \  /\  / /| |__) | (___   ___  __ _ _ __ ®
           \ \/  \/ / |  ___/ \___ \ / __|/ _` | '_ \
            \  /\  /  | |     ____) | (__| (_| | | | |
             \/  \/   |_|    |_____/ \___|\__,_|_| |_|

         WordPress Security Scanner by the WPScan Team
                         Version 3.8.13
       Sponsored by Automattic - https://automattic.com/
       @_WPScan_, @ethicalhack3r, @erwan_lr, @firefart
_______________________________________________________________

[i] It seems like you have not updated the database for some time.
[?] Do you want to update now? [Y]es [N]o, default: [N]y
[i] Updating the Database ...
[i] Update completed.

[+] URL: http://egosportcenter.com/ [51.77.242.168]
[+] Started: Wed Feb  3 11:49:25 2021

Interesting Finding(s):

[+] Headers
 | Interesting Entries:
 |  - Server: Apache
 |  - X-Powered-By: PHP/5.4.16, PleskLin
 |  - P3P: CP="ALL DSP NID CURa ADMa DEVa HISa OTPa OUR NOR NAV DEM"
 | Found By: Headers (Passive Detection)
 | Confidence: 100%

[+] robots.txt found: http://egosportcenter.com/robots.txt
 | Interesting Entries:
 |  - /wp-admin/
 |  - /wp-admin/admin-ajax.php
 | Found By: Robots Txt (Aggressive Detection)
 | Confidence: 100%

[+] XML-RPC seems to be enabled: http://egosportcenter.com/xmlrpc.php
 | Found By: Link Tag (Passive Detection)
 | Confidence: 100%
 | Confirmed By: Direct Access (Aggressive Detection), 100% confidence
 | References:
 |  - http://codex.wordpress.org/XML-RPC_Pingback_API
 |  - https://www.rapid7.com/db/modules/auxiliary/scanner/http/wordpress_ghost_scanner
 |  - https://www.rapid7.com/db/modules/auxiliary/dos/http/wordpress_xmlrpc_dos
 |  - https://www.rapid7.com/db/modules/auxiliary/scanner/http/wordpress_xmlrpc_login
 |  - https://www.rapid7.com/db/modules/auxiliary/scanner/http/wordpress_pingback_access

[+] WordPress readme found: http://egosportcenter.com/readme.html
 | Found By: Direct Access (Aggressive Detection)
 | Confidence: 100%

[+] The external WP-Cron seems to be enabled: http://egosportcenter.com/wp-cron.php
 | Found By: Direct Access (Aggressive Detection)
 | Confidence: 60%
 | References:
 |  - https://www.iplocation.net/defend-wordpress-from-ddos
 |  - https://github.com/wpscanteam/wpscan/issues/1299

[+] WordPress version 4.9.16 identified (Latest, released on 2020-10-29).
 | Found By: Rss Generator (Passive Detection)
 |  - http://egosportcenter.com/feed/, <generator>https://wordpress.org/?v=4.9.16</generator>
 |  - http://egosportcenter.com/comments/feed/, <generator>https://wordpress.org/?v=4.9.16</generator>

[+] WordPress theme in use: fitpress
 | Location: http://egosportcenter.com/wp-content/themes/fitpress/
 | Readme: http://egosportcenter.com/wp-content/themes/fitpress/readme.txt
 | Style URL: http://egosportcenter.com/wp-content/themes/fitpress/style.css?ver=1.0.0
 | Style Name: Fitpress
 | Style URI: http://www.templatemonster.com/wordpress-themes.php
 | Description: Fitpress - truely multipurpose WordPress theme for real life projects. Built with love and care by T...
 | Author: Template Monster
 | Author URI: http://www.templatemonster.com/
 |
 | Found By: Css Style In Homepage (Passive Detection)
 | Confirmed By: Css Style In 404 Page (Passive Detection)
 |
 | Version: 1.0.0 (80% confidence)
 | Found By: Style (Passive Detection)
 |  - http://egosportcenter.com/wp-content/themes/fitpress/style.css?ver=1.0.0, Match: 'Version: 1.0.0'

[+] Enumerating All Plugins (via Passive Methods)
[+] Checking Plugin Versions (via Passive and Aggressive Methods)

[i] Plugin(s) Identified:

[+] cherry-search
 | Location: http://egosportcenter.com/wp-content/plugins/cherry-search/
 | Last Updated: 2019-05-07T08:57:00.000Z
 | [!] The version is out of date, the latest version is 1.1.5
 |
 | Found By: Urls In Homepage (Passive Detection)
 | Confirmed By: Urls In 404 Page (Passive Detection)
 |
 | Version: 1.1.4 (100% confidence)
 | Found By: Readme - Stable Tag (Aggressive Detection)
 |  - http://egosportcenter.com/wp-content/plugins/cherry-search/readme.txt
 | Confirmed By: Readme - ChangeLog Section (Aggressive Detection)
 |  - http://egosportcenter.com/wp-content/plugins/cherry-search/readme.txt

[+] cherry-team-members
 | Location: http://egosportcenter.com/wp-content/plugins/cherry-team-members/
 | Last Updated: 2019-05-07T10:11:00.000Z
 | [!] The version is out of date, the latest version is 1.4.6
 |
 | Found By: Urls In Homepage (Passive Detection)
 | Confirmed By: Urls In 404 Page (Passive Detection)
 |
 | Version: 1.4.5 (80% confidence)
 | Found By: Readme - Stable Tag (Aggressive Detection)
 |  - http://egosportcenter.com/wp-content/plugins/cherry-team-members/readme.txt

[+] cherry-testi
 | Location: http://egosportcenter.com/wp-content/plugins/cherry-testi/
 | Last Updated: 2019-05-07T10:56:00.000Z
 | [!] The version is out of date, the latest version is 1.1.3
 |
 | Found By: Urls In Homepage (Passive Detection)
 | Confirmed By: Urls In 404 Page (Passive Detection)
 |
 | Version: 1.1.0.5 (90% confidence)
 | Found By: Query Parameter (Passive Detection)
 |  - http://egosportcenter.com/wp-content/plugins/cherry-testi/public/assets/css/style.css?ver=1.1.0.5
 | Confirmed By: Readme - Stable Tag (Aggressive Detection)
 |  - http://egosportcenter.com/wp-content/plugins/cherry-testi/readme.txt

[+] contact-form-7
 | Location: http://egosportcenter.com/wp-content/plugins/contact-form-7/
 | Last Updated: 2020-12-17T11:42:00.000Z
 | [!] The version is out of date, the latest version is 5.3.2
 |
 | Found By: Urls In Homepage (Passive Detection)
 | Confirmed By: Urls In 404 Page (Passive Detection)
 |
 | Version: 5.0.3 (100% confidence)
 | Found By: Query Parameter (Passive Detection)
 |  - http://egosportcenter.com/wp-content/plugins/contact-form-7/includes/css/styles.css?ver=5.0.3
 |  - http://egosportcenter.com/wp-content/plugins/contact-form-7/includes/js/scripts.js?ver=5.0.3
 | Confirmed By:
 |  Readme - Stable Tag (Aggressive Detection)
 |   - http://egosportcenter.com/wp-content/plugins/contact-form-7/readme.txt
 |  Readme - ChangeLog Section (Aggressive Detection)
 |   - http://egosportcenter.com/wp-content/plugins/contact-form-7/readme.txt

[+] forget-about-shortcode-buttons
 | Location: http://egosportcenter.com/wp-content/plugins/forget-about-shortcode-buttons/
 | Latest Version: 2.1.2 (up to date)
 | Last Updated: 2020-09-28T07:30:00.000Z
 |
 | Found By: Urls In Homepage (Passive Detection)
 | Confirmed By: Urls In 404 Page (Passive Detection)
 |
 | Version: 2.1.2 (100% confidence)
 | Found By: Query Parameter (Passive Detection)
 |  - http://egosportcenter.com/wp-content/plugins/forget-about-shortcode-buttons/public/css/button-styles.css?ver=2.1.2
 | Confirmed By:
 |  Readme - Stable Tag (Aggressive Detection)
 |   - http://egosportcenter.com/wp-content/plugins/forget-about-shortcode-buttons/readme.txt
 |  Readme - ChangeLog Section (Aggressive Detection)
 |   - http://egosportcenter.com/wp-content/plugins/forget-about-shortcode-buttons/readme.txt

[+] moto-tools-integration
 | Location: http://egosportcenter.com/wp-content/plugins/moto-tools-integration/
 |
 | Found By: Urls In Homepage (Passive Detection)
 | Confirmed By: Urls In 404 Page (Passive Detection)
 |
 | The version could not be determined.

[+] motopress-content-editor
 | Location: http://egosportcenter.com/wp-content/plugins/motopress-content-editor/
 |
 | Found By: Urls In Homepage (Passive Detection)
 | Confirmed By: Urls In 404 Page (Passive Detection)
 |
 | Version: 2.4.0 (50% confidence)
 | Found By: Readme - ChangeLog Section (Aggressive Detection)
 |  - http://egosportcenter.com/wp-content/plugins/motopress-content-editor/readme.txt

[+] mp-timetable
 | Location: http://egosportcenter.com/wp-content/plugins/mp-timetable/
 | Last Updated: 2020-12-15T16:33:00.000Z
 | [!] The version is out of date, the latest version is 2.3.12
 |
 | Found By: Urls In Homepage (Passive Detection)
 | Confirmed By: Urls In 404 Page (Passive Detection)
 |
 | Version: 2.1.10 (60% confidence)
 | Found By: Query Parameter (Passive Detection)
 |  - http://egosportcenter.com/wp-content/plugins/mp-timetable/media/css/style.css?ver=2.1.10
 | Confirmed By: Readme - ChangeLog Section (Aggressive Detection)
 |  - http://egosportcenter.com/wp-content/plugins/mp-timetable/readme.txt

[+] power-builder
 | Location: http://egosportcenter.com/wp-content/plugins/power-builder/
 |
 | Found By: Urls In Homepage (Passive Detection)
 | Confirmed By: Urls In 404 Page (Passive Detection)
 |
 | The version could not be determined.

[+] uk-cookie-consent
 | Location: http://egosportcenter.com/wp-content/plugins/uk-cookie-consent/
 | Last Updated: 2019-10-31T13:38:00.000Z
 | [!] The version is out of date, the latest version is 2.3.15
 |
 | Found By: Urls In Homepage (Passive Detection)
 | Confirmed By: Urls In 404 Page (Passive Detection)
 |
 | Version: 2.3.11 (100% confidence)
 | Found By: Readme - Stable Tag (Aggressive Detection)
 |  - http://egosportcenter.com/wp-content/plugins/uk-cookie-consent/readme.txt
 | Confirmed By: Readme - ChangeLog Section (Aggressive Detection)
 |  - http://egosportcenter.com/wp-content/plugins/uk-cookie-consent/readme.txt

[+] Enumerating Config Backups (via Passive and Aggressive Methods)
 Checking Config Backups - Time: 00:00:04 <======================================================================================================================================> (22 / 22) 100.00% Time: 00:00:04

[i] No Config Backups Found.

[!] No WPScan API Token given, as a result vulnerability data has not been output.
[!] You can get a free API token with 50 daily requests by registering at https://wpscan.com/register

[+] Finished: Wed Feb  3 11:50:00 2021
[+] Requests Done: 89
[+] Cached Requests: 7
[+] Data Sent: 25.766 KB
[+] Data Received: 14.062 MB
[+] Memory used: 222.746 MB
[+] Elapsed time: 00:00:34
```
