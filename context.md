# Satyam Edutech Landing Page Context

## Project Information
- **Business**: Satyam Edutech
- **Domain**: Commerce Coaching Institute in Durgapur
- **Target Audience**: Class 11 & 12 students (CBSE, ICSE, West Bengal Board)
- **Key Selling Points**:
  - 30+ years of excellence (Seth Sir)
  - 1-on-1 personalized mentorship
  - Strictly 6 seats per batch
  - Free demo class with zero obligation
- **Website Purpose**: Single HTML ad landing page for lead generation (booking free demo classes).

## Technical Details
- **Architecture**: Single HTML file containing HTML, CSS, and vanilla JavaScript (`index.html`).
- **Styling**: Vanilla CSS with custom CSS variables, responsive design, fluid typography (`clamp()`), and smooth transitions/animations. Theme inspired by 21st.dev and shadcn.
- **Frontend Assets**: Images stored in `images/` directory.
- **Form Integration**: Form submissions are sent to a Google Sheets Apps Script Web App Endpoint. The sheet captures Timestamp, Student Name, Phone Number, and Class.
- **Analytics/Tracking**: Integrated with Meta Pixel and Vercel Web Analytics.

## Current State & Recent Changes
- Updated UI design to a modern, minimalist aesthetic inspired by 21st.dev and shadcn. 
- Integrated Vercel Analytics into `public/` directory HTML files.
- Completed Lead validation and cleanup tasks from a generated list of leads.
- Updated testimonial photos and names.
- Setup phone number form formatting to ensure pasted inputs with country codes (e.g., `+91`) accurately extract and save only the local 10-digit phone number in Google Sheets.
- Added duplicate form submission prevention based on phone number, checking via Google Sheets Apps Script and showing an error in the UI.

## Tracking & Architecture
- **Meta Pixel**: The main page tracks `PageView`. The form redirects to `thankyou.html` on successful submission, where the explicit `Lead` event fires. This ensures accurate conversion tracking without overcounting button clicks.

## Deployment
- Can be deployed directly via Vercel for fast hosting. Any changes to `index.html` would be reflected in the final static export.
