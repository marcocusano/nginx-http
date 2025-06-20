# Laravel Installation Guide

This guide explains how to install Laravel and run the development server on port 8000.

## Prerequisites

- PHP >= 8.1
- Composer (Dependency Manager for PHP)
- A terminal or command prompt

## Steps

### 1. Install Composer

If you don't have Composer, download and install it from [getcomposer.org](https://getcomposer.org/).

### 2. Create a New Laravel Project

```bash
composer create-project laravel/laravel example-app
```

Replace `example-app` with your desired project name.

### 3. Change Directory

Navigate to your new Laravel project directory:

```bash
cd example-app
```

### 4. Start the Development Server

Run the following command to start Laravel's built-in server on port 8000:

```bash
php artisan serve --port=8000
```

### 5. Access Your Application

Open your browser and visit:

```
http://localhost:8000
```

Please refer to our NGINX configuration to know how to access your application in SSL mode:

```
https://laravel.localhost
```

You should see the Laravel welcome page.

## Additional Notes

- To stop the server, press `Ctrl + C` in your terminal.
- For more configuration, refer to the [Laravel Documentation](https://laravel.com).
