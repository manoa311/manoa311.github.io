## Table of Contents:
* [About Manoa311](#about-mano311)
* [Installation](#installation)
* [Application Design](#application-design)
  * [Landing page](#landing-page)
  * ["My Tickets" page](#mytickets-page)
  * [Admin Tickets page](#admintickets-page)
  * ["Create a Ticket" page](#createticket-page)
  * [View Ticket page](#viewticket-page)
* [Development History](#development-history)
  * [Advanced Features](#advanced-features)
* [Contact](#contact-us)

## About:
UH has many problems with broken stuff, especially restrooms. There have been too many times where I’ve entered a restroom with a broken door handle, missing soap, and rancid odors. In addition to restroom issues, there are other facility problems throughout UH.

## Installation:
- TODO

## Application Design:
Our application aims to try to end that by providing a platform for students and faculty to submit repair tickets for certain areas. Repair tickets include description of the problem, location, and image of the issue. Repair tickets may be “upvoted” for awareness by other users, so that the ticket gains attention from administrators.

- Landing page: Listing of all current tickets with navigation/filter bar (filter by ticket age, location, popularity), with login/sign up on the top right, contact information on the bottom.

- "My Tickets" page: Same as landing page, but with options to create a ticket, view your current tickets, follow a ticket (user will get notified of any updates to issue), view followed tickets, upvote tickets.

- Admin Tickets page: Same as user home page, but with options to view all users, edit tickets, delete tickets, and block users.

- Creating a ticket: when creating a ticket, the user will have to specify 1) what building the issue is in, 2) what type of facility the issue is in (e.g. bathroom, classroom), 3) specifically what the issue is in that room. Users can specify a severity level (on a scale from mild to critical). Users can upvote other tickets for awareness and report/flag to filter “trolls”. A ticket, by default, is unresolved and when seen by administrators, can be updated to received (meaning that the issue is acknowledged). Users can vote a ticket to be resolved, then administrators can mark a ticket as resolved once they verify whether or not the issue is actually fixed (upload a picture of the resolved issue?). 

- Viewing a ticket: when viewing a ticket, the user can comment on the ticket. @Administrators can add a projected finish date to a ticket after receiving it, which lets users know when they plan to work on fixing the issue.

## Development History:
### Milestone 1:
- Create basic structure of application (without functional buttons)
  - Create landing page for viewing of all tickets
  - Create admin page for viewing all tickets, but with options for deletion and update
  - Create page to view individual tickets, with options to comment on them as well as view any updates on the ticket
  - Create page to add tickets
- Add fake data for visualization of tables of tickets (w/o mongoDB collections)

### Milestone 2:
- Implement sorting on landing page
- Add search/filter bar to landing page and user/admin ticket pages
  - Implement prototypes for filters, searches, and sorting
- Add upvoting column to landing page
- Link fake data to mongoDB collections
- When viewing a ticket, link it to the actual ticket to be viewed
- Remove "Ticket-Admin" tab and detect whether or not the user is an admin. If the user is an admin, then redirect to view ticket page with additional admin options (update, delete)
- Add upvoting column for landing page
- Create "My Tickets" tab for tickets that the user is following and the tickets that the user owns

### Milestone 3:
- Implement "quick tabs", such as an "Unresolved Tickets" tab
- TODO

#### Advanced Features
These features may not necessarily get implemented due to time constraints, but they are things that we thought might make our application more useful.
  - Based on number of upvotes, increase the hue of the color of the ticket status
  - Email alerts will be sent out for unresolved tickets (on some schedule? Based on severity level? Alert after 30 days if mild/Alert after a week if critical?) until they are resolved.
  - Create a geo-map of all of the tickets mapped out

## Contact Us:
- Joaquin Torres (jftorres@hawaii.edu)
- Nolan Puletasi (pn7@hawaii.edu)
- Michael Kurihara (mkurihar@hawaii.edu)
- Jason Maligon (jmaligon@hawaii.edu)
