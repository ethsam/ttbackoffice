# ttbackoffice
php -S 127.0.0.1:8888 -t public -d display_errors=1

composer update "symfony/*" --with-all-dependencies

php bin/console do:sc:cr
php bin/console doctrine:schema:create

php bin/console do:fi:lo -n
php bin/console doctrine:fixtures:load -n
