# Smart India Hackathon Workshop
# Date:24/11/2026
## Reference Number:26016986
## Name:CHANDRU M

## Problem Title
SIH 26033: Multiple intermediaries reduce farmers earnings and increase consumer prices.

## Problem Creater's Organization
Ministry of Consumer Affairs, Food & Public Distribution

## Theme
Agriculture, FoodTech & Rural Development

## Problem Description
Expected Solution: Create a digital marketplace that:

• Connects farmers/FPOs directly with consumers and bulk buyers.
• Provides logistics support.
• Uses AI for demand forecasting and route optimization.

Benefits:

• Better prices for farmers.
• Lower prices for consumers.
• Reduced supply chain inefficiencies.

## Proposed Solution
Solution Overview: KrishiSetu (B2B & B2C Farm-to-Fork Ecosystem)
A unified, multilingual digital marketplace and logistics orchestration platform that directly connects Farmers and Farmer Producer Organizations (FPOs) with bulk buyers (retail chains, HoReCa, housing societies) and individual consumers.

How It Addresses the Problem
Eliminating Middlemen (Arhatiyas): Replaces multi-tier mandi commission layers with a transparent, direct-bidding and fixed-price storefront, allowing farmers to capture 75%–85% of the retail value (up from the current 30%–40%).

Pooled Logistics ("Milk-Run" Model): Smallholder farmers rarely have enough produce to fill a truck. The platform aggregates harvest listings from neighboring farms into FPO micro-collection hubs, sharing transport costs.

AI-Driven Demand & Price Discovery: Prevents distress selling and post-harvest wastage by predicting regional demand spikes 7–14 days in advance and suggesting dynamic, fair floor prices benchmarked against live e-NAM/Agmarknet data.

Innovation & Uniqueness
Voice-First Vernacular Interface: Built for low-literacy rural adoption using regional speech-to-text (Bhashini API) and IVR/WhatsApp bots so farmers can list produce without navigating complex menus.

Perishability-Aware Route Optimization: Unlike standard delivery algorithms, our routing engine factors in crop shelf-life, ambient temperature, and road conditions to prioritize highly perishable goods (e.g., tomatoes, leafy greens) first.

Smart Escrow & Instant UPI Settlement: Funds from bulk buyers are held in escrow upon dispatch and released directly to the farmer's bank account via UPI immediately upon QR-code verified delivery at the buyer's dock.

## Technical Approach
Technology Stack
Frontend (Farmer & Buyer Apps): Flutter (Cross-platform mobile), React.js (Web dashboard for FPOs & Bulk Buyers).

Voice & Vernacular Layer: Government of India's Bhashini API (ASR & Translation) + WhatsApp Business Cloud API.

Backend & Microservices: Node.js / Express & Python (FastAPI for AI microservices).

Database & Caching: PostgreSQL + PostGIS (for geospatial logistics queries), Redis (real-time inventory locking).

AI / ML Engine:

Demand Forecasting: Temporal Fusion Transformers (TFT) / Prophet trained on historical mandi arrivals, weather, and festival calendars.

Route Optimization: Google OR-Tools (Capacitated Vehicle Routing Problem with Time Windows - CVRPTW).

Payments & Verification: RazorpayX / UPI AutoPay (Escrow), OpenCV-based mobile camera grading (detecting produce size/defects).

## Feasibility and Viability
Feasibility AnalysisTechnical Feasibility: High. Leverages proven open-source routing engines (OR-Tools), existing UPI payment rails, and India's Digital Public Infrastructure (DPI) like Bhashini and ONDC protocols.Operational Feasibility: High. Partnering with existing 10,000+ Govt-registered FPOs solves the "last-mile aggregation" problem without needing to build physical warehouses from scratch.Economic Viability: Self-sustaining via a 2%–3% platform facilitation fee charged only to bulk buyers/retailers (zero commission for farmers) plus logistics margin optimization.Potential Challenges & Mitigation StrategiesChallengeMitigation StrategyLow smartphone/digital literacy among farmersDeploy WhatsApp-based voice bots and assign 1 digitally literate "FPO Sahayak" per village cluster to manage bulk listings.Quality disputes upon deliveryMandatory standardized AI computer-vision grading (uploading a 5-second video/photo of crates before dispatch) + tamper-evident QR crate tags.Cold-chain & rural transport shortagesOnboard local mini-truck/tempo owners (Porter/Tata Ace model) onto a driver app for hyperlocal farm-to-hub shuttles.Intermittent rural internetOffline-first SQLite local storage on the mobile app that auto-syncs listings and bids once network connectivity returns.

## Impact and Benefits
Target Audience Impact
Farmers & FPOs: Guaranteed transparent pricing, zero middleman commissions, and instant liquidity via same-day UPI settlement.

Consumers & Bulk Buyers: Access to farm-fresh, traceable produce at 15%–25% lower prices with reliable scheduled deliveries.

Multi-Dimensional Benefits
Economic: Increases net farmer income by 25%–40% while reducing retail food inflation for urban households.

Social: Empowers rural youth as FPO logistics coordinators/quality graders and reduces distress migration from agricultural belts.

Environmental: AI route optimization cuts empty-truck miles and fuel emissions by ~20%, while faster farm-to-table transit reduces post-harvest food wastage (currently ~15–20% in India's perishables supply chain).

## Research and References
Government & Policy Frameworks:

Ministry of Agriculture & Farmers Welfare: Formation and Promotion of 10,000 Farmer Producer Organizations (FPOs) Scheme Guidelines.

Agmarknet & e-NAM (National Agriculture Market): Historical mandi arrival and modal price datasets for ML price-benchmarking.

ONDC (Open Network for Digital Commerce): Beckn Protocol specifications for interoperable hyperlocal logistics and agriculture cataloguing.

Technical & Academic References:

Google OR-Tools Documentation: Vehicle Routing Problem with Time Windows (VRPTW) for multi-stop agricultural pickup optimization.

Bhashini (National Language Translation Mission): ULCA APIs for Indian vernacular Automatic Speech Recognition (ASR).

ICAR-CIPHET Report: Assessment of Quantitative Harvest and Post-Harvest Losses of Major Crops and Commodities in India (benchmarking wastage reduction metrics).
