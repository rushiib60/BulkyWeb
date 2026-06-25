# BulkyWeb

An ASP.NET Core MVC e-commerce web application for managing and selling books online.

## Features

- Product catalogue with category management
- Shopping cart and order management
- Role-based access control (Admin, Employee, Customer)
- Stripe payment gateway integration
- Razor Pages UI with Bootstrap

## Tech Stack

- **Backend:** ASP.NET Core MVC (.NET 6+)
- **Frontend:** Razor Views, Bootstrap, CSS
- **Database:** Entity Framework Core (SQL Server)
- **Payments:** Stripe API

## Getting Started

### Prerequisites

- [.NET 6 SDK](https://dotnet.microsoft.com/download)
- SQL Server or LocalDB
- A Stripe account (for payment features)

### Setup

1. Clone the repository:
   ```bash
   git clone https://github.com/rushiib60/BulkyWeb.git
   cd BulkyWeb
   ```

2. Update the connection string in `appsettings.json`:
   ```json
   "ConnectionStrings": {
     "DefaultConnection": "Server=.;Database=BulkyDb;Trusted_Connection=True;"
   }
   ```

3. Add your Stripe keys in `appsettings.json`:
   ```json
   "Stripe": {
     "PublishableKey": "your_publishable_key",
     "SecretKey": "your_secret_key"
   }
   ```

4. Apply database migrations:
   ```bash
   dotnet ef database update
   ```

5. Run the application:
   ```bash
   dotnet run --project BulkyWeb
   ```

6. Open your browser at `https://localhost:5001`

## Project Structure

```
BulkyWeb/
├── Controllers/      # MVC controllers
├── Models/           # Domain models
├── Views/            # Razor view templates
└── wwwroot/          # Static assets (CSS, JS, images)
```
