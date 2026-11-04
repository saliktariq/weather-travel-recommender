# Weather-Aware Travel Recommender

Recommends destinations and day-by-day activities based on the weather forecast and what's actually open at the destination.

> **Status: early development.** This README describes what the app will do. Setup instructions, a demo and eval results will be added as they're built.

## The idea

A good trip plan changes with the weather. A rainy day in Lisbon calls for different plans than a clear one, and a recommendation is only useful if the place it suggests really exists and is open.

## How it will work

1. You give a destination, or a shortlist of destinations, and your dates
2. It fetches the weather forecast for those dates
3. It fetches the activities and venues available there
4. An LLM builds a day-by-day plan matched to the forecast, using only the venues it retrieved
5. Each plan explains why each activity was picked for that day

## How it will be measured

An eval set of test trips will check that:

- every activity fits the forecast (no beach day in the rain)
- every venue in a plan is real and came from the activities data
- cost and response time per plan stay within a set budget

Results will be published here.

## Tech stack (planned)

Python · FastAPI · an LLM API with tool calling · a weather API · an activities API

## Roadmap

- [ ] Weather and activities API clients
- [ ] First plan generator using tool calling
- [ ] Eval set of test trips, with results in this README
- [ ] Web demo
- [ ] Write-up of what worked and what didn't