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

## Phase 2 — Information Relevance and System Boundary

### 1. Relevant and Irrelevant Information

The system should retain information that contributes meaningfully to emergency detection, response coordination, resource allocation, responder safety, or communication.

Examples of essential information include:

- Incident type or category
- Incident location
- Initial reporting time
- Reporting source
- Confidence or verification status of the report
- Estimated number of people affected
- Current locations and availability of emergency vehicles
- Current availability of emergency personnel
- Available hospital capacity
- Current road closures or severe traffic congestion
- Emergency vehicle fuel or battery status when operational readiness depends on it

Some information may be potentially relevant depending on the incident or sophistication of the system, including:

- Current weather conditions
- Structural instability of damaged buildings
- Social-media activity relating to the incident
- Identifiers of emergency personnel assigned to an incident

Information that normally does not contribute meaningfully to emergency-response coordination should remain outside the abstraction. Examples include:

- Clothing colour of the reporting citizen
- CCTV camera brand when technical capabilities such as resolution can be represented directly
- Property prices in the affected neighbourhood
- Detailed patient medical histories, because clinical diagnosis and treatment are outside the scope of this system
- Nearby restaurant menus

The system should therefore retain information based on relevance to its objective rather than merely because that information exists in the real world.

### 2. System Boundary

#### Responsibilities Inside the System

The emergency-response system is responsible for:

- Receiving emergency reports
- Creating and maintaining incident records
- Classifying the reported emergency
- Evaluating confidence or verification information
- Notifying relevant emergency authorities
- Recommending appropriate available emergency resources
- Tracking emergency-resource dispatch and location status
- Displaying incident information to authorised decision-makers
- Issuing authorised public warnings
- Tracking whether incidents remain active or have been resolved
- Receiving relevant information from external systems such as CCTV, traffic, hospital-capacity, and vehicle-location systems

#### External Human or System Responsibilities

The following activities occur outside the software itself:

- Human dispatchers authorising high-consequence emergency-resource deployment
- Ambulance drivers physically driving ambulances
- Doctors and other healthcare professionals treating injured people
- Healthcare professionals determining medical diagnoses
- Firefighters physically extinguishing fires
- Police officers and other responders performing real-world emergency operations

These activities are part of the broader emergency-response process, but they are performed by external humans or systems rather than by this software.

#### Explicitly Out-of-Scope Activities

The first version will not attempt to:

- Predict earthquakes or similar disasters months in advance
- Conduct subsequent criminal investigations
- Replace professional emergency responders or other human decision-makers
- Perform autonomous physical emergency-response operations

### 3. Information Entering the System

Information entering the system may include:

- Emergency type or description
- Geographic location
- Estimated number of people affected
- Reporting source and timestamp
- CCTV images or live video
- Road and traffic information
- Hospital and emergency-facility availability
- Emergency-vehicle location and availability
- Emergency-personnel availability
- Other sensor or operational information relevant to the incident

### 4. Information and Actions Leaving the System

Outputs from the system may include:

- Alerts sent to the appropriate emergency or administrative authorities
- Authorised public emergency warnings
- Detailed incident records and reports
- Recommendations for suitable hospitals, police stations, fire stations, ambulances, or other response resources
- Incident-resolution and status updates
- Emergency-vehicle dispatch and current-location information

### 5. Human-in-the-Loop Dispatch Decision

For Version 1, the software should recommend an appropriate emergency resource rather than automatically dispatching it.

For example, the system may conclude that Ambulance A is the best available resource for Incident X, but a human dispatcher should retain final authority to approve the dispatch.

This design provides additional protection against software bugs, incomplete or stale information, incorrect assumptions, and situations where human responders possess contextual information that is not represented in the software.

The trade-off is that human approval may add some latency. For the first version, this additional delay is accepted in exchange for greater oversight, accountability, and reliability.

### 6. Real-World Information vs. Information in the Abstraction

The existence of information in the real world does not automatically mean that it belongs inside the system's abstraction.

The real world contains vastly more information than the emergency-response system requires. The abstraction should retain information only when it contributes sufficiently to the system's objectives, constraints, decisions, or required outputs.

Therefore:

> Real-world existence does not imply computational relevance.

A useful abstraction deliberately preserves task-relevant information while discarding information that adds unnecessary complexity without improving the system's ability to solve its intended problem.