# 🚆 Melbourne Public Transport Chatbot

![Python](https://img.shields.io/badge/Python-3776AB?logo=python&logoColor=white) ![Rasa](https://img.shields.io/badge/Rasa-5A17EE?logo=rasa&logoColor=white) ![GTFS](https://img.shields.io/badge/Data-GTFS%20%7C%20PTV%20API-0072CE) ![Team](https://img.shields.io/badge/Team%20project-Chameleon%20%C2%B7%20Deakin-orange)

**Just ask "when's my next train?" and get a straight answer.**

---

## The idea

Getting around Melbourne usually means juggling a timetable app, a map and service alerts at the same time. Our team wanted something simpler: a chatbot you can talk to in plain English that pulls all of that together.

This was built by a Deakin University capstone team as part of the **Melbourne Open Data Playground (MOP)** project with Chameleon. This page tells the story of the project and **the parts I built**.

> 📂 **Full source code:** [MOP-Code → Public Transport Chatbot](https://github.com/Chameleon-company/MOP-Code/tree/master/usecases/UPDATE%20NEEDED/T2_2025_Public_Transport_Chatbot_v2/code/mpt_bot)
>
> 🧾 **Every change I made:** [my commit history](https://github.com/Chameleon-company/MOP-Code/commits/master?author=Chaitanya932000)

## What it can do

- 🚉 **Find the next train** between two stations, using official GTFS timetable data
- 📡 **Live updates** from the Public Transport Victoria (PTV) API, plus current weather from the Bureau of Meteorology
- 🗺️ **Maps** of train, tram and bus routes and stops
- 💬 **A friendly web chat** with quick-action buttons and pop-up panels

## My part in it (Aug – Sep 2025)

**Making "find my next train" reliable.** The original version broke easily: a misspelt or missing station name, an odd time format or duplicate trips in the timetable could throw an error. I added input checks, fallbacks when a station couldn't be found, and fixes for time parsing and data-frame indexing, plus duplicate-trip removal. Now the bot replies with a helpful message instead of failing. *(`gtfs_utils.py`, `actions.py`)*

**Bringing in live data.** I added real-time transport updates and wrote a setup guide so teammates could connect the PTV and weather APIs with their own keys.

**Maps.** I updated the train, tram and bus map features.

**Teaching the bot to understand people.** I extended the training examples, rules and domain so it recognises more of the ways people actually ask questions, and fixed a training-data bug.

**The chat experience.** I reworked the web page with a pop-up system, feature buttons and a cleaner, more usable layout. *(`index.html`, `chat.js`)*

## Under the hood

| | |
|---|---|
| **Conversational AI** | Rasa (intents, entities, rules, custom actions), spaCy |
| **Data** | pandas, GTFS timetable data, PTV Timetable API, fuzzy matching |
| **Maps & location** | Folium, geopy |
| **Front end** | HTML, JavaScript |

## What I learned

- Real-world data (like transport timetables) is full of edge cases, and good software expects them.
- How a chatbot really "understands" a question: intents, entities and the actions behind them.
- Working with live APIs, and keeping API keys out of shared code.
- Contributing to a big shared codebase with lots of teammates, through branches, commits and reviews.

---

<sub>**Chaitanya Patil** · [LinkedIn](https://www.linkedin.com/in/chaitanya932000) · [More of my work](https://github.com/Chaitanya932000)<br>
Credit to the Chameleon / Melbourne Open Data Playground team at Deakin University. All project code lives in the team repository linked above.</sub>
