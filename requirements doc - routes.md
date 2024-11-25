# Requirements

## User Needs

### User stories
1. As an older lady, I want to use this personalised cycling system in exercise to keep fit so I won’t unconsciously push myself too hard - Charisse
2. As someone with anaemia who gets tired in longer journeys, I want to use routes to still want to enjoy the scenic landscape of Bristol, without going on unnecessarily strenuous routes for me - Charisse
3. As a beginner, I want to know how the weather will affect my travel including traffic, cautions incl cycling up and down hills etc as well as guidance on how best to approach this, so I feel more confident to actually get out there - Charisse

### Actors
TODO: List and describe the actors/users for this product.

### Use Cases
TODO: Describe each use case (at least one per team member).
    Give each use case a unique ID, e.g. UC1, UC2, ...
    Summarise these using the use-case template below.

    
UC1 Charisse - User 1 has a history of Anemia and can get tired on longer journeys. With it set to rain in 10 minutes, traffic is predicted to increase by 15%, prolonging user 1's journey to 1 hour instead of 30 minutes, with two steep hills along the way. Routes adapts User 1's journey : On this route User 1 will have a pitstop where they can rest inside a cafe before continuing, and there will only be one hill ahead instead of two. This route will take 35 minutes excluding the rest time. There will also be information about the elevation of that hill, how far the pitstop is from where they are currently, hydration and when the rain will stop etc. 


| UC1 | UC1: USE-CASE NAME | 
| -------------------------------------- | ------------------- |
| **Description** | I want to get home as quickly as possible in the least strenious way but I also want a pitstop on the way in a park |
| **Actors** | Cyclist |
| **Assumptions** | User is signed in
| **Steps** | 1. Input text prompt 2. Create custom route from database 3. Display route and it's features e.g pitstop 4. prompt User to accept or decline route 5. Save route(if route was accepted) |
| **Variations** | 4. User declines route |
| **Non-functional** | 1.The system should generate a text prompt for feedback on the declined route (to find out why the user doesn't like the route), 2. Based on this alter the route 3. Display the new route 3. Prompt User to accept or decline the new route|
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
