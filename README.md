# SweetAlert2 Module for Mendix

## Getting Started
_NOTE: It is recommended that you use a minimum of Mendix 8.2, as you may run into further limitations from not being able to call Microflows from Nanoflows._
## Configuration
- Download the module and give all users the User role so they can access the content.
- Give your button(s)/link(s) the ‘Call a Nanoflow’ action, using the JavaScript actions directly or use the nanoflows starting with **SUB_**
- If using only the nanoflow, create your decision paths and configure the parameters for the sub-nanoflow
- If calling microflow from nanoflow, return a status or value that would allow your nanoflow to fire the alerts based on the return of your microflow
- Feed in your parameters based on your decision path

## Features
- Does not require context (but it would help for customization)
- Allows custom HTML message content
- Relies on nanoflows which will help reduce server-side processing normally done with only microflows

## Limitations
- Is not currently plug-and-play, will require the steps below
- Real-time alerts are not possible without extra javascripting or use of something like the microflow timer widget.

## Additional Required Configuration
- Locate the ‘vendor’ folder in the following directory: C:\PATH\TO\MENDIX\PROJECT\\javascriptsource\sweetalert2
- Copy the ‘vendor’ folder into the projects theme folder
- Reference the contents of the ‘vendor’ folder into the index.html file
- Re-run the application