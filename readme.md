# Plugin Architecture Exploration

So we are thinking about building a platform for issuing badges, doing assessment, etc.

One way to build that is to have a collection of services that interact with each other via API. We have done this in the past and we know how to do it. The downside is deployment: if we want this to be a product that people can use on their own, to have a full badge offering they would need to have the expertise to deploy several services and configure them properly.

Another way to build that is to have a “core” which provides basic functionality and to build out features using a plugin architecture. A classic example of this is WordPress. The core of WordPress provides the basic functionality of getting data into a database and then displaying that at a URL, and plugins provide all sorts of functionality, from comments to spam checking to polls to even badge issuing.

There are a few upsides to the plugin architecture:
* feels more like a “product”
* much easier to deploy than a collection of services
* extensibility built in from the start

However, we as a team have never attempted to build something like that before and personally I don't have much experience with it. That is the purpose of this repository – to try to explore what it would take to build out that type of system and to come up with some sort of general estimate of the engineering effort should we decide to go down that path.