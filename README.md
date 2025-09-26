# ABApp
React App for the UofSC ABA club.
The casual slack app for orgs.


## Stack for ABApp
**Frontend**
    - React Native + Expo
**Backend**
    - Firebase
**Extras**
    - Push notifications (Expo + Firebase)
    - Calendar API for Google Calendar.


## **Features**
- **Users** --> Different Account Types
    - Owner (Club Leader)
    - Admin (Club Exec Board)
    - Member (Club Member)

- **Push Notifications for Event Syncing**
    - Automatically Add to Everyones Calendar
    - Send a reminder (Options for Morning of, Hour before, 30 minutes before, custom)
    - WhenToMeet availability feature per user (Can change whenever)
    - Event signup
        - Headcount vs "signup" (everyone expected to attend vs who wants to do the event)
        - fill out form ( Who has car, extra information )

- **Announcments and Messages**
    - Announce to the group
        - Pinned at top of GC
    - Pinned messages like GroupME
        - Grouped pins of messages
    - Exec only GC

- **No direct messages between members**

- **Big feature: Making it feel casual**
    - not professional like Slack
    - not too casual like instagram
    - make messages feel iMessage
    - Emojis instead of yes or no for polls and stuff

## Problems
- Multiple GC's (Too many people for 1)
    - Create large groupchat
    - Instagram feels too professional



## User Discovery
    - Streaks for meetings attended? 
        - Could be trophies
        - Only admin can see?

    - Message reactions
        - Emojis for yes or no
        - iMessage vs Insta vs discord style

    - What features theyd want as members vs as exec