# Migrating account data

This guide is here to show you how to export your current Ferdi setup from the online server or from an accountless session for safe keeping or transferring to a new instance using only a browser.

## Exporting

Depending on where you have your data you have to visit separate sites to retrieve it.\
This has no impact on your current instances.

### Account

If you use a Ferdi account you need to reach their servers.\
If the servers are not accessible you sadly have no other options for getting your data as there are no local copies. So it is advised to do this as soon as there's a chance just to be safe.\
If you run your own server you naturally need to replace `https://api.getferdi.com` with its own domain.

1. Open [https://api.getferdi.com/user/login](https://api.getferdi.com/user/login) in any browser.
2. Log in to your Ferdi account. (If you forgot your password you can reset it using the email address you registered with.)
3. Click on the "Import/Export account data" option then click the "Export data" button or open this link [https://api.getferdi.com/user/export](https://api.getferdi.com/user/export) in the same browser for instant access.
4. Save the `export.fedi-data` file to anywhere you'd like for safe keeping.

### Accountless


If you use Ferdi without an account then your app is running a local server to manage your data, but this does not work if you are logged in to an account.

1. Have Ferdi running on your system without an account.
2. Open [http://localhost:45569/export](http://localhost:45569/export) in any browser for instant access.
3. Save the `export.fedi-data` file to anywhere you'd like for safe keeping.

## Importing

Depending on where you'd like to import your data to you have to visit separate sites to upload it.\
Setting up new instances or migrating to an accountless setup will require all services to be logged in by hand again.\
Importing data does not override list of local services, but adds them to the current list. This is normal behavior.

### Account

Due to current risks of loosing access to Ferdi's services it is ill-advised to use their servers in the future.\
You should set up your own server while you wait for official Ferdium solutions if automatic syncing is important.\
This is just here as an example and the `https://api.getferdi.com` domain should be replaced with the appropriate alternative. 

1. Open [https://api.getferdi.com/user/transfer](https://api.getferdi.com/user/transfer) in any browser.
2. Using the File browser button find the previously saved `export.fedi-data` file on your system and click the "Import data" button.
3. Restart your application.

### Accountless

Accountless instances have all the same functionality as account based ones with the exception of multi-instance syncronization.\
If you don't intend to use this app on multiple machines with regularly changing settings and lists of services there's no benefit to having an account.\
Having a backup of your `export.fedi-data` whenever you make changes to your setup provides a similarly secure although slower alternative to automatic syncing that doesn't rely on a server's constant availability.

1. Open [http://localhost:45569/transfer](http://localhost:45569/transfer) in any browser.
2. Using the File browser button find the previously saved `export.fedi-data` file on your system and click the "Import data" button.
3. Restart your application.