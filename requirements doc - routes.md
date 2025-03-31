# Requirements - Authored by Charisse

## User Needs

### User stories - A brief user stories to explain how various actors would interact with the system to accomplish a goal.
1. As an international student, I want to recieve different routes to get home so I can explore different parts of bristol in my day to day life 
2. As a beginner, I want to know of low traffic areas, so I can practise riding in a quiter environement
3. As a worker that cycles to and from my workplace, I want to view and ride the quiet route through the park I took last Wednesday to peacefully reflect on my day as I go home 

### Actors
1. Cyclists (of all levels incl beginner)

### Use Cases - description of usecases ID'd by UC1, UC2 etc

| UC1 | UC1: Requesting to cycle on a path | Author: Charisse Oppon |
| -------------------------------------- | ---------|---------- |
| **Description** | As part of my explorations, today I want to cycle through an urban park as I go home |
| **Actors** | Cyclists (of all levels incl beginner) |
| **Assumptions** | <ol><li> User's home address is in the database already as part of onboarding.</li><li>App supports geolocation (to find out where they are currently).</li><li> Geolocation access granted during onboarding (while app is in use)</ol></li>|
| **Steps** | <ol><li>System prompts the User with "Hi (name)! How are ya, what would you like today ?"</li><li>System will request to use the user's current location via a popup, prompting user to "allow" or "don't allow"</li><li>System will retrieve the nearest route details from the database that matches the criteria</li><li> System will format and display one option with route name i.e Avon cycle way and current + destination adresses and a visual map of the route from their current to their destination</li><li>Prompt User to accept or decline route</li><li>If route was accepted, save route on users profile (without changing pages)</li></ol> |           
| **Variations** |<ol><li> User declines access to their currrent location</li><li> Users geolocation has been turned off (preventing pop up from appearing)</li><li> Users requested route criteria cannot be matched in the database </li><li> Route doesn't have a route name </li><li> User declines route</li></ol> |   
| **Non-functional** |<ol><li> The system should prompt the User to re-enable geolocation and guide them to the device’s settings.</li><li>The system should display "This route cannot be found, what about Route 1.x, Route 2.x or 3.x routes" suggesting three similar routes that can be found in the database and prompt the user to accept one of the routes by clicking on the option.</li><li>System should display "Un-named route", the characteristic and the status i.e. Un-named route, cycle path in an urban area and traffic free route.</li><li>The system should display 2 prompts in a pop-up i.e "Route doesn't match my criteria" and "Want a different option". Based on the option selected alter the route, display new route and prompt for user to accept or decline route.</li></ol>|                   
| **Issues** | N/A |


| UC2 | UC2: Managing Past Saved Routes| Author: Charisse Oppon |
| -------------------------------------- | -------|------------ |
| **Description** | I want to view the quiet route through the park I took last Wednesday and either take it again or delete it from my user profile |
| **Actors** | Cyclists (of all levels incl beginner) |
| **Assumptions** | <ol><li>User's home postcode in database already as part of onboarding.</li><li>App supports geolocation.</li><li>Geolocation access granted during onboarding (while app is in use).</ol></li>|
| **Steps** | <ol><li>System displays past saved routes stored locally (found in the profile).</li><li>System expands selected past route details in a popup), including details from the preview and two extra buttons : "Take this route again" or "Delete saved route".</li><li>System will load the screen with the selected route and save the route as "Route taken again on (date)"- If user selects "Take this route again".</li></ol> |                     
| **Variations** | <ol><li> No past saved routes found (i.e no routes have been accepted yet).</li><li>User selects "Delete saved route".</li></ol> |         
| **Non-functional** |<ol><li>System should display "No saved routes at the moment".</li><li>System should display "Route succesfully deleted" and delete the route from 'Past saved routes' section.</li></ol>          
| **Issues** | N/A |

TODO: Your Use-Case diagram should include all use-cases.

![Insert your Use-Case Diagram Here](images/use-case.png)

## Software Requirements Specification
### Functional requirements

| UC1 | Authored by Charisse Oppon |

- FR.1 The system **must** retrieve nearest route details that matches criteria from database ‘Open data Bristol’.
- FR.2 The system **must** format retrieved route name i.e Avon cycle way from the 'Open data Bristol' database and their current + destination adresses with a visual map of the route.
- FR.3 The system **should** send formatted route details to the boundary results object.
- FR.4 The system **should** save the route details (if accepted) to User profile entity.

| UC2 | Authored by Charisse Oppon |

- FR.1 The system **must** retrieve requested saved past route from User profile.
- FR.2 The system **must** send requested saved past route to the boundary results object.
- FR.3 The system **could** save the requested past route again (if accepted), to User profile as “Route taken again on (date)”.

### Non-Functional Requirements
TODO: Consider one or more [quality attributes](https://en.wikipedia.org/wiki/ISO/IEC_9126) to suggest a small number of non-functional requirements.
Give each non-functional requirement a unique ID. e.g. NFR1, NFR2, ...
Indicate which UC the requirement comes from 

Global non-function requirements : (not tied to a specific UC)
- **NFR1:** All user data (e.g., geolocation, home address, number etc) **must** be encrypted both whilst being transferred and when stored in the database. **(Security)**
- **NFR2**: The system **should** provide a simple user interface that requires no more than 3 minutes of onboarding. **(Usability)**
- **NFR3** The system should load within 3 seconds. **(Reliability)**
