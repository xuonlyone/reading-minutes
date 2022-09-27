# Clean Architecture

## preface

The languages have gotten a little better. The tools have gotten fantastically better. But the basic building blocks of a computer program have not changed.

```mermaid
flowchart LR;
  preface --> Pre1(findings);
  Pre1 --> Pre11(The architecure rules are the same);

  preface --> Pre2(conclusion);
  Pre2 --> Pre21(the rules of software architecture are independent of every other variable.);
```

## Part 1 Introduction

### Charpter 1 What is design and architecture

For starters, the auther asserts that there is no difference between design and architecture.

The measure of design quality is simply the measure of the effort required to meet the needs of the customer. If that effort is low, and stays low throughout the lifetime of the system, the design is good.


```mermaid
flowchart LR;
  Ch0(notes) --> Ch1(Goal);
  Ch1 --> CH11(The goal of software architecture is to minimize the human resource required to build and maintain the required system.);

  Ch0 --> Ch2(Case);
  Ch2 --> Ch21(story of the Tortoise and the Hare);
  Ch21 --> Ch211(The Hare, so confident in its intrinsic speed, does not take the race seriously, and so naps hile the Tortoise crosses the finish line.);
  Ch2 --> Ch22(developer);
  Ch22 --> Ch221(overconfident in their ability to remain productive.);
  Ch22 --> Ch222(writing messy code makes them go fast in the short term, and just slows them down in the long term.);
  Ch22 --> Ch223(making messes is always slower than staying clean);
  Ch22 --> Ch224(Their overconfidence will drive the redesign into the same mess as the original project.);
  Ch2 --> Ch23(way);
  Ch23 --> Ch231(The only way to go fast, is to go well.);

  Ch0 --> Ch3(Conclusion);
  Ch3 --> Ch31(the best option: taking the quality of its software architecture seriously);
  Ch3 --> Ch32(to know what good software architecture is);
  Ch3 --> Ch33(to know which attributes of system architecture lead to that end);

```

### chapter 2 A Tail of Two Values

```mermaid
flowchart LR;
  Ch0(notes) --> Ch1(Values);
  Ch1 --> Ch11(behavior);
  Ch1 --> Ch12(architecture);

  Ch11 --> Ch111(misconception);
  Ch111 --> Ch1111(make the machine implement the requirements);
  Ch111 --> Ch1112(fix any bugs);

  Ch12 --> Ch121(misconception);
  Ch121 --> Ch1211(for stakeholder);
  Ch1211 --> Ch12111(providing a stream of changes of roughly similar scope);
  Ch121 --> Ch1212(for developer);
  Ch1212 --> Ch12121(giving them a stream of jigsaw puzzle pieces that  they must fit into a puzzle of ever-increasing complexity.);

  Ch0 --> Ch2(Eisenhower's Matrix);
  Ch2 --> Ch21(priority);
  Ch21 --> Ch211(1. Urgent and important);
  Ch21 --> Ch212(2. Not urgent and important);
  Ch21 --> Ch213(3. Urgent and not important);
  Ch21 --> Ch214(4. Note urgent and not important);

  Ch11 --> Ch112(first value);
  Ch12 --> Ch122(second value);
  Ch112 --> Ch1121(urgent but not always particularly important);
  Ch122 --> Ch1221(important but never particularly urgent);

  Ch0 --> Ch3(responsibility);
  Ch3 --> Ch31(the importance of architecture over the urgency of features);
  Ch3 --> Ch32(fight for the architecture);

```

# Part 2 Starting with the Bricks: Programming Paradigms

## Chapter 3 Paradigm Overview

```mermaid
flowchart LR;
  Ch0(notes) -->Ch1(programming paradigms);
  Ch1 --> Ch11(structed programming);
  Ch1 --> Ch12(object-orient programming);
  Ch1 --> Ch13(functional programming);

  Ch11 --> Ch111(discoverd by Edsger Wybe Dijkstra, 1968);
  Ch11 --> CH112(Structured programming imposes discipline on direct transfer of control.);

  Ch12 --> Ch121(by Ole Johan Dahl and Kristen Nygaard, 1966);
  Ch12 --> Ch122(Object-oriented programming imposes discipline on indirect transfer of control.);

  Ch13 --> Ch131(by Alonzo Church, in 1936);
  Ch13 --> Ch132(Functional programming imposes discipline upon assignment.);

  Ch0 --> Ch2(align with concerns of architecture);
  Ch2 --> Ch21(fuction);
  Ch2 --> Ch22(separation of components);
  Ch2 --> Ch23(data management);

```

## Chapter 4 Structured Programming

```mermaid
flowchart LR;
  Ch0(notes) --> Ch1(Edsger Wybe Dijkstra);
  Ch1 --> Ch11(born: Rotterdam, 1930);
  Ch1 --> Ch12(took a job with the Mathematical Center of Amsterdam, 1952)
  Ch1 --> Ch13("married Maria Debets with job title 'theoretical physicist'( authorities were unwilling to accept 'programmer' as profession), 1957")
  Ch1 --> Ch14(letter to the editor of CACM, 1968)
  Ch14 --> Ch141("Go To Statement Considered Harmful")

  Ch0 --> Ch2(problems)
  Ch2 --> Ch21(programming is hard)
  Ch2 --> Ch22(programmers don't do it very well)

  Ch0 --> Ch3(discovery)
  Ch3 --> Ch31(All programs can be constructed from just three structures: sequence, selection, and iteration.)
  Ch0 --> Ch4(foundation)
  Ch4 --> Ch42(modules can be functionally decomposed)
  Ch0 --> Ch5(disciplines)
  Ch5 --> Ch51(structured analysis)
  Ch5 --> Ch52(structured design)
  Ch0 --> Ch6(Tests)
  Ch6 --> Ch61(a program can be proven incorrect by a test, but it can not be proven correct)
  Ch0 --> Ch7(conclusion)
  Ch7 --> Ch71(software is like a science and is driven by falsifiablility)

```

## Chapter 5 Object-Oriented Programming 


```mermaid
flowchart LR
  Ch0(OO) --> Ch1(Encapsulation)
  Ch0 --> Ch2(Inheritance)
  Ch0 --> Ch3(Polymorphism)

  Ch1 --> Ch11(it is difficult to accept that OO depends on strong encapsulation)
  Ch1 --> Ch12(Indeed, many OO languages have little or no enforced encapsulation)


  Ch2 --> Ch21(Inheritance is simply the redeclaration of a group of variables and functions within an enclosing scope.)
  Ch2 --> Ch22(make the masquerading of data structures significantly more convenient.)

  Ch3 --> Ch31(polymorphism is an application of pointers to functions.)
  Ch3 --> Ch32(OO languages may not have given us polymorphism, but they have made it much safer and much more convenient.)
  Ch3 --> Ch33(OO imposes discipline on indirect transfer of control )

```

OO is the ability, through the use of polymorphism, to gain absolute control over every source code dependency in the system. It allows the architect to create a plugin architecture, in which modules that contain high-level policies are independent of modules that contain low-level details. The low-level details are relegated to plugin modules that can be deployed and developed independently from the modules that contain high-level policies.

## Chapter 6 Functional Programming

If we have enough storage and enough processor power, we can make our applications entirely immutable—and, therefore, entirely functional.

## Conclusion
Software—the stuff of computer programs—is composed of sequence, selection, iteration, and indirection. Nothing more. Nothing less.

# Part 3 Design Principles

```mermaid
flowchart LR
  Ch0(Design Principles) --> Ch1(goal)
  Ch1 --> Ch11(Tolerate change)
  Ch1 --> Ch12(Easy to understand)
  Ch1 --> Ch13(Are the basis of components that can be used in many software systems)

  Ch0 --> Ch2(SOLID)
  Ch2 --> Ch21(SRP: The Single Responsibility Principle)
  Ch2 --> Ch22(OCP: The Open-Closed Principle)
  Ch2 --> Ch23(LSP: The Liskov Substitution Principle)
  Ch2 --> Ch24(ISP: The Interface Segregation Principle)
  Ch2 --> Ch25(DIP: The Dependency Inversion Principle)
```

## Chapter 7 SRP: The single responsibility principle

```mermaid
flowchart LR
  Ch0(SRP) --> Ch1(A module should be responsible to one, and only one, actor.)
  Ch0 --> Ch2(symptoms of violating it)
  Ch2 --> Ch21(Accidental duplication)
  Ch2 --> Ch22(Merges)
  Ch0 --> Ch3(solutions)
  Ch3 --> Ch31(separate the data from the functions)
  Ch3 --> Ch32(use the Facade pattern)
```

The Single Responsibility Principle is about functions and classes—but it reappears in a different form at two more levels. At the level of components, it becomes the Common Closure Principle. At the architectural level, it becomes the Axis of Change responsible for the creation of Architectural Boundaries.

## Chapter 8 OCP: The Open-Closed Principle

```mermaid
flowchart LR
  Ch0(OCP) --> Ch1(A software artifact should be open for extension but closed for modification)
  Ch0 --> Ch2(If component A should be protected from changes in component B, then component B should depend on component A.)

```

## Chapter 9 LSP: The Liskov substitution Principle

```mermaid
flowchart LR
  Ch0(LSP) --> Ch1(If for each object o1 of type S there is an object o2 of type T such that for all programs P defined in terms of T, the behavior of P is unchanged when o1 is substituted for o2 then S is a subtype of T)
```


## Chapter 10 ISP: The Interface Segregation Principle

```mermaid
flowchart LR
  Ch0(ISP) --> Ch1(ISP & language)
  Ch1 --> Ch11(statically typed language)
  Ch1 --> Ch12(dynamically typed language)
  Ch11 --> Ch111(Create source code dependencies with include, import, use...)
  Ch12 --> Ch121(inferred at runtime)
  Ch12 --> Ch122(more flexble, less tightly coupled)

  Ch0 --> Ch2(ISP & architecture)
  Ch2 --> Ch21(harmful to depend on modules that contain more than you need)
```

## Chapter 11 DIP: The Dependency Inversion Principle

```mermaid
flowchart LR
  Ch0(DIP) -->Ch1(the most flexible systems are those in which source code dependencies refer only to abstractions, not to concretions)
  Ch0 --> Ch2(It is the volatile concrete elements of our system that we want to avoid depending on.)
  Ch0 --> Ch3(coding practices)
  Ch3 --> Ch31("Don’t refer to volatile concrete classes.")
  Ch3 --> Ch32("Don’t derive from volatile concrete classes.")
  Ch3 --> Ch33("Don’t override concrete functions.")
  Ch3 --> Ch34("Never mention the name of anything concrete and volatile.")
```


# Part 4 Component Principles

## Chapter 12 Components

Components are the smallest entities that can be deployed as part of
a system.
Regardless of how they are eventually deployed, well-designed components always retain the ability to be independently deployable and, therefore, independently developable.

```mermaid
flowchart LR
  Ch0(Components) --> Ch1(units of deployment)
  Ch0 --> Ch2(the granule of deployment)
  Ch2 --> Ch21(compiled languages)
  Ch21 --> Ch211(aggregations of binary files)
  Ch2 --> Ch22(interpreted languages)
  Ch22 --> Ch221(aggregations of source files)

```

## Chapter 13 Component Cohesion

```mermaid
flowchart LR
  Ch0(Component Cohesion) 
  Ch0 --> Ch1(REP: The Resue/Release Equivalence Principle)
  Ch0 --> Ch2(CCP: The Common Closure Principle)
  Ch0 --> Ch3(CRP: The Common Reuse Principle)

  Ch1 --> Ch11(The granule of reuse is the granule of release.)
  Ch1 --> Ch12(Classes and modules that are grouped together into a component should be releasable together.)

  Ch2 --> Ch21(Gather into components those classes that change for the same reasons and at the same times. )
  Ch2 --> Ch22(Separate into different components those classes that change at different times and for different reasons.)

  Ch3 --> Ch31("Don’t force users of a component to depend on things they don’t need.")

```


## Chapter 14 Component Coupling

```mermaid
flowchart LR
  Ch0(Component Coupling)
  Ch0 --> Ch1(ADP: The Acyclic Dependencies Principle)
  Ch0 --> Ch2(SDP: The Stable Dependencies Principle)


  Ch1 --> Ch11(Allow no cycles in the component dependency graph.)
  Ch1 --> Ch12(break a cycle of components)
  Ch12 --> Ch121("Apply the Dependency Inversion Principle (DIP).")
  Ch12 --> Ch122("Move the class(es) that they both depend on into that new component")

  Ch2 --> Ch21(Depend in the direction of stability.)
  Ch2 --> Ch22(Stability Metrics)
  Ch22 --> Ch221(Fan-in)
  Ch221 --> Ch2211(Incoming dependencies)
  Ch221 --> Ch2212(the number of classes outside this component that depend on classes within the component)
  Ch22 --> Ch222(Fan-out)
  Ch222 --> Ch2221(Outgoing dependencies)
  Ch222 --> Ch2222(the number of classes inside this component that depend on classes outside the component)
  Ch22 --> Ch223(I:Instability)
  Ch223 --> Ch2231("I = Fan-out,(Fan-in + Fan-out)")
  Ch223 --> Ch2232(I=0,maximally stable component)
  Ch223 --> Ch2233(I=1,maximally unstable component)
  Ch2 --> Ch23(Not all components should be stable)

  Ch0 --> Ch3(The Stable Abstractions Principle)
  Ch3 --> Ch31(A component should be as abstract as it is stable)
  Ch3 --> Ch32(SAP: Stable Abstractions Principle)
  Ch32 --> Ch321(a stable component should also be abstract so that its stability does not prevent it from being extended)
  Ch32 --> Ch322(an unstable component should be concrete since it its instability allows the concrete code within it to be easily changed)
  Ch3 --> Ch33(Measuring abstraction)
  Ch33 --> Ch331(Nc: The number of classes in the component.)
  Ch33 --> Ch332(Na: The number of abstract classes and interfaces in the component.)
  Ch33 --> Ch333("A: Abstractness. A = Na ÷ Nc.")
  Ch333 --> Ch3331(The A metric ranges from 0 to 1)
  Ch333 --> Ch3332(0 implies that the component has no abstract classes at all)
  Ch333 --> Ch3333(1 implies that the component contains nothing but abstract classes)
  Ch3 --> Ch34(The main sequence)
  Ch34 --> Ch341(The Zone of Pain)
  Ch34 --> Ch342(The Zone of Uselessness)
  Ch34 --> Ch343(Distance from the main sequence)
  Ch343 --> Ch3431("Distance. D = |A+I–1|")
  Ch3431 --> Ch34311(0 indicates that the component is directly on the Main Sequence.)
  Ch3431 --> Ch34312(1 indicates that the component is as far away as possible from the Main Sequence.)

```
### ADP
The component structure cannot be designed from the top down. It is not one of the first things about the system that is designed, but rather evolves as the system grows and changes.
Component dependency diagrams have very little do to with describing the function of the application. Instead, they are a map to the buildability and maintainability of the application. This is why they aren’t designed at the beginning of the project.

### SDP
Any component that we expect to be volatile should not be depended on by a component that is
difficult to change.

# Part 5 Architecture

## Chapter 15 What is architecture

```mermaid
flowchart LR
  Ch0(Software Architecture)
  Ch0 --> Ch1(concept)
  Ch1 --> Ch11(software architect)
  Ch11 --> Ch111(the best programmers)
  Ch11 --> Ch112(continue to take programming tasks)
  Ch11 --> Ch113(guide the team toward a design that maximinzes productivity)
  Ch1 --> Ch12(primary purpose)
  Ch12 --> Ch121(support the life cycle of the system)
  Ch121 --> Ch1211(easy to understand)
  Ch121 --> Ch1212(easy to develop)
  Ch121 --> Ch1213(easy to maintain)
  Ch121 --> Ch1214(easy to deploy)
  Ch1 --> Ch13(ultimate goal)
  Ch13 --> Ch131(minimize the lifetime coset of the system)
  Ch13 --> Ch132(maximize programmer productivity)

  Ch0 --> Ch2(development)
  Ch2 --> Ch21(Different team structures imply different architectural decisions.)

  Ch0 --> Ch3(deployment)
  Ch3 --> Ch31(make a system that can be easily deployed with a single action.)
  
  Ch0 --> Ch4(operation)
  Ch4 --> Ch41(communicates the operational needs of the system.)

  Ch0 --> Ch5(maintenace)
  Ch5 --> Ch51(The primary cost of maintenance is in spelunking and risk.)

  Ch0 --> Ch6(keeping options open)
  Ch6 --> Ch61(software has two types of value)
  Ch61 --> Ch611(behavior)
  Ch61 --> Ch612(structure)
  Ch612 --> Ch6121(makes software soft)
  Ch6 --> Ch62(two major elements)
  Ch62 --> Ch621(policy)
  Ch621 --> Ch6211(embody all the business rules and procedures)
  Ch621 --> Ch6212(the true value of the system lives)
  Ch62 --> Ch622(details)
  Ch622 --> Ch6221(do not impact the behavior of the policy)
  Ch6 --> Ch63(goal)
  Ch63 --> Ch631(recognize policy as the most essential element of the system)
  Ch63 --> Ch632(make the details irrelevant to that policy)
  Ch6 --> Ch64(A good architect maximizes the number of decisions not made.)
```


