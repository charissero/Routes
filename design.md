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

## Wireframe/Wireflow - Please zoom in if needed.
![Routeswireflow](https://github.com/user-attachments/assets/360e74e4-db27-43d8-ac45-486c5f6cf3f5)
