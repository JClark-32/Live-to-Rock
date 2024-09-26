```mermaid
classDiagram
  Home
  Home -- LifePerformances
  Home -- Groupies
  Home -- JamSession
  Home -- BackStagePass
  Home -- Calendar
  Home -- MerchPage
  Home -- PlugIn

  LifePerformances 
  LifePerformances <-- Youtube Video
  Youtube Video : Youtube API
  LifePerformances : String[] Comments
  LifePerformances : int Likes

  Groupies <|-- ForumnPost
  ForumnPost : int PostID
  ForumnPost : String message
  ForumnPost <-- User
  ForumnPost : int Likes

  JamSession
  JamSession <-- BlogPost

  BlogPost : int PostID
  BlogPost : String Message
  BlogPost <-- User

  BackStagePass <-- Podcast
  Podcast : Podcast API

  Calendar <-- Event

  Event : int EventID
  Event : Date EventDate
  Event : Time EventTime

  Event <-- User

  MerchPage : Merch API

  PlugIn : String Email
  PlugIn <-- User

  User: String Username
  User: String Password
  User: String Status

  User <-- Admin Panel
  AdminPanel
  AdminPanel
```

