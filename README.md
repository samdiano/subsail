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
   cd subsail
   ```

3. Install PHP dependencies using Composer:

   ```shell
   composer install
   ```

4. Copy the example environment file and configure it according to your environment:

   ```shell
   cp .env.example .env
   ```

5. Create an alias for Sail (optional but recommended):

   ```shell
   alias sail='bash vendor/bin/sail' 
   ```

   This step allows you to use the `sail` command directly instead of `./vendor/bin/sail`.

5. Generate the application key:

   ```shell
   sail php artisan key:generate
   ```

6. Install JavaScript dependencies using npm or Yarn:

   ```shell
   sail npm install
   ```

7. Compile the frontend assets using Vite:

   ```shell
   sail npm run dev
   ```

8. Start the Docker containers using Laravel Sail:

   ```shell
   sail up -d
   ```

10. Configure Valet to test subdomains locally:

      ```shell
      valet link
      ```

This will allow you to access subdomains by appending `{subdomain}` to `subsail.test`, e.g., `blog.subsail.test`.

11. Access the application in your browser:

    - If you're using Valet, visit [http://subsail.test](http://subsail.test) for the main domain.
    - For subdomains, use the format `http://{subdomain}.subsail.test`, e.g., [http://blog.subsail.test](http://blog.subsail.test) for the `blog` subdomain.