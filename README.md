<<<<<<< HEAD
<p align="center"><a href="https://laravel.com" target="_blank"><img src="https://raw.githubusercontent.com/laravel/art/master/logo-lockup/5%20SVG/2%20CMYK/1%20Full%20Color/laravel-logolockup-cmyk-red.svg" width="400" alt="Laravel Logo"></a></p>

<p align="center">
<a href="https://github.com/laravel/framework/actions"><img src="https://github.com/laravel/framework/workflows/tests/badge.svg" alt="Build Status"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://img.shields.io/packagist/dt/laravel/framework" alt="Total Downloads"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://img.shields.io/packagist/v/laravel/framework" alt="Latest Stable Version"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://img.shields.io/packagist/l/laravel/framework" alt="License"></a>
</p>

## About Laravel

Laravel is a web application framework with expressive, elegant syntax. We believe development must be an enjoyable and creative experience to be truly fulfilling. Laravel takes the pain out of development by easing common tasks used in many web projects, such as:

- [Simple, fast routing engine](https://laravel.com/docs/routing).
- [Powerful dependency injection container](https://laravel.com/docs/container).
- Multiple back-ends for [session](https://laravel.com/docs/session) and [cache](https://laravel.com/docs/cache) storage.
- Expressive, intuitive [database ORM](https://laravel.com/docs/eloquent).
- Database agnostic [schema migrations](https://laravel.com/docs/migrations).
- [Robust background job processing](https://laravel.com/docs/queues).
- [Real-time event broadcasting](https://laravel.com/docs/broadcasting).

Laravel is accessible, powerful, and provides tools required for large, robust applications.

## Learning Laravel

Laravel has the most extensive and thorough [documentation](https://laravel.com/docs) and video tutorial library of all modern web application frameworks, making it a breeze to get started with the framework. You can also check out [Laravel Learn](https://laravel.com/learn), where you will be guided through building a modern Laravel application.

If you don't feel like reading, [Laracasts](https://laracasts.com) can help. Laracasts contains thousands of video tutorials on a range of topics including Laravel, modern PHP, unit testing, and JavaScript. Boost your skills by digging into our comprehensive video library.

## Laravel Sponsors

We would like to extend our thanks to the following sponsors for funding Laravel development. If you are interested in becoming a sponsor, please visit the [Laravel Partners program](https://partners.laravel.com).

### Premium Partners

- **[Vehikl](https://vehikl.com)**
- **[Tighten Co.](https://tighten.co)**
- **[Kirschbaum Development Group](https://kirschbaumdevelopment.com)**
- **[64 Robots](https://64robots.com)**
- **[Curotec](https://www.curotec.com/services/technologies/laravel)**
- **[DevSquad](https://devsquad.com/hire-laravel-developers)**
- **[Redberry](https://redberry.international/laravel-development)**
- **[Active Logic](https://activelogic.com)**

## Contributing

Thank you for considering contributing to the Laravel framework! The contribution guide can be found in the [Laravel documentation](https://laravel.com/docs/contributions).

## Code of Conduct

In order to ensure that the Laravel community is welcoming to all, please review and abide by the [Code of Conduct](https://laravel.com/docs/contributions#code-of-conduct).

## Security Vulnerabilities

If you discover a security vulnerability within Laravel, please send an e-mail to Taylor Otwell via [taylor@laravel.com](mailto:taylor@laravel.com). All security vulnerabilities will be promptly addressed.

## License

The Laravel framework is open-sourced software licensed under the [MIT license](https://opensource.org/licenses/MIT).
=======
# Dynamic Task Widget

A full-stack Laravel application featuring a task management widget with real-time AJAX interactions.

## Features

-   ✅ User authentication (Laravel Breeze)
-   ✅ Create tasks without page reload
-   ✅ Toggle task completion status
-   ✅ Real-time UI updates
-   ✅ Responsive design (Tailwind CSS)
-   ✅ RESTful API
-   ✅ Secure CSRF protection

## Tech Stack

-   **Backend**: Laravel 12.x,
-   **Frontend**: Blade Templates, Vanilla JavaScript
-   **Database**: SQLite (or MySQL)
-   **Authentication**: Laravel Breeze

## Installation

### Prerequisites

-   PHP 8.2 or higher
-   Composer
-   Node.js & NPM
-   SQLite or MySQL

### Setup Steps

1. **Clone the repository**

```bash
   https://github.com/MohamedSalamaMousa/Dynamic-Task-Widget-.git
   cd Dynamic-Task-Widget
```

2. **Install dependencies**

```bash
   composer install
   npm install
```

3. **Environment setup**

```bash
   cp .env.example .env
   php artisan key:generate
```

4. **Database setup**

    For SQLite:

```bash
   touch database/database.sqlite
```

Update `.env`:

```
   DB_CONNECTION=sqlite
```

5. **Run migrations**

```bash
   php artisan migrate
```

6. **Build assets**

```bash
   npm run build
```

7. **Start the server**

```bash
   php artisan serve
```

8. **Access the application**
    - URL: http://127.0.0.1:8000
    - Register a new account
    - Navigate to Dashboard

## API Endpoints

| Method | Endpoint      | Description            |
| ------ | ------------- | ---------------------- |
| GET    | `/tasks`      | Fetch all user tasks   |
| POST   | `/tasks`      | Create a new task      |
| PUT    | `/tasks/{id}` | Toggle task completion |

## Demo Video

Watch the full demonstration: [demo-video.mp4](./demo-video.mp4)

## Project Structure

```
app/
├── Http/Controllers/
│   └── TaskController.php    # Task CRUD operations
├── Models/
│   ├── Task.php              # Task model
│   └── User.php              # User model with tasks relationship
database/
└── migrations/
    └── xxxx_create_tasks_table.php
resources/
└── views/
    └── dashboard.blade.php   # Main task widget UI
routes/
└── web.php                   # Application routes
```

## Testing

### Manual Testing Checklist

-   [x] User registration and login
-   [x] Tasks load on page load (AJAX GET)
-   [x] Add task without page reload (AJAX POST)
-   [x] Toggle task completion (AJAX PUT)
-   [x] Visual feedback (line-through, grey text)
-   [x] Only user's tasks are visible
-   [x] Input validation works

### Browser DevTools Testing

1. Open DevTools (F12) → Network tab
2. Add a task → Verify POST request to `/tasks`
3. Toggle checkbox → Verify PUT request to `/tasks/{id}`
4. All requests should return 200/201 status

## Features Demonstrated

1. **Database Layer**

    - Migration with proper foreign keys
    - Eloquent relationships (User hasMany Tasks)

2. **Backend API**

    - RESTful controller methods
    - Authentication middleware
    - Request validation
    - JSON responses

3. **Frontend**

    - AJAX GET for loading tasks
    - AJAX POST for creating tasks
    - AJAX PUT for updating tasks
    - Dynamic UI updates
    - No page reloads

4. **Security**
    - CSRF protection
    - User authorization
    - SQL injection prevention (Eloquent ORM)
    - XSS prevention (HTML escaping)

## License

Open-source. Free to use for learning purposes.

## Author

[Your Name]

## Acknowledgments

Built as part of a technical assessment to demonstrate full-stack Laravel development skills.
>>>>>>> 60955b1 (video)
