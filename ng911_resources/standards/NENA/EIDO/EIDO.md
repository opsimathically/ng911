# EIDO

**EIDO (Emergency Incident Data Object)** is a **standardized, structured data package** used within **U.S. Next Generation 911 (NG911)** systems to represent **all known information about a specific emergency incident** in a machine-readable, interoperable form.

In practical terms, **EIDO is the data container that NG911 systems use to share incident information consistently across systems, agencies, and jurisdictions**.

An EIDO is:
- A **digital incident record**
- Built from **multiple data sources**
- Continuously updated as new information arrives
- Shareable across NG911, CAD, and responder systems

It replaces fragmented, vendor-specific incident data with a **common, standards-based incident representation**.

Before NG911:
- Incident data was siloed in PSAP call-handling systems
- Transfers between agencies lost context
- Multimedia and sensor data could not be shared reliably

EIDO solves this by:
- Creating **one authoritative incident data object**
- Enabling **real-time data sharing and updates**
- Supporting **automation and advanced analytics**

## Documentation


This is the current standard PDF: (hasn't been updated since 2021)
[Standard PDF 021.1b-2021](https://cdn.ymaws.com/www.nena.org/resource/resmgr/standards/NENA-STA-021.1b-2021_2024121.pdf)

Always double check [the NENA standards page](https://www.nena.org/page/standards) to ensure that the PDF you're using for development is not out of date.

## What an EIDO Contains

An EIDO can include (not all fields are mandatory):

### Core Incident Data
- Incident identifier (globally unique)
- Incident type (fire, medical, law enforcement, etc.)
- Timestamp(s) and lifecycle state

### Location Information
- Civic address
- Geospatial coordinates
- Vertical (Z-axis) location
- Location confidence/uncertainty

### Caller / Source Information
- Phone number or device identifier
- Text, voice, video, or sensor source
- Accessibility indicators (e.g., RTT usage)

### Multimedia and Data Feeds
- Text transcripts
- Images and video
- Telematics (vehicle crash data)
- IoT or alarm system data

### Operational Metadata
- Jurisdictional ownership
- Agency handling the incident
- Call transfers and updates
- Data provenance and timestamps

## How EIDO Is Used in NG911

### Within the NG911 Call Flow
- Created when an emergency communication is received
- Enriched as new data arrives (caller updates, multimedia, sensors)
- Passed along with the call during transfers

### Between Systems
- Shared from NG911 systems to:
  - Computer-Aided Dispatch (CAD)
  - Emergency Operations Centers (EOC)
  - Mutual aid partners
- Maintains **context continuity**, even across jurisdictions

## What EIDO Is *Not*

To avoid confusion:
- EIDO is **not** a CAD record (though it may feed CAD)
- EIDO is **not** a call audio file
- EIDO is **not** vendor-proprietary
- EIDO is **not** limited to voice calls

It is a **data abstraction layer for emergency incidents**.

## Why EIDO Matters Operationally

EIDO enables:
- Fewer call re-questions during transfers
- Better situational awareness for dispatchers
- Faster, more informed responder deployment
- Improved interoperability during large-scale or multi-agency incidents
- Future capabilities such as AI-assisted triage and analytics
