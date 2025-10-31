# ServiceNow_ITSM_Project3
ITSM Project 3: Agentic AI Auto-Resolution Flow
# ServiceNow ITSM | Agentic AI Auto-Resolution Flow (Yokohama PDI)

## Overview
This project simulates an **Agentic AI** that detects known issues
(e.g., password reset / VPN / email access) and automatically resolves
incidents in **ServiceNow ITSM**.

## Flow Logic
1. **Trigger:** Incident – Created or Updated (For every update)  
2. **If:** Short description contains password OR VPN OR email access  
     AND State is not Resolved AND AI Close Notes is empty  
3. **Update #1:** Populate Resolution Code & Resolution Notes, assign to Service Desk group  
4. **Update #2:** Change State to Resolved  
5. *(Optional)* Send email notification to caller

## Key Highlights
- Handles mandatory Resolution Code and Resolution Notes before state change  
- Demonstrates “self-healing” AI workflow logic in Flow Designer  
- Built and tested on ServiceNow **Yokohama PDI**

## Outcome
Incident records with password/VPN/email keywords are auto-resolved with  
AI notes and summaries added automatically.

## Diagram
![Flow Diagram](Diagrams/ITSM_Agentic_AI_AutoResolution.png)
