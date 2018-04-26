---
title: "Indy.Code() 2018 - Day 2"
---

# Making the Most of Working With Dot Net Core

Dave Rael - Host of the *Developer On Fire* podcast.
[http://github.com/raelyard/KnowYourToolsNetCore]

This session was a sort of high-level overview of the dot net core ecosystem.
I did not find a large amount of material here that I thought was new
information for our team.  A couple of packages worth noting:

Chocolatey - package manager for Windows.  Most of us probably already have this installed.

Boxstarter - tool for configuring a development environment using Chocolatey.

Machine.Specification - Another BDD style testing framework.

ShouldBy - An assertion library which works with XUnit and Machine.Specification

# Continuous Deployment with IoT

Presenter: @ericlandes

Eric introduced a new concept to me: Canary Build.  This is a build with some
features turned on via feature toggle.  Used as a way to trial new features to
a smaller group of users.

VSTS - A Blue-Green deplloy is called a slotted deployment in VSTS land.

Azure has a provisioning service for something called IoT Hub

Most of the rest of this talk covered topics familiar to anyone who has used a
continuous integration and continuous deployment system.

# Always Start With a Deadline

Presenter: Virginie Adams @adamsva05

Given the variables Scope (MVP), Time (Deadlines) and Cost (Team Funding), at least one of these must be fixed.

Fixed Scope: Project managers love this.  Fetures can be specified very clearly, progress tracked and predictions made.

Fixed Cost: two possible scenarios.
  * Timeline is really too far out to make a reasonable estimate.
  * Scope reduction to fit budget causes project to be cancelled.

Fixed Time: Focuses priorities.

How to pick a deadline:
 * Do you need to beat someone to market?
 * Have you done something similar?
 * Do you have resource constraints?
 * Is this a good time for the business?

Having a fixed deadline provides a franme of reference feor fixing either scope or cost.

To make it work, think iteratively: what is the smallest happy path?
Use this constraint to adjust variables accordingly.  Repeat until  you get something you can work with.

Important Factor: other groups will need to coordinate with you in order to make the project successful.

*Why Deadline Is Important:* Customer faith is lost by a lack of delivery.

Think of a realistic deadline with meaning.

Understand your cost (team size)

Find Your MVP

Analyze & create your plan.

Retrospect and adjust.
