# KeyCloak-UserCreation

## [import-users.sh](./import-users.sh) - Administer Keycloak accounts from the command-line
See [users.csv](./users.csv) for example format.
### Prerequisites in the Keycloak realm:
1. Create client (eg. keycloak_acct_admin) for this script. Access Type: public. & Turn On Direct Access Grants
1. Add the realm admin user (eg. realm_admin) to the realm
1. In the realm admin user's settings > Clients > "keycloak_acct_admin" > Rolese, assign it all available roles (specifically view-users & manage-users)
1. Add an admin user to the Real, That admin user will be used by This shell script to create Users.

### Import users found in csv
```sh
$ ./import-users.sh --import users.csv
```

### Delete users found in csv
```sh
$ ./import-users.sh --delete users.csv
```
