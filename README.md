# Laravel Hackathon Starter Installation

<a name="installing-laravel"></a>
### Installing Laravel Hackathon Installer

#### Via Laravel Hackathon Starter Installer

First, download the Laravel Hackathon Starter Pack Installer using Composer:

    composer global require "unicodeveloper/hackathon-installer"

Make sure to place the `~/.composer/vendor/bin` directory (or the equivalent directory for your OS) in your PATH so the `larathon` executable can be located by your system.

Once installed, the `larathon new` command will create a fresh Laravel Hackathon Starter Pack installation in the directory you specify. For instance, `larathon new mvp` will create a directory named `mvp` containing a fresh Laravel Hackathon Starter Pack installation with all of it's dependencies already installed. This method of installation is much faster than installing via Composer:

    larathon new mvp

#### Via Composer Create-Project

Alternatively, you may also install Laravel Hackathon Starter Pack by issuing the Composer `create-project` command in your terminal:

    composer create-project --prefer-dist unicodeveloper/laravel-hackathon-starter hotel

<a name="configuration"></a>
### Configuration

All of the configuration files for the Laravel framework are stored in the `config` directory. Each option is documented, so feel free to look through the files and get familiar with the options available to you.

#### Directory Permissions

After installing Laravel, you may need to configure some permissions. Directories within the `storage` and the `bootstrap/cache` directories should be writable by your web server or Laravel will not run. If you are using the [Homestead](/docs/{{version}}/homestead) virtual machine, these permissions should already be set.

#### Application Key

The next thing you should do after installing Laravel Hackathon Starter is set your application key to a random string. If you installed Laravel via Composer or the Hackathon installer, this key has already been set for you by the `php artisan key:generate` command. Typically, this string should be 32 characters long. The key can be set in the `.env` environment file. If you have not renamed the `.env.example` file to `.env`, you should do that now. **If the application key is not set, your user sessions and other encrypted data will not be secure!**