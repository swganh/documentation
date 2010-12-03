#Event System#

Massively multiplayer online games are by necessity big. Really, really big. Think about all the different categories of features that make up these games (referred to in the MMOServer code as **Services**): crafting, combat, chat, trading, movement... and the list goes on. With something on this scale traditional single threaded game programming techniques go right out the window, server code is almost guaranteed to be run on multiple cores/processors if not multiple physical machines.

With code potentially running from another physical machine how on earth are these services suppose to communicate with one another? And, how do these services communicate with one another without developing a tight coupling on specific implementations? To answer these questions lets look at the requirements necessary for communicating between two services.

###Communication is key###

There are two ways in which services needs to communicate with other aspects of the server: to inform an unknown number of interested parties that something significant has occurred (**Event Dispatch**) and to make requests directly to a specific type of service (**Service Locator**). This article focuses on the motivation behind the Event Dispatch and common usage patterns to help you quickly get up to speed with one of the most vital components of the SWG:ANH MMOServer engine.


  Discuss a concrete example that will be used throughout the article to  explore the Event systems functionality and the general motivation behind it.

The Event Dispatch consists of three main components starting with the **dispatcher** that serves as the focal point for services to communicate their current state with one another. Service helper objects, known as **listeners**, **connect** to the dispatcher and wait for specific types of messages, or **events**, to be **delivered**. Other services **notify** the dispatcher that an event has occurred, which in turn notifies all the listeners that have expressed interest in that event type.

##Events##


##Event Dispatcher##


##Listeners##