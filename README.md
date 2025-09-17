# Library App

## Description

Library App is a modular, testable library management system built with .NET 8.0. It provides a console-based interface for searching patrons, managing loans, and renewing memberships. The application uses JSON files for data storage and follows clean architecture principles with clear separation between core logic, infrastructure, and presentation layers.

## Project Structure

- AccelerateDevGitHubCopilot.sln
- README.md
- src/
  - Library.ApplicationCore/
    - Library.ApplicationCore.csproj
    - Entities/
    - Enums/
    - Interfaces/
    - Services/
  - Library.Console/
    - appSettings.json
    - CommonActions.cs
    - ConsoleApp.cs
    - ConsoleState.cs
    - Library.Console.csproj
    - Program.cs
    - Json/
      - Authors.json
      - Books.json
      - BookItems.json
      - Loans.json
      - Patrons.json
  - Library.Infrastructure/
    - Library.Infrastructure.csproj
    - Data/
      - JsonData.cs
      - JsonLoanRepository.cs
      - JsonPatronRepository.cs
- tests/
  - UnitTests/
    - UnitTests.csproj
    - PatronFactory.cs
    - LoanFactory.cs
    - ApplicationCore/
      - PatronService/
        - RenewMembership.cs
      - LoanService/
        - ExtendLoan.cs
        - ReturnLoan.cs

## Key Classes and Interfaces

- **Entities**
  - `Patron`, `Loan`, `BookItem`, `Book`, `Author`  
    (src/Library.ApplicationCore/Entities/)
- **Enums**
  - `MembershipRenewalStatus`, `LoanExtensionStatus`, `LoanReturnStatus`, `CommonActions`, `ConsoleState`  
    (src/Library.ApplicationCore/Enums/, src/Library.Console/)
- **Interfaces**
  - `IPatronRepository`, `ILoanRepository`, `IPatronService`, `ILoanService`  
    (src/Library.ApplicationCore/Interfaces/)
- **Services**
  - `PatronService`, `LoanService`  
    (src/Library.ApplicationCore/Services/)
- **Infrastructure**
  - `JsonData`, `JsonPatronRepository`, `JsonLoanRepository`  
    (src/Library.Infrastructure/Data/)
- **Console Application**
  - `ConsoleApp`, `Program.cs`  
    (src/Library.Console/)

## Usage

1. **Build the project:**
   ```sh
   dotnet build
   ```
2. **Run the application:**
   ```sh
   dotnet run --project src/Library.Console/Library.Console.csproj
   ```
3. **Execute commands:**
   - Search for patrons, manage loans, or renew memberships using the console interface.
   - The application will read and write data to the specified JSON files in the `src/Library.Console/Json/` directory.

## Features

- Modular architecture for easy testing and maintenance.
- Console-based user interface for interacting with the library system.
- JSON file integration for data storage and retrieval.
- Clean architecture principles ensuring separation of concerns.

## Future Enhancements

- Implement a graphical user interface (GUI) for improved user experience.
- Add authentication and authorization for secure access.
- Integrate with external APIs for extended functionality (e.g., book information, author details).
- Provide data migration tools for transitioning to/from other library management systems.
