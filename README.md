# Thomas Kägi

- **MSc ETH** in Mechanical Engineering
- 29\. June 1984
- Fluent in German and English
- With Swiss & British citizenship
- Speaker at Basel One 2022 about software quality

I have a nack for enabling people and boosting teams. Product quality will improve and your team members will shine if you add me to one (or many) of your projects. As such I thoroughly enjoy deep dives into hard problems, to then re-surface with a solution that *just works*. I preferably do that around .Net ecosystems, but have proven to be capable on other stacks as well.  
Thanks to my love for quality, my passion for design and my sixth sense for detecting issues, I consider myself a productive software engineer as well as a talented emerging architect.

In my current position as *Subject Matter Expert Technical Quality* I promote engineering excellence by organising internal meetup events about technology, and software design & engineering practices. I enjoy establishing similar formats when working for client projects.

ToDo: Add GPG key, "Suche keine rolle, sondern eine Aufgabe."

***Contact:*** [github](https://github.com/atmoos), [TEL & EMAIL], [linkedin](https://www.linkedin.com/in/thomas-k%C3%A4gi-46410a141/)

## Projects

Most projects I've worked for revolved around the .Net ecosystem, which is where I am naturally most comfortable. However, I enjoy challenges as well as stepping out of my comfort zone every so often. As such, I've enjoyed working for a broad variety of target environments and architectures, be those

- Plugin development, for
  - *WPF* desktop engineering apps
  - medical instruments running customised Linux versions
  - including the use of [ONNX](https://onnx.ai/) ML models.
- Containerised event based architectures
  - *RabbitMQ* & *Docker*
- Test automation frameworks
  - python & [squish](https://www.qt.io/product/quality-assurance/squish)
  - Gherkin BDD
- Distributed systems in the (*Azure*) cloud
  - *Event Hub*, *Service Bus*, *Stream Analytics*, *Blob Storage* & *Cosmos DB*
  - Azure *Web Apps* (*Angular*) and *Functions*
- *Electron* based desktop apps
  - *Vue.js* & *ASP.Net* (Core)
- Service based architectures for desktop apps
  - WPF, [ZeroC ICE](https://zeroc.com/ice) & *MS SQL* (2012)
- Versioning & deployment
  - preferably `git` repos
  - nuget package management
  - Azure pipelines
  - github actions
- Quality & architecture monitoring
  - Sonar Qube
  - [ndepend](https://www.ndepend.com/)
  - Roslyn

```mermaid
flowchart TD
  foo --- bar
```

### Subject Matter Expert - Consulting Services

3\.2023 - 2\.2024 @ **ERNI AG** Manila, Philippines & Singapore

***On architecture:*** High level cloud architectures ([C4)](https://c4model.com/) & heading an architecture book club.

Due to my track record of improving quality in projects, I was sent to our subsidiary in Manila as a cultural bridge and ambassador of quality. We chose to set a focus on improving processes revolving around sales activities.

Additionally, I lead the (technical) design phase of multiple solutions aimed at the local market as well as supporting the sales team during client visits in the Philippines and Singapore.

***Technology:*** Azure Cloud, .Net, Maui & Xamarin, [BLE](https://en.wikipedia.org/wiki/Bluetooth_Low_Energy)

### Tech Lead & Architect - Medical Industry

10\.2021 - 2\.2023 @ **ERNI AG** for a client in Rotkreuz, Switzerland

***Architecture:*** Microkernel architecture embedded in an event-driven system.

As a tech lead and architect I was an integral part in implementing cutting edge diagnostic instrument workflows. Technical lead of a full stack team developing an electron maintenance app. Complete re-write of a generalised ML algorithm instrument plugin using [ONNX](https://onnx.ai/) model. Also, I designed and lead the sw-development of a new plugin for the newest diagnostic instrument.

***Technology:*** RabbitMQ, Docker, Asp.Net (core), electron, Vue.js, ONNX

### Architect & Senior Engineer - Medical Industry

9\.2020 - 9\.2021 @ **ERNI AG** for a client in Rotkreuz, Switzerland

***Architecture:*** Event based architecture with a broker topology

Supporting architect of an expert system cloud solution used to analyse and detect anomalies in the runtime data of various diagnostic instruments.

Lead a small team of developers implement new features. Analysed and fixed various performance bottlenecks caused by implementation mishaps through to non-optimal design.

***Technology:*** Azure Cloud, .Net, Asp.Net (core), Specflow, MSTest

### Tech Lead & Senior Engineer - Medical Industry

10\.2019 - 8\.2020 @ **ERNI AG** for a client in Rotkreuz, Switzerland

***Architecture:*** Embedded in an event driven (mediator) architecture, implemented based around a command pattern.

Developer and development architect on the service software component for a high precision med-tech instrument. Improvement of core components and features (cancellation), aiding the team in design decisions and leading team members technically. Drive and support the transition from WPF to WebApp.

***Technology:*** RabbitMQ, Docker, .Net, WPF, Specflow, MSTest

### Product Owner - Manufacturing Industry

10\.2018 - 4\.2019 @ **ERNI AG** for a client in Thun, Switzerland

***Architecture:*** Service based translation layer.

I acted as co-designer and product owner for a project done in collaboration with a shoring team in in Bratislava. The service's primary task is to serve as a stateless translation layer (wrapper) for a COM API that is exposed as an XML based protocol.

***Technology:*** XML protocol over TCP/IP, COM API, .NET (core & Framework)

### SW-Engineer - Manufacturing Industry

3\.2018 - 3\.2019 @ **ERNI AG** for a client in Thun, Switzerland

***Architecture:*** Layered test architecture.

Support the team transitioning form auto-generated, but brittle and slow end-to-end tests, to more stable BDD tests that reflected requirements.

I improved robustness of a partially built internal framework by eliminating crashes and false positives, as well as improving performance form 5h runtime down to 2h.

***Technology:*** Squish, Gherkin, python 3, Jenkins CI, SVN

### SW-Engineer - Electronics Industry

1\.2016 - 2\.2018 @ **Sensirion AG** Stäfa, Switzerland

***Architecture:*** Event based architecture using the mediator topology,later evolving into microservices.

The core task was to build a control and monitoring software (desktop app) for a multi slot robotic sensor calibration system. Two unsuccessful attempts had been made previously. By decoupling components and simplifying designs and interfaces, my approach lead to success.

Tactics for success:

- Strict application of [SOLID](https://en.wikipedia.org/wiki/SOLID) principles
- Temporal and logical decoupling of processors
- Simplification of design, leading to:
  - New internally widely adopted command pattern implementation
  - Separately testable components

***Technology:*** .Net Framework, WPF, Beckhoff [PLC](https://en.wikipedia.org/wiki/Programmable_logic_controller), Sockets

### Mechanical Engineer - Robotics ETH Start-Up

1\.2015 - 6\.2015 @ *Rapyuta Robotics AG* Zürich, Switzerland

I began work there as one of the first employees. The main task was to integrate mechanical
components into their solution. Furthermore, I implemented the calibration algorithm and test
set-up used to parametrise transformation matrices used to compensate raw sensor data.
Other tasks included: Development of a test bed for electric propulsion motors, evaluation and
acquisition of electric motors and evaluation of suppliers for carbon fibre based components.

***Technology:*** python, C++, [ROS](https://www.ros.org/)

### Junior SW-Engineer - Electronics Industry

3\.2013 - 12\.2014 @ **Sensirion AG** Stäfa, Switzerland

***Architecture:*** Layered architecture with RPC using ZeroC's ICE

My first job as a sw engineer. I designed a transparently parralelisable wrapper implementation of the RPC API targeting the firmware implementation of a calibration unit.

***Technology:*** .Net Framework, [ZeroC ICE](https://zeroc.com/ice)

### Practical Trainings

8\.2012 - 2\.2013 Internship @ **Sensirion AG**, Stäfa, Switzerland

8\.2000 - 8\.2004 Apprenticeship @ **LCA Automation AG**, Affoltern a.A., Switzerland

## Consulting

Since May 2019 for **ERNI AG**

During my time at **ERNI AG** I was involved in numerous consulting mandates. These typically involve my capability of quickly analysing a situation on a high level, understanding the status quo, identifying areas of interest (typically issues) and then coming up with viable ideas and solutions for the next steps. This has worked well irrespective of the technologies involved.

- Client meetings in **Metro-Manila, Philippines** and **Singapore**
  - Consulting for regular cloud applications
    - Including performance reviews
  - Consulting for AI/ML solutions embedded in medical and manufacturing environments
  - *Design Thinking* workshop for a multi-domain manufacturer
  - Cultural trainings bridging CH with PH
- Architecting a UI test framework using [Squish](https://www.qt.io/product/quality-assurance/squish) by Qt for a cpp solution, **Rotkreuz**
  - The test framework was to be implemented using python
- Review and design extension of a solution based on a broker architecture, **Schlieren**
  - Workflow management system using [Camunda](https://camunda.com/)
  - The broker orchestrates interaction between Camunda workflows and python processor scripts
- Code review of
  - service based system with focus on performance, **Zürich**
  - monolithic Xamarin application with focus on quality, **Zürich**
- Knowledge transfer process set-up for a near shoring team, **Bratislava, Slovakia**
- XML code-gen solution review and PoC, **Zollikofen**

## Software Engineering Passion

I use my passion in software engineering to connect components and technologies in a robust and maintainable fashion. This is supported by my love of also connecting people and teams and their respective expertise.

### Architecture

- Projects at EPH
- Experience in the industry
- Leading through book club sessions at EPH on FoSA

I am familiar with following architectures:

### Software Engineering

- My team abilities
- Analytic skills
- Mention tools only in a side note and stress importance of "portability" and openness.
  - VSCode, Draw.io, .editorconfig, etc
  - Don't want a "locked in" situation
  - Developers know best how they are most productive

### My Own SWE Projects

I just love exploring new ideas and technology, which leads me to regularly embark on technological adventures. Out of these many projects, I'd like to mention on the project that is most mature: [Quantities](https://github.com/atmoos/Quantities).

It is a .Net library to efficiently and safely handle physical quantities. A small code sample is possibly most illustrative:

```csharp
Time duration = Time.Of(2, Metric<Hour>()); // 2 h
Length kilometres = Length.Of(4, Si<Kilo, Metre>()); // 4 km
Length miles = kilometres.To(Imperial<Mile>()); // 2.4854 mi

Velocity slow = kilometres / duration; // 4 km/h

// (4km == 2.4854 mi)? --> true
Console.WriteLine($"({kilometres} == {miles})? -> {kilometres == miles}");
```

## Other Passions

- Avid sailor
- Dancer in training
- Keen traveller and hiker
- Baking sourdough bread
- Single board computers
  - [keeping nanosecond time](https://www.ntppool.org/scores/84.254.80.94)
  - [blocking adds](https://pi-hole.net/) on my home network
  - [providing VPN](https://www.wireguard.com/) services
