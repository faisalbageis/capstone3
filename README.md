# Darbak | دربك


A ride-sharing and match-planning platform for football fans attending the Asian Cup in Saudi Arabia. Fans can offer seats, request rides, save matches, and use AI to help plan their matchday.

## Features

- Ride search, car availability checks, and seat reservations.
- Driver acceptance/rejection of requests and passenger management.
- Saved matches, ride recommendations, and matches without arranged rides.
- Google Maps meeting points and directions links.
- AI matchday plans, two-match attendance estimates, review moderation, and review summaries.
- User ratings/statistics, automatic WhatsApp notifications, and welcome emails.
- Match/stadium management, Football API fixture import, and user banning.

## Technology

Java 17 · Spring Boot · Spring Data JPA/Hibernate · MySQL · Jakarta Validation · Lombok · Maven.

Integrations: OpenRouter AI, Google Maps JavaScript, API-Football, UltraMsg WhatsApp, Spring Mail/Gmail SMTP, and OpenPDF. The demo frontend uses plain HTML, CSS, and JavaScript.

## Extra endpoints

All routes below use the prefix **`/api/v1`**.

| Method | Path | Purpose |
|---|---|---|
| POST | `/RideRequest/add/{user_id}/{ride_id}` | Request a seat |
| GET | `/RideRequest/ride/{ride_id}` | Ride’s requests |
| GET | `/RideRequest/user/{user_id}` | User’s requests |
| POST | `/RideRequest/accept/{request_id}/{driver_id}` | Accept request |
| POST | `/RideRequest/reject/{request_id}/{driver_id}` | Reject request |
| DELETE | `/RideRequest/cancel/{request_id}/{passenger_id}` | Cancel request |
| GET | `/RideRequest/user/{user_id}/pending` | Pending requests |
| GET | `/RidePerticipant/user/{user_id}/ride/{ride_id}` | Specific participant |
| GET | `/RidePerticipant/ride/{ride_id}` | Ride’s participants |
| GET | `/RidePerticipant/ride/{ride_id}/role/{role}` | Participants by role |
| POST | `/review/add` | Add review with AI moderation |
| GET | `/match/attendance-check/{match1_id}/{match2_id}` | AI attendance feasibility |
