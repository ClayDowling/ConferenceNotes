---
title: "Nebraska Code Notes"
---

* Table of Contents
{:toc}

# Functional Programming & the Path to Zen

Brian Newton

What makes a productive programming environment?

 - Low unnecessary friction
   - Remove as much ceremony as possible
   - All friction should pay for itself
   - Terse and expressive language
 - Low context switching
   - Reduce frequency & cost
 - Automated error detection
   - Strong typing
   - Automated testing
 - Code Should Be Predictable
   - Should be able to predict what code will do by looking at it.
   - Prediction should be correct after changing other parts of the code.
 
Why Functional Programming
  - It encourages a productive programming environment.
  - Emphasis of modularity via composition of functions & data
  
How Does Functional Programming Facilitate this?
 - Fist Class Functions
   - Partial function application
   - Function composition
   - Transforming functions: take a function as an argument to another function
     to change its behavior. 
   - Pipelining: Output of one function is used as the input to the last
     parameter of the next function in the pipeline.  Looks closer to a fluent
     interface, unrolls nested calls so your code doesn't look like lisp.
 - Immutability
   - Avoiding shared mutable state
   - Pure functions - no side effects

 - Discriminated Unions
   - Fast type building.
     type Shape = 
       | Rectangle of int * int
       | Square of int
       | Circle of int

 - Pattern matching.  Wasn't entirely clear how this worked, needs further
   exploration but good potential for fast results.

 - Check out type providers, units of measure.

## Resources
 - Schott Wlaschin
   - F# FOr fun and Profit - F# Blog
   - Domain Modeling Made Functional

 - FSharp.org

 Slides:  https://bnewt.gitlab.io/functional-programming-zen

# Kotlin

Erik Shafer: @faelor / erikshafer on github

Features:
  - Concise
  - Expressive
  - Functional
  - Null Safety
  - Interoperability
  - Multi-Platform

Variable Declarations
  val - read only
  var - mutable variabl e

  var myVariable: Array<String> ?
  mutalbe, nullable array of strings

Kotlin:

  val f = {x: String -> "Value: $x"}
  f("blah")

Java:

  Function<String, String> f = x -> "Value: " + x;
  f.apply(t:"blah");


Class declarationsl:

  class Book {
    var name: String
    var athor: String?

    constructor(name: String, author: String?) {
      this.name = name
      this.author = author
    }
  }

or

  class Book(var name: String, author: String?)

## Default Arguments

  class Book(val name: String = "Hitch Hiker's Guide",
             val author: String = "D. Adams")

  val myBook = Book(author = "Adams, Douglas")

## Null Safety:

If something can be null, the compiler will not be having any attempt to deal with potentially nullable stuff without you taking precautions.

## Data Classes

Identifying a class as a data class (with keyword), automatic generation of
equals, hashCode, toString, copy operators.

## Class Declarations

A simple object with read only brand and expiration properties:

  class AppleSauce(val brand: String, val expiration: Date)

  data class Movee(val name: String, val runTime: Int, val genre: String = "Humdram")

  fun convertGenre(movee: Movee): String = when(movee.genre) {
      "Comedy" -> "CMD"
      "Action" -> "ACT"
      else -> throw IllegalArgumentException("Not an acceptable format")
    }
  }

  fun main(args: Array<String>) {
    val m1 = Movee("Star Wars", 110)
    val m2 = Movee("Office Space", 97, "Comedy")
    val m3 = Movee(runtime = 136, name = "The Matrix", genre="Action")

    var message = 
    if (m1 == m2) {
      "equals"
    } else {
      "nope"
    }
    println(message)

    println(convertGenre(m3))
  }

## Class Extension

Similar to C# partial classes, but does not require that the original class declare
itself as partial.

# Facilitation for All

Jess Osborn

Why Are Facilitartors Important?
  - They listen.  Help guide the conversation
  - They know your objectives
    - What is the outcome?  From single meeting to complex multi-day event.
    - Set the Stage
  - Assign Takeaways
  - Send out notes and decisions.

Tips and Techniques
  - Time Box - sets constraints and keeps it respectful of participants' time.
  - Silent Brainstorming
    - Good for introverts and extroverts
    - Can help get the good ideas, not just the loud ones.
  - Silence
    - Gives time for people to gather thoughts, maybe say something they were not going to.
  - Parking lots: Helps effectively deal with distracting but non-agenda items
    that arise during the course of a meeting.  Park it and save it for
    something that can be addressed later.
  - Ground Rules
    - Let everyone participate
    - Listen with an open mind
    - Be respectful
    - Can be a living document
  - Know Your Audience
    - Technical vs Non-technical
    - CEO vs Entry level employees
    - Are they the right people in the room?
    - Who doesn't need to be there?
  - Room Considerations
    - Web cam
    - Phone
    - TV/Projector
    - Whiteboard?
  - Supplies
    - Sticky Notes
    - Sharpies
    - Pipe Cleaners
    - Whiteboard Markers
  - Consensus Voting
    - Dot Voting
    - Roman Voting (up/down)
    - Fist of Five - 5: Great idea, 4: Good, 3: Neutral, 2: Don't Like, 1: This
      will probably kill the project/team
  - Agenda
    - send one if you can
    - helps people decide if they need to be there
    - gives a heads up on discussion
    - doesn't need to be rigid, better to allow flexibility
  - Take notes
    - May need to delegate this.
    - Record decisions, action items & parking lot items.
  - Recap at end of the meeting.  Ensures everyone has a clear understanding of
    the outcome and takeaways.  Confirm that everyone agrees with this recap.

# Introduction to Jewelbots

@LIKEOMGITSFEDAY
#CodingWithJewelBots

Programs for getting people into coding:

  Coder Dojo
  Coding & Cupcakes: Gets people to get their daughters involved
  Coding & Cocktails: Gets people to get the moms involved

Why aren't girls jumping into coding?
  - Psychological Barriers
  - Lack of encoragement & role models


What got her into coding?  Social networks & tools that encouraged self
expression via customizing pages.

New social media doesn't offer opportunities for customization, focus on consumption.


## Psychological Barriers
  - We tell kids who are on task that they're "so smart" rather than an
    emphasis on effort.  Girls tend to be more on task as kids, so no
    association with effort, just something they have innately.  Boys wouldn't
    recognize a task if it bit them, continually coached to give more effort,
    so associate success with effort.
  - Lack of role models in the business.
  - Girls are scrutinized for appearance almost from birth.

## How to Help
  - Exposure to opportunities - yay Jewelbots
  - Positive Reinforcement - encourage hard work & perseverance
  - More Female Role Models
  - Have her wardrobe reflect her empowerment

## Simone Giertz

"The Queen of Shitty Robots" or "Queen of the Most Wonderfully Craptasti Machines"

## What Are Jewelbots

Friendship bracelets for the iPhone era.  Bluetooth enabled.  Programable.

Created by Sara Chipps (Girl Develop It), Brooke Moreland

### Features

 - Arduino compatible, 
 - Organized around social coding.
 - Forum community for support and ideas
 - Open Source

 - Need jewelbots board manager from github

## Jennifer's Rules of Mentoring

- Keep your hands off the keyboard.  Strong pair only.
- Let them make mistakes.
- Don't give here the answer, help her find it.
- Teach her how to read the docs.
- Help her create diagrams of her ideas.
- Be patient.


## Workshop Success

- Pre-workshop: Make technical requirements known - laptop with admin rights to
  download, wifi, usb port.
- Prep your mentors with guide + debugging tips.
- Communicate goals of the workshop - explain the "what" & "why."
- Installing boards may take 10-15 minutes.
- Be prepared for different learning speeds.
- Have a guide/curriculum strategy prepared.
- Have follow up resources ready - encourage joining Jewelbots community.
- Expect some chaos .. and have a blast!

## Ongoing Learning Resources

- Jewelbots Forums
- STEM Subscripttion boxes
- Little Bits

"codewithJennifer" for $20 off JewelBots

Slides at tehfedaykin.github.io/CodingWithJewelbots


# The Trials and Tribulations of Fully Remote Teams

[Mike Cole](http://colemike.com) @colemike

Problems early on:  Isolation, Guilt, Confusion, Paranoia, Imposter Syndrome,
Work-Life Balanced.

New Challenges: Dedicating full attention to meetings, Time Zones, Effective
communication over IM (no mannerisms, facial expressions, sarcasm detection).

Common Problems:
  Distractions
  No Collaboration
  Isolation
  Disconnect from Company Culture
  Times Zones.  Low Quality Communication Platform
  Missing Small Talk

Upsides:
- No geographical restrictions, work with your pets, very casual dress code.
- Safe and sound at home.  Work with different personalities
- Healthy cheap lunches
- Work on the road
- Less wear and tear on vehicles
- I control the thermostat
- Lunch naps

## Tips for Remote Employees

Have your own dedicated workspace where you will not be interrupted and where
you can close your door at the end of the day.

Have a shut down ritual to help you transition back to "after work" time.
- Shut down your machine
- Walk around the block
- Dress down

Do you really need your company's email or IM on your phone?

Be structured about your work schedule.  Don't unintentionally get into a place
where near the end of the day you have to finish your 8 hours.

Splurge on nice office furniture.

Upgrade your internet plan and home networking gear.

Make your office space yours.

Look for opportunities to be included.

Commit frequently.

Exercise.

Have a separate workstation for personal use.

Have explicit buy-in with family/roommates
  - Explicitly request their buy in.
  - Set limits and expectations.

That Dog Probem...

Stuff will happen:
  - Your dog will bark
  - Your internet will go down
  - Your PC will blue screen
  - You will take TV breaks
  - You will miss calls
  - Your router will die

Depression is real and dangereous
  - Isolation
  - Lack of belonging
  - Lack of purpose
  - Widthdrawal from social events

Depression Cures:
  - Get out
  - Meet up with other people who do what you do


## Tips for Remote Employers

If one person is remote, everybody is remote.

If you don't feel this way, your remote employees are feeling left out.

Buy everybody nice headsets and webcams.  Give easy access to your meeting software.

Have an onboarding plan in place.

Have a "mentor" in place to establish rapport with remote employees.

Don't stop at "Open Door Policy" - actively seek to engage.  Communication must
be deliberate.

Look for excuses to get the team together in person to bond (include team leads/managers).
  - In office visits
  - Holiday parties
  - Retreats - Not a rave, not a work day
  - Conferences
  - Evereybody visit a co-worker's location

Have remote alternatives to local-only perks (food, fun days, gym memberships).

Establish and respect "quiet hours" for your remote devs.

Make your remote workers feel they belong, or they will feel like contractors with benefits.

Remote: Office Not Required - book on working remote

http://hanselman.com for more information on working remote.


If you want to try this:

 1. Define your career goals
 1. Decide on how often you'd like to work from the office
 1. Research a potential employer: are they remote-friendly or remote-first?

Job Sites:

careers.stackoverflow.com
weworkremotely.com
remoteok.io
workingnomads.co


# Using Async/Await in C# As Designed

[Keith Voels](mailto:keithvoels@gmail.com)

https://github.com/keithdv/AsyncAwaitAsDesigned for code samples

See also "The zen of async: Best practices for gest performance" on youtube,
from Microsoft Tech Ed

## Why Use It?
- Prevent UI blocking in client application
- Provides significant performance gains running server-side code by reducing thread contention.
- A blocked thread will go find something else to execute
- Thread launching is fairly expensive, so reducing the number of threads which
  need launching will boost performance.

## Task-Based Asynchronouos Programming (TAP)

- A task represents the initiation and completion of an asynchronous operation
- Delegate + Execution = Task

Delegates
  - Delegate
  - ContinueWith

Execution
  - Status
  - Exception
  - Task<T>.Result
  - Execution Context (Hidden)

Async/Await are keywords.  They make the code look synchronous, but they tell
the compiler that when the thread blocks here to go run other code.  This means
we don't need a thread for every task, and it will be created only as needed by
the Thread Pool.  This can probably greatly reduce the cost of running our code.

## Understanding Execution Context, SynchronizationContext and ConfigureAwait - TAP Challenges

- Thread Local Storage is out.  Because my task will run in multiple threads.
  Code can/will start running with the wrong data.
- Saving data to  ExecutionContext (property on Task) means it will always be
  present for the task.  This keeps data storage in the heap, rather than a
  thread task.
- SynchronizationContext: a place to store data for tasks using non thread safe
  features (e.g. UI).  Queues work to run in the UI thread (or whatever thread
  the task is associated with).
 
  When we await something on a SyncrhonizationContext, we've added ourselves to
  the queue of work and when it comes around we'll get run.

async void - looses exceptions, which are put onto the instance of a Task normally.

Variables with AsyncLocal<> decorator live in the correct Task.  They are
automatically added to the ExecutionContext.

ConfigureAwait(false) tells scheduler that a task which was awaiting on the
SynchronousContext can now run on any other thread to be completed.  Relieves
deadlocks.  Don't do this when actually updating a UI.

## Task Window

Monitors all tasks which have been created, and their current run/wait status.
Clicking on a task will show you where it was created in the code.

TaskCompletionSource - Gives a handle to put myself into the thread scheduler
without blocking thread.  Requires more research.

# GitHub Pages: A Platform for Cheapskates

Mike Cole @colemike

Note: These notes are actually hosted on GitHub Pages

Third Party Bits:
- Disqus
- FormSpree
- SnipCart

More advanced setups:
- CloudCannon
- Netlify

Data feature allows us to use liquid filters to serve data up in structured
ways that function like read-only REST servers.

# Package All The Things

Hyperpolyglot.org - Great resource for figuring out how to get stuff from one language to another.

