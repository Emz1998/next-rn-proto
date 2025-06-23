# Updated Plan for NextRN Mobile App Improvements

## Overview
Since the final version uses `phone-mockup.html` with an iframe displaying `prototype-init.html`, I'll modify `prototype-init.html` to work properly within the 375×812px iPhone frame.

## 1. Critical Layout Fixes (High Priority)

### Fix Main Container Structure
- Remove `h-screen` and `overflow-hidden` from body to allow proper scrolling
- Adjust flex containers to work within iframe constraints
- Ensure sidebar stays fixed at 64px width
- Make main content area properly scrollable

### Fix Navigation Issues
- Keep left sidebar visible and fixed width
- Implement dynamic navigation (bottom bar on scroll for threads)
- Add top navigation bar for chat/messages section

## 2. Add Missing Features

### Authentication Pages
- Create login page with email/password fields
- Create signup page with:
  - Name, email, password fields
  - Student/RN role selection
  - School/institution field

### Chat Rooms Feature
- Add horizontal scrollable chat room list at top of chat section
- Style like Messenger with circular avatars
- Include online status indicators

### Settings Page
- Profile settings with photo upload
- Notification preferences
- Account settings
- Privacy settings

## 3. Fix Specific UI Problems

- **Problem 1**: Fix sidebar getting squished by constraining main content
- **Problem 2**: Add notification panel space at top
- **Problem 3**: Enable vertical scrolling on all pages
- **Problem 4**: Change muted icon colors to --foreground
- **Problem 5**: Remove extra icons from help page
- **Problem 6**: Reduce chat input height, change placeholder
- **Problem 7**: Convert thread input to popup modal
- **Problem 8**: Implement dynamic navigation switching
- **Problem 9**: Ensure all content is scrollable

## 4. CSS Improvements

### Structure Changes
- Organize CSS into logical sections
- Use CSS variables consistently
- Add mobile-specific adjustments
- Ensure all styles work within 375px width

### Responsive Adjustments
- Optimize for 375×812px viewport
- Adjust font sizes for mobile
- Ensure touch-friendly tap targets (min 44px)
- Add proper padding/margins for mobile

## 5. Implementation Order

1. Fix the main layout structure and scrolling
2. Add authentication pages (login/signup)
3. Implement chat rooms feature
4. Complete settings page design
5. Fix all UI problems in sequence
6. Refine CSS structure
7. Test everything within phone mockup frame

## Note on Approach
- Keep all existing styles/colors as requested
- Only restructure CSS for better maintainability
- Ensure everything works within the iPhone mockup frame
- Maintain mobile-first approach throughout