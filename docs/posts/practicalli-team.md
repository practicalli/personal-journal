---
title: Practicalli Team
date: 2023-10-21
categories:
  - practicalli
---

Practicalli was created in 2019 by Johnny Stevenson as an idea born from the years spent learning Clojure in the community.  I consider Practicalli a team effort as it relies on feedback and questions from the wider Clojure community, as well as the legion of libraries that have been created.

My interest in Clojure was accidental at first but eventually became a passion it is hard to live without.

The work created by Practicalli initially focused on learning the language, its idioms and common libraries.  The work has broadened to include commercial experiences gained with Clojure since 2017.

Although the published content is the sole effort of one person, it would not have been possible by the vast amount of work created by Cognitect and the Clojure community.

I thank Bruce Durling for starting my journey into Clojure and the 100's of people I've met in person and online from the community that have motivated and inspired me.

!!! WARNING "Work In Progress"

<!-- more -->


## Accidental Clojure

Over a decade of of Java development, including lots of Enterprise Java, Object Oriented databases and Corba integration work, I was looking for something to invigerate my career.

I had a great appreciation for the Java platform but the project work seemed to be very similar and some challenges didnt seem to fit the Object Oriented approach so well.

Scala programming language was making a lot of noise and was viewed as a useful way to start adoptiong a functional style of programming.

??? INFO "Haskel studied at University"
    A module on the Haskel language whist studying Software Engineering had planted the seed of functional programming and a declarative approach to writing code.

    Although Haskel as a language was an interesting option to take, the haskel ecosystem was not as widespread as Java and was seen as a far bigger jump.  There was a limited understanding of job opportunities using Haskel, certainly compared to Java and Scala.

I volunteered to start running a practical community event to practice Scala together.  I attended the Python and Clojure dojo events to see how to run an event for Scala.

After finding a company willing to host (and more importantly provide pizza and drinks) I started running a monthly Scala dojo.

I kept going to the Clojure dojo as it was a very welcoming group and I was also facinated and highly confused by the language itself.

During the first year of Clojure dojo events I slowly became very attached to the simplicity of solutions that could be created with language (even though I did strugle to understand the language as I wasnt dedicating enough time to learn it).

I was also attracted by the thought of using Emacs for development, an editor that felt less complicated and heavyweight compared to IntelliJ used by most people for Java and Scala.

!!! INFO "Startup & compilation speed challenges"
    IntelliJ has a very powerful indexing capability, however, for Scala it was indexing Java and Scala standard libraries which did add a few minutes when starting a projects.

    The Scala compiler in its early days did take some time to complete.  As all the code was required to compile before running, then the feedback time during development was a bit of a constraint.

    Tooling optomisations and faster laptops did make things better during the first year, although still in a different time frame compared to the instant feedback with Clojure.


## Conference talks

To focus my efforts to learn Clojure and share my enthusiasm, I started submitting talk proposals for conferences.  An additional benefit was to go to the conferences for free.

JAX London accepted my first Clojure talk proposal.  I was very nervous giving the first talk and was still struggling to explain some of the concepts.  However, the audience was very supportive apart from one person sat right at the front who started to heckle me half way through.  They wanted 'real world' examples of Clojure even though the talk was advertised as a simple introduction.  Out of frustration I replied, "this isnt the real world, its JAX London".  The audience laught out quite loudly, exept for the heckler who I think became more annoyed.

I learned a lot about what I didnt understand about Clojure and undeterred I worked on creating better talks.

I was hired by Atlassian as an Enginner and product ambassador (developer relations) which gave me a chance to present talks at conferences all over Europe.

The talk I enjoyed the most was at JavaDays in Sofia, Bulgaria.  I had moved away from slides and simply walked through live code examples, evaluating the code so the audience could see the REPL workflow as well as seeing the code in action.

Working at Salesforce I was also encouraged to submit talks to conferences (as well as present with other community members at Salesforce specific events).  I would submit talks and workshops on Salesforce and Clojure topics to double the chance of being accepted.  Almost all conferences accepted Clojure talks over the Salesforce talks, although CodeMotion Rome did accept a Salesforce workshop as well as a Clojure talk.

The most sureal environment I gave a Clojure talk at was CeBit, a huge conference in Hanover, Germany.  The conference is so huge it is spread over 18 aircraft hanger sized buildings and there are busses to shuttle people around the conference as it takes at least 30 minutes to walk from one side of the conference to the other.  I gave a talk at their "Developer Zone" which was a small stage in one of the huge buildings, with about 30 chairs lined up.  Before I was introduced there was only a few people sitting, although by the time I had introduced myself it was standing room only (and quite a few people very slowly walking past).  I recorded the presentation on a GoPro camera, which did a surprisingly good job of capturing the talk (I believe I used a separate microphone to capture the audio at a good quality). 

[Video: Clojure presentation at CeBit - Germany](){target=_blank .md-button}

## London Clojurians

Clojure dojo events and presentations

ClojureX conference

reClojure conferece

[Article: London Clojurians - a relatively brief history](https://practical.li/blog/posts/london-clojurians-community-a-brief-history/){target=_blank .md-button} 


## Hack The Tower

Hack The Tower was a monthly practical developer event over 5 years, held in the Salesforce offices with food and drink sponsored by Salesforce (the event started in the Salesforce office of Tower 42, moving to the huge space in the Heron tower - eventually renamed to the Salesforce Tower)

??? INFO "Salesforce Tower controversy"
    There was a brief period where people were compliaining about Salesforce renaming the building after a company.

    Ironically, the original Heron tower name came from the Heron company that owned the building.

    The original office space was in Tower 42 which originally was the Nat West Tower, a bank in the UK.  This building is quite unique architecture as the structure was divided vertically into 3 segments, representing the Nat West logo when looing at the buiding from above.  The name was changed when the building was sold, renaming to Tower 42 as there are 42 floors in the building.

After attending a highly enjoyable hack day at the Guardian office in London, organised by Robert Rees, I wanted to do more events like this.

I had recently joined Salesforce (late 2012) and realised I could run a Saturday event from the Salesforce offices as they were not used at the weekend.

I had no idea if people would turn up, so I created the event in the London Salesforce Developers, London Java Community, London Scala User Group and London Clojurians communities.

The event premise was simple: work together to experiment with languages, libraries or even IoT (e.g. robots), learning more than you would do by working alone.

After a few successful events, I started running a Clojure workshop as part of Hack The Tower.  I would find interesting tutorials and libraries and spend the day live coding a Clojure project, with everyone else following on (and occasionally trying other ideas).

Early workshops included setting up a Clojure development environment.  Initially I encouraged the use of LightTable as the editor, as its instant feedback really helped understand if the code was correct as it was being typed.

Once I discovered Spacemacs and added many of the Clojure specific key bindings, I created the Practicalli Spacemacs to help speed up the install setup and give people other options beyond LightTable.

Early versions of the Practicalli books evolved from the lessons learned during these workshops.

[Hack The Tower (Hack Together London)](https://hacktogetherldn.github.io/){target=_blank .md-button} 

[Article: Hack The Tower 2013](https://jr0cket.co.uk/2013/02/hack-tower-february-2013.html){target=_blank .md-button} 


## ClojureBridge London

Organised 12 ClojureBridge London events between 2014 to 2019, introducing Clojure to over 300 women and one extremely talented young girl (accompanied by her very supportive mother).

Approximately half of the women attending were already using a programming language to some extent for work or their own projects.  The rest of the attendees were learning a language for the first time.

One of the most appreciated aspects of the event was the one-to-one ratio of students and mentors (at almost all events).  The equal ratio allowed students to learn at their own pace and learn those aspects that were of most value to them.

The event would not have been successful without the great number of volunteers that provided their own time for free.  All the volunteers learned a great deal too, helping them understand areas they were less clear about and aspects of the language they could spend more time learning more deeply.

[ClojureBridge London Website](https://clojurebridgelondon.github.io){target=_blank .md-button} 

## More workshops

Dev Winter and Dev Summer conferences in Cambridge

Devoxx London 

Clojure and ClojureScript workshops


## 100 Days of Code

After working at Citi managing 6 teams building and deploying Clojure projects between 2017 and 2018, I took a break from commercial work to recharge my batteries and continue my journey into Clojure.

I was inspired by the 100 days of code idea to spend the next 100 days working on Clojure challenges and projects.  Each day I wrote a journal entry to consolidate the lessons learned that day, helping me ingrain the concepts and functions I was learning.

As part of this learning effort I soon started a weekly live broadcast, sharing how to get set up in Clojure and solving Clojure challenges (e.g. 4EverClojure and Exercism) 

After 2 years of live broadcasts I had created over 100 hours of live coding in Clojure.

[YouTube: Learning Clojure with Practicalli](https://www.youtube.com/playlist?list=PLpr9V-R8ZxiDjyU7cQYWOEFBDR1t7t0wv){target=_blank .md-button} 

[Journal: 100 Days Of Clojure Code](https://practical.li/journal/category/100daysofcode/){target=_blank .md-button} 

[Clojurians Slack channel: 100DaysOfCode](https://practical.li/journal/category/100daysofcode/){target=_blank .md-button} 


## Practicalli

Initially using GitBook to self-publish books via GitHub pages, providing a few features to support code syntax highlighting, callouts and other features to help the reader consume the content effectively.

At the end of 2022 all books were migrated to Material for MkDocs which provided a very professional look to the books and even more content presentation features (much better code syntax highlighting, collapseable admonitions, code block line highlighting and annotations) 

## The Future

!!! QUOTE "John Connor, Terminator 3"
    The future has not been written. There is no fate but what we make for ourselves


The future of Practicalli is not written, although as long as I am able I will continue to evolve the content, update supporting projects and code examples.

In 2024 there will be more content on more general aspects of Software Engineering, via the Practicalli Engineering Playbook.

Rather than starting live broadcasts again, time will be made to create high quality screencasts.  Some of these videos will replace the live broadcasts with updated content and others will include new content (clojure workflow with tools, building projects, code challenges, etc).

Once important aspect I would like to challenge is a detailed guide to libraries available in the the Clojureverse.  Whist there are some websites that list some of the libraries available, little or no context about their use and alternatives is provided.

Suggestions as to what content and projects would be useful to the community is always welcome.

Thank you
Johnny.
