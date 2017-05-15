# Build EJBCA Server From Scratch

Usage:
./ejbca-setup

Answer questions and get a running EJBCA@Wildfly10

# Set Up

Some parameters needed to be set in script.

## Required Settings

Set your hostname (visible in Internet), database etc.

httpsserver_hostname="ejbca.example.com"
database_host="mysql"
database_name="ejbca"
database_url="jdbc:mysql://${database_host}:3306/${database_name}?characterEncoding=UTF-8"
database_driver="org.mariadb.jdbc.Driver"
database_username="ejbca"
database_password="very***bad***database***password"

## Optional Settings

Change only if you know what you are doing

WILDFLY_VERSION="10.1.0.Final"
EJBCA_VERSION="6_5.0.5"
MARIADB_CONNECTOR_VERSION="1.5.8"

## Set Up First Certificate/CA

superadmin_cn="SuperAdmin"
ca_name="ManagementCA"
BASE_DN="O=Example CA,C=DE"
ca_dn="CN=ManagementCA,${BASE_DN}"

