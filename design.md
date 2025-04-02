# Design - documentation and wireframe/flow

### Design explanation : Below describes the user journey for requesting a cycling route (UC1) and managing past saved routes (UC2) within the app, illustrated in the wireflow/wireframe. 
- There is also additional notation to account for how variations can be illustrated in alignment with the requirements.
   
# UC1
Starting from the Home Screen(**Splash Page**): The user is greeted with a prompt asking for their preferred route type and a white box for them to type into.

Location Access Prompt: Once recieved the system will requests permission to use the user’s current location via a pop up message in which the user can click **allow** or **don't allow**.
- If the user clicks **allow**, another popup will appear where the user can manually enter a location or just click the location icon (after which the popup will disappear)
  
Route Suggestions: Once the user clicks the location icon or enters their location, another popup will appear in it's place with the **user's selected a route, a map image, their starting and finishing destination along with a message **accept** or **decline**. 
- Once the route has been accepted by the user, the user will be taken to the home page (**splash page**) where the route details will be on the full screen.

# UC2
Starting from their user profile entity labelled as (their name) : The user clicks a past saved route, which will then expand with details from the preview, the starting + final location and two extra buttons : "Take this route again" or "Delete saved route".
- If the user clicks **"Take this route again"**, the system will load to the home page with the user's selected route, a map image, and their starting and finishing destination on the full screen.

## How the System will handle variations and Non-Functional Considerations
While the wireflow primarily illustrates the standard process, **variations** noted in the requirements such as unavailable routes, declined location access, or user-requested modifications will be handled through contextual UI elements like pop-ups, inline messages, and alternative route suggestions, ensuring a seamless user experience.

UC1
- If the user has turned off their geolocation access should prompt the User to re-enable geolocation via a popup icon with the message "re-enable geolocation" which once clicked will take them to the device settings (there will also be an x to exit from the popup).
- If the requested route cannot be found the system should display a popup icon with the message "This route cannot be found, what about Route 1.x, Route 2.x or 3.x routes" suggesting three similar routes that can be found in the database and prompt the user to accept one of the routes by clicking on that option, this will then load the route details on the home page as the full screeen.
- If the requested route doesn't have a name the system should display "Un-named route", the characteristic and the status i.e. Un-named route, cycle path in an urban area and traffic free route.
- If the user declines the route suggested by the system, the system should display 2 prompts in a pop-up i.e "Route doesn't match my criteria" and "Want a different option". Based on the option selected alter the route, display new route and prompt for user to accept or decline route in a new popup.

UC2	
- If there are no past saved routes yet the system should display a text in that section notes "No past saved routes" (i.e no routes have been accepted yet).
- If the User selects "Delete saved route", the system should remove the saved past route from the profile entity and display a pop-up message noted "Past saved route has been succesfully deleted".

## Wireframe/Wireflow - Please zoom in if needed.
![Routeswireflow](https://github.com/user-attachments/assets/1fe2830d-0483-4670-9f61-e9b17a095308)
