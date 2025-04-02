# Threat Response: InfoSec Under [Control/Crisis] Kiosk


## The Idea
This is a custom Splunk "dashboard" to help users who are not familiar with Splunk SPL run searches effectively across multiple log sources without writing a single query. It'll take one person (power user) to set this up (and possibly create the macros it needs), but it will benefit the whole team.

Since every log source has a different taste of username in it, for example, it could be john.doe@company.com, jdoe@company.com, or jdoe, etc. The idea of this "dashboard" is to leverage a prebuilt "**user identities**" lookup file and generate a "search string" that contains all usernames of a specific user; then feed it to multiple Splunk macros to search across multiple sources.

This "dashboard" allows the analysts to have an overview of a specific user/IP/domain/anything within the scopes of the pre-defined macros. It also allows the analysts to jump between log sources as well as quick filtering without re-running the searches.

## User Guide
[User Guide Here](https://github.com/KikDaCat/TRISUCCK/blob/23050a816cf82ced0eda4dacaad7eaafb1308255/TRISUCCK-UserGuide.pdf)

## What it needs?
- A predefined "**user identities**" lookup file
> The lookup file will be used [here (line #1907)](https://github.com/KikDaCat/TRISUCCK/blob/844234754f6cb30d13bd80dfc7cc769ac0eb063f/TRISUCCK_Public.xml#L1907)
- Predefined macros
> Most of the macros that are used in the dashboard are [here](https://github.com/KikDaCat/TRISUCCK/blob/main/TRISUCCK-Macros.txt). Please modify it to fit your needs.
- The dashboard is designed to be modular, you can add new panes and macros to serve your needs.
- Most of the panes in the dashboard are interactive. However, since it used mostly SimpleXML, please be careful when you modify and/or add a new pane to the dashboard. Please refer to the current setup, the pane's elements will have this "*something_[panename]*" naming.
- Please feel free to leave a comment, I'll try to help as much as I can :)

## What it looks like
![enter image description here](https://github.com/KikDaCat/TRISUCCK/blob/844234754f6cb30d13bd80dfc7cc769ac0eb063f/TRISUCCK-Demo.png)

