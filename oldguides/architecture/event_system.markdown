#Event System#

Massively multiplayer online games are by necessity big. Really, really big. Think for just a moment about all the different categories of features that make up a game (referred to in the MMOServer code as **Services**): crafting, combat, chat, trading, movement... and the list can easily go on for some time. There is so much functionality provided by these services that in mots MMORPGs they need to be run across multiple processes and/or physical machines.

Alright, we've established that the scope of developing a MMORPG is rediculous, if you don't believe me just ask for helpful starting advice at [StackOverflow](http://www.stackoverflow.com/) or [GameDev.net](http://www.gamedev.net/)[^1]. Still with me? Good, insanity is a must to proceed. Now you might be thinking: how do we manage all of this complexity without it turning into a big bowl of code spaghetti?

[^1]: If you're a hobbiest programmer with a mind on building an MMORPG expect to be met with many a "don't do it" suggestions along the way.

The key to managing the complexity of many interacting services is good communication. There are two ways in which services need to communicate with each other: to inform an unknown number of interested parties that something significant has occurred (via the **Event Dispatcher**) and to make requests directly to a specific type of service (via the **Service Locator**). This article focuses on the motivation behind the Event Dispatcher and common usage patterns to help you quickly get up to speed with one of the most vital components of the SWG:ANH MMOServer engine.

##Overview##

The Event Dispatcher consists of three main components starting with the **dispatcher** that serves as the focal point for services to communicate their current state with one another. Service helper objects, known as **listeners**, **connect** to the dispatcher and wait for specific types of messages, or **events**, to be **delivered**. Other services **notify** the dispatcher that an event has occurred, which in turn notifies all the listeners that have expressed interest in that event type.

##Events##

Events are a way for a service to package information about an observable behavior that is either being performed or about to be performed. They are like a standardized language that all services have agreed upon as an acceptible way to communicate with one another.

The most basic event type is, unsurprisingly, called the basic_event. It consists of a **subject**, the object responsible for invoking the event, and the **event data**, a collection of information that gives context for the event.

##Event Dispatcher##


##Listeners##