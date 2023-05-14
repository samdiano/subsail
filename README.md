# SubSail

This is a simple web application built with Laravel Sail, Vite, and Vue.js that demonstrates how subdomains can be used in a Laravel app. It allows you to test subdomains using Valet.

## Features

- Subdomain support in Laravel
- Vue.js for interactive frontend
- Laravel Sail for easy Docker-based local development
- Vite for lightning-fast frontend development

## Prerequisites

Make sure you have the following installed on your local machine:

- Docker
- Composer
- Node.js
- Valet

## Getting Started

Follow these instructions to get the application up and running on your local machine:

1. Clone the repository:

   ```shell
   git clone git@github.com:samdiano/subsail.git
   ```

2. Navigate to the project root directory:

   ```shell
   cd subdomain-app
   ```

3. Install PHP dependencies using Composer:

   ```shell
   composer install
   ```

4. Copy the example environment file and configure it according to your environment:

   ```shell
   cp .env.example .env
   ```

5. Generate the application key:

   ```shell
   php artisan key:generate
   ```

6. Install JavaScript dependencies using npm or Yarn:

   ```shell
   npm install
   ```

7. Compile the frontend assets using Vite:

   ```shell
   npm run dev
   ```

8. Start the Docker containers using Laravel Sail:

   ```shell
   ./vendor/bin/sail up -d
   ```

10. Configure Valet to test subdomains locally:

    - If you're using Valet on macOS:

      ```shell
      valet link
      ```

    - If you're using Valet on Linux:

      ```shell
      valet domain test
      ```

    This will allow you to access subdomains by appending `test` to your local domain, e.g., `subdomain.test`.

11. Access the application in your browser:

    - If you're using Valet, visit [http://subdomain.test](http://subdomain.test)
    - If you're not using Valet, visit [http://localhost](http://localhost)
