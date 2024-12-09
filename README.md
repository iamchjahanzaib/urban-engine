# The booking system
1. Create a database
    1. Install Docker: https://www.docker.com/
    2. Load the postgres image: docker pull postgres
    3. Create a container: docker run --name booking_system_database -e POSTGRES_PASSWORD=Secret1234! -d -p 5432:5432 postgres
    4. Connect to the database: docker exec -it booking_system_database psql -U postgres -d postgres
    5. Copy the file booking_system_structure.sql to the clipboard.
    6. Paste the file into the psql terminal
2. Run the command: deno run --allow-net --allow-env --allow-read --watch app.js

# Pages
1. http://localhost:8000/register --> GET and POST
2. http://localhost:8000/login --> GET and POST
3. http://localhost:8000/logout --> GET
4. http://localhost:8000/resources --> GET and POST
5. http://localhost:8000/reservation --> GET and POST
6. http://localhost:8000/resourcesList --> GET
# Logbook
| Date | Used Hours    | Subject(s) NAME    | Output |
| :-----: | :---: | :---: | :--- |
| 30.10.2024 |  2h   | Cisco Introduction to Cybersecurity  | Done |
| 31.10.2024 |  2h   |Cisco Introduction to Cybersecurity   | Done |
| 1.11.2024 |  2h   | Module2:Attacks Concepts and Techniques  | Done |
| 2.11.2024 |  2h   |Module2:Attacks Concepts and Techniques   | Done |
| 3.11.2024 |  2h   | Module3:protecting your data and privacy  | Done |
| 4.11.2024 |  2h   |Module3:protecting your data and privacy    | Done |
| 5.11.2024 |  2h   | Module4:protecting the organization  | Done |
| 6.11.2024 |  2h   |Module4:protecting the organization   | Done |
| 7.11.2024 |  2h   |Module5:will your future in cybersecurity  | Done |
| 8.11.2024 |  1h   |Module5:introduction the cybersecurity final exam   | Done |
| 9.11.2024 |  2h   |lab1: sql injection(SQL injection vulnerability in WHERE clause allowing retrieval of hidden data)  | Done |
| 10.11.2024 |  2h   |lab1: Authentication(Username enumeration via different responses)   | Done |
| 14.11.2024 |  2h   |lab1: Access Control(Unprotected admin functionality)   | Done |
| 15.11.2024 |  2h   |lab2: sql injection(SQL injection vulnerability allowing login bypass)   | Done |
| 15.11.2024 |  2h   |lab2: Authentication(2FA simple bypass)   | Done |
| 16.11.2024 |  2h   |lab2:  Access Control(Unprotected admin functionality with unpredictable URL)   | Done |
| 18.11.2024 |  3h   |Booking_system_project(working)   | Done |
| 22.11.2024 |  3h   |Booking_system_project(working)   | Done |
| 26.11.2024 |  3h   |Booking_system_project(working)   | Done |
| 1.12.2024 |  3h   |registration_page_first_test(working)   | Done |
| 2.12.2024 |  3h   |phase_2(step1+step2)   | Done |
| 5.12.2024 |  3h   |registration_page_first_test(step3+final report submit)   | Done |
| 6.12.2024 |  1h   |lab3:User role controlled by request parameter(access control)   | Done |
| 6.12.2024 |  1h   |lab4:User role can be modified in user profile(access control)   | Done |
| 8.12.2024 |  1h   |lab3:Password reset broken logic(Authentication)   | Done |

















