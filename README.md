# Mail Dan
## Description
A simple script to display unread mail count for one or more Google accounts. It's intended for use in a tmux topbar, but works equally well as a command prompt.

When run under OS X, the script will derive the count from the Mail app if it's running rather than hit Google's servers.

Note that the account passwords **are stored unencrypted**, so be sure to generate an app password for use, and don't use your main Google password. It remains with me to implement the secure storage of passwords on the local system.

## Usage
The script can be invoked as follows, either with or without the mail count to show you if you've got new email:

```shell
$ mail_dan
📪  0

$ mail_dan --ignore_mail_count
📪
```

To configure, create a file named `~/.mail_dan_accounts` which contains a list of Google accounts and their app specific passwords, eg:

```
your_email_1@gmail.com app_specific_password1
your_email_2@gmail.com app_specific_password2
```