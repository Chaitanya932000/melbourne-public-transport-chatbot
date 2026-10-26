# 🚆 Melbourne Public Transport Chatbot

![Python](https://img.shields.io/badge/Python-3.x-blue) ![Rasa](https://img.shields.io/badge/Rasa-NLU%20chatbot-5A17EE) ![GTFS](https://img.shields.io/badge/Data-GTFS%20%7C%20PTV%20API-0072CE) ![Team project](https://img.shields.io/badge/Team-Chameleon%20%C2%B7%20Deakin-orange)

A conversational assistant that helps people get around Melbourne: finding the next train, checking live transport updates and seeing train, tram and bus routes on a map. It's built on public transport timetable data and real-time feeds.

> **Team project.** This chatbot was built by a Deakin University capstone team as part of the **Melbourne Open Data Playground (MOP)** project with Chameleon. The full source code lives in the team repository. This page summarises the project and **my own contributions** to it.
>
> 📂 **Code:** [Chameleon-company/MOP-Code → Public Transport Chatbot](https://github.com/Chameleon-company/MOP-Code/tree/master/usecases/UPDATE%20NEEDED/T2_2025_Public_Transport_Chatbot_v2/code/mpt_bot)
>
> 🧾 **My commits:** [View all my changes](https://github.com/Chameleon-company/MOP-Code/commits/master?author=Chaitanya932000)

---

## 💡 The problem

Planning a trip on Melbourne's public transport often means switching between timetable apps, maps and service alerts. The aim of this project was a single, friendly chat interface where someone can just ask *"When's the next train from Flinders Street to Richmond?"* and get a clear answer.

## ✨ What the chatbot does

- **Find my next train:** understands station names in plain language and returns upcoming departures from GTFS timetable data
- **Real-time updates:** live transport information via the Public Transport Victoria (PTV) Timetable API, plus weather from the Bureau of Meteorology
- **Interactive maps:** train, tram and bus routes and stops shown on maps
- **Web chat interface:** a browser-based chat window with feature buttons and pop-up panels

## 🙋 My contributions (Aug–Sep 2025)

| Area | What I did |
|---|---|
| **Find next train** | Made the trip-finding logic more robust: input validation for station names, fallbacks when stations aren't found, fixes to DataFrame indexing and time parsing, and removal of duplicate trips (`gtfs_utils.py`, `actions.py`) |
| **Real-time data** | Added real-time transport updates to the chatbot and wrote a setup guide for the PTV and weather APIs |
| **Maps** | Updated the train, tram and bus map features |
| **Conversation design** | Updated the NLU training data, rules and domain so the bot understands more user requests, and fixed a training-data bug |
| **Web interface** | Improved the chat web page with a pop-up system, feature buttons and better UI/UX (`index.html`, `chat.js`) |

## 🛠️ Tech stack

| Layer | Tools |
|---|---|
| Conversational AI | Rasa (NLU, rules, stories, custom actions), spaCy |
| Data | pandas, GTFS timetable data, PTV Timetable API, fuzzy string matching |
| Maps & location | Folium, geopy |
| Front end | HTML, JavaScript |

## 📚 What I learned

- Working with real, messy transport data (GTFS) and making code handle bad or missing input gracefully
- Designing a chatbot's conversation flow: intents, entities, rules and custom actions
- Connecting live APIs and handling keys safely
- Contributing to a large shared codebase through Git branches, commits and team review

---

**Chaitanya Patil** · Master of Data Science, Deakin University
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Chaitanya%20Patil-0A66C2?logo=linkedin&logoColor=white)](https://www.linkedin.com/in/chaitanya932000) · [GitHub profile](https://github.com/Chaitanya932000)

*Credit: Chameleon / Melbourne Open Data Playground project team, Deakin University. All project code belongs to the team repository linked above.*
