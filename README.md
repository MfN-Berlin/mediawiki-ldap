MediaWiki 1.31 with LDAP-support compiled into Php7.2, Apache and Debian stretch-slim.

Running
1. `git clone https://code.naturkundemuseum.berlin/Alvaro.Ortiz/mediawiki-ldap.git`
2. `cd mediawiki-ldap`
3. `docker build -t mediawiki-ldap .`
4. `docker-compose up -d`

To verify that it worked, do:
```
docker exec -ti mediawiki-ldap script -q -c "php /tmp/test.php" | grep LDAP
```
If it worked, the answer should be:
```
LDAP Support => enabled
Vendor Name => OpenLDAP
```