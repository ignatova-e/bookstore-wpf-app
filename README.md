# Bookstore WPF App

A small educational project built with C# and a SQL Server database. It was developed for Windows as a WPF desktop application. The app represents a bookstore and provides a book catalog with authorization, search, category filtering, and price sorting.

The project was first created as a shoe store application, then adapted to a bookstore for a class assignment. Because the adaptation had to be completed in a limited time, some legacy shoe-store names remain in code, file names, and database objects (for example, `ShoeTest`). These names are historical; the project’s intended domain is a bookstore.

## Development setup

The database server was started in Docker. Windows was run in parallel using Parallels Desktop, where Microsoft SQL Server Management Studio (SSMS) and Visual Studio were installed. The application was developed and run in that Windows environment.

To prepare the database, open the scripts in `database/` in SSMS and run them in this order:

1. `script.sql` — creates the `ShoeTest` database, tables, and relationships.
2. `ShoeTest_insert.sql` — inserts sample data into the tables.

Before running the application, check the `ShoeTestEntities` connection string in `WpfApp1/App.config` and update it for your SQL Server host and credentials.

## Project layout

- `database/` — SQL Server database creation and sample-data scripts.
- `WpfApp1/` — the WPF application source: XAML screens, C# code, Entity Framework models, and product images.
- `WpfApp1.sln` — Visual Studio solution.
- `docs/images/` — documentation screenshots and the database diagram.

## Screenshots

### Authorization

![Authorization screen](docs/images/авторизация.png)

### Product catalog

![Product catalog](docs/images/каталог.png)

### Search by product name

![Product search](docs/images/поиск%20по%20названию.png)

### Category filtering

![Category filtering](docs/images/фильтрация.png)

### Price sorting

![Price sorting](docs/images/сортировка.png)

## Database diagram

![Database diagram](docs/images/диаграмма%20БД.png)
