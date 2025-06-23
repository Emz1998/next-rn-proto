# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

NextRn is a mobile-first social and micro-learning platform connecting student nurses with registered nurses (RNs) for real-time mentorship, academic support, and career guidance. The app uses a hotel metaphor for different spaces:

- **Lobby (Threads)**: Social discussions and free expression space
- **Lounge (Chat)**: Intimate 1-on-1 conversations and paid DMs ($2/question)
- **Stage (Livestream)**: Educational sessions with Super Chat monetization
- **Guest Room**: Personal space for organization, reflection, and progress tracking
- **Hall of Excellence**: Recognition gallery for outstanding nurses

## Architecture

### Technology Stack
- **Frontend**: HTML5 prototype with Tailwind CSS 4.0 (browser version)
- **Icons**: Lucide icons via CDN
- **Target Platform**: React Native for iOS & Android (single codebase)
- **Mobile-first**: Designed for phones, tablet optimization later

### Navigation Pattern
The app follows a Discord-like navigation pattern:
- **Main Dashboard**: Icon-based sidebar (64px width) visible for room selection
- **Inside Rooms**: Sidebar completely hidden for immersive, full-width content
- **Room Switching**: Back navigation returns to main dashboard

### Current Implementation
The prototype is a single HTML file (`prototype-init.html`) with:
- Icon-based left navigation (64px)
- Secondary sidebar with channels/content (224px) - **TO BE REMOVED**
- Full-width main content area
- JavaScript for section switching and basic interactions

### Prototype Requirements
- **Phone Screen Mockups**: All prototypes must be designed within phone screen frames to simulate actual mobile device experience
- **Responsive Design**: Optimize for standard mobile viewports (375px-414px width)
- **Touch Interactions**: Design for thumb-friendly navigation and gestures

## Development Guidelines

### Git Workflow Requirements
**CRITICAL**: After completing ANY task or feature implementation:
1. **ALWAYS commit changes to git** with descriptive commit messages
2. **ALWAYS update development-log.md** with detailed documentation of changes
3. **Include commit hash and file changes** in the development log entry
4. **Document technical decisions and design rationale** for future reference
5. **Use conventional commit format** for consistency and clarity

### UI/UX Principles
- **Mobile-first responsive design**: Portrait primary, landscape optional for livestream
- **Dark theme**: Professional medical aesthetic with blue accent colors
- **Hotel metaphor**: Maintain spatial concept in navigation and user experience
- **Touch-friendly**: All interactive elements optimized for mobile taps and gestures

### Key Features to Implement
- Threaded discussions with like/bookmark functionality
- Paid DM queue system with payment processing
- Live streaming with Super Chat ($1 highlights)
- Personal dashboard with study tools, clinical tracking, and reflection prompts
- Push notifications for replies, DM responses, and livestream alerts
- Offline caching for last 50 messages and bookmarked posts

### Performance Requirements
- Cold start time: < 2 seconds
- Battery drain: ≤ 3% per hour active use
- Crash-free session rate: ≥ 99.6%

## Monetization Features
- Paid DMs: $2 per question to verified RNs
- Super Chats: $1 livestream message highlighting
- Tip jar system for additional RN compensation
- Premium subscriptions for enhanced features

## Target Metrics
- 5,000 downloads within 3 months of launch
- DAU/MAU ratio ≥ 35%
- Day-30 retention ≥ 25%
- Monthly GMV ≥ $8,000 by month 6

## File Structure Notes
- `prd.md`: Complete product requirements document
- `prototype-init.html`: Current HTML prototype
- `claude-instructions.md`: Step-by-step development process guide
- `reference.png`: UI reference showing desired sidebar removal
- `development-log.md`: Track all development work and changes made to the project