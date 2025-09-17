```mermaid
graph TD

    A["Classroom Booking Utility Tree"]:::utility

    %% Performance
    A --> B["Performance"]:::qa
    B --> B1["Response Time"]:::qar
    B1 --> B1a["(H,H) Availability queries return in < 2 sec"]:::asr

    B --> B2["Concurrency"]:::qar
    B2 --> B2a["(H,H) Only one successful booking per room/time slot"]:::asr

    %% Availability
    A --> C["Availability"]:::qa
    C --> C1["Uptime"]:::qar
    C1 --> C1a["(H,H) System must be available during booking hours (>99%)"]:::asr

    %% Reliability
    A --> D["Reliability"]:::qa
    D --> D1["Fault tolerance"]:::qar
    D1 --> D1a["(H,H) Allow rollback of cancellations within 1 min"]:::asr

    D --> D2["Auditability"]:::qar
    D2 --> D2a["(H,H) Maintain complete logs of booking actions"]:::asr

    %% Usability
    A --> E["Usability"]:::qa
    E --> E1["Learnability"]:::qar
    E1 --> E1a["(H,H) Users can create or cancel a booking in < 5 clicks"]:::asr

    E --> E2["Accessibility"]:::qar
    E2 --> E2a["(H,H) Mobile and desktop support for booking functionality"]:::asr

    %% Security
    A --> F["Security"]:::qa
    F --> F1["Account Control"]:::qar
    F1 --> F1a["(H,H) Staff, Registrar and Admin permissions are enforced post login"]:::asr

    %% Styles (now with black text)
    classDef utility fill:#9cf,stroke:#000,stroke-width:2px,color:#000;
    classDef qa fill:#f66,stroke:#000,stroke-width:2px,color:#000;
    classDef qar fill:#9f9,stroke:#000,stroke-width:2px,color:#000;
    classDef asr fill:#f9f,stroke:#000,stroke-width:2px,color:#000;