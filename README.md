# Hometeq - Smart Home E-Commerce Platform

## Overview

Hometeq is an online retail platform specializing in smart home technology and IoT devices. The site offers a wide range of cloud-controlled tech products designed to make your home and life smarter, including smart security systems, smart energy management devices, smart speakers, and more.

## Features

- **Product Catalog**: Browse and view detailed information about smart home devices
- **User Authentication**: Secure login and signup system for customers
- **Product Management**: Add and edit products (for administrators)
- **Shopping Cart**: Add products to basket and manage quantities
- **Checkout System**: Complete purchase transactions
- **About Us Page**: Learn more about Hometeq's mission and product categories
- **Responsive Design**: Clean, user-friendly interface with custom styling

## Project Structure

```
Hometeq/
├── index.php                  # Home page - product catalog
├── aboutus.php                # About us page with company information
├── login.php                  # Login page
├── login_process.php          # Login form processing
├── signup.php                 # User registration page
├── signup_process.php         # Signup form processing
├── logout.php                 # Logout functionality
├── detectlogin.php            # Login status detection
├── prodbuy.php                # Product details page
├── addproduct.php             # Add new product page
├── addproduct_process.php     # Product creation processing
├── editproduct.php            # Edit existing product
├── basket.php                 # Shopping cart display
├── checkout.php               # Checkout page
├── clearbasket.php            # Clear shopping cart
├── db.php                     # Database connection configuration
├── template.php               # Common page template
├── headfile.html              # Header/navigation template
├── footfile.html              # Footer template
├── mystylesheet.css           # Custom stylesheet
├── homteq_db_tables.sql       # Database schema and sample data
├── images/                    # Product images directory
└── bgimg.jpg                  # Background image
```

## Technology Stack

- **Backend**: PHP
- **Database**: MySQL/MariaDB
- **Frontend**: HTML, CSS
- **Server**: Web server supporting PHP (e.g., Apache)

## Product Categories

The platform specializes in:

1. **Smart Security** - Home monitoring cameras, motion sensors, and alerts
2. **Smart Energy** - Smart thermostats and heating control systems
3. **Smart Speakers** - Voice-controlled smart devices

## Getting Started

### Prerequisites

- PHP (5.x or higher)
- MySQL/MariaDB database server
- Web server (Apache recommended)

### Installation

1. Clone the repository:
   ```bash
   git clone <repository-url>
   cd Hometeq
   ```

2. Create a database:
   ```bash
   mysql -u username -p
   CREATE DATABASE w1833548_0;
   USE w1833548_0;
   SOURCE homteq_db_tables.sql;
   ```

3. Configure database connection in `db.php`:
   ```php
   $dbhost = "your_host";
   $dbuser = "your_user";
   $dbpass = "your_password";
   $dbname = "w1833548_0";
   ```

4. Place the project files in your web server's document root

5. Access the application at `http://localhost/Hometeq/`

## Key Files Description

- **db.php**: Establishes MySQL connection using MySQLi
- **detectlogin.php**: Checks user session and displays login status
- **index.php**: Main landing page displaying all available products
- **homteq_db_tables.sql**: Contains database schema with product table and sample product data

## Database Schema

### Product Table
- `prodId`: Product ID (Primary Key)
- `prodName`: Product name
- `prodPicNameSmall`: Small image filename for listings
- `prodPicNameLarge`: Large image filename for product details
- `prodDescripShort`: Short product description
- `prodDescripLong`: Detailed product description
- `prodPrice`: Product price (decimal)
- `prodQuantity`: Stock quantity

## Security Considerations

⚠️ **Note**: This appears to be a learning/educational project. Before using in production:

- Never commit database credentials to version control
- Use environment variables or configuration files for sensitive data
- Implement proper input validation and sanitization
- Use prepared statements to prevent SQL injection
- Implement HTTPS/SSL encryption
- Add proper authentication and authorization checks
- Implement CSRF protection
- Hash passwords securely

## Usage

1. **Browse Products**: Visit the homepage to view available smart home products
2. **View Details**: Click on a product to see full details and specifications
3. **Create Account**: Sign up for a new account
4. **Login**: Log in with your credentials
5. **Shop**: Add products to your basket
6. **Checkout**: Complete your purchase

## Development Notes

- The project uses MySQLi for database operations
- Sessions are used for user authentication and shopping cart management
- HTML templates are included from separate files for modularity
- Images are stored in the `images/` directory
