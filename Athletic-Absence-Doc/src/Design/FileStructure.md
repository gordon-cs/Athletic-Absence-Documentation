- API: contains code for API, written in C#, and SQL queries
    - api-core: all the code for the API solution
        - AthleticFormCore: contains code for AthleticFormCore project
        - AthleticSQLServer: contains code for our mock-database
            - SQL Queries: SQL queries for setting up non-Gordon database
                - CreateConflictsView.sql: Creates Conflicts view
                - CreateTable.sql: Creates tables in database
                - DatabaseCreation.sql: Creates database
                - DropConflictsView.sql: Drops Conflicts view
                - DropEnrolledIn.sql: Drops StudentEnrolledIn view
                - DropTables.sql: Drops tables in database
                - InsertData.sql: Inserts data into database
                - TestInsert.sql: Another file that inserts one row into the InEvent table
            - (Deprecated, at this point) ServerConfiguration: contains code for setting up docker container for non-Gordon database
                - .prettierignore
                - Docker-compose.yml: YAML file for setting up container for non-Gordon database. Now that we have access to the Gordon database, this won’t be used.
            - .prettierc.json
        - Controllers: controllers for the project, gather data together, performs logic for data, the controllers control the way that the user interacts with the data (see “API Endpoints” below for more details)
            - AccountsController.cs: controller for displaying account information and all students with their current enrollment schedule
            - ConflictsController.cs: controller for conflicts information
            - EmailController.cs: controller with code for displaying email information and sending emails
            - EventsController.cs: controller for reading, adding, deleting, and restoring events
            - ReportsController.cs: controller for reading report sent to professors
AthleticFormCore.csproj: project file for AthleticFormCore project
Program.cs: actual program that is run
Startup.cs: code for starting up project
AthleticFormLibrary: contains code for AthleticFormLibrary project
DataAccess: contains code that allows you to access database
AthleticContext.cs: allows project to access database
Emailer: contains code for sending emails
EmailClient.cs: code for sending emails.  In SendMail to send an email replace first.last@gordon.edu with your email and password with your password to send an email from your account.  Eventually, we will replace this with the Athletics account but we will not commit the Athletics account username and password to GitHub.
Interfaces: interfaces that some of our classes inherit from
IEmailer.cs: interface that EmailClient.cs inherits from
IReportGeneration.cs: interface that ReportGenerator.cs inherits from
IScheduler.cs: interface that EmailScheduler.cs inherits from
Models: classes for different tables/views in database
Account.cs: stores data for account information
AthleticConflict.cs: stores data about athletic conflicts
AthleticEvent.cs: stores data about athletic events
PlayersInEvent.cs: stores data about which players are in which events
PlayersInTeam.cs: stores data about which players are on which team
SectionMaster.cs: contains course information
StudentsEnrolledIn.cs: contains information about which students are enrolled in which courses
Team.cs: contains information about teams
Static Pages
ReportFormat.html: static html page that serves as a mockup for the report that is sent to the professor
Utilities: files that perform some of the major tasks including generating reports and scheduling times for sending emails
Scheduler: contains code for scheduling emails
EmailScheduler.cs: contains code for scheduling when to send emails.  Our reports are sent to the professors every Sunday at 6 AM.
ReportGenerator.cs: contains code for generating reports sent to professors
AthleticFormLibrary.csproj: project file for AthleticFormLibrary project
Injector.cs: registers classes that inherit from interfaces so that these classes can inherit from them
Tests: contains unit tests, which are pytests written in Python to test API
pytest_components.py: contains code for getting and posting a request through Python
test_accounts.py: testing the ability to get account and student enrolled in information
test_athleticForm_pytest.py: constants that are used throughout the test project.  Currently only contains the host url but may contain more later on.
test_emails.py: tests ability to send emails
test_events.py:  tests ability to get all events
test_reports.py: tests to see that report is generating correct information
AthleticFormSolution.sln: runnable solution file
athletic-form-ui: contains code for UI, written in React.js
public: contains favicon.ico and index.html
favicon.ico: Gordon Athletics logo.  Our main logo for the project
index.html: html page that renders react component. 
src: contains source code for project
Components: contains components that are commonly used throughout the project
CoachEventCard.tsx: cards on coach’s events page
DeletedEventCard.tsx: cards on deleted events page
EventCard.tsx: cards on Robyn’s events page
EventDetailsBase.tsx: component that is shared between Robyn’s details page and the coach’s details page
Helpers: contains TypeScript files with functions that are commonly used as helper functions throughout the project
DateTimeHelpers.ts: these functions make it so that the date and time are easy for people to read and a function converting military time to standard time.
FilterHelpers.tsx: these functions help with sorting and filtering events
Services: do controller requests in React project and connect backend to frontend
AxiosService.ts: fetches the base backend url
EventService.ts:  contains functions that do controller actions in React project
Views: different React pages
AddEvent.tsx: page for adding events
ClassConflicts.tsx: displays class conflicts for an athlete in an athletic event
CoachEventDetails.tsx: displays event details for the coach.  Displays information about an athletic event, which students have conflicts and their approval status.
CoachEventsPage.tsx: displays all non-deleted events for coaches. Displays event information for each event.  Red stripes on top for if the events have conflicts.  Also, displays the number of students with conflicts for each event.
DeleteEvent.tsx: page for deleting an athletic event
DeletedEventsPage.tsx: page that displays all deleted events.  These events can be recovered.
EventDetails.tsx: displays event details for Robyn.  Simply displays data about events.
EventsPage.tsx: displays all non-deleted events for Robyn.  Displays event information for each event.  Robyn also has the ability to add, edit, and delete events.
RecoverEvent.tsx: page for recovering a deleted event.
UpdateEvent.tsx: page for updating an event.
styles: scss styling for React pages
addEvent.scss: styling for AddEvent.tsx
eventCard.scss: styling for EventCard.tsx and CoachEventCard.tsx
eventsPage.scss: styling for EventsPage.tsx and CoachEventsPage.tsx
App.tsx: renders React page
index.tsx: renders App.tsx
react-app-env-d.ts
.editorconfig
.prettierc.json
package-lock.json: contains exact dependency tree for packages in athletic-form-ui directory
package.json: similar to package-lock.json, contains information about packages in athletic-form-ui directory but not exact dependency tree
tsconfig.json
.gitignore: list of files for GitHub to ignore
README.md:  contains documentation for project
package-lock.json: contains exact dependency tree for packages in athletic-form directory
package.json: similar to package-lock.json, contains information about packages in athletic-form directory but not exact dependency tree