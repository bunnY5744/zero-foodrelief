# Zero – India's AI-Powered Food Waste to Food Relief Network

> **Autonomously converting surplus restaurant food into meals for those in need. Zero human effort. Zero waste. Zero hunger.**

---

## 🎯 Project Overview

**Zero** is an AI-driven infrastructure platform that detects surplus food at Swiggy restaurants before closing time, intelligently matches it to the nearest NGOs and orphanages using Claude AI, and dispatches automated pickup alerts—all without human intervention.

We're solving one of India's most critical contradictions: **13.7 crore tonnes of food waste annually while 195 million people face hunger.**

**Target Impact (Year 1):** 10 lakh meals delivered through autonomous food relief.

---

## 📊 Problem Statement

### India's Food Waste Crisis

- **13.7 crore tonnes** of food wasted annually (Ministry of Environment, Forest & Climate Change)
- **40% of India's food waste** originates from retail and food service sectors
- **195 million people** face hunger or food insecurity
- **Current gap:** Surplus food and relief organizations operate in silos with no real-time coordination
- **Manual matching:** NGOs spend hours locating food sources; restaurants lack distribution channels
- **Time criticality:** Cooked food viability window: **4–6 hours** maximum

### The Human Cost
- **41 million children** suffer from stunting due to malnutrition
- **51% of women** between 15–49 are anaemic
- **Economic loss:** ₹92,000 crore annually in wasted food resources

---

## 🔧 How It Works: The Autonomous Matching Engine

```
┌─────────────────────────────────────────────────────────────────┐
│                     ZERO MATCHING WORKFLOW                       │
└─────────────────────────────────────────────────────────────────┘

┌──────────────────────────────────────────────────────────────────┐
│ STEP 1: SURPLUS DETECTION (T+0 min)                              │
│ Swiggy API → Real-time inventory monitoring                      │
│ Triggers: >20% unsold cooked items at T-120 min before close    │
└──────────────────────────────────────────────────────────────────┘
                               ↓
┌──────────────────────────────────────────────────────────────────┐
│ STEP 2: FOOD PROFILE GENERATION (T+0–1 min)                     │
│ Claude AI analyzes:                                              │
│ • Item type, quantity, nutritional value, allergens             │
│ • Expiry window, temperature requirements                       │
│ • Dietary compatibility (vegan/non-veg/multi-cuisine)           │
└──────────────────────────────────────────────────────────────────┘
                               ↓
┌──────────────────────────────────────────────────────────────────┐
│ STEP 3: NGO/ORPHANAGE MATCHING (T+1–3 min)                       │
│ Claude AI + Google Maps API:                                    │
│ • Query PostgreSQL: NGOs within 5 km radius                     │
│ • Match: Operational hours, dietary requirements, capacity      │
│ • Rank by: Distance, need-urgency, vehicle availability         │
│ • Output: Top 3 matches with ETA & benefit score                │
└──────────────────────────────────────────────────────────────────┘
                               ↓
┌──────────────────────────────────────────────────────────────────┐
│ STEP 4: AUTONOMOUS ALERT DISPATCH (T+3–4 min)                    │
│ • SMS + WhatsApp to NGO driver/coordinator                      │
│ • In-app notification (React.js real-time)                      │
│ • Restaurant: Pickup location, time window, qty                 │
│ • Logistics: Route optimization, traffic-aware ETA              │
└──────────────────────────────────────────────────────────────────┘
                               ↓
┌──────────────────────────────────────────────────────────────────┐
│ STEP 5: FULFILLMENT TRACKING (T+4–120 min)                       │
│ • GPS tracking of pickup journey                                │
│ • Real-time beneficiary feedback                                │
│ • Impact logging: Meals served, lives touched                   │
└──────────────────────────────────────────────────────────────────┘

Total Autonomous Decision-to-Alert: 4 MINUTES
Human Touchpoint Required: ZERO
```

---

## 🏗️ Technical Architecture

| **Layer** | **Technology** | **Purpose** |
|-----------|---|---|
| **Frontend** | React.js | Real-time dashboard for NGOs, restaurants, admins |
| **Backend API** | Node.js (Express) | REST APIs, webhook handlers, orchestration logic |
| **AI Engine** | Claude AI (Anthropic API) | Food matching, route optimization, contextual analysis |
| **External Integration** | Swiggy Food MCP Server | Real-time inventory & restaurant data ingestion |
| **Geolocation** | Google Maps API | Distance calculation, ETA, route optimization |
| **Database** | PostgreSQL | NGO profiles, restaurant outlets, meal transactions, impact metrics |
| **Notifications** | Twilio/WhatsApp Business API | SMS & WhatsApp alerts to pickup coordinators |
| **Analytics** | Custom dashboards | Real-time impact tracking, sustainability KPIs |

---

## 💻 Tech Stack Summary

```
Frontend:       React.js, Redux, Tailwind CSS, Google Maps SDK
Backend:        Node.js, Express.js, PostgreSQL (node-postgres)
AI/ML:          Claude 3 (Anthropic), prompt engineering for matching logic
External APIs:  Swiggy Food MCP, Google Maps, Twilio
DevOps:         Docker, AWS EC2, GitHub Actions CI/CD
Database:       PostgreSQL 14+, PostGIS for geo-queries
```

---

## 🎯 Impact Goals & Sustainability Model

### Year 1 Targets
- **10 lakh meals** delivered through autonomous matching
- **500+ restaurant partners** across 5 Indian metros
- **200+ NGO/orphanage integrations**
- **1,000+ tonnes** of food redirected from waste
- **Carbon offset:** 2,500 tonnes CO₂ equivalent
- **Social reach:** 300,000+ individuals served

### Sustainability & Revenue Model

| **Revenue Stream** | **Mechanism** | **Stakeholder** |
|---|---|---|
| **Restaurant Freemium** | Free surplus matching; premium for demand forecasting | Swiggy partners & independent restaurants |
| **Impact Credits** | ESG compliance certification & carbon credits | Corporates, QSRs (CSR mandates) |
| **NGO Grants** | Per-meal subsidy from govt programs & foundations | NGOs, social enterprises |
| **B2B Analytics** | Anonymized food waste insights, supply chain optimization | FMCG companies, logistics networks |
| **Premium Dashboards** | Advanced reporting, API access, white-label solutions | Enterprise partnerships |

---

## 👥 Who Uses Zero?

### **Restaurants (Swiggy Network)**
- **Problem:** Food waste, disposal costs, brand reputation
- **Solution:** Automatic surplus matching, CSR credit, customer goodwill
- **Benefit:** ₹0 operational cost, positive PR

### **NGOs & Orphanages**
- **Problem:** Food sourcing, last-minute supply gaps, logistics coordination
- **Solution:** Real-time food availability, autonomous dispatch, zero coordination overhead
- **Benefit:** Predictable meals, reduced volunteer dependency, measurable impact

### **Delivery Drivers & Logistics Partners**
- **Problem:** Dead runs, underutilized capacity between food orders
- **Solution:** Surplus-to-charity pickups, meal delivery efficiency
- **Benefit:** Additional income, social impact participation

### **Government & Social Welfare Bodies**
- **Problem:** Food insecurity metrics, wastage monitoring, CSR compliance
- **Solution:** Real-time data, scalable infrastructure, verifiable impact
- **Benefit:** Policy insights, transparent relief metrics

### **Impact Investors & Corporates**
- **Problem:** ESG compliance, sustainability KPIs, authentic social impact
- **Solution:** Verifiable meal-level impact tracking, carbon offset, scalable model
- **Benefit:** Measurable ROI, brand alignment, regulatory compliance

---

## 📈 Why Zero?

✅ **Autonomous:** AI-driven matching eliminates human coordination bottlenecks  
✅ **Scalable:** API-first architecture; easy to add restaurants, NGOs, cities  
✅ **Profitable:** Multiple revenue streams; unit economics favor growth  
✅ **Measurable:** Every meal tracked, verified, and reported in real-time  
✅ **Urgent:** Closing India's hunger-waste paradox through technology  

---

## 🚀 Vision: 2030 & Beyond

- **Year 1:** 10 lakh meals, 5 metros, 500 restaurants
- **Year 2:** 50 lakh meals, 10 metros, pan-India NGO network
- **Year 3:** 1 crore meals, integrated with public food safety databases
- **2030:** Autonomously feeding 5 crore+ Indians; zero food waste in integrated supply chains

---

## 📧 Contact & Community

- **GitHub:** [@bunnY5744](https://github.com/bunnY5744)
- **Impact:** Every surplus meal detected is a life touched. Join the mission.

---

**Zero – Because food waste is a policy failure we can automate away.**
