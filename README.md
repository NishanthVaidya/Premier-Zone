# ⚽ Premier League Stats App

![Java](https://img.shields.io/badge/Java-17%2B-blue)
![Spring Boot](https://img.shields.io/badge/Spring%20Boot-2.5.4-brightgreen)
![License](https://img.shields.io/badge/License-MIT-lightgrey)

A RESTful API built with Spring Boot that provides access to player statistics from the English Premier League. This application allows users to retrieve, search, filter, add, update, and delete player data, making it ideal for football analytics platforms, scouting dashboards, and fan engagement tools.

## 📸 Demo

> `GET http://localhost:8080/api/players?team=Arsenal&pos=Defender`  
> Returns all defenders from Arsenal in the dataset.

## 🧩 Features

- **Retrieve Player Data:** Access comprehensive statistics for Premier League players.
- **Search and Filter:** Query players by:
  - `name` – e.g., `?name=Bruno`
  - `team` – e.g., `?team=Manchester United`
  - `pos` (position) – e.g., `?pos=Midfielder`
  - `nation` (nationality) – e.g., `?nation=Portugal`
- **Add New Players:** Introduce new player records into the dataset.
- **Update Player Information:** Modify existing player data.
- **Delete Players:** Remove player records by name.
- **CORS Support:** Enabled for seamless integration with frontend applications.

## 🛠 Tech Stack

- **Backend:** Java 17+, Spring Boot 2.5.4
- **Build Tool:** Maven
- **Data Format:** CSV
- **API Style:** RESTful

## 🚀 Getting Started

### ✅ Prerequisites

- Java JDK 17 or higher
- Maven 3.x
- Git
- IDE (e.g., IntelliJ IDEA, VS Code)

### 📦 Installation & Running

1. **Clone the Repository:**
   ```bash
   git clone https://github.com/NishanthVaidya/Premier-Zone.git
   cd Premier-Zone
Build the Project:

bash
Copy
Edit
mvn clean install
Run the Application:

bash
Copy
Edit
mvn spring-boot:run
Access the API: Open your browser or API client and navigate to:

bash
Copy
Edit
http://localhost:8080/api/players
📊 API Endpoints
GET /api/players
Retrieve a list of players with optional filters.

Query Parameters:

name – Filter by player name.

team – Filter by team name.

pos – Filter by position.

nation – Filter by nationality.

Examples:

Get all players:

bash
Copy
Edit
GET /api/players
Get players named "Bruno":

pgsql
Copy
Edit
GET /api/players?name=Bruno
Get midfielders from Liverpool:

bash
Copy
Edit
GET /api/players?team=Liverpool&pos=Midfielder
POST /api/players
Add a new player to the dataset.

Request Body:

json
Copy
Edit
{
  "name": "Bukayo Saka",
  "team": "Arsenal",
  "pos": "Midfielder",
  "nation": "England",
  "age": 21
}
Example:

bash
Copy
Edit
POST /api/players
Content-Type: application/json

{
  "name": "Bukayo Saka",
  "team": "Arsenal",
  "pos": "Midfielder",
  "nation": "England",
  "age": 21
}
PUT /api/players
Update an existing player's information.

Request Body:

json
Copy
Edit
{
  "name": "Bruno Fernandes",
  "team": "Manchester United",
  "pos": "Midfielder",
  "nation": "Portugal",
  "age": 28
}
Example:

bash
Copy
Edit
PUT /api/players
Content-Type: application/json

{
  "name": "Bruno Fernandes",
  "team": "Manchester United",
  "pos": "Midfielder",
  "nation": "Portugal",
  "age": 28
}
DELETE /api/players/{playerName}
Delete a player by their name.

Example:

bash
Copy
Edit
DELETE /api/players/Bruno%20Fernandes
🗂 Project Structure
bash
Copy
Edit
Premier-Zone/
├── src/
│   └── main/
│       └── java/
│           └── com/nvpl/premier_zone/
│               ├── player/         # Player Model, Controller, Service, Repository
│               └── PremierLeagueStatsApplication.java
├── prem_stats.csv                  # Player data source
├── pom.xml                         # Maven build file
└── README.md
📝 License
This project is licensed under the MIT License. See the LICENSE file for details.

🤝 Contributing
Contributions are welcome! Please fork the repository and submit a pull request with your changes. For major changes, please open an issue first to discuss what you'd like to change.

bash
Copy
Edit
# Fork the repository
git clone https://github.com/NishanthVaidya/Premier-Zone.git
cd Premier-Zone

# Create a new branch for your feature
git checkout -b feature/your-feature-name

# Commit your changes
git commit -m "Add new feature"

# Push to your fork
git push origin feature/your-feature-name

# Submit a pull request
📫 Contact
Author: Nishanth Vaidya
LinkedIn: Nishanth Vaidya
