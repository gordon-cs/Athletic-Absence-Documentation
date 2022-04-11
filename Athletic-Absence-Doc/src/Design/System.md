# System Overview

Prior to the launch of our system, student athletes have to fill out a form for when they have to miss class for an athletic competition, have their coach sign it, and deliver it to their professor. The professors then need to clarify what the expectations are for the days that the students are missing class. The problem with this is that students often make a mistake with this paper form such as not having the coach sign it or not following up with the professor. There are also issues where games get canceled, but students skip classes anyways. Carter Shaw’s idea is that instead of having to fill out a paper form that is prone to mistakes, we should automate the process with our system, maybe using Gordon360 in some way, by including the course schedule and athletics event schedule and alerting the professors for when they will have students missing class. Read more about our problem statement here.

The primary features of this application include: allowing the person scheduling transport to give that data to a database, providing a 'handshake' system so the software can tell if a student has been approved to miss class by their professor, and allowing this information to be available to coaches, professors, and student-athletes via email and through our UI. Here’s our standard workflow:

- Event gets scheduled
- Bus gets scheduled and added through out UI
- Student IDs are retrieved for all students on the team
- Schedules for each student are checked against departure times
- Emails are sent to the students and the professors of the classes they will be missing
- Conflicts are visible to coaches who are able to monitor that these are resolved
- Any updates or last minute cancellations cause a resend of the emails to any professors that will be affected
- This process continues over the course of each athletic season
