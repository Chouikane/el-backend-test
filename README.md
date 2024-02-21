## Project Introduction: Football Data API with Django, DRF, and MongoDB 

### Project Scope:
This project revolves around constructing a RESTful API for a football data service, connecting to external APIs to fetch data, and presenting it to users in an organized manner.

This project consists of two main parts: 
1.  **Data Integration:** In the first part, we'll focus on connecting to external football data services, fetching competitions, teams, and match schedules, and storing them in our MongoDB database.
2.  **API Development:** The second part involves developing RESTful API endpoints to serve the fetched football data to users, providing filtering and querying capabilities for enhanced user experience. (Django & Django Rest Framework)


### Task 1: Data Integration
The primary objective of this task is to connect to external football data services, retrieve data related to competitions, teams, and match schedules, and store it in our MongoDB database.
- Service base url: `https://test-api-three-zeta.vercel.app/`
- Authorization Key:  `KEYFORTEST` (Ensure that this provided  key is passed with each request as header "API_KEY"  to gain access to the endpoints)
#### Requirements:
- Fetch data from the following endpoints of the external API:
     - `/competitions`: Returns all competitions, with fields for `id` and `name`.
     - `/teams`: Returns all teams, with fields for `id` and `name`.
     - `/matches`: Returns the complete schedule (matches) of a specified competition. Mandatory parameters include `competition_id` and `page` (incremented to collect full data). Fields include `id`, `round`, `date`, `time`, `status` (one of Played|Playing|Fixture), `home_team` (`id`, `name`), `away_team` (`id`, `name`), `home_score`, `away_score`, and `competition` (`id`, `name`).


### Task 2: API Development
Based on the frontend app description below, your task is to design and implement the necessary RESTful API endpoints to serve the required football data. 

#### Frontend App Description:
   - The app will consist of three main pages:
     1. Competitions Page:
          - This page will display a list of all available football competitions.
          - Users should be able to see basic information about each competition, such as its ID and name.
     2. Team Page:
          - This page will provide detailed information about a specific football team.
          - Users should see the team's ID and name.
          - The page should also display data for the team's last 5 played matches (results) and upcoming 5 matches (fixtures).
     3. Matches Page:
          - This page will allow users to view a list of football matches.
          - By default, it should display all matches for today.
          - Users should have the option to filter matches by date (YYYY-MM-DD), team ID or competition ID and round combined.


#### Testing:
- Write thorough unit tests for all API endpoints to ensure functionality and reliability.

#### Dockerization
- Dockerize the project to facilitate easy deployment and management, providing a Docker Compose configuration
