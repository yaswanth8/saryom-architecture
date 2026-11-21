# Saryom architecture

**Your neighbourhood, in one place.** Buy and sell, share a meal, share a ride, or keep track of your job search, with people near you.

This repo holds the architecture notebook for Saryom: a React app in front of an API gateway and eight Spring Boot services that talk to each other through events, all running on free tiers.

**Read it here:** https://yaswanth8.github.io/saryom-architecture/

The page is one self-contained `index.html` (no build step). It covers:

1. The system map (click any box for details)
2. Event flow: who publishes and who listens on the 24 topics
3. One request traced end to end (a buyer making an offer)
4. Design patterns and their trade-offs
5. Hosting on free tiers and CI/CD
6. Observability (OpenTelemetry → Grafana Cloud)
7. Known gaps

## Keeping it up to date

The source of truth is the 13 Saryom repositories. When the architecture changes (a new service, topic, binder, deploy target or monitoring change), update `index.html` in the same week:

- Edit the relevant section of `index.html`. Service boxes and details live in the `SVC` and `DETAIL` objects in the script at the bottom, topics in `EVENTS`, pattern cards in `CARDS`.
- Bump the "last updated" date in the footer.
- Commit to `main`. GitHub Pages republishes within a minute or two.

In the Saryom Claude project, the coordinator owns this: when a thread changes the architecture, it updates this repo as part of finishing that work.

## What never goes in here

This repo is public. No secrets, tokens, connection strings, Grafana credentials, private dashboard links, or details that would help someone attack the live services.

## Hosting

GitHub Pages, free for public repositories (Settings → Pages → Deploy from a branch → `main` / root).
