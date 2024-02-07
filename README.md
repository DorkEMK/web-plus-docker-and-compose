# Docker Deployment of an Application
Training project.

The service consists of three pre-prepared parts: a backend service on Node.js, a database (PostgreSQL), and a frontend on React (served by nginx).
For the service deployment, the following was done:

- The backend was configured to use environment variables.
- A Dockerfile for the backend was created.
- A Dockerfile for the frontend was created.
- Domains were registered and configured.
- A docker-compose file was described.
- The application was deployed on Yandex Cloud (currently unavailable).

**Launch the Application**

- Clone the repository
- Create .env files
- Start the server: ```docker-compose up -d```

**Links (currently unavailable)**
- IP адрес 51.250.77.9
- Frontend [https://kupipodaruday.dorkemk.nomoredomainsrocks.ru/](https://kupipodaruday.dorkemk.nomoredomainsrocks.ru/)
- Backend [https://api.kupipodaruday.dorkemk.nomoredomainsrocks.ru/](https://api.kupipodaruday.dorkemk.nomoredomainsrocks.ru/)
