# NYC Metro Challenge

## The Data Science Challenge

### Introduction

To have a better understand on how u work, your strengths and weakness, we're proposing a challenge!

You are going to work with the [NYC metro database](http://web.mta.info/developers/turnstile.html), which has the field description attached below. To help your work, we present the database already merged at this (link)[https://drive.google.com/file/d/1VnNIZMOVHTX2hE9zasi8PQQNd9xwwdYL/view].

The main goal is to forecast the number of people that uses the metro. You can let the imagination work and do this the way you prefer, choosing the temporal/spatial sampling rate (by station/turnstile, day/hour/week etc). This choice is part of the challenge.

Please, do not put everything in a huge ANN model directly, take a nice look at the data and perform a great exploratory data analysis. We prefer to receive the results in a notebook way, but if you wish to provide a nice script, there is no problem =) (If it's nicely commented, of course).

Good Luck!

### Field Description

- C/A = Control Area (A002)
- UNIT = Remote Unit for a station (R051)
- SCP = Subunit Channel Position represents an specific address for a device (02-00-00)
- DATEn = Represents the date (MM-DD-YY)
- TIMEn = Represents the time (hh:mm:ss) for a scheduled audit event
- DEScn = Represent the "REGULAR" scheduled audit event (occurs every 4 hours)
- ENTRIESn = The cumulative entry register value for a device
- EXISTn = The cumulative exit register value for a device
