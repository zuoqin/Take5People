- title : Take 5 People projects
- description : My daily achievements @Take5People
- author : Alexey Zorchenkov
- theme : night
- transition : default

***

### March 28th, 2016

#### Problem

- Client complain that leave application data, such as dates, leave hours, etc... takes a lot of time
- After investigation I found that Leave Data table OnUpdate triggers takes considerable time to execute
- Key issue is that each time user updates leave data, system needs to recalculate leave balances, as well as other data

---

#### Current System Synchronous workflow

![Synchronous](images/synchronous.png)

---

#### Solution

- Take5People implements Service Broker services, which is part of SQL Server 2008 and above
- Complicated calculation logic, which was part of Database Leave Detail Table OnUpdate Trigger will move to independent Stored Procedure
-- SQL Server will asynchroniously call given stored procedure when a new update message arrives


---

#### Next generation system workflow

![Asynchronous](images/asynchronous.png)

---


***

### March 29th, 2016

![Reactive Manifesto](images/responsive-manifesto.svg)

***

### WebSharper

- More productive with less code
- A fundamentally different web framework for developing functional and reactive .NET applications
- Markup-driven, strongly-typed reactive applications in minutes

***


### AKKA

- Scalable, distributed real-time transaction processing
- Fault Tolerance
- Location Transparency
- Persistence

***


### Heroku

- Heroku is a platform as a service (PaaS) 

![Heroku](images/heroku.png)

---
- id : Heroku-1

#### Cloud

- enables developers to build and run applications entirely in the cloud
- it’s the best platform for building with modern architectures, innovating quickly, and scaling precisely to meet demand

![Heroku Cloud](images/startup.png)

---

- id : Heroku-2

#### Focus

- Heroku handles the hard stuff — patching and upgrading, 24/7 ops and security, build systems, failovers, and more — so your developers can stay focussed on building great apps

![Heroku Support](images/focus.png)

---

- id : Heroku-3

#### Ecosystem

- Powerful platform, unparalleled ecosystem
- it’s the best platform for building with modern architectures, innovating quickly, and scaling precisely to meet demand

![Heroku Architecture](images/ecosystem.png)

---

- id : Heroku-4

#### Applications


- Today every company needs apps to engage their customers and run their businesses. Step up your ability to build, manage, and deploy great apps at scale with Heroku.

![Heroku Applications](images/apps.png)

---

***


### System Workflow

![System Workflow](images/workflow.png)

***

### The Reality of a Developer's Life 

**When I show my boss that I've fixed a bug:**
  
![When I show my boss that I've fixed a bug](http://www.topito.com/wp-content/uploads/2013/01/code-07.gif)
  
**When your regular expression returns what you expect:**
  
![When your regular expression returns what you expect](http://www.topito.com/wp-content/uploads/2013/01/code-03.gif)
  
*from [The Reality of a Developer's Life - in GIFs, Of Course](http://server.dzone.com/articles/reality-developers-life-gifs)*

