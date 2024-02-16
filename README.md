# SweetAlert2 Module for Mendix

## Getting Started
_NOTE: The basic modal and toast will not require any additional setup. The modals for user input, countdown/timer, and chaining will require alterations to fit your needs._

## How to Use
- Download the module and give all users the User role so they can access the content.
- Give your button(s)/link(s) the ‘Call a Nanoflow’ action, using the JavaScript actions directly or use the nanoflows starting with **SUB_**.
- If using only the nanoflow, create your decision paths and configure the parameters for the sub-nanoflow.
- If calling microflow from nanoflow, return a status or value that would allow your nanoflow to fire the alerts based on the return of your microflow.
- Feed in your parameters based on your decision path.

## Features
- Does not require context (but it would help for customization).
- Allows custom HTML message content.
- Relies on nanoflows which will help reduce server-side processing normally done with only microflows.
- Animate.css integration.
- Parts of modals can be given custom classes.

## Limitations
- Is not currently plug-and-play, will require the steps below.
- Real-time alerts are not possible without extra code or use of something like the microflow timer widget.
- Not all Animate.css animation seem to work as well as others when used on toast notifications.

## Additional Required Configuration
- Locate the ‘vendor’ folder in the following directory: C:\PATH\TO\MENDIX\PROJECT\javascriptsource\sweetalert2
- Copy the ‘vendor’ folder into the projects main theme folder, where index.html can be found
- Reference the contents of the ‘vendor’ folder into the head element of the index.html file in your theme folder.
-  **_If you do not have an index.html file in your theme folder, you should be able to find one in the deployment/web folder, after running your project at least once._**
- Use this code:
```
<script type="text/javascript" src="vendor/SweetAlert2/sweetalert2.all.min.js"></script>
<link rel="stylesheet" href="vendor/SweetAlert2/sweetalert2.min.css" />
<link rel="stylesheet" href="vendor/Animate.css/animate.min.css" />
```
- Re-run the application