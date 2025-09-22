# Laravel Task Manager

A streamlined and secure task management application built with Laravel and Blade. This project serves as a complete solution for an assessment task, allowing users to register, log in, and perform full CRUD (Create, Read, Update, Delete) operations on their own tasks.

The application has been refined to provide a focused user experience, removing unnecessary components like the dashboard and profile pages, and redirecting logged-in users directly to their task list.


*(This is an example screenshot. You can create your own and replace the link.)*

## Features

-   **User Authentication**: Secure user registration and login functionality powered by Laravel Breeze.
-   **Task Management (CRUD)**: Logged-in users can create, view, update, and delete their own tasks.
-   **Task Attributes**: Each task includes a title, description, and a status (`pending`/`done`).
-   **Data Security**: Implemented using Laravel Policies to ensure users can only access and modify their own tasks. Unauthorized access attempts are blocked with a 403 error.
-   **Clean Frontend**: A simple, functional, and responsive user interface built with Blade and Tailwind CSS.
-   **Streamlined User Flow**:
    -   The landing page automatically redirects guests to the login page.
    -   Users are redirected to their task list immediately after login.
    -   Simplified navigation with no unnecessary links.

## Tech Stack

-   **Backend**: Laravel 11
-   **Frontend**: Blade, Tailwind CSS, Alpine.js
-   **Authentication**: Laravel Breeze
-   **Database**: MySQL (configurable in `.env`)

## Setup and Installation

Follow these steps to get the project up and running on your local machine.

### 1. Prerequisites

Ensure you have the following installed on your system:
-   PHP (>= 8.2)
-   Composer
-   Node.js & npm
-   A database server (e.g., MySQL, MariaDB)

### 2. Clone the Repository

Clone this repository to your local machine. Replace `your-username` with your actual GitHub username.

```bash
git clone https://github.com/rashadamd/task-manager.git
cd task-manager-main
```

### 3. Install Dependencies

Install the required PHP and JavaScript dependencies.

```bash
# Install PHP dependencies
composer install

# Install JavaScript dependencies
npm install
```

### 4. Configure Environment

Create your environment file by copying the example file.

```bash
cp .env.example .env
```

Open the `.env` file in a text editor and configure your database connection details:

```env
DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=task_manager
DB_USERNAME=root
DB_PASSWORD=your_password
```
*(Remember to create a new database named `task_manager` or your chosen name.)*

### 5. Generate Application Key

Generate a unique application key for your project.

```bash
php artisan key:generate
```

### 6. Run Database Migrations

Create the necessary `users` and `tasks` tables in your database.

```bash
php artisan migrate
```

### 7. Compile Frontend Assets

Compile the CSS and JavaScript files for the frontend. For development, you can leave this running in a separate terminal.

```bash
npm run dev
```

### 8. Start the Development Server

Finally, start the Laravel development server.

```bash
php artisan serve
```

The application will now be available at **[http://127.0.0.1:8000](http://127.0.0.1:8000)**.

## Usage Flow

1.  Navigate to the base URL. You will be automatically redirected to the **Login** page.
2.  Click the **"Register here"** link to create a new account.
3.  After registering and logging in, you will be directed to the **"My Tasks"** page.
4.  Use the **"Add New Task"** button to create new tasks.
5.  Use the **"Edit"** and **"Delete"** actions in the task list to manage your existing tasks.