#Design Overview
## UI

Our API is split between our coach view and our scheduler view for the most part. It includes functions to add and remove cards, view the details of cards by clicking on an event, and show different information depending on what type of user is viewing the page.
[CoachEventsPage.tsx](https://github.com/gordon-cs/athletic-form/blob/main/athletic-form-ui/src/Views/CoachEventsPage.tsx) and [CoachEventDetails.tsx](https://github.com/gordon-cs/athletic-form/blob/main/athletic-form-ui/src/Views/CoachEventDetails.tsx): The Coach pages.
[EventsPage.tsx](https://github.com/gordon-cs/athletic-form/blob/main/athletic-form-ui/src/Views/EventsPage.tsx) and [EventDetails.tsx](https://github.com/gordon-cs/athletic-form/blob/main/athletic-form-ui/src/Views/EventDetails.tsx): The Scheduler pages.
[EventCardBase.tsx](https://github.com/gordon-cs/athletic-form/blob/main/athletic-form-ui/src/Components/EventCardBase.tsx): The template used by both of these
[UpdateEvent.tsx](https://github.com/gordon-cs/athletic-form/blob/main/athletic-form-ui/src/Views/UpdateEvent.tsx) and [AddEvent.tsx](https://github.com/gordon-cs/athletic-form/blob/main/athletic-form-ui/src/Views/AddEvent.tsx): both do what their names suggest, and update/add a card.
[ClassConflicts.tsx](https://github.com/gordon-cs/athletic-form/blob/main/athletic-form-ui/src/Views/ClassConflicts.tsx): used to generate a table of information to show which students have scheduling conflicts. Used across various 'details' pages.
[DeletedEventsPage.tsx](https://github.com/gordon-cs/athletic-form/blob/main/athletic-form-ui/src/Views/DeletedEventsPage.tsx): tracks removed or past events, so that the user can recover or view them.

## Interfaces

Because of the dependencies in our system, it is necessary that we use high-level interfaces to model our classes from. We use these to adhere to the dependency inversion principle, preventing our classes from relying on low-level modules that are often subject to change.
[IEmailer.cs](https://github.com/gordon-cs/athletic-form/blob/main/API/api-core/AthleticFormLibrary/Interfaces/IEmailer.cs): This interface models our emailer.
[IReportGeneration.cs](https://github.com/gordon-cs/athletic-form/blob/main/API/api-core/AthleticFormLibrary/Interfaces/IReportGeneration.cs): This is the interface models our report generation, specifically to form the bodies of our emails.
[IScheduler.cs](https://github.com/gordon-cs/athletic-form/blob/main/API/api-core/AthleticFormLibrary/Interfaces/IScheduler.cs): This interface models all scheduled operations in the application. Our weekly email notifications are a prime example of this.