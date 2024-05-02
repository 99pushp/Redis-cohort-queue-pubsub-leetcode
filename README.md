# Redis-cohort-queue-pubsub-leetcode
This contains code for the leetcode like pub-sub basic implementation

# LeetCode-like Platform Architecture README

Welcome to the README for a LeetCode-like platform architecture! This document provides an overview of the system's architecture, highlighting key components and their functionalities. Let's dive in!

# Overview

This system is designed to handle code submissions from users for various coding problems. It ensures seamless processing of code submissions and real-time notifications to users.

# Components

1. Client (Browser/Postman)
Description: Initiates code submission requests.
Functionality: Sends data including code, problem ID, and language in the body of a POST request.
3. Primary Backend Server Node
Description: Central server handling incoming requests.
Functionality:
Receives requests from clients.
Enqueues requests in Redis for efficient task management.
4. Redis Queue
Description: In-memory data structure store.
Functionality:
Acts as a queue for incoming code submission requests.
Ensures efficient handling and scalability.
5. Worker Instances
Description: Multiple instances responsible for processing code submissions.
Functionality:
Pull requests from the Redis queue.
Process code submissions efficiently.
6. Web Socket Server
Description: Facilitates real-time communication with clients.
Functionality:
Receives events from worker instances.
Sends real-time notifications to subscribed users via web sockets.

# Workflow

Code Submission: Clients submit code, problem ID, and language through a POST request.

Request Handling: The primary backend server receives the request and enqueues it in Redis.

Processing: Worker instances pull requests from the Redis queue and process code submissions.

Real-time Notifications: Upon processing completion, events are published to the web socket server.

User Notifications: Subscribed users receive real-time notifications in their browsers.

# Technologies Used

Node.js: Powers the backend server and worker instances.

Redis: Used as a queue for task management.

Web Sockets: Facilitates real-time communication with clients.

Express.js: Framework for building the backend server.

Postman: Testing tool for API endpoints.

Getting Started

# To set up and run this system locally, follow these steps:

Clone the repository.

Install Node.js and Redis.

Start Redis server.

Install dependencies using npm install.

Run the server using npm start.

Test code submission functionality using Postman.

