# GigaBillig (Historical Price Average Finder)

## Overview

This C# application scrapes historical price data of products from specified websites and calculates the average price over time. It's designed as a foundational tool for detecting pricing anomalies, with the potential for expansion into a full price monitoring and error detection system.

## Features

- Scrapes price data from web pages.
- Calculates the historical average price for specified products.
- Stores historical price data in a local database (SQLite).
- Simple console interface for user interaction.

## Requirements

- .NET 8.0 or higher
- Visual Studio or any C# compatible IDE
- NuGet packages:
  - `HtmlAgilityPack`
  - `Microsoft.EntityFrameworkCore`
  - `Microsoft.EntityFrameworkCore.Sqlite`

## Getting Started

### Installation

1. **Clone the Repository:**

   ```bash
   git clone https://github.com/yourusername/HistoricalPriceFinder.git
   cd HistoricalPriceFinder
   ```

2. **Install Required NuGet Packages:**

   In the terminal or using the NuGet Package Manager in Visual Studio, run the following commands:

   ```bash
   dotnet add package HtmlAgilityPack
   dotnet add package Microsoft.EntityFrameworkCore
   dotnet add package Microsoft.EntityFrameworkCore.Sqlite
   ```

3. **Build the Project:**

   Use your IDE or the command line:

   ```bash
   dotnet build
   ```

### Usage

1. **Run the Application:**

   ```bash
   dotnet run
   ```

2. **Specify the URL:**

   The application will prompt you to enter a URL containing historical price data. Adjust the scraping logic if necessary to fit the structure of the target website.

3. **View Results:**

   The application will output the historical average price for the product specified.

### Example

Here is a sample output of the application:

```bash
Enter the product URL: http://example.com/historical-prices
Scraping data...
Historical Average Price: $49.99
```

### Customization

- **Scraping Logic:** 
  - Modify the XPath query in the `GetHistoricalPrices` method to target different elements based on the website's HTML structure.
- **Database Storage:**
  - The application uses SQLite for simplicity. If you prefer another database, modify the `ApplicationDbContext` configuration.

### Future Enhancements

- **Automated Data Collection:** 
  - Schedule regular scraping of specified URLs to automatically update historical price data.
- **User Interface:**
  - Implement a GUI using WinForms, WPF, or ASP.NET Core for a more user-friendly experience.
- **Alert System:**
  - Add an alert system that notifies users when prices drop significantly or when a potential error is detected.

## Contributing

Contributions are welcome! Please fork the repository and create a pull request with your changes.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Contact

For any inquiries, feel free to contact me at your.email@example.com.
