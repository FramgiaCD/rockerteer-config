# Configuration for deploying Laravel Project using Rockerteer
- For more information and detailed usages, please refer [Rocketeer Documentation](http://rocketeer.autopergamene.eu/)
- Download all `php` files and move them into `.rocketeer` folder
```
git clone --depth=1 --branch=master git@github.com:FramgiaCD/rockerteer-config.git .rocketeer && rm -rf .rocketeer/.git
```
- You have to change some configurations in the following files:
    - `config.php` The `application_name`, `connection` host and username.
    - `remote.php` The `root_directory` (project deploy path)
    - `scm.php` The `repository` url
- Run `rocketeer setup` first, to create deploy folders in the remote server.
- SSH into the server, add necessary configurations into `.env` file inside `shared` folder.
- Run `rocketeer deploy` to start deploying.
- You should create the `storage/logs/laravel.log`, and make sure that it's permissions has been changed.
