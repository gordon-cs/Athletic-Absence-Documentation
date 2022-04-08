api/AccountsController/
 - Gets all accounts of students within Athletics

api/AccountsController/StudentsEnrolledIn/{email}/{yearCode}/{termCode}
 - Gets students enrolled in a class by parameter

api/AccountsController/email
 - Gets account by email

api/ConflictsController
 - Gets all students with conflicts

api/ConflictsController/{eventId}
 - Gets all students with conflicts for an event with id = {eventId}

api/EmailController/{emails}/{number}
 - Sends an email to {email}, leave {number} = 0 for default message

api/EventsController
 - Return all our Athletic Events as a list

api/EventsController/add
 - Posts a new event to our database and adds all necessary players to it

api/EventsController/update/{id}
 - Modifies the event with id = {id}

api/EventsController/delete/{id}
 - Puts the event with id = {id} into the recycle bin

api/EventsController/restore/{id}
 - Removes the event with id = {id} from the recycle bin and back into the main events pool

api/ReportsController/{number}
 - Generates a report, leave {number} = 0 for default

api/TeamsController
 - Gets all teams in the database

api/TeamsController/{sport}
 - Gets the roster for the team denoted by {sport}

api/TeamsController/add
 - Adds new players to team rosters

api/TeamsController/{sport}/delete/{gordonId}
 - Removes player with id = {gordonId} from team denoted by {sport}

api/YearTermController/year/{date}
 - Gets the year from {date}

api/YearTermController/term/{date}
 - Gets the term from {date}


