# FloodRescueNet Design Guidelines

## Design Approach: Hybrid Emergency-Focused Design
**Justification**: This is a critical emergency response application requiring both quick usability and clear visual hierarchy. Drawing inspiration from emergency service apps while maintaining accessibility standards.

**Key Design Principles**:
- **Clarity over beauty**: Every element must be immediately understandable
- **High contrast**: Ensure visibility in poor lighting/stress conditions
- **Large touch targets**: Accommodate all users including elderly
- **Offline-first visual feedback**: Clear indicators for network status

## Core Design Elements

### A. Color Palette
**Primary Colors**:
- Emergency Red: 355 85% 55% (SOS, urgent alerts)
- Safety Green: 145 65% 45% ("I'm Safe" status)
- Warning Orange: 35 90% 60% ("Trapped" status)
- Help Blue: 210 80% 50% ("Need Help" status)

**Supporting Colors**:
- Background: 220 15% 8% (dark mode primary)
- Surface: 220 12% 12% (card backgrounds)
- Text Primary: 0 0% 95%
- Text Secondary: 220 10% 70%

### B. Typography
**Font Stack**: Inter (Google Fonts)
- Headers: 600 weight, sizes 24px-32px
- Body: 400 weight, 16px minimum for readability
- Emergency buttons: 500 weight, 18px
- Status indicators: 500 weight, 14px

### C. Layout System
**Spacing**: Tailwind units of 4, 6, and 8 (consistent 16px, 24px, 32px spacing)
- Component padding: p-4
- Section spacing: space-y-6
- Button heights: h-12 minimum for touch accessibility

### D. Component Library

**Emergency Status Cards**:
- Large, color-coded buttons with clear icons
- Prominent visual feedback for selected state
- Offline queue indicators

**Interactive Map Component**:
- Full-width container with overlay controls
- Color-coded road status (green=safe, red=blocked, orange=caution)
- Floating action buttons for map controls

**SOS Button**:
- Fixed position, highly visible
- Pulsing animation when activating
- Clear countdown/confirmation state

**Shelter Cards**:
- Distance prominently displayed
- Capacity indicators with visual bars
- Contact information easily accessible

**Photo Upload Interface**:
- Large drop zone with clear instructions
- Progress indicators for uploads
- Offline queue management

**Emergency Contacts Dashboard**:
- Grid layout with large touch targets
- Icons for quick recognition
- One-tap calling functionality

### E. Navigation & Information Architecture

**Bottom Navigation**:
- 5 primary sections: Status, Map, Shelters, SOS, Contacts
- Icons with labels for clarity
- Badge indicators for urgent updates

**Offline Indicators**:
- Persistent connection status bar
- Queue counters for pending messages
- Sync progress indicators

## Mobile-First Considerations

**Touch Accessibility**:
- Minimum 44px touch targets
- Generous spacing between interactive elements
- Swipe gestures for secondary actions

**Performance**:
- Minimal animations to preserve battery
- Progressive loading for map data
- Efficient offline storage indicators

**Emergency Context**:
- High contrast mode support
- Large text options
- Voice-over compatibility
- Quick action shortcuts from lock screen

This design prioritizes immediate usability and clear communication over aesthetic flourishes, ensuring the app functions effectively during high-stress emergency situations while remaining accessible to all user demographics.