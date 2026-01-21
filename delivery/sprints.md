# Delivery Sprints

## Sprint Delivery Approach

Sprints in Fundamentalis are defined and delivered based on clearly articulated goals and outcomes rather than fixed time-based deadlines. Each sprint is considered complete once its stated objectives and acceptance criteria are fully met, ensuring that functionality is delivered with the required level of quality and coherence before progressing to the next stage of development.

## Sprint 1 — Core System Foundation

### Goal
Establish the foundational capabilities of the platform by enabling user authentication and the core restaurant, menu, and ordering workflows, including basic order management from the restaurant perspective.

### Scope

- User account registration and authentication via the web interface
- Creation and management of a restaurant associated with a user account
- Creation and management of food menus for a restaurant
- Creation and management of menu products
- Creation of food orders composed of products from a restaurant’s menu
- Restaurant-side visibility of all food orders associated with the restaurant

### Outcome
At the end of this sprint, the system supports a complete end-to-end flow in which an authenticated user can set up a restaurant, define its menu and products, place food orders, and view all incoming orders from the restaurant side to support basic operational workflows..


## Sprint 2 — Core System Polishing and On-Premise Ordering

### Goal
Enhance the core system by introducing an on-premise ordering experience driven by QR code–based sessions, along with flexible dish customization capabilities.

### Scope

- QR code scanning to access a restaurant’s menu
- Automatic creation of a session upon QR code scan (e.g., table session)
- Association of the session with a specific table or contextual identifier within the restaurant
- In-session capabilities for end users, including:
  - Browsing the menu
  - Placing food orders
  - Completing payment
  - Requesting waiter assistance
- Dish customization features, including:
  - Adding or removing ingredients
  - Selecting optional modifiers or variants
  - Providing free-text special instructions or additional indications per dish

### Outcome
At the end of this sprint, the platform delivers a complete in-restaurant experience where customers can scan a QR code to start a session, customize dishes according to their preferences, place and pay for orders, and interact with restaurant staff through the system, all within a polished and user-friendly flow.

## Sprint 3 — Community and Discovery

### Goal
Introduce community-driven features that enhance user engagement, trust, and discovery through profiles, reviews, ratings, and restaurant exploration.

### Scope

- User profile customization (e.g., avatar, display information, preferences)
- Rating of individual food items
- Rating of restaurants
- Creation of written reviews associated with foods and restaurants
- Discovery of new restaurants through a map-based interface with filtering capabilities
- Viewing ratings and reviews submitted by other users
- Enhanced customization options for restaurant profiles, including richer descriptive and visual information

### Outcome
By the end of this sprint, the platform evolves beyond core ordering functionality into a community-oriented experience, enabling users to personalize their presence, share feedback, discover new restaurants, and make informed decisions based on collective user reviews and ratings.

## Sprint 4 — Restaurant Management and Analytics

### Goal
Provide restaurant owners and managers with actionable insights into their business performance through operational and financial analytics.

### Scope

- Restaurant management dashboard accessible to authorized owners/managers
- General operational metrics, including:
  - Most ordered dishes
  - Order volume over time
  - Peak ordering periods
  - Average order value
- Financial metrics, including:
  - Total revenue over selected periods
  - Revenue breakdown by dish and category
  - Payment method distribution
- Customer and engagement insights, including:
  - Number of active sessions and orders per table
  - Repeat customer indicators (where applicable)
  - Average preparation and fulfillment times
- Menu performance insights, including:
  - Best- and worst-performing menu items
  - Impact of dish customizations on order frequency

### Outcome
At the end of this sprint, restaurant managers have access to a comprehensive management dashboard that consolidates key business metrics, enabling data-driven decisions around menu optimization, pricing, staffing, and overall operational efficiency.

## Sprint 5 — AI-Powered Personalization and Insights

### Goal
Integrate artificial intelligence capabilities to deliver personalized user experiences, improve ordering safety and relevance, and provide restaurants with contextual customer insights.

### Scope

- Personalized restaurant recommendations based on user behavior, preferences, and historical interactions
- Personalized dish recommendations, including:
  - Highlighting preferred cuisines or dish types when scanning a restaurant QR code
  - Surfacing frequently ordered or highly rated items aligned with the user’s tastes
- Ingredient and dietary awareness features, including:
  - Detection and flagging of potential allergens based on user-defined sensitivities
  - Proactive warnings displayed before order confirmation when a selected dish contains restricted ingredients
- Contextual user insights for restaurants, including:
  - A brief, privacy-aware user profile summary available during active sessions (e.g., preferences, frequent choices, dietary notes), when applicable and permitted

### Outcome
By the end of this sprint, the platform leverages AI to provide intelligent, personalized, and safer interactions for users while equipping restaurants with meaningful, high-level customer insights that enhance service quality without compromising user privacy.