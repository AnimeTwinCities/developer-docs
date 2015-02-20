Application Analytics
=====================

The Anime detour applications track certain events by the user
in order to analyze usage and improve the application experience.
The goal of this document is to track each of the events for
both of the applications.

Tracking details
----------------

### Events

[A] | [I] | Category | Action          | Label        | Value | Description
----|-----|----------|-----------------|--------------|-------|------------
 Y  |     | Event    | View Details    | `event.name` |       | User clicks on an event card to see a more detailed view/description.
 Y  |     | Event    | Favorite        | `event.name` |       | User marks the event as favorited/starred.
    |     | Guest    | View Details    | [guest name] |       | User clicks on a guest name to see a the full bio info.
    |     | Home     | Suggested Click | `event.name` |       | User clicks on a suggested event from the home page.
    |     | Settings | Notifications   |              | 0|1   | User has enabled or disabled notifications. 0=off 1=on
    | N/A | Settings | Dev-enable      |              |       | User enabled developer options.


### Screens

[A] | [I] | Name         | Description
----|-----|--------------|------------
 Y  |     | Home         | The initial overview/landing page.
 Y  |     | Event        | Full Details about a single event.
 Y  |     | Schedule     | List of all the programming events & panels.
 Y  |     | Favorites    | List of panels/events that the user has starred.
 Y  |     | Guests       | List of the official guests for the con.
 Y  |     | Guest Detail | Full details about a single guest.
    |     | Map          | Hotel floor plan map.
    |     | Settings     | Application specific preferences.


### Key

#### `[A]`
Whether the tracking is implemented in Android

#### `[I]`
Whether the tracking is implemented in iOS

#### Guest Name
Guest names are represented in the concatenated name in format:
`guest.FirstName + " " + guest.LastName`

[A]: #a
[I]: #i
[Guest Name]: #guest-name
