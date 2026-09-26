# Main Notification System

## Problem Statement
* design a scalable notification system that alerts users with time sensitive information: 
    1. breaking news, 
    2. event reminders. 
    3. order updates


## What are the initial questions to ask so we can define the functional and non-functional requirements
> What is news feed? what does a news feed service do?
* seems to me a well defined service by META.  
* Constantly updating list of stories in the middle of your homepage
* includes status update
* photo/video/links/likes from ppl, groups that you follow on FB

* who are the users that would install the system
* who are the end users that would use the system
* What's the expected num of users or TPS into the system


## Similar questions
* Twitter timeline
* instsgram

## Key Concepts
* from monolithic setup -> decoupled, highly reliable distributed architecture

> multi-channel notification eco-system
* contact info and Data Modeling
* decoupled architecture and scalability
* Reliability and delivery guarantees
* System Control and User Preferences
* Security, Monitoring and Tracking

## Functional Requirements
* Notification Channels
    * mobile push notifications
    * SMS msg
    * email
* supported devises
    * IOS
    * Android
    * laptop/desktop
* notification triggers
    * by client application
    * scheduled from server side

* User preferences
    * users can opt-out or manage their settings and not receiving notifications

## Non-Functional Requirements
* Daily Vol and throughput
    * 10 MM push notifications
    * 5 MM emails
    * 1 MM SMS MSGs

* Latency
    * soft realtime system
    
* Reliability
    * delay is okay
    * data loss is unacceptable

## Questions
* how was the article evolving from monolithic design to distributed design?