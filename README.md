
# 🗺️ Transit AI - Real-Time Telemetry & Congestion Grading Platform

[![Live Demo](https://img.shields.io/badge/🚀_Live_Demo-Visit_Website-00C853?style=for-the-badge)](https://transit-ai-1mot.onrender.com/)
[![GitHub](https://img.shields.io/badge/GitHub-Repository-181717?style=for-the-badge&logo=github)](https://github.com/rameshshanmugam2005-hub/TRANSIT_AI)

Transit AI is an advanced, enterprise-grade public transit visualization, real-time routing telemetry, and smart ticket validation platform designed to resolve urban commuting inefficiencies. Optimized for dense metropolitan hubs like Chennai, India, the application transforms volatile GPS telemetry and regional road link speeds into highly structured, actionable transit intelligence.


PROJECT LINK:https://transit-ai-1mot.onrender.com/


---

## 📌 1. The Problem Statement

Metropolitan public transit systems face compounding systemic issues that result in wasted commuter hours, increased carbon footprints, and system-wide gridlocks:

1. **Unpredictable Route Delays & Traffic Volatility**: Commuters lack visibility into actual road speeds. A bus might be 1.5 km away, but gridlocked in a high-congestion segment, rendering basic ETA models highly inaccurate.
2. **Hidden Passenger Density (Crowded Cabinets)**: Commuters board buses blindly without knowing if they will stand for hours. High cabin density prevents elder and disabled commuters from traveling comfortably.
3. **Wet-Cash Boarding Bottlenecks**: Manual paper ticketing and physical cash transactions at gates and bus entryways cause massive dwell-time delays, slowing down transit cycles.
4. **Weak Connectivity Failures (Network Edge Commuters)**: Standard high-density satellite mapping frameworks fail to load on weak 2G or 3G cellular signals at regional urban edges.

---

## ⚡ 2. The Solution (Transit AI Core Innovations)

Transit AI implements a comprehensive suite of hardware-simulated, software-driven solutions to solve urban transport issues:

*   **Live Vector Telemetry Radar Map**: A lightweight HTML5 Canvas rendering engine that draws station nodes, route highway segments, and moving buses. Uses high-contrast glowing elements for desktop-first aesthetic precision.
*   **Layered Road Congestion Heatmaps**: Real-time road speeds are analyzed and classified into interactive segment speed grades:
    *   🟢 **Fluid Links**: High speeds (Avg 52 km/h, 92% flow index).
    *   🟡 **Slow Crawl Links**: Moderate congestion (Avg 28 km/h, 58% flow index).
    *   🔴 **Gridlocked Links**: Deadlock congestion (Avg 9 km/h, 18% flow index).
*   **Seat Occupancy Load Audits**: Live seating telemetry (Fluid, Crowded, or Full density) is displayed on hover to help commuters optimize comfort.
*   **Instant QR Ticket Clearance Gate**: A simulated conductor scanner using device camera frames or high-speed manual codes to clear passenger logs immediately.
*   **Eco-Sensing Data Saver Protocol**: An edge-friendly performance module that dynamically reduces network polling intervals and compresses payload size to optimize cellular bandwidth on weak signals.
*   **Multi-Engine AI Assistant Routing Proxy**: An integrated chatbot utilizing Google Gemini (Flash & Pro), Anthropic Claude, OpenAI GPT-4, and DeepSeek R1 to provide natural language travel support based on live bus schedules and congestion data.

---

## 📊 3. Architecture & Telemetry Flow Diagram

Transit AI processes active GPS coordinates, passenger seating sensors, and road traffic feeds into a synchronized web environment:

```
                  ┌──────────────────────────────┐
                  │  Active Bus Fleet Telemetry  │
                  │   (GPS + Occupancy Sensors)  │
                  └──────────────┬───────────────┘
                                 │
                                 ▼ (JSON Updates)
                  ┌──────────────────────────────┐
                  │    Express Node.js Server    │
                  │   (Live Scheduler Engine)    │
                  └──────────────┬───────────────┘
                                 │
         ┌───────────────────────┴───────────────────────┐
         ▼                                               ▼
┌─────────────────────────────────┐             ┌─────────────────────────────────┐
│     Eco-Sensing Compression     │             │    Multi-Engine AI Router       │
│  (Bandwidth-Throttled Polling)  │             │   (Gemini, DeepSeek, Claude)    │
└────────────────┬────────────────┘             └────────────────┬────────────────┘
                 │                                               │
                 ▼                                               ▼
┌─────────────────────────────────┐             ┌─────────────────────────────────┐
│       HTML5 Canvas Radar        │             │      Floating AI Assistant      │
│  (Dynamic Heatmaps & Toggles)   │             │   (Natural-Language Answers)    │
└─────────────────────────────────┘             └─────────────────────────────────┘
```

---

## 🛠️ 4. Tech Stack & Engineering Specifications

*   **Frontend**: 
    *   HTML5 Canvas (Vector geometry, custom particle glows, pulsing telemetry packets).
    *   Vanilla CSS3 Variable System (Dynamic dark/light themes, responsive grids).
    *   Tailwind CSS (Aesthetic layouts, modern typography, mobile-first design system).
*   **Backend**: 
    *   Node.js (Express) (Serves static routes, hosts the state-preserving bus simulator, and manages chat proxies).
*   **AI Integration**: 
    *   Google Gemini API SDK (Securely proxied to hide keys, using intelligent prompt schemas containing real-time bus locations).

---

## 🚀 5. How to Run & Deploy

### Prerequisites
Make sure you have [Node.js](https://nodejs.org/) installed on your machine.

### Installation
1. Install base dependencies:
   ```bash
   npm install
   ```
2. Configure your environment variables inside a `.env` file (see `.env.example` for details):
   ```env
   GEMINI_API_KEY=your_google_gemini_api_key_here
   ```

### Execution
Start the developmental local proxy and telemetry simulator:
```bash
npm start
```
The application will launch on **port 3000** automatically. Open [http://localhost:3000](http://localhost:3000) inside your browser.
