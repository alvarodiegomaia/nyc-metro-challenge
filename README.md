# NYC Metro Challenge

## The Data Science Challenge

### Introduction

To have a better understand on how u work, your strengths and weakness, we're proposing a challenge!

You are going to work with the [NYC metro database](http://web.mta.info/developers/turnstile.html), which has the field description attached below. To help your work, we present the database already merged at this [link](https://drive.google.com/file/d/1VnNIZMOVHTX2hE9zasi8PQQNd9xwwdYL/view).

The main goal is to forecast the number of people that uses the metro. You can let the imagination work and do this the way you prefer, choosing the temporal/spatial sampling rate (by station/turnstile, day/hour/week etc). This choice is part of the challenge.

Please, do not put everything in a huge ANN model directly, take a nice look at the data and perform a great exploratory data analysis. We prefer to receive the results in a notebook way, but if you wish to provide a nice script, there is no problem =) (If it's nicely commented, of course).

Good Luck!

#### Field Description

- C/A = Control Area (A002);
- UNIT = Remote Unit for a station (R051);
- SCP = Subunit Channel Position represents an specific address for a device (02-00-00);
- DATEn = Represents the date (MM-DD-YY);
- TIMEn = Represents the time (hh:mm:ss) for a scheduled audit event;
- DEScn = Represent the "REGULAR" scheduled audit event (occurs every 4 hours);
- ENTRIESn = The cumulative entry register value for a device;
- EXISTn = The cumulative exit register value for a device.

# Regular Field Description

## Metropolitan Transportation Authority Turnstile Usage Overview

### General Description

The Metropolitan Transportation Authority (MTA) is a public benefit corporation responsible for public transportation in the state of New York serving 12 counties in southeastern New York, along with two counties in southwestern Connecticut under contract to the Connecticut Department of Transportation, carrying over 11 million passengers on an average weekday system-wide, and over 800,000 vehicles on its seven toll bridges and two tunnels per weekday.

The MTA has the responsibility for developing and implementing a unified mass transportation policy for the New York metropolitan area, including all five boroughs of New York City and the suburban counties of Dutchess, Nassau, Orange, Putnam, Rockland, Suffolk and Westchester.

MTA carries out these planning and other responsibilities both directly and through its subsidiaries and affiliates, and provides oversight to these subordinate agencies, known collectively as "The Related Entities". These entities consists of the following:

- MTA Long Island Rail Road (LIRR);
- MTA Metro-North Railroad (MNR);
- MTA Island Railway (SIR);
- MTA Bridges and Tunnels (MTA B&T);
- MTA Capital Construction (MTACC);
- MTA Regional Bus Operations :
    - MTA BUS;
    - MTA New York City Bus;
    - MTA New York City Transit (NYCT).

Turnstile Usage is generated from MTA New York City Transit (NYCT), from the devices used for entry and exits to/from the stations.

Turnstile data is derived from the physical device at a Control Area (Station) used to collect fares for entry into the system. These fares are collected via swipes from a plastic media name MetroCard. The collected data is then transmitted to a mainframe application called Automated Fare Collection system (AFC).

The data file consists of entries and exits audit data are generated from the Control Areas where any of the divisions/lines it serves. In addition to NYCT transit subway stations, the MTA also receives data from the Port Authority Trans Hudson rail (PATH) and Port Authority light rail system (AIRTRAIN), as these two entities use MetroCards as a form of payment to ride the system.

The following is a break-down of where the turnstile usage data may come from:

- Divisions:
    - IRT – Interborough Rapid Transit Company;
    - Lines:
        - 1, 2, 3, 4, 5, 6, 7, S.
    - IND - Independent Subway System;
    - Lines:
        - A, B, C, D, E, F, G, M.
    - BMT – Brooklyn-Manhattan Transit Company;
    - Lines:
        - J, L, N, Q, R, Z.
- Associated agencies:
    - PATH;
    - Lines:
        - Hoboken-World Trade Center, Hoboken-33rd St, Newark-World Trade Center, Journal Square- 33rd St.
    - JFK Air-Train;
    - Lines:
        - Howard Beach – JFK, Jamaica Center - JFK.

Currently the active AFC network of turnstiles consists of approximately the following (by agency):

- NYCT – 4260;
- PATH – 383;
- JFK – 20.

### Data Collection Methodology

The audit register data is extracted from a central database weekly on Saturdays for posting. The actual register data is generated at the turnstile device every 4 hours at which time the device uploads the data to a central database.

#### Statistical and Analytic Issues

The data is broken down to Daily and Hourly periods. The data is 10 digits long and will roll-over to zero (0) on over-flow. Other factors that may impact the data are:
- Hardware failure where the hard drive needs to be replaced, and initialized;
- Data corruption from faulty devices, or heavy banging on the turnstile.

### Limitation of Data Use

There are no limitations at this time.