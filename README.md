# Laravel Backup Example
This example repository shows, how to store Laravel backups on local storage,
Google Drive, and Dropbox.


## Video Tutorials
1. [Set up Automatic DB Backup in Laravel](https://www.youtube.com/watch?v=tKu7EqGgu_A)
2. [Store Automatic Laravel Backup On Google Drive](https://www.youtube.com/watch?v=6kxXkrlRuJU)
3. [Store Automatic Laravel Backup On Dropbox](https://www.youtube.com/watch?v=hgcg8vDFJq0)


## How To Use This?

Download or clone this repo
```shell
$ git clone https://github.com/qirolab/laravel-fortify-example.git
```

Install all dependency required by Laravel.
```shell
$ composer install
```

Generate app key, configure `.env` file and do migration.
```shell
# create copy of .env
$ cp .env.example .env

# create Laravel key
$ php artisan key:generate

# run migration
$ php artisan migrate
```

## Configuration for Google drive
For Google drive backup, you need to provide these following variables in the `.env` file.

```
GOOGLE_DRIVE_CLIENT_ID=xxx.apps.googleusercontent.com
GOOGLE_DRIVE_CLIENT_SECRET=xxx
GOOGLE_DRIVE_REFRESH_TOKEN=xxx
GOOGLE_DRIVE_FOLDER_ID=null
```

To get the values for all these environment variables follow the steps mentioned
this article:
- **[Setup Laravel Backup On Google Drive](https://qirolab.com/posts/how-to-setup-laravel-backup-on-google-drive-1607368130)**

## Configuration for Dropbox
For Dropbox, add the following variable in the `.env` file.

```
DROPBOX_AUTH_TOKEN=xxx
```
Follow the steps on this article to get its value:

- **[Store Laravel backup on Dropbox](https://qirolab.com/posts/how-to-store-laravel-backup-on-dropbox-1607451784)**

## Take backups
```
php artisan backup:run
```
