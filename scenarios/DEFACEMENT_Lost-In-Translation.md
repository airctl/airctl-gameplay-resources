# AIRCTL Project Quick Play Scenario: "Lost in Translation"

<img width="1481" height="279" alt="image" src="https://github.com/user-attachments/assets/ad347097-26fa-4f2e-a600-1afa017c945a" />


## Scenario Detections Map:
INITIAL ACCESS - HIJACKED MODEL REPOSITORY
- Functional Baselines, Cross-Validation, Server Analysis

PIVOT and ESCALATE - NEW SERVICE CREATION/MODIFICATION
- Endpoint Analysis, Endpoint Security Protection Analysis

C2 and EXFIL - DNS AS C2
- Network Threat Hunting - Zeek/RITA Analysis, Firewall Log Review

PERSISTENCE - MALICIOUS SERVICE
- Endpoint Analysis, Memory Analysis, Endpoint Security Protection Analysis

## Preamble
We are an AI startup and we provide subtitles and bilingual translations using machine learning. There are curse words coming into the translations - at least this is what the users are reporting. 

We have a really good PR team, and we have a lot of good network analysts for firewall review. Now there is a need to figure out why our data is being poisoned. 


## Hints (no particular order)
- We could try functional baselines, do we have those?
- It’s a public-facing incident and not just an internal incident – this means that the service is exposed externally.
- The service is a paid service and we have payment information via endpoints we sell access to.

## Card Flip Scripts
**INITIAL ACCESS - HIJACKED MODEL REPOSITORY**
- Read when Flipped: Someone hijacked our translation models and inserted incorrect translation examples into the model training process so that all the examples translated to obscene words in another language.
- OPTIONAL HINT: You can see the code that they used to do this and that they’re accessing other services and endpoints that have access to the model.


**PIVOT and ESCALATE - NEW SERVICE CREATION/MODIFICATION**
- Read when Flipped: There’s a suspicious program we detect when we look at our endpoints that seems to be doing something.
- OPTIONAL HINT: It’s unclear what it is though without more review.

**C2 and EXFIL - DNS AS C2**
- Read when Flipped: Good thing we looked around to see if there was any additional movement in our networks!
- OPTIONAL HINT: I wonder what is going on with our endpoints...

**PERSISTENCE - MALICIOUS SERVICE**
- Read when Flipped: The attackers made a malicious service run every time the entire translation model is invoked, and it’s doing so much more than just poisoning the model! It’s making every result profane if the model didn’t do it!
- OPTIONAL HINT: We see that it’s increasing memory usage and also showing up in endpoint logging.

## Scenario Resources
- Play here: https://airctl.github.io/
- Model Poisoning in MITRE ATLAS: https://atlas.mitre.org/techniques/AML.T0018.000

## Scenario Information

### Requirements
Backdoors & Breaches Decks
- Backdoors & Breaches Core Deck V2.2
- AIRCTL Project AIRCTL Deck - as launched 2024-10-22 on https://airctl.github.io/

### Authors
- Sam Ziegler, Portland State University 
- Emily Soward, AIRCTL Project
- Jonathan Reiter, AIRCTL Project

### Publication Date
- August 14th, 2025

### License & References
- https://github.com/airctl/airctl-gameplay-resources/blob/main/scenarios/AIRCTL-Project-Quick-Play-Scenarios-Guide.md
- https://github.com/airctl
- https://airctl.github.io/

### Disclaimer
This is a work of fiction intended to portray realistic scenarios. The names, characters and incidents portrayed in it are works of imagination. Any resemblance to actual persons, living or dead, events or localities is entirely coincidental.
