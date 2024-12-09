# Requirements

## User Needs

### User stories - Write brief user stories to explain how various actors would interact with the system to accomplish a goal.
1. As an international student, I want personalised routes I can take around bristol depending on how I'm feeling - Charisse
2. As a beginner, I want to know be aware of low traffic areas, so I can practise riding in a quiter environement and feel more confident doing so - Charisse

### Actors
1. Cyclists (of all levels incl beginner)
2. People new to bristol

### Use Cases
TODO: Describe each use case (at least one per team member).
    Give each use case a unique ID, e.g. UC1, UC2, ...
    Summarise these using the use-case template below.

    
UC1 Charisse - User 1 has a history of Anemia and can get tired on longer journeys. With it set to rain in 10 minutes, traffic is predicted to increase by 15%, prolonging user 1's journey to 1 hour instead of 30 minutes, with two steep hills along the way. Routes adapts User 1's journey : On this route User 1 will have a pitstop where they can rest inside a cafe before continuing, and there will only be one hill ahead instead of two. This route will take 35 minutes excluding the rest time. There will also be information about the elevation of that hill, how far the pitstop is from where they are currently, hydration and when the rain will stop etc. 


| UC1 | UC1: USE-CASE NAME | 
| -------------------------------------- | ------------------- |
| **Description** | As an international student, I want a personalised route today where I can be in an urban area to sight see as I go home |
| **Actors** | International student |
| **Assumptions** | 1. User is signed in 2. User's home postcode in database already as part of onboarding 3. App supports geolocation
| **Steps** | 1. User inputs request to go through an urban area on the way home for sightseeing purposes
              2. System requests for access to geolocation
              3. If access granted, system will retrieve nearest route from the database that matches the criteria
              4. Display route name, characteristics and status i.e  Avon cycle way, Cycle path in ubran area, traffic free route 
              5. Prompt User to accept or decline route 
              5. If route was accepted, save route on users profile |
| **Variations** 1. User requests for a route criteria that cannot be found in the database 
                 2. User declines route
                 4. Route doesn't have a route name 
                 5. User declines route |
| **Non-functional** | 1. The system should...... 2.The system should generate a text prompt for feedback on the declined route (to find out why the user doesn't like the route), alter the route based on this, display new route and collect feedback for new route 
| **Issues** | TODO: OPTIONAL - List of issues that remain to be resolved |


TODO: Your Use-Case diagram should include all use-cases.

![Insert your Use-Case Diagram Here](images/use-case.png)

## Software Requirements Specification
### Functional requirements
TODO: create a list of functional requirements. 
    e.g. "The system shall ..."
    Give each functional requirement a unique ID. e.g. FR1, FR2, ...
    Indicate which UC the requirement comes from.


### Non-Functional Requirements
TODO: Consider one or more [quality attributes](https://en.wikipedia.org/wiki/ISO/IEC_9126) to suggest a small number of non-functional requirements.
Give each non-functional requirement a unique ID. e.g. NFR1, NFR2, ...

Indicate which UC the requirement comes from.
