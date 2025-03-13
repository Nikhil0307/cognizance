---
title: "DDD: Designing_systems"
date: "2025-03-12"
tags:
  - "Designing_systems"
  - "DDD"
---

Domain Driven Architecture
Basically this architecture is composed of 3 layers: 
- Domain 🧊
	- The domain layer defines the data structures in plain python objects: The business objects
	- This layer doesn't depend on any other layer
- Application 🧑‍💻
	- This layer holds the Engine of the Application : The business logic
- Infrastructure 🎑
	- This layer will be the tyres of the application, which interacts with the external world(simply interacting with other services -- API, DB, Files, etc.)
- did we miss dependency injection ?? 🤔
