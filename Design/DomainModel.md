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

  Home : Pages[] Pages

  LifePerformances 
  LifePerformances <-- Youtube Video
  LifePerformances : YoutubeVideo[] Videos

  YoutubeVideo : Video YoutubeVideo
  LifePerformances : String[] Comments
  LifePerformances : int Likes

  Groupies <|-- ForumnPost
  Groupies : ForumnPost[] ForumnPosts


  ForumnPost : int PostID
  ForumnPost : String message
  ForumnPost <-- User
  ForumnPost : int Likes

  JamSession
  JamSession <-- BlogPost
  JamSession : BlogPost[] BlogPosts

  BlogPost : int PostID
  BlogPost : String Message
  BlogPost <-- User

  BackStagePass <-- Podcast
  BackStagePass : Podcast[] Podcasts

  Podcast : Podcast Podcast

  Calendar <-- Event
  Calendar : Event[] Events

  Event : int EventID
  Event : Date EventDate
  Event : Time EventTime

  Event <-- User

  MerchPage : Merch[] Merch

  PlugIn : String Email
  PlugIn <-- User

  User: String Username
  User: String Password
  User: String Status

  User <-- Admin Panel
  AdminPanel
  AdminPanel
```

