# Reference Architectures

This is a selection of architectures I was involved in. Either as an architect or lead developer.

**Note**: All diagrams follow [C4](https://c4model.com/). However, to keep this document reasonably short, I chose to not follow it exactly and sometimes mix (abstraction) layers.

## ᛟ Messaging System

Date: 2023  
Role: Architect

### Topology

Event based serverless messaging system.

![Messaging system topology](./assets/MessagingSystem.webp "Message System")

This C4-Context diagram was laid out by myself and the lead developer & project architect at the project start. He then further detailed the container diagram of the resulting ecosystem.

### Challenges

Thanks to our expert developers and outstanding team work the realisation of this system went very smoothly. The most interesting challenge occurred after the first deployment.

Every morning each user (out of many hundreds denoted $u$) receives on average $\mu$ ML generated messages out of a total of $m$ messages. It was required that each user receives the messages at the same time early in the morning. The initial implementation took about **two hours** to send all messages, clearly not meeting the requirements.  
After some careful inspection it was identified that the messaging dispersal "algorithms" was implemented in $O(u \cdot \mu + m)$ time complexity and that the associated azure functions (incl. durable functions) were running into timeouts.  
Careful analysis showed that some parts could be effectively parallelised and, most importantly, the algorithm could be implemented in $O(u + m)$ time complexity.

This change doesn't seem that relevant. However, it turned out to be a significant improvement. The average runtime was reduced to a mere **four seconds** after boing deployed!

**Note**: This level of speed-up may indicate that there was more going on than "just" suboptimal complexity. I can no longer prove it, but there may have been some saturation in the service bus happening or scaling-out limits of Azure functions being reached.

## ᛟ Expert Cloud System

Date: 2021  
Role: Tech lead & supporting architect

### Topology

Event based architecture based on a broker topology & relying on eventual consistency.

**Note**: This was *not my design*. I include it as it was a project most influential in my journey to becoming an architect. The depiction of the system has been greatly simplified as well as names intentionally left vague. This is to protect the former clients IP.

![Expert system topology](./assets/ExpertSystem.webp "Expert System")

Conceptual notes:

- the service bus is responsible for relaying the majority of messages
- the web app actually consists of two apps, each with
  - Angular frontend with ASP.Net core backend
  - REST API defined in Swagger
- Some "trigger-connections" have been omitted for brevity

### Challenges

The design proved to be very capable and also able to evolve over time. I was mostly involved with changes to "sub-designs" or in-depth problem analysis.

- Design and realization of ambulance cloud pattern with lead architect
- Fixing memory issues in "Data Extraction"
  - Space complexity from $O(n) \to O(1)$
- Fixing performance bottlenecks
  - CosmosDB specialities and overly hasty implementations caused significant slowdown
- *Unsolved* issue of conceptually not knowing when stream analytics completes. (Akin to the halting problem?)
  - We knew when anomalies where found, but
  - *not* when none were found.

## ᛟ Sensor Calibration System

Date: 2018  
Role: Architect & lead developer

### Topology

Event based architecture using a mediator topology. All communication is asynchronous and bi-directional.

![Calibration software topology](./assets/CalibrationControl.webp "Calibration System")

Everything within the "Control Software" box was designed by myself. The calibration processes were designed by process engineers, where I chose to realise them using a very simple variation of the command pattern that I designed myself. However, I had a lot of help by a team member implementing the calibration processes.

#### Some Caveats

For historical reasons, this system had been developed as a monolith. Hence, the all the blue boxes really are C4-components. However after first deployment it was quickly realised that we'd be running into many of the issues associated with monoliths.  
I had prepared the system in such a way that it in principle could be broken apart and be separated out into C4-containers.

This was later achieved between one to two years later by my successor.

### Challenges

This system had been designed and implemented twice before I was given the task. Very briefly some of the chief design concerns I set out to solve:

- Improving structural connascence
  - Partitioning based on sub-domains
  - Temporal decoupling of all sub-domains
- Reducing the code complexity overall
- Improving robustness and reliability
  - This included such simple things as allowing for cancellation
  - Well defined error behaviour
- Paving the way for a distributed system
  - possibly using a message broker such as RabbitMQ or Apache Kafka
