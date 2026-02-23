# TicketHive 🎫

A web-based ticket purchasing system for concert events, built with ASP.NET Core MVC.

## Overview

TicketHive is a ticket management application that allows users to browse concerts and purchase tickets online. The application provides a complete ticketing solution with concert management and purchase tracking capabilities.

## Features

- **Concert Management**: Browse and manage concert events
- **Ticket Purchasing**: Purchase tickets for available concerts
- **Purchase Tracking**: View, edit, and manage purchase records
- **Secure Payments**: Credit card payment processing with masked card number display
- **Responsive Design**: Modern, mobile-friendly user interface

## Technology Stack

- **Framework**: ASP.NET Core MVC
- **.NET Version**: .NET 9
- **Language**: C# 13.0
- **Database**: Entity Framework Core (for data persistence)

## Getting Started

### Prerequisites

- [.NET 9 SDK](https://dotnet.microsoft.com/download/dotnet/9.0)
- A code editor (Visual Studio 2022 recommended, or Visual Studio Code)
- SQL Server or SQL Server Express (for database)

### Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/andrewbeaverNSCC/TicketHive.git
   cd TicketHive
   ```

2. Restore dependencies:
   ```bash
   dotnet restore
   ```

3. Update the database connection string in `appsettings.json` (if needed)

4. Apply database migrations:
   ```bash
   dotnet ef database update
   ```

5. Run the application:
   ```bash
   dotnet run
   ```

6. Open your browser and navigate to `https://localhost:5001` (or the URL shown in the console)

## Project Structure

```
TicketHive/
├── Controllers/         # MVC Controllers
│   ├── ConcertsController.cs
│   └── PurchasesController.cs
├── Models/             # Data models
│   ├── Concert.cs
│   └── Purchase.cs
├── Views/              # Razor views
│   ├── Concerts/
│   ├── Purchases/
│   └── Shared/
└── wwwroot/           # Static files (CSS, JS, images)
    └── css/
```

## Usage

### Browsing Concerts
Navigate to the Concerts page to view all available concert events.

### Purchasing Tickets
1. Select a concert from the available events
2. Enter the number of tickets you wish to purchase
3. Provide your contact information (name and email)
4. Enter payment details
5. Confirm your purchase

### Managing Purchases
- View all purchases in the Purchases index
- Edit purchase details if needed
- View detailed information about specific purchases
- Delete purchases when necessary

## Models

### Purchase
- Purchase tracking with ticket quantities
- Customer contact information
- Credit card payment details (with secure masking)
- Concert association

### Concert
- Concert event information
- Related purchase records

## Security Note

For production use, ensure proper security measures are implemented:
- Use a secure payment gateway instead of storing card details directly
- Implement HTTPS
- Add authentication and authorization
- Follow PCI DSS compliance guidelines for payment data

## Contributing

This is an educational project. If you'd like to contribute:
1. Fork the repository
2. Create a feature branch
3. Commit your changes
4. Push to the branch
5. Open a pull request

## License

This project is for educational purposes.

## Author

Andrew Beaver - NSCC

## Acknowledgments

- Built as part of a Web Application Development course
- NSCC Semester 3 project
