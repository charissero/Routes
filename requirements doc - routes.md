# Requirements

## User Needs

### User stories - Write brief user stories to explain how various actors would interact with the system to accomplish a goal.
1. As an international student, I want to recieve different personalised routes I can take to get around different parts of bristol with different scenary - Charisse
2. As a beginner, I want to know be aware of low traffic areas, so I can practise riding in a quiter environement and feel more confident doing so - Charisse
3. As a worker that cycles to my workplace, I want to take the quiet route through the park I took last Wednesday to peacefully reflect on my day as I go home - Charisse

### Actors
1. Cyclists (of all levels incl beginner)
2. Students
3. Workers

### Use Cases
TODO: Describe each use case (at least one per team member).
    Give each use case a unique ID, e.g. UC1, UC2, ...
    Summarise these using the use-case template below..

| UC1 | UC1: Recieve Cycle path in an urban area | Author: Charisse Oppon |

| -------------------------------------- | ------------------- |

| **Description** | As an international student, I want a personalised route today where I can cycle in an urban area to sight-see as I go home |

| **Actors** | International student (beginner level cyclist) |

| **Assumptions** | 1. User is signed in 2. User's home postcode in database already as part of onboarding 3. App supports geolocation |

| **Steps** | 1. User inputs request to go through an urban area on the way home for 
                 sightseeing purposes
              2. System requests for access to geolocation
              3. If access granted, system will retrieve nearest route details from the database 
                 that matches the criteria
              4. System will format and display route details i.e route name, characteristics and 
                 status - Avon cycle way, Cycle path in ubran area, traffic free route 
              5. Prompt User to accept or decline route 
              6. If route was accepted, save route on users profile |
              
| **Variations** | 3. User requests for a route criteria that cannot be found in the database 
                   2. Users geolocation is turned off
                   4. Route doesn't have a route name 
                   5. User declines route |
                   
| **Non-functional** | 1. The system should display "This route cannot be found, what about x routes" and suggest three similar routes that can be found in the database and collect feedback from user. 2. The system should prompt the User to re-enable geolocation and guide them to the device’s settings. 4. System should display "Unamed route", the characteristic and the status. 5. The system should generate a text prompt for feedback on the declined route (to find out why the user doesn't like the route), alter the route based on this, display new route and collect feedback for new route. |
                          
| **Issues** | TODO: OPTIONAL - List of issues that remain to be resolved |


| UC2 | UC2: Revisiting a past saved route| Author: Charisse Oppon |

| -------------------------------------- | ------------------- |

| **Description** | As a worker that cycles to my workplace, I want to take the quiet route through the park I took last Wednesday, to peacefully reflect on my day as I go home |

| **Actors** | Worker (intermediate cyclist) |

| **Assumptions** | 1. User is signed in 2. User's home postcode in database already as part of onboarding 3. App supports geolocation 4. All accepted routes are saved into Users profile |

| **Steps** | 1. User inputs request to take the quiet route through the park they took last 
                 Wednesday
              2. System requests for access to geolocation
              3. If access granted, system will retrieve the requested past saved route from 
                 User profile 
              4. Display the saved past route details i.e route name, characteristics and 
                 status i.e  Unamed route, Canalside path, traffic free route 
              5. Prompt User to accept or decline route 
              6. If route was accepted, save route on users profile - on User profile save as 
                 "Route taken again on (date)" |
              
| **Variations** | 2. Users geolocation is turned off
                   3. Route described isn't in the User profile i.e hasn't been saved
                   4. Route doesn't have a route name 
                   5. User declines route |
                   
| **Non-functional** | 2. The system should prompt the User to re-enable geolocation and guide them to the device’s settings. 3. System should display error message "Saved route not found" and suggest a route from database that matches the requested route preferance 4. System should display "Unamed route", the characteristic and the status. 5. The system should generate a text prompt for feedback on the declined route (to find out why the user doesn't like the route), alter the route based on this, display new route and collect feedback for new route. |
                          
| **Issues** | TODO: OPTIONAL - List of issues that remain to be resolved |

TODO: Your Use-Case diagram should include all use-cases.

![Insert your Use-Case Diagram Here](images/use-case.png)

## Software Requirements Specification
### Functional requirements

| UC1 | Authored by Charisse Oppon |

- FR.1 The system **must** get User geolocation from geolocation object.
- FR.2 The system **must** retrieve nearest route details that matches criteria from database ‘Open data Bristol’.
- FR.3 The system **must** format retrieved route details i.e route name, characteristics and status in user friendly way for display from database ‘Open data Bristol’.
- FR.4 The system **should** send formatted route details to the boundary results object.
- FR.5 The system **should** save the route details (if accepted) to User profile entity.

| UC2 | Authored by Charisse Oppon |

- FR.1 The system **must** get User geolocation from geolocation object.
- FR.2 The system **must** retrieve requested saved past route from User profile.
- FR.3 The system **must** send requested saved past route to the boundary results object.
- FR.4 The system **could** save the requested past route again (if accepted), to User profile as “Route taken again on (date)”.

### Non-Functional Requirements
TODO: Consider one or more [quality attributes](https://en.wikipedia.org/wiki/ISO/IEC_9126) to suggest a small number of non-functional requirements.
Give each non-functional requirement a unique ID. e.g. NFR1, NFR2, ...
Indicate which UC the requirement comes from.

- *NFR1:* All sensitive user data (e.g., geolocation, home address, number etc) *must* be encrypted both whilst being transferred and when stored in the database. *(Security)*
- *NFR2:* In the first iteration of Routes, the system *should* fully function on all IOS devices including response times to a precision of 4 seconds which will be measured under testing with 5 users. *(Portability)*
- *NFR3:* The user request *must* be accurately reflected in the systems suggested route output i.e distance from live location for that suggestion, the environment, qualitative noise pollution levels in the area etc. *(Reliability)*
