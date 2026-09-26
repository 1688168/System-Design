# Main Notification System

## Key Concepts
* from monolithic setup -> decoupled, highly reliable distributed architecture

> multi-channel notification eco-system
* contact info and Data Modeling
* decoupled architecture and scalability
* Reliability and delivery guarantees
* System Control and User Preferences
* Security, Monitoring and Tracking

## Problem Statement
* design a scalable notification system that alerts users with time sensitive information: 
    1. breaking news, 
    2. event reminders. 
    3. order updates

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