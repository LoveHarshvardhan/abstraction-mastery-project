# Abstraction Mastery Project

## Stage

0.1.16 — Abstraction Mastery Project

## Purpose

This project demonstrates my understanding of abstraction as a foundation of computational thinking.

The project will apply concepts including:

- relevant vs. irrelevant information
- representation
- levels of abstraction
- abstraction barriers
- information hiding
- data abstraction
- procedural abstraction
- algorithmic abstraction
- modelling
- granularity
- trade-offs
- abstraction failures
- abstraction leakage
- mathematical abstraction
- programming abstraction
- abstraction in artificial intelligence

## Project Status

In Progress

## Phase 1 — Problem Formulation

### 1. Core Problem

The system must help coordinate responses to emergency incidents occurring within an urban area. Information about an incident is reported to the system, after which the appropriate emergency or administrative authorities must be informed. Decision-makers need reliable information quickly enough to determine an appropriate response, allocate available resources, and protect affected citizens.

### 2. Primary Objective

The primary objective of the system is to support a timely and appropriate emergency response by receiving information about an incident, notifying the relevant authorities, tracking the status of dispatched emergency services, and communicating important response outcomes to the concerned authorities and citizens.

### 3. Inputs

The system may receive information including:

* Incident type or category
* Incident location
* Reporting source
* Initial reporting time
* Images or live video from CCTV cameras
* Estimated number of people affected
* Locations and availability of nearby police stations, hospitals, fire stations, and other response facilities
* Availability and current status of ambulances, fire engines, police vehicles, boats, and other emergency resources

### 4. Outputs

The system may produce outputs including:

* Alerts to police authorities
* Alerts to fire departments
* Alerts to government or private hospitals
* Alerts to relevant municipal or administrative bodies
* Public or citizen emergency alerts
* Emergency-resource dispatch and response-status information

### 5. Constraints

The system must operate under real-world constraints including:

* Limited numbers of emergency vehicles
* Limited police, fire-service, and emergency personnel
* Limited hospital beds, doctors, nurses, and other medical resources
* Incomplete CCTV or sensor coverage across the urban area
* Limited availability of specialised rescue equipment such as boats during severe flooding
* Roads, bridges, or other infrastructure becoming inaccessible or damaged during an emergency

### 6. Explicit Non-Goals

The first version of the system will deliberately not attempt to:

* Automate the driving of ambulances, fire engines, police vehicles, or other rescue vehicles
* Diagnose patients or determine medical treatment
* Replace or directly command police officers, firefighters, medical personnel, or other human decision-makers
* Model long-term reconstruction or the post-disaster physical landscape after an incident has been resolved
* Predict emergency incidents before they occur

The system is intended to support human emergency-response operations rather than replace the professionals responsible for making critical real-world decisions.
