
---
### Core Technologies

[![My Skills](https://skillicons.dev/icons?i=kotlin,ktor,idea,mongodb&theme=dark)](https://skillicons.dev)
- **Kotlin** for robust backend development
- **Ktor** for server and client connectivity
- **MongoDB** for a flexible data layer
- **Koin** for efficient dependency injection
- **Keycloak** for secure authentication
### Architectural Patterns and Key Design Choices

![freshnearme.drawio.svg](assets%2Ffreshnearme.drawio.svg)


This project is still a work in progress, presented architecture approach has **not yet** been fully implemented across all modules. The depicted relationships between modules are symbolic and are intended to illustrate potential ways in which modules might interact with each other. They do not represent the exact, current dependencies between modules. The purpose of this section is to show the general concept and direction in which the project is evolving.


---
## Detailed Breakdown of Functionalities by Module

### User Module Functionalities

- **Retrieve Basic User Information**: Gets basic details about a user, specified by the user ID.

- **Fetch User Offers**: Retrieves offers associated with a specific user, identified by their user ID.

- **Get Detailed User Info (Authenticated)**: Obtains comprehensive information about the currently authenticated user.

- **Retrieve User Wishlist (Authenticated)**: Gets the wishlist belonging to the currently authenticated user.

- **Update User Wishlist (Authenticated)**: Allows the currently authenticated user to update their wishlist.

- **Update User Offers (Authenticated)**: Enables the currently authenticated user to update their offers.

### Categories Module Functionalities

- **Create Category (Admin Only)**: Allows administrators to create new categories by submitting category data.

- **Update Category (Admin Only)**: Enables administrators to update existing categories. The specific update logic is
  to be implemented.

- **List All Categories**: Retrieves a list of all available categories.

- **Get Category Details**: Fetches details of a specific category identified by its unique ID.
  Based on the provided Kotlin code for offer routes, here's a straightforward description of each route's functionality
  within the Offer Module:

### Offer Module Functionalities

- **List All Offers**: Retrieves a list of all offers, optionally filtered by category, distance, and coordinates.

- **Search Offers by Name**: Fetches offers based on a search query for offer names. Requires the query parameter '
  name'.

- **Get Single Offer by ID**: Retrieves details of a specific offer, identified by its ID.

- **Add New Offer (Authenticated)**: Allows authenticated users to add a new offer. Requires an `OfferDto` object in the
  request body.

- **Update Existing Offer (Authenticated)**: Enables authenticated users to update an existing offer specified by its
  ID. Requires an `OfferDto` object in
  the request body.

### Ratings Module Functionalities

- **Retrieve Ratings by User** Retrieves all ratings given to a user, identified by their user ID.

- **Retrieve Rating by ID**: Fetches details of a specific rating using its unique rating ID.

    - **Post a New Rating (Authenticated)** Allows authenticated users to submit a new rating.
    - **Update an Existing Rating (Authenticated)** Enables users to update a rating, identified by its rating ID.
    - **Delete a Rating (Authenticated)** Permits users to delete a rating using its rating ID.
    - **Retrieve Ratings by user (Authenticated)** Fetches all ratings given by the currently authenticated user.

### Auth Module Functionalities

- **User Registration**:
    - Triggered by Keycloak registration events.
    - Saves new user data in the database upon successful registration.

- **User Login**:
    - Triggered by Keycloak login events.
    - Updates existing user data in the database following a successful login.

---
### Chat service Features

The chat service uses **WebSocket** for seamless communication within the platform.

#### Real-Time Messaging
- Users can instantly message each other in real-time, providing an engaging and interactive chat experience.

#### Conversation Rooms
- Participants can create private conversation rooms linked to specific products, allowing for private discussions.

- Users can retrieve the complete history of messages in any of their direct conversations.

- Individuals can easily access all their direct conversations, streamlining communication and enabling quick transitions between multiple discussions.

This service enables straightforward, direct, and private correspondence between users.

---

## User Authentication Process

1. **User Login and Registration**:
    - Users can log in or register through a traditional website form or via a REST API endpoint.
    - This process is managed by Keycloak.


2. **Credential Storage**:
    - After successful authentication, Keycloak stores the user's credentials in its database.


3. **User Registration Notification**:
    - When a new user registers, the Backend-API receives a notification.
    - Keycloak sends an HTTP request with the user's data to the specified endpoint, requiring the creation of a
      custom [SPI](https://github.com/Lycan7hropus/keycloak-listener-kotlin) for registration and login event listening.


4. **Storing User Info in the Database**:
    - The Backend-API saves the user's information in the application's database after successful validation and
      authorization.
    - This information is used for personalizing the user experience and managing the account.


5. **Token Validation**:
    - The Backend-API and chat service validate the token by sending it to the Keycloak server.
    - The server provides information about the user or returns a response if the token is invalid.

![authflow.drawio.svg](assets%2Fauthflow.drawio.svg)

---
### Installation
Detailed installation instructions will be provided. Stay tuned for updates.

![](https://media.tenor.com/0pfgtiySgtIAAAAM/endwork-cats-end-work.gif)

![footer.png](assets%2Ffooter.png)
