# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

NextRn is a mobile-first social and micro-learning platform connecting student nurses with registered nurses (RNs) for real-time mentorship, academic support, and career guidance. The app uses a hotel metaphor for different spaces:

- **Lobby (Threads)**: Social discussions and free expression space
- **Lounge (Chat)**: Intimate 1-on-1 conversations and paid DMs ($2/question)
- **Stage (Livestream)**: Educational sessions with Super Chat monetization
- **Guest Room**: Personal space for organization, reflection, and progress tracking
- **Hall of Excellence**: Recognition gallery for outstanding nurses

## Current Development Phase

The project is in the prototype improvement phase with the following goals:
1. **Add missing features**: Authentication pages, chat rooms, settings page
2. **Fix UI problems**: See `ui-problems/` folder for specific issues
3. **Restructure CSS**: Improve maintainability while keeping exact same styling

## Commands

### Development
- **View prototype**: Open `phone-mockup.html` in browser (wraps prototype in iPhone frame)
- **Direct prototype**: Open `prototype-init.html` directly
- **No build process**: Uses Tailwind CSS browser version via CDN

### Testing
- Manual testing in browser with 375×812px viewport (iPhone 14 Pro)
- Use browser dev tools device emulation for mobile testing

## Architecture

### Technology Stack
- **Frontend**: HTML5 prototype with Tailwind CSS 4.0 (browser version)
- **Icons**: Lucide icons via CDN
- **Target Platform**: React Native for iOS & Android (future conversion)
- **Mobile-first**: Designed for phones (375-414px width)

### File Structure
```
next-rn-proto/
├── prototype-init.html      # Main prototype file
├── phone-mockup.html        # iPhone frame wrapper (375×812px)
├── ui-problems/             # Screenshots of UI issues to fix
├── prd.md                   # Product requirements document
├── README.md                # Current development instructions
├── ui-improvement-plan.md   # Detailed plan for improvements
└── claude-log.md           # Development progress log
```

### Navigation Pattern
- **Icon-based sidebar**: 64px width, always visible
- **Main content area**: Flexible width, scrollable
- **Section switching**: Hash-based navigation with JavaScript

### Current UI Issues (Priority Order)
1. **Layout overflow**: Content pushing/squishing navigation
2. **Missing scrolling**: Pages need vertical scroll capability
3. **Dynamic navigation**: Bottom bar on scroll, top bar for chat
4. **Input improvements**: Thread input as popup, chat input refinements
5. **Icon colors**: Change from muted to --foreground where needed

## Development Guidelines

### Critical Rules
**STYLING**: DO NOT CHANGE colors, text sizes, or spacing - only fix structure
**CSS APPROACH**: Continue using Tailwind CSS (not vanilla CSS)
**VIEWPORT**: All designs must work within 375×812px iPhone frame

### Git Workflow Requirements
After completing each task:
1. **Commit changes** with descriptive message
2. **Update claude-log.md** with what was done
3. **Push after completing each sub-goal**

### CSS Variables in Use
```css
--background, --foreground, --primary, --muted, --border, etc.
```
These are already defined and should be used consistently.

## Current Tasks (from README.md)

### Sub-Goal 1: Add Missing Features
- Design authentication pages (login/signup with appropriate forms)
- Add horizontal scrollable chat rooms (Messenger-style)
- Design comprehensive settings page

### Sub-Goal 2: CSS Structure Improvements
- Improve CSS organization (while keeping exact styling)
- Use global variables effectively
- Implement consistent naming conventions

### Sub-Goal 3: Fix UI Problems
See `ui-problems/` folder for visual references of each issue.

## Performance Requirements
- Cold start time: < 2 seconds
- Battery drain: ≤ 3% per hour active use
- Crash-free session rate: ≥ 99.6%

## Important Notes
- This is a prototype for handoff to next development team
- Focus on mobile-first design (phones only for now)
- All features should work within the phone mockup iframe