Digital Forensic & OSINT Triage Framework
Standard Operating Procedure (SOP) for Missing Persons Intelligence
Author: Michael Watson
Role: Cyber-Investigation & IT Analyst | Certified Paralegal
Target Environments: Kali Linux, CSI Linux, CAINE
________________________________________
Legal & Ethical Disclaimer
This framework is provided for educational and professional methodology demonstration purposes only. In the State of California, any investigative activity conducted for consideration must be performed by a licensed Private Investigator or under the direct supervision of a licensed Attorney (BPC § 7523 / § 6450). This SOP is designed for use within a pro bono non-profit environment (e.g., Trace Labs) or under Attorney-Client Privilege as part of a litigation support team.
________________________________________
Mission Objective
To establish a verifiable, repeatable methodology for identifying unidentified individuals in digital media and mapping their network associations to assist law enforcement in missing persons cases.
________________________________________
Technical Stack
•	Operating Systems: Kali Linux (Offensive OSINT), CSI Linux (Forensic Case Management).
•	Visual Forensics: ffmpeg, PimEyes, FaceCheck.id.
•	Identity Resolution: Sherlock, Maigret.
•	Network Mapping: Maltego, WitnessMe.
•	Data Scrapers: instaloader, toutatis.
________________________________________
Phase-by-Phase Execution
Phase 1: Visual Forensics & Biometric Triage
Goal: Extract high-fidelity facial "fingerprints" from source media for identity resolution.
1.	High-Quality Frame Extraction: Utilize ffmpeg on Kali Linux to isolate I-frames from video discovery to ensure maximum biometric accuracy.
o	ffmpeg -i input_video.mp4 -vf "select=eq(pict_type\,I)" -vsync vfr frame_%03d.png
2.	Biometric Cross-Referencing: Submit extracted frames to specialized facial recognition engines (PimEyes, FaceCheck.id) via the CSI Linux Gateway to identify public-facing profiles (social media, modeling portfolios, etc.).
3.	International Contextual Search: Leverage Yandex Images for broad-spectrum identity resolution in multi-national maritime or travel contexts.
Phase 2: Social Media Network Analysis
Goal: Identify "outlier" engagement patterns within the Subject’s digital orbit.
1.	Target Handle Profiling: Execute Sherlock or Maigret to map the target's handle across all known social platforms.
o	maigret [Target_Handle] --parse
2.	Engagement Audit: Analyze "likes" and comments on recent posts (6-month window). Cross-reference active users who follow the primary subject but do not follow the missing person to identify potential Third-Party Persons of Interest.
Phase 3: Geolocation & "Soft Launch" Forensics
Goal: Correlate location data with temporal evidence.
1.	Location Scraping: Utilize instaloader on Kali to scrape public posts and tags from specific marinas, bars, or ports visited by the subject during the critical time window.
2.	Visual Correlation: Perform side-by-side analysis of subject media and public tags to find matching environmental artifacts (e.g., yacht equipment, unique deck furniture, or specific maritime weather patterns).
Phase 4: Forensic Case Management & Chain of Custody
Goal: Maintain evidentiary integrity for potential judicial review.
1.	Environment Isolation: Conduct all "active" scraping within a CSI Linux Case Management container to ensure all logs and screenshots are timestamped and forensically preserved.
2.	Digital Footprinting: Use WitnessMe to capture full source-code metadata of social media profiles before they can be deleted or altered.
3.	Relationship Mapping: Deploy Maltego to create a link-analysis chart, visually mapping the connections between the primary subject and newly identified third parties.
________________________________________
Reporting & Escalation Protocols
Findings must never be shared publicly or used to contact private individuals. Unauthorized contact may compromise federal investigations or result in harassment charges.
1.	Authorized Tip Lines: Submit formal leads via the FBI Electronic Tip Form (tips.fbi.gov).
2.	Local Jurisdictions: Coordinate with the relevant local or international Criminal Investigation Department (CID) for maritime or international matters.
3.	Legal Counsel: If working in a litigation support capacity, deliver all findings directly to the lead Attorney as Confidential Work Product.
