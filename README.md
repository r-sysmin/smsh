# SMSH

**take layout/information structure and visual design inspiration from the screenshot
BuildRight Cost Estimator - Product Specification

1. Product Overview

BuildRight Cost Estimator is an interactive web application designed for solo contractors and small construction businesses to provide instant, professional cost estimates to potential clients. The tool guides users through a simple, multi-step process to calculate ballpark project costs based on project type, size, materials, and location. Built with React, Vite, Framer Motion, Tailwind CSS, and Shadcn UI components, this tool transforms the traditional spreadsheet-based estimation process into a modern, engaging experience that captures leads while delivering immediate value. The interface prioritizes clarity, professionalism, and trust-building to help solopreneurs compete with larger firms.

2. Key Features & Requirements

Landing Hero Section

Requirements:

Communicate clear value proposition immediately upon page load

Display trust indicators showing tool credibility and usage

Provide prominent call-to-action to start the estimation process

Show preview/teaser of the calculator interface

Mock Data:

Headline: "Get Your Construction Project Cost Estimate in 3 Minutes"

Subheading: "Professional, accurate estimates that help you plan your project with confidence"

Trust Indicators:

"12,847 estimates generated this month"

"±15% accuracy rating"

"Trusted by 2,400+ contractors nationwide"

Supporting Text: "From kitchen remodels to new builds, get instant ballpark estimates based on real project data. No spreadsheets, no guesswork."

Visual Requirements:

Hero section with bg-gradient-to-br from-slate-50 to-blue-50 py-20 px-6

Headline in text-5xl font-bold text-slate-900 leading-tight mb-6

Trust indicators in horizontal row with icons, using flex gap-8 items-center justify-center

Primary CTA button with bg-amber-500 hover:bg-amber-600 text-white px-8 py-4 rounded-lg text-lg font-semibold shadow-lg transition-all

Background subtle pattern or grid overlay at opacity-5

Project Type Selection

Requirements:

Display 6-8 common project types as selectable cards

Each card shows icon, project name, and brief description

Single selection with clear visual feedback

Progress indicator showing Step 1 of 5

Navigation buttons (Next disabled until selection made)

Mock Data:

Project Types:

Kitchen Remodel: "Transform your kitchen with new cabinets, countertops, and appliances"

Bathroom Remodel: "Upgrade fixtures, tile, and vanities for a modern bathroom"

Home Addition: "Add square footage with a room addition or second story"

Basement Finishing: "Convert unfinished basement into livable space"

Deck or Patio: "Outdoor living space with quality materials and craftsmanship"

New Construction: "Ground-up residential construction project"

Roof Replacement: "Full roof tear-off and replacement with new materials"

Garage Construction: "Detached or attached garage with options for finishes"

Visual Requirements:

Cards in responsive grid: grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6

Individual card: bg-white p-6 rounded-xl border-2 border-slate-200 hover:border-amber-500 cursor-pointer transition-all

Selected state: border-amber-500 bg-amber-50 shadow-lg

Card icon at top: w-12 h-12 mb-4 with construction-related icon colors

Project name: text-xl font-semibold text-slate-900 mb-2

Description: text-sm text-slate-600 leading-relaxed

Framer Motion: Cards fade in with stagger effect, selected card scales to scale-105

Project Details Input

Requirements:

Collect square footage with input validation (100-10,000 sq ft)

Select project complexity level (Simple, Standard, Complex)

Additional fields based on project type (e.g., number of bathrooms for bathroom remodel)

Real-time validation and helpful error messages

Visual indicators showing how inputs affect cost

Mock Data:

Square Footage Range: 100 - 10,000 sq ft

Complexity Levels:

Simple: "Basic finishes, minimal structural changes" (0.85x multiplier)

Standard: "Mid-range finishes, moderate complexity" (1.0x multiplier)

Complex: "Custom features, significant structural work" (1.35x multiplier)

Additional Fields (Kitchen Remodel):

Number of cabinets: 10-30 linear feet

Countertop type selection

Appliance upgrades: Yes/No

Visual Requirements:

Main container: max-w-2xl mx-auto bg-white rounded-xl shadow-xl p-8

Form section with space-y-8

Input fields: w-full border-2 border-slate-200 rounded-lg px-4 py-3 focus:border-amber-500 focus:ring-2 focus:ring-amber-200 transition-all

Complexity cards in row: flex gap-4 with similar styling to project cards but smaller

Validation messages: text-sm text-red-500 mt-1 for errors

Helper text: text-sm text-slate-500 mt-1

Framer Motion: Slide in from right when step loads

Material Tier Selection

Requirements:

Present three material quality tiers with clear differentiation

Show example materials/brands for each tier

Display cost multiplier for each tier

Visual comparison layout to aid decision-making

Highlight most popular option

Mock Data:

Budget Tier (0.80x multiplier):

"Value-focused materials that meet code"

Examples: Stock cabinets, laminate counters, standard fixtures

"Best for: Rentals, flips, or tight budgets"

Standard Tier (1.0x multiplier) - Most Popular:

"Quality materials with good durability"

Examples: Semi-custom cabinets, quartz counters, mid-range fixtures

"Best for: Owner-occupied homes, balanced quality"

Premium Tier (1.30x multiplier):

"High-end finishes and top-tier materials"

Examples: Custom cabinets, granite/marble, designer fixtures

"Best for: Luxury homes, maximum value"

Visual Requirements:

Three-column layout: grid grid-cols-1 md:grid-cols-3 gap-6

Each tier card: bg-white rounded-xl p-6 border-2 border-slate-200 hover:border-amber-500 transition-all cursor-pointer

Standard tier with badge: absolute -top-3 left-1/2 transform -translate-x-1/2 bg-amber-500 text-white px-4 py-1 rounded-full text-sm font-semibold

Tier heading: text-2xl font-bold mb-2 with tier-specific colors (slate-700, amber-600, blue-600)

Multiplier display: text-lg font-semibold text-slate-600 mb-4

Example list: space-y-2 text-sm text-slate-600

Best for section: mt-4 pt-4 border-t border-slate-200 text-sm italic text-slate-500

Selected state: border-amber-500 bg-amber-50 shadow-xl scale-105

Location & Regional Adjustment

Requirements:

Collect location via zip code or city/state selection

Display identified region and cost adjustment factor

Show comparison to national average

Provide context about why location affects cost

Mock Data:

Regional Cost Adjustments:

Northeast (NY, NJ, CT, MA): 1.25x - "High labor costs, strict building codes"

West Coast (CA, WA, OR): 1.20x - "High material and labor costs"

Southeast (FL, GA, NC, SC): 0.95x - "Moderate costs, competitive market"

Midwest (IL, OH, MI, IN): 0.90x - "Lower costs, strong contractor availability"

Southwest (TX, AZ, NM): 0.92x - "Competitive pricing, growing markets"

Mountain (CO, UT, ID): 1.05x - "Material transport costs, specialized labor"

Example Input: Zip code "78701" → Identified as Austin, TX → Southwest region

Visual Requirements:

Location input section: bg-slate-50 rounded-xl p-8

Zip code input: Large, centered input with text-2xl text-center styling

Region identification card appears below: mt-6 bg-white rounded-lg p-6 border-2 border-amber-500

Region name: text-xl font-bold text-slate-900

Adjustment factor: text-3xl font-bold text-amber-600

Comparison badge: inline-flex items-center px-3 py-1 rounded-full bg-blue-100 text-blue-800 text-sm font-medium

Context explanation: text-sm text-slate-600 mt-3

Framer Motion: Region card fades in and slides up when identified

Cost Calculation Results

Requirements:

Display estimated total cost with animated counting effect

Break down cost into major categories

Show confidence range (±15%)

Display estimated project timeline

Compare to national average for similar projects

Provide context and disclaimers about estimate accuracy

Mock Data:

Total Estimate: $47,500 (range: $40,375 - $54,625)

Cost Breakdown:

Materials: $19,000 (40%)

Labor: $21,375 (45%)

Permits & Fees: $2,850 (6%)

Contingency: $4,275 (9%)

Timeline: 6-8 weeks

National Average Comparison: "8% below national average for similar kitchen remodels"

Confidence Level: "Based on 847 similar projects in your region"

Visual Requirements:

Results container: bg-gradient-to-br from-slate-900 to-slate-800 text-white rounded-2xl p-10 shadow-2xl

Total cost display: text-6xl font-bold mb-2 with counting animation

Range display: text-xl text-slate-300

Breakdown section: mt-8 bg-white/10 rounded-xl p-6 backdrop-blur-sm

Category rows: flex justify-between items-center py-3 border-b border-white/20

Category label: text-lg text-slate-200

Category amount: text-xl font-semibold

Progress bars: mt-2 h-2 bg-white/20 rounded-full overflow-hidden with filled portion using bg-amber-500

Timeline badge: inline-flex items-center px-4 py-2 bg-blue-500 rounded-full text-white font-semibold

Comparison section: mt-6 p-4 bg-green-500/20 rounded-lg border border-green-500/30

Framer Motion: Numbers count up from 0, breakdown items fade in with stagger

Lead Capture Form

Requirements:

Integrate seamlessly with results display

Collect essential contact information (name, email, phone)

Ask about project timeline to qualify lead

Include privacy statement and consent

Show clear value proposition for submitting

Display success state after submission

Mock Data:

Form Fields:

Full Name: required

Email Address: required, with validation

Phone Number: required, formatted as (XXX) XXX-XXXX

Project Timeline: dropdown with options

Timeline Options:

"Ready to start immediately"

"Within 1-3 months"

"3-6 months"

"6-12 months"

"Just planning ahead"

CTA Text: "Get Your Detailed Quote"

Privacy Statement: "We respect your privacy. Your information will only be used to provide you with a detailed quote and project consultation. No spam, ever."

Success Message: "Thanks! Your detailed quote has been prepared. Check your email in the next 5 minutes for your comprehensive project breakdown and next steps."

Visual Requirements:

Form section: mt-8 bg-white rounded-2xl p-8 shadow-xl

Heading: text-3xl font-bold text-slate-900 mb-2

Subheading: text-slate-600 mb-6

Input fields: w-full px-4 py-3 border-2 border-slate-200 rounded-lg focus:border-amber-500 focus:ring-2 focus:ring-amber-200

Select dropdown: Same styling as inputs with dropdown icon

Labels: block text-sm font-semibold text-slate-700 mb-2

Submit button: w-full bg-amber-500 hover:bg-amber-600 text-white font-bold py-4 rounded-lg text-lg shadow-lg transition-all

Privacy text: text-xs text-slate-500 mt-4 leading-relaxed

Success state: Replace form with bg-green-50 border-2 border-green-500 rounded-xl p-8 containing success icon and message

Framer Motion: Form slides in from bottom, success state scales in with bounce

Progress Indicator

Requirements:

Show current step and total steps

Display step names for context

Allow clicking previous steps to go back

Highlight current step clearly

Show completion status of previous steps

Mock Data:

Steps:

Project Type

Project Details

Materials

Location

Results

Visual Requirements:

Progress bar container: fixed top-0 left-0 right-0 bg-white shadow-md z-50 py-4 px-6

Steps container: flex items-center justify-center gap-4

Step indicator: flex items-center

Step circle: w-10 h-10 rounded-full flex items-center justify-center font-semibold

Completed: bg-green-500 text-white

Current: bg-amber-500 text-white

Upcoming: bg-slate-200 text-slate-600

Step label: text-sm font-medium text-slate-600 ml-2 (hidden on mobile)

Connector line: w-12 h-1 bg-slate-200 (green when previous step completed)

Overall progress bar: absolute bottom-0 left-0 h-1 bg-amber-500 transition-all duration-300 with dynamic width

How It Works Section

Requirements:

Explain the estimation process

Build trust in the methodology

Address common questions preemptively

Use visual steps or icons

Mock Data:

Process Steps:

Select Your Project: "Choose from common construction projects or describe your custom needs"

Add Details: "Input square footage, complexity, and material preferences"

Get Instant Estimate: "Receive a detailed cost breakdown based on real project data"

Connect with Pro: "Optional: Get matched with vetted contractors in your area"

Accuracy Statement: "Our estimates are built from 15,000+ completed projects across all 50 states, updated monthly with current material and labor costs."

Visual Requirements:

Section: bg-slate-50 py-16 px-6

Heading: text-4xl font-bold text-center text-slate-900 mb-12

Steps grid: grid grid-cols-1 md:grid-cols-4 gap-8 max-w-6xl mx-auto

Step card: bg-white rounded-xl p-6 shadow-md text-center

Step number: w-12 h-12 bg-amber-500 text-white rounded-full flex items-center justify-center text-xl font-bold mx-auto mb-4

Step title: text-xl font-semibold text-slate-900 mb-2

Step description: text-slate-600 text-sm

Accuracy badge: mt-8 text-center p-4 bg-blue-50 border-2 border-blue-200 rounded-lg max-w-3xl mx-auto

FAQ Section

Requirements:

Address common questions about accuracy, usage, and next steps

Collapsible/expandable format for easy scanning

Cover objections and build credibility

Mock Data:

FAQs:

Q: "How accurate are these estimates?" A: "Our estimates typically fall within ±15% of final project costs. Accuracy depends on project complexity and how detailed your inputs are. These are ballpark figures to help with planning - a detailed quote from a contractor will provide exact pricing."

Q: "Are there any hidden fees?" A: "No. This tool is completely free to use. We make money by connecting contractors with qualified leads, but using the calculator has no cost to you."

Q: "Do I have to provide my contact information?" A: "You can see the basic estimate without providing any information. We only ask for your details if you want a detailed quote or to connect with contractors."

Q: "What if my project is unique?" A: "Our estimator works best for common project types. For highly custom projects, we recommend connecting with a contractor directly for a detailed quote."

Q: "Can contractors see my project details?" A: "Only if you choose to share your information. Your estimate remains private unless you opt to request a detailed quote."

Q: "How current is your pricing data?" A: "We update our cost database monthly based on real project data, supplier pricing, and regional labor rates."

Visual Requirements:

Section: py-16 px-6 bg-white

Heading: text-4xl font-bold text-center text-slate-900 mb-12

FAQ container: max-w-3xl mx-auto space-y-4

Question row: border-2 border-slate-200 rounded-lg overflow-hidden

Question button: w-full text-left px-6 py-4 font-semibold text-slate-900 text-lg flex items-center justify-between hover:bg-slate-50

Answer panel: px-6 py-4 bg-slate-50 text-slate-700 leading-relaxed (hidden when collapsed)

Chevron icon: Rotates 180deg when expanded

Framer Motion: Smooth height animation when expanding/collapsing

Testimonials Section

Requirements:

Show social proof from contractors using the tool

Display results/metrics from using the estimator

Include photos/names for authenticity

Rotate or display multiple testimonials

Mock Data:

Testimonials:

"This tool has completely changed how I generate leads. I've gone from emailing spreadsheets to sending professional estimates in minutes. My close rate is up 40%." - Marcus Rivera, Rivera Renovation (Houston, TX)

"I embedded this on my website and now capture 15-20 qualified leads per month. The clients appreciate the transparency, and I save hours per week." - Jennifer Walsh, Walsh Home Builders (Denver, CO)

"As a solo contractor, looking professional matters. This tool makes me look like a much bigger operation, and clients love the instant feedback." - David Park, Park Construction Services (Charlotte, NC)

Visual Requirements:

Section: bg-slate-900 text-white py-16 px-6

Heading: text-4xl font-bold text-center mb-12

Testimonials grid: grid grid-cols-1 md:grid-cols-3 gap-8 max-w-6xl mx-auto

Testimonial card: bg-white/10 backdrop-blur-sm rounded-xl p-6 border border-white/20

Quote text: text-lg text-slate-200 leading-relaxed mb-6

Author info: flex items-center gap-3

Author photo: w-12 h-12 rounded-full bg-amber-500 (or actual photo)

Author name: font-semibold text-white

Author title: text-sm text-slate-400

Mobile Responsiveness

Requirements:

Single column layout on mobile devices

Touch-friendly button sizes (minimum 44x44px)

Simplified navigation for small screens

Optimized form inputs for mobile keyboards

Reduced animation complexity on mobile for performance

Responsive Breakpoints:

Mobile: < 768px

Tablet: 768px - 1023px

Desktop: ≥ 1024px

Mobile-Specific Adjustments:

Progress indicator: Show only current step number and total

Project type cards: Full width, stacked vertically

Material tiers: Stack vertically instead of side-by-side

Form inputs: Full width with proper mobile keyboard types

Cost breakdown: Simplified view with expandable details

Font sizes: Reduce by 0.25rem on mobile for better fit

3. Design System

Color Palette

Primary Colors:

Construction Orange: #F59E0B (bg-amber-500, text-amber-500) - CTAs and highlights

Dark Orange: #D97706 (bg-amber-600, text-amber-600) - Hover states

Light Orange: #FCD34D (bg-amber-300, text-amber-300) - Accents

Brand Colors:

Professional Blue: #3B82F6 (bg-blue-500, text-blue-500) - Trust elements

Dark Blue: #1E40AF (bg-blue-800, text-blue-800) - Headers

Light Blue: #DBEAFE (bg-blue-50, text-blue-50) - Backgrounds

Neutral Colors:

Pure White: #FFFFFF (bg-white, text-white)

Light Gray: #F8FAFC (bg-slate-50, text-slate-50)

Medium Gray: #E2E8F0 (bg-slate-200, text-slate-200)

Dark Gray: #475569 (bg-slate-600, text-slate-600)

Charcoal: #1E293B (bg-slate-800, text-slate-800)

Near Black: #0F172A (bg-slate-900, text-slate-900)

Status Colors:

Success Green: #10B981 (bg-green-500, text-green-500)

Warning Amber: #F59E0B (bg-amber-500, text-amber-500)

Error Red: #EF4444 (bg-red-500, text-red-500)

Info Teal: #14B8A6 (bg-teal-500, text-teal-500)

Typography

Font Families:

Primary: Inter (font-sans) - All body text, headings, UI elements

Monospace: Mono (font-mono) - Cost figures, technical data

Font Sizes:

Extra Small: 0.75rem (text-xs) - Helper text, disclaimers

Small: 0.875rem (text-sm) - Secondary text, labels

Base: 1rem (text-base) - Body text, inputs

Large: 1.125rem (text-lg) - Emphasized body text

Extra Large: 1.25rem (text-xl) - Subheadings

2XL: 1.5rem (text-2xl) - Section headings

3XL: 1.875rem (text-3xl) - Major headings

4XL: 2.25rem (text-4xl) - Hero text

5XL: 3rem (text-5xl) - Primary hero headline

6XL: 3.75rem (text-6xl) - Cost display

Font Weights:

Regular: 400 (font-normal) - Body text

Medium: 500 (font-medium) - Subtle emphasis

Semibold: 600 (font-semibold) - Buttons, labels

Bold: 700 (font-bold) - Headings, important text

Extrabold: 800 (font-extrabold) - Hero text, major CTAs

Line Heights:

Tight: 1.25 (leading-tight) - Large headings

Normal: 1.5 (leading-normal) - Body text

Relaxed: 1.75 (leading-relaxed) - Long-form content

Letter Spacing:

Tight: -0.025em (tracking-tight) - Large headings

Normal: 0 (tracking-normal) - Body text

Wide: 0.025em (tracking-wide) - Uppercase labels

Core Components

Buttons:

Primary Button: bg-amber-500 hover:bg-amber-600 text-white font-semibold px-6 py-3 rounded-lg shadow-md hover:shadow-lg transition-all duration-200 active:scale-95

Secondary Button: bg-white text-amber-600 border-2 border-amber-500 font-semibold px-6 py-3 rounded-lg hover:bg-amber-50 transition-all

Outline Button: bg-transparent border-2 border-slate-300 text-slate-700 font-medium px-6 py-3 rounded-lg hover:border-slate-400 hover:bg-slate-50 transition-all

Text Button: text-amber-600 font-semibold hover:text-amber-700 underline-offset-4 hover:underline transition-all

Icon Button: w-10 h-10 flex items-center justify-center rounded-lg hover:bg-slate-100 transition-all

Cards:

Standard Card: bg-white rounded-xl shadow-md border border-slate-200 overflow-hidden

Elevated Card: bg-white rounded-xl shadow-xl border border-slate-200 overflow-hidden

Interactive Card: bg-white rounded-xl shadow-md border-2 border-slate-200 hover:border-amber-500 hover:shadow-lg transition-all duration-200 cursor-pointer

Selected Card: bg-amber-50 rounded-xl shadow-lg border-2 border-amber-500

Glass Card: bg-white/10 backdrop-blur-md rounded-xl border border-white/20

Form Elements:

Text Input: w-full px-4 py-3 border-2 border-slate-200 rounded-lg text-slate-900 placeholder-slate-400 focus:border-amber-500 focus:ring-2 focus:ring-amber-200 transition-all

Input with Error: border-red-500 focus:border-red-500 focus:ring-red-200

Select Dropdown: w-full px-4 py-3 border-2 border-slate-200 rounded-lg text-slate-900 bg-white focus:border-amber-500 focus:ring-2 focus:ring-amber-200 appearance-none cursor-pointer transition-all

Checkbox: w-5 h-5 text-amber-500 border-2 border-slate-300 rounded focus:ring-2 focus:ring-amber-200

Radio Button: w-5 h-5 text-amber-500 border-2 border-slate-300 focus:ring-2 focus:ring-amber-200

Label: block text-sm font-semibold text-slate-700 mb-2

Helper Text: text-sm text-slate-500 mt-1

Error Message: text-sm text-red-500 mt-1 flex items-center gap-1

Progress Elements:

Progress Bar Container: w-full h-2 bg-slate-200 rounded-full overflow-hidden

Progress Bar Fill: h-full bg-amber-500 transition-all duration-500

Step Indicator: flex items-center justify-between

Step Circle Complete: w-10 h-10 bg-green-500 rounded-full flex items-center justify-center text-white font-bold

Step Circle Active: w-10 h-10 bg-amber-500 rounded-full flex items-center justify-center text-white font-bold shadow-lg

Step Circle Incomplete: w-10 h-10 bg-slate-200 rounded-full flex items-center justify-center text-slate-600 font-bold

Step Connector: flex-1 h-1 mx-2 bg-slate-200 (green when completed)

Badges:

Info Badge: inline-flex items-center px-3 py-1 rounded-full bg-blue-100 text-blue-800 text-sm font-medium

Success Badge: inline-flex items-center px-3 py-1 rounded-full bg-green-100 text-green-800 text-sm font-medium

Warning Badge: inline-flex items-center px-3 py-1 rounded-full bg-amber-100 text-amber-800 text-sm font-medium

Popular Badge: inline-flex items-center px-4 py-1 rounded-full bg-amber-500 text-white text-sm font-semibold shadow-md

Animation Specifications (Framer Motion)

Page Transitions:

Step Entry: initial={{ opacity: 0, x: 100 }} animate={{ opacity: 1, x: 0 }} exit={{ opacity: 0, x: -100 }} transition={{ duration: 0.3, ease: "easeInOut" }}

Fade In: initial={{ opacity: 0 }} animate={{ opacity: 1 }} transition={{ duration: 0.4 }}

Slide Up: initial={{ opacity: 0, y: 20 }} animate={{ opacity: 1, y: 0 }} transition={{ duration: 0.4 }}

Interactive Animations:

Card Hover: whileHover={{ scale: 1.02, y: -4 }} transition={{ duration: 0.2 }}

Button Press: whileTap={{ scale: 0.95 }}

Selection: animate={{ scale: [1, 1.05, 1] }} transition={{ duration: 0.3 }}

Number Animations:

Cost Counting: Animate from 0 to target value over 1.5 seconds with easing

Use custom hook or component to increment number smoothly

Format with currency symbol and comma separators during animation

Success States:

Success Celebration: initial={{ scale: 0.8, opacity: 0 }} animate={{ scale: 1, opacity: 1 }} transition={{ type: "spring", bounce: 0.5, duration: 0.6 }}

Checkmark: Draw animation from center outward

Stagger Animations:

Card Grid: transition={{ staggerChildren: 0.1 }} on parent container

List Items: Each child fades in with 0.1s delay between items

Responsive Layout System

Container Widths:

Mobile (<768px): px-4 max-w-full

Tablet (768px-1023px): px-6 max-w-3xl mx-auto

Desktop (≥1024px): px-8 max-w-7xl mx-auto

Grid Systems:

Two Column: grid grid-cols-1 md:grid-cols-2 gap-6

Three Column: grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6

Four Column: grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-4 gap-6

Spacing Scale:

Extra Small: 4px (space-y-1, gap-1)

Small: 8px (space-y-2, gap-2)

Medium: 16px (space-y-4, gap-4)

Large: 24px (space-y-6, gap-6)

Extra Large: 32px (space-y-8, gap-8)

2XL: 48px (space-y-12, gap-12)

3XL: 64px (space-y-16, gap-16)

Section Padding:

Mobile: py-12 px-4

Tablet: py-16 px-6

Desktop: py-20 px-8

Accessibility Requirements

Focus States:

All interactive elements must have visible focus indicators

Focus ring: focus:outline-none focus:ring-2 focus:ring-amber-500 focus:ring-offset-2

Skip to content link for keyboard navigation

Color Contrast:

All text must meet WCAG AA standards (4.5:1 for normal text, 3:1 for large text)

Use tools to verify contrast ratios during development

Avoid relying solely on color to convey information

Form Accessibility:

All inputs must have associated labels (visible or aria-label)

Error messages must be linked to inputs via aria-describedby

Required fields indicated both visually and semantically

Fieldset and legend for radio/checkbox groups

Keyboard Navigation:

All interactive elements accessible via keyboard

Logical tab order throughout the application

Enter/Space to select cards and buttons

Escape to close modals or cancel actions

Screen Reader Support:

Semantic HTML elements (header, nav, main, section, footer)

ARIA labels for icons and icon-only buttons

ARIA live regions for dynamic content updates (cost calculations)

Alt text for all meaningful images

Loading & Empty States

Loading States:

Skeleton screens for content loading: animate-pulse bg-slate-200 rounded

Spinner for form submissions: animate-spin w-8 h-8 border-4 border-slate-200 border-t-amber-500 rounded-full

Progress indicator for multi-step calculations

Empty States:

No results: Friendly message with illustration

Form validation: Inline error messages with icons

Network errors: Retry button with helpful message

Success States:

Checkmark animation after form submission

Confetti or celebration effect for completed estimate

Clear next steps and confirmation message

This project was built with [Lovable](https://lovable.dev).

## Build with Lovable

Continue developing this project in the [Lovable editor](https://lovable.dev/projects/9d93a6f0-22ea-4553-b812-074f8d225bf1).

- **Ship faster**: describe what you want to build and Lovable handles the code.
- **Stay in sync**: every change made in Lovable is committed straight to this repository.
- **Full ownership**: this code is yours. Push to `main` on GitHub and your changes sync back into Lovable, ready for your next prompt.

## Development

Prefer working locally? You need Node.js and npm — [install with nvm](https://github.com/nvm-sh/nvm#installing-and-updating).

```sh
git clone <this-repository-url>
cd <repository-name>
npm i
npm run dev
```
