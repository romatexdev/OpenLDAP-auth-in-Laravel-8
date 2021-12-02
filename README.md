<p align="center"><a href="https://laravel.com" target="_blank"><img src="https://raw.githubusercontent.com/laravel/art/master/logo-lockup/5%20SVG/2%20CMYK/1%20Full%20Color/laravel-logolockup-cmyk-red.svg" width="400"></a></p>

<p align="center">
<a href="https://travis-ci.org/laravel/framework"><img src="https://travis-ci.org/laravel/framework.svg" alt="Build Status"></a>
</p>

Laravel 8 with LdapRecord framework in OpenLDAP settings

## Setup

 1. Clone the project
 2. Change in the project folder
 3. Run `composer install`
 4. Copy the `.env.example` to `.env`
 5. Setup the your database in the `.env` file
 6. Add these lines at the end of the `.env` file  
```
LDAP_LOGGING=true
LDAP_CONNECTION=default
LDAP_HOST=ldap.forumsys.com
LDAP_USERNAME=null
LDAP_PASSWORD=null
LDAP_PORT=389
LDAP_BASE_DN="dc=example,dc=com"
LDAP_TIMEOUT=5
LDAP_SSL=false
LDAP_TLS=false
```
 7. Run `php artisan key:generate`
 8. Run `php artisan migrate`
 10. Open site and login with username `einstein` and password `password` (Check [Online LDAP Test Server](https://www.forumsys.com/tutorials/integration-how-to/ldap/online-ldap-test-server/) for more information of the Online LDAP Test Server)
 
 ### If you want to import all ldap users run `php artisan ldap:import users`
