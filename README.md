# Fine Freelancing Marketplace

A full-stack two-sided freelancing platform built with **ASP.NET Core**, designed to connect clients with skilled freelancers through structured job postings, proposal management, rating systems, and tiered premium memberships.

**Live Demo:** [Add your MonsterASP.NET or Render URL here]

---

## Key Features

* **Role-Based Access Control:** Separate workflows and permissions for **Clients**, **Freelancers**, and **Administrators** powered by ASP.NET Core Identity.
* **Job Posting & Discovery:** Clients can publish detailed project scopes, budgets, and timelines, while freelancers browse and filter relevant opportunities.
* **Hiring & Candidate Evaluation:** Streamlined application review workflow allowing clients to inspect freelancer portfolios, past ratings, and proposals before hiring.
* **Ratings & Reviews:** Post-project feedback system calculating freelancer reputation scores based on communication and delivery quality.
* **Tiered Premium Features:**
  * Unlimited job postings and dual client/freelancer account capabilities.
  * Advanced search filters and personalized job recommendations.
  * Ad-free workspace experience.

---

## Tech Stack

* **Backend:** C#, ASP.NET Core (MVC / Web App)
* **ORM & Database:** Entity Framework Core, SQL Server (or PostgreSQL)
* **Authentication:** ASP.NET Core Identity
* **Frontend:** Razor Views, HTML5, CSS3, Bootstrap, JavaScript

---

## Getting Started (Local Setup)

### Prerequisites
* [.NET SDK](https://microsoft.com) (6.0 / 7.0 / 8.0+)
* [SQL Server](https://microsoft.com) or SQL Server Express / LocalDB
* [Git](https://git-scm.com)

### 1. Clone the Repository
```bash
git clone https://github.com
cd asp-dot-net-core-Final-Project/Fine-FreeLancing-Website
```

### 2. Configure the Database Connection
Open `appsettings.json` inside the project folder and update `DefaultConnection` to match your local database server:
```json
{
  "ConnectionStrings": {
    "DefaultConnection": "Server=(localdb)\\mssqllocaldb;Database=FineFreelancingDb;Trusted_Connection=True;MultipleActiveResultSets=true"
  }
}
```

### 3. Apply Entity Framework Migrations
Restore dependencies and create the database tables:
```bash
dotnet restore
dotnet ef database update
```
*(If `dotnet-ef` is not installed, run `dotnet tool install --global dotnet-ef` first.)*

### 4. Run the Application
```bash
dotnet run
```
Open your browser and navigate to `https://localhost:5001` (or the local port shown in your terminal).

---

## Project Structure

```text
├── Fine-FreeLancing-Website/
│   ├── Controllers/        # Request handling and business logic
│   ├── Models/             # Domain entities and ViewModels
│   ├── Views/              # Razor UI templates
│   ├── Data/               # EF Core DbContext and migrations
│   ├── wwwroot/            # Static assets (CSS, JS, images)
│   └── Program.cs          # App configuration and service registration
└── README.md
```

---

## License

This project is open-source and available under the MIT License.
