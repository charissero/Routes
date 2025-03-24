# Requirements - Authored by Charisse

## User Needs

### User stories - A brief user stories to explain how various actors would interact with the system to accomplish a goal.
1. As an international student, I want to recieve different personalised routes I canexplore different parts of bristol in my day to day life 
2. As a beginner, I want to know be aware of low traffic areas, so I can practise riding in a quiter environement and feel more confident doing so 
3. As a worker that cycles to and from my workplace, I want to take the quiet route through the park I took last Wednesday to peacefully reflect on my day as I go home - Charisse

### Actors
1. Cyclists (of all levels incl beginner)
2. Students
3. Workers

### Use Cases - description of usecases ID'd by UC1, UC2 etc

| UC1 | UC1: Requesting to cycle on a path in an urban area | Author: Charisse Oppon |

| -------------------------------------- | ------------------- |

| **Description** | As part of my explorations, today I want to cycle through an urban park as I go home |

| **Actors** | International student (beginner level cyclist) |

| **Assumptions** | 1. User is signed in 2. User's home address is in the database already as part of onboarding 2. App supports geolocation(to find out where they are currently) 2. Geolocation access granted during onboarding (while app is in use)|

| **Steps** | 1. System prompts the User with "Hi (name)! How are ya, what would you like today ?"
              2. System will request to use the user's current location via a popup, prompting user to "allow" or "don't allow"
              3. System will retrieve the nearest route details from the database that matches the criteria
              4. System will format and display one option with route name i.e Avon cycle way and current + destination adresses and a visual map of the route from their current to their destination
              5. Prompt User to accept or decline route 
              6. If route was accepted, save route on users profile (without changing pages) |
              
| **Variations** | 2. User declines access to their currrent location
                   2. Users geolocation has been turned off (preventing pop up from appearing)
                   3. Users requested route criteria cannot be matched in the database 
                   4. Route doesn't have a route name 
                   5. User declines route |
                   
| **Non-functional** | 2. The system should prompt the User to re-enable geolocation and guide them to the device’s settings.
                       3. The system should display "This route cannot be found, what about Route 1.x, Route 2.x or 3.x routes" suggesting three similar routes that can be found in the database and prompt the user to accept one of the routes by clicking on the option. 
                       4. System should display "Un-named route", the characteristic and the status i.e. Un-named route, cycle path in an urban area and traffic free route  
                       5. The system should display 2 prompts in a pop-up i.e "Route doesn't match my criteria" and "Want a different option". Based on the option selected alter the route, display new route and prompt for user to accept or decline route. |
                          
| **Issues** | TODO: OPTIONAL - List of issues that remain to be resolved |


| UC2 | UC2: Revisiting a past saved route| Author: Charisse Oppon |

| -------------------------------------- | ------------------- |

| **Description** | As a worker that cycles to and from my workplace, I want to take the quiet route through the park I took last Wednesday, to peacefully reflect on my day as I go home |

| **Actors** | Worker (intermediate cyclist) |

| **Assumptions** | 1. User is signed in 2. User's home postcode in database already as part of onboarding 2. App supports geolocation 2. Geolocation access granted during onboarding (while app is in use)|  |

| **Steps** | 1. System prompts the User with "Hi (name)! How are ya, what would you like today ?"
              2. System will retrieve the requested past saved route from User profile 
              4. Format and display the saved past route details i.e route name i.e Avon cycle way, starting address + destination and a visual map of the route from the starting address to their destination
              5. Prompt User to accept or decline route 
              6. If route was accepted, save route on users profile - on User profile save as 
                 "Route taken again on (date)" |
              
| **Variations** | 2. Past saved route not recognised from the past saved database
                   3. Route doesn't have a route name 
                   4. User declines route |
                   
| **Non-functional** | 2. The system should display "Past saved route not found, please try again". 
                       3. System should display "Unamed route", the characteristic and the status i.e. Un-named route, cycle path in an urban area and traffic free route.
                       5. The system should display prompt pop-up "Not accurate to requested" if selected, system should repeat step 2, display the route and prompt for user to accept or decline route. |
                          
| **Issues** | TODO: OPTIONAL - List of issues that remain to be resolved |

TODO: Your Use-Case diagram should include all use-cases.

![Insert your Use-Case Diagram Here](images/use-case.png)

## Software Requirements Specification
### Functional requirements

| UC1 | Authored by Charisse Oppon |

- FR.1 The system **must** retrieve nearest route details that matches criteria from database ‘Open data Bristol’.
- FR.2 The system **must** format retrieved route details i.e route name, characteristics and status in user friendly way for display from database ‘Open data Bristol’.
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
- **NFR1:** All sensitive user data (e.g., geolocation, home address, number etc) **must** be encrypted both whilst being transferred and when stored in the database. **(Security)**
- **NFR2:** In the first iteration of Routes, the system **should** fully function on all IOS devices including response times to a precision of 4 seconds, which will be measured under testing with 5 users. **(Portability)**
- **NFR3:** The user request **must** be accurately reflected in the systems suggested route output i.e distance from live location for that suggestion, the environment, qualitative noise pollution levels in the area etc. **(Reliability)**
- **NFR4**: The system **should** provide a simple, intuitive user interface that requires no more than 5 minutes of onboarding. **(Usability)**
