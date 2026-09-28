# Fully Autonomous Initial Mars Colony

*How robots, and eventually artificial minds, could build a working Mars outpost and prove it ready for people before the first person arrives.*

*Last reviewed: September 28, 2026*

Every plan to settle Mars meets the same wall. Mars is between 3 and 22 light-minutes away. For about two weeks every 26 months the Sun sits between the two planets and Earth stops sending commands, and Martian dust storms can dim the sky for months. People who land there need air, water, power, shelter, and a way home on the first day, not after the first decade.

This book describes a different order of operations. Machines go first. Three waves of cargo landers, launched in the 2035, 2037, and 2039 windows, deliver reactors, water wells, oxygen and propellant plants, habitat shells, greenhouses, and a robotic workforce. That workforce, coordinated by a site intelligence called the Orchestrator, builds the outpost and runs it through dust storms and communication gaps without instructions from Earth. The first crew leaves Earth only after the colony has shown, for more than a year, that it can keep them alive and send them home.

Two kinds of limit remain. Several steps the plan depends on have not yet been demonstrated: ship-to-ship refueling in Earth orbit, landing 100 t-class cargo on Mars, a 100 kWe-class fission reactor qualified for Mars (none has been built), a crew heat shield for a 12–14 km/s return to Earth (no crew has entered above about 11 km/s; the book's working assumption is a shield qualified for about 12.5 km/s and a return timed to enter no faster), and a robot fleet that runs a site for at least 120 days without contact. And one limit the plan does not close at all: every transit these windows offer at entry speeds the plan's vehicles can survive gives the crew more radiation than NASA's 600 mSv career limit, so the first crew flies above it under individual waivers, each accepted in writing ([chapter 2](02.%20Baseline%20and%20budgets.md), [chapter 12](12.%20Human%20readiness%20and%20health.md)).

The book also takes a position on where that workforce is heading. Today's Mars rovers drive themselves for short stretches and choose their own science targets. The book assumes machine intelligence will keep climbing until it reaches minds that are self-aware, indistinguishable from a person in conversation, and far more capable than any human engineer. The plan does not wait for those minds. Every budget closes at level A3 (site autonomy for known work) except one named case: a dust storm that finds no reactor running before the second reactor comes online in January 2039, either in the first weeks before the first reactor starts or after it trips. The colony then sheds to a survival load of a few kilowatts that storm sunlight and batteries can carry, and restarts the reactor (chapter 2, [the storm case](02.%20Baseline%20and%20budgets.md#the-storm-case)). No spacecraft has reached A3 yet, and [chapter 1](01.%20Mission%20concept%20and%20autonomy.md) sets out the Earth campaign that would prove it. If those minds do arrive, the first Martians may not be human, and this book asks what that would mean.

> Thesis: An initial Mars outpost can be built and proven human-ready before any person arrives, by a robotic workforce whose autonomy climbs from today's rovers to self-aware artificial minds. The plan must close its budgets and stay safe at every autonomy level; each level gained makes it faster, richer, and more capable.

This is an independent, open research project. It does not represent any space agency or company.

## The plan at a glance

| Window | Departs | Lands | What it delivers |
|---|---|---|---|
| Pathfinder (optional) | Apr 2033 | Jan 2034 | Landing test and site survey |
| Wave 1 | Jun 2035 | Jan 2036 | First 100 kWe reactor, water wells, oxygen plant, construction robots |
| Wave 2 | Sep 2037 | Oct 2038 | Second reactor, habitat, methane and oxygen propellant plant, greenhouse |
| Wave 3 | Sep 2039 | Sep 2040 | Mars ascent vehicle, third reactor, habitat outfitting, medical bay |
| Support | Oct 2041 | Sep 2042 | Earth return vehicle to Mars orbit, and a support lander with food and robot spares |
| First crew | Nov 2043 | Sep 2044 | Four people |
| Food flight | Jan 2046 | Dec 2046 | Food and other stores that cover a missed return window, flown whether or not the crew leaves on time |

All numbers, dates, and budgets come from [chapter 2](02.%20Baseline%20and%20budgets.md).

## Autonomy levels

| Level | Name | In one line |
|---|---|---|
| A0 | Teleoperation | Humans steer in real time; impossible at Mars distances |
| A1 | Sequenced operation | Machines execute uploaded commands and stop when something looks wrong |
| A2 | Task autonomy | Machines plan within a single task; Mars rovers do this today |
| A3 | Site autonomy for known work | A fleet runs the site for at least 120 days without contact and fixes anticipated faults; required for every wave |
| A4 | Open-ended autonomy | Handles novel problems with expert engineering judgment |
| A5 | Artificial mind | Self-aware, indistinguishable from a person, far beyond human capability; assumed to arrive eventually |

[Chapter 1](01.%20Mission%20concept%20and%20autonomy.md) defines the levels, the evidence for each, and the questions a self-aware colonist would raise.

## Contents

1. [Mission concept and autonomy](01.%20Mission%20concept%20and%20autonomy.md): why machines go first, what "fully autonomous" means, the six autonomy levels, and the ethics of artificial minds on Mars.
2. [Baseline and budgets](02.%20Baseline%20and%20budgets.md): constants, launch windows, waves, and the power, water, propellant, and mass budgets that every chapter must honor.
3. [Site selection](03.%20Site%20selection.md): where to land, and how to be sure the ice is really there.
4. [Transportation and landing](04.%20Transportation%20and%20landing.md): cargo landers, orbital refueling, landing heavy payloads, and the crew's way home.
5. [Power](05.%20Power.md): fission reactors as the backbone, solar as the supplement, and surviving a four-month dust storm.
6. [ISRU and life support](06.%20ISRU%20and%20life%20support.md): making water, oxygen, propellant, and breathable air from local resources (in situ resource utilization, or ISRU).
7. [Habitat](07.%20Habitat.md): an ice-shielded inflatable home, built and pressure-tested by robots.
8. [Manufacturing and construction](08.%20Manufacturing%20and%20construction.md): landing pads, roads, shields, and what Martian materials can and cannot do.
9. [Food and agriculture](09.%20Food%20and%20agriculture.md): what four people need to eat, and how much of it the colony can grow.
10. [Communications](10.%20Communications.md): relays, delay-tolerant networking, and living with silence.
11. [Maintenance and robotics](11.%20Maintenance%20and%20robotics.md): the robot fleet, spares, and machines that repair machines.
12. [Human readiness and health](12.%20Human%20readiness%20and%20health.md): radiation dose and the crew's waivers, medicine, and what the colony must prove before people come.
13. [Timeline and gates](13.%20Timeline%20and%20gates.md): the dated plan, the exit criteria for each wave, and what slips if something is late.
14. [Critical challenges](14.%20Critical%20challenges.md): the seven risks that could stop the colony, and what autonomy can and cannot fix.
15. [Terraforming and the long view](15.%20Terraforming%20and%20the%20long%20view.md): beyond the first crew, from local climate control to what terraforming physics allows. The first base's builders are machines, not minds, though they may one day host minds.

[Appendix A. Risk register](Appendix%20A.%20Risk%20register.md): every tracked risk with likelihood, impact, detectability, controls, and owner.

## How to read this book

Read it straight through for the full argument. If you want the numbers first, start with [chapter 2](02.%20Baseline%20and%20budgets.md), then [chapter 13](13.%20Timeline%20and%20gates.md) for the schedule and [chapter 14](14.%20Critical%20challenges.md) for what could go wrong. Engineers checking a single subsystem can start with its chapter. Chapters 3 to 14 share one skeleton: requirements, design, a short paragraph on what would change the chapter's conclusion, autonomy, evidence and readiness, risks, and open questions. [Chapter 1](01.%20Mission%20concept%20and%20autonomy.md) (the autonomy levels), chapter 2 (the numbers), and [chapter 15](15.%20Terraforming%20and%20the%20long%20view.md) (the long view) follow their own shape.

Four kinds of text appear throughout, and each is marked:

- Facts carry a numbered citation to a source, preferably primary (NASA, the European Space Agency, NASA's Jet Propulsion Laboratory, peer-reviewed journals, Internet Engineering Task Force and Consultative Committee for Space Data Systems standards, NASA's Office of Inspector General, the Committee on Space Research).
- Design choices and estimates appear in blocks that begin with "Assumption:", each with its justification.
- Reasoned claims the evidence cannot yet prove appear in blocks that begin with "Hypothesis:". Each names its basis, the measurements, analogs, or theory it rests on, and the test that would confirm or refute it.
- Visions of the future appear in italic scenarios, labeled with a place and a year.

Only the scenarios are imagined. Where the book calculates a figure itself, the text says so, and where it reasons from an analog, such as a lunar test or an Earth practice, it names the analog and how far it carries.

## Contributing

Corrections and improvements are welcome through issues and pull requests.

- Cite a source for every factual claim, preferably primary. Link directly to the document, without tracking parameters.
- Mark design choices with `> Assumption:` and a one-line justification, and claims you cannot yet prove with `> Hypothesis:`, their basis, and the test that would settle them.
- Take numbers from [chapter 2](02.%20Baseline%20and%20budgets.md). If you think one is wrong, propose the change there so every chapter moves together.
- Use SI units, sentence-case headings, and the chapter structure: requirements, design, what would change this conclusion, autonomy, evidence and readiness, risks, open questions, references.

Give any chapter you change a new "Last reviewed" date.

## Suggested citation

> *Fully Autonomous Initial Mars Colony* (GitHub repository, sagol/Fully-Autonomous-Initial-Mars-Colony), accessed Month D, YYYY.

For facts, cite the original sources linked in each chapter.

## License

Original text is licensed under Creative Commons Attribution 4.0 (CC BY 4.0). Third-party material keeps its own license. See [LICENSE](LICENSE).
