api/Accounts/StudentsEnrolledIn/{email}/{yearCode}/{termCode}
 - Gets students enrolled in a class by parameter

api/Accounts/{email}
 - Gets account by email

api/Conflicts
 - Gets all students with conflicts

api/Conflicts/{eventId}
 - Gets all students with conflicts for an event with id = {eventId}

api/Email/{fromEmail}/{password}/{emails}/{number}
 - Post request that sends an email to {emails} from {fromEmail} and {password}, leave {number} = 0 for default message called in test_sendEmail() in test_emails.py to check to be sure that mailer is working.  When running this test, replace the fromEmail and password with your Gordon email and password.

api/Events
 - Return all our Athletic Events as a list.  This method is used in CoachEventDetails, CoachEventsPage, DeletedEventsPage, EventDetails, and EventsPage.  In these different files, we filter from the list.  In CoachEventDetails and EventDetails, we find an event by a given event id and show details about that event.  In CoachEventsPage and EventsPage, we filter all the events that are not marked as deleted and show all these events. In DeletedEventsPage, we filter all the events that are marked as deleted and show all these events.

api/Events/add
 - Posts a new event to our database and adds all necessary players to it

api/Events/update/{id}
 - Modifies the event with id = {id}

api/Events/delete/{id}
 - Puts the event with id = {id} into the recycle bin

api/Events/restore/{id}
 - Removes the event with id = {id} from the recycle bin and back into the main events pool

api/Reports/{number}
 - Generates a report, leave {number} = 0 for default

api/Teams
 - Gets all teams in the database

api/Teams/{sport}
 - Gets the roster for the team denoted by {sport}

api/Teams/add
 - Adds new players to team rosters

api/Teams/{sport}/delete/{gordonId}
 - Removes player with id = {gordonId} from team denoted by {sport}

api/YearTerm/year/{date}
 - Gets the year from {date}

api/YearTerm/term/{date}
 - Gets the term from {date}


