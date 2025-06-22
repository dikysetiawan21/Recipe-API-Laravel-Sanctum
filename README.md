# Food Recommendation API 🍽️

## 🚀 About The Project

Food Recommendation API is a powerful Laravel-based backend service that provides intelligent food recommendations based on various factors like mood, occasion, dietary restrictions, and weather conditions. This API helps users discover perfect meal suggestions tailored to their current situation and preferences.

### ✨ Features

- **Personalized Food Recommendations**: Get food suggestions based on multiple parameters
- **Comprehensive Food Database**: Detailed food information including ingredients, preparation time, and nutritional values
- **Multi-factor Filtering**: Filter by category, cuisine type, dietary restrictions, mood, occasion, and weather conditions
- **User Authentication**: Secure JWT-based authentication system
- **RESTful API**: Clean and consistent API endpoints following REST principles
- **Search Functionality**: Search foods by name, ingredients, or tags
- **Responsive Design**: Optimized for both web and mobile applications

## 🛠️ Built With

- **Backend Framework**: Laravel 12
- **Authentication**: JWT (JSON Web Tokens)
- **Database**: SQLite (can be configured for MySQL/PostgreSQL)
- **API Documentation**: OpenAPI/Swagger (recommended for future implementation)
- **Validation**: Laravel's built-in validation system

## 🚀 Getting Started

### Prerequisites

- PHP 8.2 or higher
- Composer (Dependency Manager for PHP)
- SQLite (or MySQL/PostgreSQL)
- Web Server (Apache/Nginx) or PHP's built-in server

### Installation

1. Clone the repository
   ```bash
   git clone https://github.com/dikysetiawan21/Recipe-API-Laravel-Sanctum.git
   cd Recipe-API-Laravel-Sanctum
   ```

2. Install PHP dependencies
   ```bash
   composer install
   ```

3. Copy the environment file and generate application key
   ```bash
   cp .env.example .env
   php artisan key:generate
   ```

4. Configure your database in the `.env` file
   ```env
   DB_CONNECTION=sqlite
   DB_DATABASE=/absolute/path/to/your/database.sqlite
   ```

5. Create the SQLite database file
   ```bash
   touch database/database.sqlite
   ```

6. Run database migrations and seeders
   ```bash
   php artisan migrate --seed
   ```

7. Start the development server
   ```bash
   php artisan serve
   ```

The API will be available at `http://localhost:8000`

## 📚 API Endpoints

### Authentication
- `POST /api/auth/register` - Register a new user
- `POST /api/auth/login` - Login user
- `POST /api/auth/logout` - Logout user (requires authentication)
- `POST /api/auth/refresh` - Refresh authentication token

### Foods
- `GET /api/foods` - Get all foods
- `POST /api/foods` - Create a new food (admin only)
- `GET /api/foods/{id}` - Get food details
- `PUT /api/foods/{id}` - Update food (admin only)
- `DELETE /api/foods/{id}` - Delete food (admin only)
- `GET /api/foods/recommend` - Get food recommendations based on parameters

### Categories
- `GET /api/categories` - Get all categories
- `POST /api/categories` - Create a new category (admin only)
- `GET /api/categories/{id}` - Get category details
- `PUT /api/categories/{id}` - Update category (admin only)
- `DELETE /api/categories/{id}` - Delete category (admin only)

### Other Resources
Similar endpoints are available for:
- Cuisine Types
- Dietary Restrictions
- Moods
- Occasions
- Weather Conditions

## 🛡️ Authentication

This API uses JWT (JSON Web Tokens) for authentication. To access protected routes, include the token in the request header:

```
Authorization: Bearer YOUR_JWT_TOKEN
```

## 🤝 Contributing

Contributions are what make the open-source community such an amazing place to learn, inspire, and create. Any contributions you make are **greatly appreciated**.

1. Fork the Project
2. Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3. Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the Branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📝 License

Distributed under the MIT License. See `LICENSE` for more information.

## 👨‍💻 Author

**Diky Setiawan**  
📧 Email: dikysetiawan21@gmail.com  
🔗 GitHub: [@dikysetiawan21](https://github.com/dikysetiawan21)  
💼 LinkedIn: [Diky Setiawan](https://linkedin.com/in/dikysetiawan21)

## 🙏 Acknowledgments

- [Laravel](https://laravel.com/) - The PHP Framework For Web Artisans
- [JWT Auth](https://github.com/tymondesigns/jwt-auth) - For API Authentication
- [Laravel Documentation](https://laravel.com/docs) - For the excellent documentation

---

<div align="center">
  <p>Made with ❤️ using Laravel</p>
  <p>© 2025 Recipe API. All rights reserved.</p>
</div>