# justup
Justup is a deployment tool written in C.

Current status: **TESTING**

The project is created for simple sites, that usually don't use servers with SFTP, WebDAV or something like that, when there isn't any other way except use FTP.

#### Usage
```bash
// print list of prepared files for deploy
# justup status

// execute deploy command, delete, add and modify files on remote server
# justup push
# justup push `file1` `file2`

// apply changes without sending to server
# justup save
# justup save `file1` `file2`

// create and switch between profiles; them like branches in git/svn
# justup profile `master/dev/something_else`
```

#### Configuration file of profile

> You can find all configuration files in `.justup/` hidden folder.
> The file created automatically when you switch between profiles; master profile is default.

```ini
protocol = ftp              # At the moment available only `ftp`
host = localhost            # ftp host, domain
user = user                 # ftp user
pass = root123              # ftp password
basedir = /var/www/site/    # Path to project hosted on remote server
```

No testing. No examples.
Only clean hardcore code.


But it will be soon.

Thanks @benhoyt for small and helpful library [inih](https://github.com/benhoyt/inih) which I use to parse configuration files.
