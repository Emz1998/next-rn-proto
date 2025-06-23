# Instruction for Claude

This file is to give initial instruction for claude on what we need to achieve in this project.

## Main Goal

Our goal is to improve our prototype and facilitate the process for the next agent who will build and develop the app after handoff.

## Mobile App Improvement Guidelines

### Sub-Goal 1: Add some missing features

- **Design the Authentication page**
  -Design the login page
  -Design the signup page - Must include forms for suitable credentials

- **Add Chat rooms in Chat message page**
  -Horizontal scrollable chat rooms on top like on "Messenger"

- **Design Settings Page**
  -Add suitable settings page"

### Sub-Goal 2: Rehaul the design structure.

**Critical**: DO NOT CHANGE THE STYLING. KEEP THE SAME COLOR, SAME TEXT SIZE, SAME SPACING

- **ONLY CHANGE THE CSS STRUCTURE**
  -We only make changes on the css structure
  -We restructure the css so that it can be restyled easily , using global variables, good naming-convention and etc

### Sub-Goal 3:Fix Current UI Problems

**NOTE** Refer to the /ui-problems folder for the list of current ui problems screenshots

- **UI Problem 1**
  -Reference: @problem-1.png
  -Issue: Main content is overflowing and pushing the navigation, making it squished.

  - **UI Problem 1.1**
    -Reference: @problem-1.1.png
    -Issue: This is related to the problem 1. The main livestream is over flowing vertically and horizontally. The page is not even scrollable.

- **UI Problem 2**
  -Reference: @problem-2.png
  -Issue: We need to take account for the notification panels and make a space for it. Right now it's taking all the height of the screen when in reality, there should be a notification panel on top. Please make a mockup that also include the notification panel.

- **UI Problem 3**
  -Reference: @problem-3.png
  -Issue: Contents are overflowing but not scrollable. And also the + button must only be present in threads.

- **UI Problem 4**
  -Reference: @problem-4.png
  -Issue: The color must be "--foreground for this icons" not muted

- **UI Problem 5**
  Reference: @problem-9.png
  -Issue: Remove those little icons on top of the help page.

- **UI Problem 6**
  Reference: @problem-6.png
  -Issue: Too much height. Place holder must only be "Ask a question". And the "+" button shouldnt appear in chat message.

- **UI Problem 7**
  Reference: @problem-7.png
  -Issue: The threads input should only appear as a popup when the + button is triggered to give more space to the user

- **UI Problem 8**
  Reference: @problem-8.png
  -Issue: Evertime a user scroll on the thread page the side must switch to bottom navbar(which only have switch page icon (use the "arrow-up-down" in lucide for switching pages. When this icon is triggered. a popup must show which contains the other nav icons)). When the user select main chat page(the page that contain chat rooms). It shouldnt have the bottom bar but instead it should have a top bar which contains a "navigation switch (arrow-up-down) and a 3 dots settings. When the user selected a chat room the top bar must contain a back button , a navigation switch, and 3 dots setting.

- **UI Problem 9**
  Reference: N/A
  -Issue: All the pages are not scrollable vertically. Please implement it.

  **CRITICAL\*\***PLEASE ANSWER THIS QUESTION\*\*
  -Would it be easier for you to do this in vanilla css? or just continue with tailwind css?
  -If you want vanilla css, would you be able to replicate the exact design in vanilla css?
