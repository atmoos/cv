# Reference Architectures

This is a selection of architectures I was involved in. Either as an architect or lead developer.

## ᛟ Nudge System

Date: 2023  
Role: Lead architect

## ᛟ Expert Cloud System

Date: 2021  
Role: Tech lead & supporting architect

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

This system had been designed and implemented twice before I was given the task to attempt a design an implementation. Very briefly some of the chief concerns I set out to solve:

- Improving structural connascence
  - Partitioning based on sub-domains
  - Temporal decoupling of all sub-domains
- Reducing the code complexity overall
- Improving robustness and reliability
  - This included such simple things as allowing cancellation
  - Well defined error behaviour
