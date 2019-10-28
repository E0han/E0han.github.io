# Software Modelling and Design Notes


<!-- vscode-markdown-toc -->
* 1. [Design Models](#DesignModels)
	* 1.1. [Analysis, Design and Implementation](#AnalysisDesignandImplementation)
	* 1.2. [Object-Oriented Software Design  (OOD)](#Object-OrientedSoftwareDesignOOD)
		* 1.2.1. [Layers](#Layers)
	* 1.3. [Core App. Logic](#CoreApp.Logic)
	* 1.4. [Responsibility](#Responsibility)
		* 1.4.1. [Doing responsibilities include:](#Doingresponsibilitiesinclude:)
		* 1.4.2. [Knowing responsibilities include knowledge of:](#Knowingresponsibilitiesincludeknowledgeof:)
		* 1.4.3. [Responsibilities and Methods are Related](#ResponsibilitiesandMethodsareRelated)
	* 1.5. [Responsibility-Driven Design (RDD)](#Responsibility-DrivenDesignRDD)
	* 1.6. [Visibility in Design](#VisibilityinDesign)
* 2. [Patterns](#Patterns)
	* 2.1. [What will be covered:](#Whatwillbecovered:)
	* 2.2. [Advantages of patterns](#Advantagesofpatterns)
	* 2.3. [Low Coupling](#LowCoupling)
		* 2.3.1. [Solution](#Solution)
		* 2.3.2. [Evaluate the effect of coupling](#Evaluatetheeffectofcoupling)
		* 2.3.3. [Contraindications](#Contraindications)
	* 2.4. [High Cohesion](#HighCohesion)
		* 2.4.1. [Problem](#Problem)
		* 2.4.2. [Functional cohesion:](#Functionalcohesion:)
		* 2.4.3. [Solution](#Solution-1)
		* 2.4.4. [Contrasting levels of Cohesion](#ContrastinglevelsofCohesion)
		* 2.4.5. [Contraindications](#Contraindications-1)
	* 2.5. [Coupling and Cohesion](#CouplingandCohesion)
	* 2.6. [Creator](#Creator)
		* 2.6.1. [Problem:](#Problem:)
		* 2.6.2. [Example](#Example)
	* 2.7. [Solution](#Solution-1)
		* 2.7.1. [Sequence diagram and design diagram:](#Sequencediagramanddesigndiagram:)
		* 2.7.2. [Contraindications (Where you shouldn’t apply the pattern)](#ContraindicationsWhereyoushouldntapplythepattern)
	* 2.8. [Information Expert](#InformationExpert)
		* 2.8.1. [Problem](#Problem-1)
		* 2.8.2. [Solution](#Solution-1)
		* 2.8.3. [Contraindications](#Contraindications-1)
	* 2.9. [Controller](#Controller)
	* 2.10. [Polymorphism](#Polymorphism)
		* 2.10.1. [Problem](#Problem-1)
		* 2.10.2. [Solution](#Solution-1)
		* 2.10.3. [Example: Monopoly Game Version 2](#Example:MonopolyGameVersion2)
		* 2.10.4. [Generalisation-Specialisation Class Hierarchy](#Generalisation-SpecialisationClassHierarchy)
	* 2.11. [Pure Fabrication](#PureFabrication)
		* 2.11.1. [Problem](#Problem-1)
		* 2.11.2. [Solution](#Solution-1)
		* 2.11.3. [Example:](#Example:)
		* 2.11.4. [Contraindications](#Contraindications-1)
	* 2.12. [Indirection间接](#Indirection)
		* 2.12.1. [Problem](#Problem-1)
		* 2.12.2. [Solution](#Solution-1)
		* 2.12.3. [Contraindications](#Contraindications-1)
	* 2.13. [Protected Variations](#ProtectedVariations)
		* 2.13.1. [Problem](#Problem-1)
		* 2.13.2. [Solution](#Solution-1)
		* 2.13.3. [Open-Closed Principle (OCP)](#Open-ClosedPrincipleOCP)
		* 2.13.4. [Contraindications](#Contraindications-1)
	* 2.14. [Relationships between GRASP principles](#RelationshipsbetweenGRASPprinciples)
* 3. [Apply some GoF design patterns](#ApplysomeGoFdesignpatterns)
	* 3.1. [Adapter](#Adapter)
		* 3.1.1. [Scenario](#Scenario)
		* 3.1.2. [Problem](#Problem-1)
		* 3.1.3. [Solution](#Solution-1)
		* 3.1.4. [Example](#Example-1)
		* 3.1.5. [Another Example: Disney Madness](#AnotherExample:DisneyMadness)
		* 3.1.6. [What GRASP principles are used by Adapter?](#WhatGRASPprinciplesareusedbyAdapter)
		* 3.1.7. [Issues arising from Adapter](#IssuesarisingfromAdapter)
	* 3.2. [(Concrete) Factory](#ConcreteFactory)
		* 3.2.1. [Problem](#Problem-1)
		* 3.2.2. [Solution](#Solution-1)
		* 3.2.3. [Factory class example](#Factoryclassexample)
		* 3.2.4. [Coding Example](#CodingExample)
		* 3.2.5. [Issues arising from Factory](#IssuesarisingfromFactory)
	* 3.3. [Singleton Pattern](#SingletonPattern)
		* 3.3.1. [problem](#problem)
		* 3.3.2. [Solution](#Solution-1)
		* 3.3.3. [Example](#Example-1)
		* 3.3.4. [Coding Example](#CodingExample-1)
		* 3.3.5. [Static: Why some and not all?](#Static:Whysomeandnotall)
	* 3.4. [Strategy](#Strategy)
		* 3.4.1. [Problem](#Problem-1)
		* 3.4.2. [Solution](#Solution-1)
		* 3.4.3. [Example](#Example-1)
		* 3.4.4. [Strategy factory](#Strategyfactory)
	* 3.5. [Composite](#Composite)
		* 3.5.1. [Problem](#Problem-1)
		* 3.5.2. [Solution](#Solution-1)
		* 3.5.3. [Examples 1: Composite shape](#Examples1:Compositeshape)
		* 3.5.4. [Coding Example](#CodingExample-1)
	* 3.6. [Composite Strategies](#CompositeStrategies)
	* 3.7. [Façade](#Faade)
		* 3.7.1. [problem](#problem-1)
		* 3.7.2. [Solution](#Solution-1)
		* 3.7.3. [UML package diagram: Facade](#UMLpackagediagram:Facade)
		* 3.7.4. [Example: Facade Vs. GRASP Controller](#Example:FacadeVs.GRASPController)
		* 3.7.5. [Example: Facade Vs. Adapter](#Example:FacadeVs.Adapter)
	* 3.8. [Observer (aka. Publish-Subscribe)](#Observeraka.Publish-Subscribe)
		* 3.8.1. [Problem](#Problem-1)
		* 3.8.2. [Solution](#Solution-1)
		* 3.8.3. [Example](#Example-1)
		* 3.8.4. [Coding Example](#CodingExample-1)
		* 3.8.5. [Example: Alarm Events, different Subscribers](#Example:AlarmEventsdifferentSubscribers)
* 4. [State Machine](#StateMachine)
	* 4.1. [Definitions:](#Definitions:)
	* 4.2. [HOW TO APPLY SMD](#HOWTOAPPLYSMD)
	* 4.3. [Transition Action and Guard Example](#TransitionActionandGuardExample)
		* 4.3.1. [Choice Pseudo-state](#ChoicePseudo-state)
	* 4.4. [Nested States](#NestedStates)
* 5. [Architectural Analysis and Logical Architecture](#ArchitecturalAnalysisandLogicalArchitecture)
	* 5.1. [Software Architecture](#SoftwareArchitecture)
	* 5.2. [Architectural Analysis](#ArchitecturalAnalysis)
		* 5.2.1. [Examples: Significant Functional requirements](#Examples:SignificantFunctionalrequirements)
		* 5.2.2. [Example: Significant Non-Functional Requirements](#Example:SignificantNon-FunctionalRequirements)
	* 5.3. [Identification and Resolution](#IdentificationandResolution)
	* 5.4. [Example: New LMS Requirenment](#Example:NewLMSRequirenment)
	* 5.5. [Common Steps](#CommonSteps)
	* 5.6. [Priorities](#Priorities)
	* 5.7. [Architecture Factor Table](#ArchitectureFactorTable)
	* 5.8. [Technical Memo](#TechnicalMemo)
* 6. [Logical Architecture](#LogicalArchitecture)
	* 6.1. [Layered Architecture](#LayeredArchitecture)
		* 6.1.1. [Example: UML Package Diagram Notations: Layer](#Example:UMLPackageDiagramNotations:Layer)
		* 6.1.2. [Example: Common layers](#Example:Commonlayers)
	* 6.2. [Guidelines:](#Guidelines:)
		* 6.2.1. [Mixing Views of the architecture](#MixingViewsofthearchitecture)
		* 6.2.2. [System Sequence Diagram and Layers](#SystemSequenceDiagramandLayers)
		* 6.2.3. [Using Layers Helps Address Problems](#UsingLayersHelpsAddressProblems)
* 7. [Modelling and Design in the Software process](#ModellingandDesignintheSoftwareprocess)
	* 7.1. [Schedule-Oriented Terms in UP](#Schedule-OrientedTermsinUP)
	* 7.2. [Inception 开始](#Inception)
		* 7.2.1. [Outcome:](#Outcome:)
		* 7.2.2. [Inception Artefacts (Partial) 人工](#InceptionArtefactsPartial)
	* 7.3. [Requirements to Design - Iteratively](#RequirementstoDesign-Iteratively)
		* 7.3.1. [Spreading Use Cases across Iterations](#SpreadingUseCasesacrossIterations)
	* 7.4. [Agile Modelling & Lightweight UML Drawing](#AgileModellingLightweightUMLDrawing)
	* 7.5. [Object Design Skill vs. UML Drawing Skill](#ObjectDesignSkillvs.UMLDrawingSkill)

<!-- vscode-markdown-toc-config
	numbering=true
	autoSave=true
	/vscode-markdown-toc-config -->
<!-- /vscode-markdown-toc -->


##  1. <a name='DesignModels'></a>Design Models
###  1.1. <a name='AnalysisDesignandImplementation'></a>Analysis, Design and Implementation
- **Analysis**:  investigation of the problem & requirements.
	- **Object-oriented analysis**: emphases finding and describing objects and concepts in the problem domain.
- **Design**: a conceptual solution to a problem that meets the requirements
	- **Object-oriented design**: a conceptual solution that emphasises强调 defining software objects and their collaboration
- **Implementation**: a concretesolution to a problem that meets the requirements
	- **Object-oriented implementation**: implementation in object-oriented languages and technologies

###  1.2. <a name='Object-OrientedSoftwareDesignOOD'></a>Object-Oriented Software Design  (OOD)
OOD: a conceptual solution that emphasises强调 defining software objects and their collaboration
- **Assignment of responsibilities** 
	- Principles and patterns
- **Structure and connectedness**
	- Multiple Levels, including high-level architecture
- **Interfaces: methods, data types, and protocols (communication)**
	- Interfaces: the way which these elements connect together 
	- External and Internal

####  1.2.1. <a name='Layers'></a>Layers 
One of common ways of structuring software systems.
Example:
Simple layer system, with 3 layer, going down and become more general.
![](assets/smd/Screen%20Shot%202019-10-25%20at%207.01.42%20pm.png)
The logic layer may can be used for multiple applications , but they all tied up to the business core and design concepts

###  1.3. <a name='CoreApp.Logic'></a>Core App. Logic
OO technology can be applied throughout an application. The reason that focus on the core application logic layer:
	- Other layers tend to be technology/platform dependent. 
	- Design approach/patterns for other layers tends to be technology constrained and changeable. 
	- OO design of core logic layer similar across technologies.
	- Essential OO design skills are applicable to other layers.

###  1.4. <a name='Responsibility'></a>Responsibility
Def: A contract or obligation of a classifier
####  1.4.1. <a name='Doingresponsibilitiesinclude:'></a>Doing responsibilities include:
	- Create object, perform calculation
	- initiate action in other objects
	- control and coordinate activities in other objects
####  1.4.2. <a name='Knowingresponsibilitiesincludeknowledgeof:'></a>Knowing responsibilities include knowledge of:
	- Private encapsulated data
	- Related objects
	- Derivable or calculable items
####  1.4.3. <a name='ResponsibilitiesandMethodsareRelated'></a>Responsibilities and Methods are Related
![](assets/smd/Screen%20Shot%202019-10-25%20at%207.29.27%20pm.png)

###  1.5. <a name='Responsibility-DrivenDesignRDD'></a>Responsibility-Driven Design (RDD)
RDD sees an OO Design as a community of collaborating responsible objects. RDD involves assigning responsibilities to classes, which should be based on proven principles
- **E.g.** Domain Sale has a time attribute:
	- Have a low representation gap should lead us to believe that Design Sale should know its time

###  1.6. <a name='VisibilityinDesign'></a>Visibility in Design
Design requires assigning responsibilities and objects cooperating to achieve required outcomes:
	- Grouping highly related responsibilities (Cohension)
	- Minimising dependency on other elements (Coupling)
Objects require visibility of each other to cooperate:
	- Ability of object to "see" or refer to another object
	- *Eg. For A to send a message to B, B must be visible to A*

##  2. <a name='Patterns'></a>Patterns
A pattern is a recurring successful application of expertise in a particular domain
###  2.1. <a name='Whatwillbecovered:'></a>What will be covered:
- GRASP: general responsibility assignment software patterns (or principles)
- Creator 
- Information Expert
- Controller

###  2.2. <a name='Advantagesofpatterns'></a>Advantages of patterns
* Capture expertise and make it accessible to non-experts in a standard form learn from the expertises.
* Facilitate communication among practitioners by providing a common language. 
* Make it easier to reuse successful applications of expertise.
* Facilitate generating modified applications.
* Improve understandability.
* Simplify documentation.


###  2.3. <a name='LowCoupling'></a>Low Coupling
Coupling is the measure of how strongly one element is connected to, has knowledge of  or relies on others
Problems for a class with high coupling:
	- Forced changes: result of changes in related classes 
	- Harder to understand in isolation
	- Harder to reuse, as harder to isolate
####  2.3.1. <a name='Solution'></a>Solution
Assign responsibility so that coupling remains low. Use this principle to evaluate alternatives.
####  2.3.2. <a name='Evaluatetheeffectofcoupling'></a>Evaluate the effect of coupling
![](assets/smd/Screen%20Shot%202019-10-25%20at%208.22.57%20pm.png)

####  2.3.3. <a name='Contraindications'></a>Contraindications
High coupling to stable elements is rarely a problem
- Standard java Libraries can be used extensively without concern as their use does not generate concerns relating to stability, understanding or reuse.
*Note: coupling is **essential**. We are only choosing where it can be kept low without compromising other design aspects* 

###  2.4. <a name='HighCohesion'></a>High Cohesion 
####  2.4.1. <a name='Problem'></a>Problem
How to keep objects focussed, understandable, and manageable, and as a side effect, support Low Coupling?
####  2.4.2. <a name='Functionalcohesion:'></a>Functional cohesion:
A measure of how strongly related and focussed the responsibilities of an element are.
####  2.4.3. <a name='Solution-1'></a>Solution
Assign a responsibility so that cohesion remains high. Use this to evaluate alternatives.
- Class with low cohesion:
	- Hard to comprehend
	- hard to reuse 
	- Hard to maintain
	- Delicate; constantly affected by change
####  2.4.4. <a name='ContrastinglevelsofCohesion'></a>Contrasting levels of Cohesion
![](assets/smd/Screen%20Shot%202019-10-25%20at%208.30.20%20pm.png)

####  2.4.5. <a name='Contraindications-1'></a>Contraindications
Lower cohesion is sometimes justified to meet nonfunctional requirements
Eg. To meet performance requirements, larder, less cohesive classes are used to reduce processing overheads

*Note: Coupling and cohesion are fundamental design properties which are interdependent: both must be considered together.*

###  2.5. <a name='CouplingandCohesion'></a>Coupling and Cohesion
![](assets/smd/Screen%20Shot%202019-10-25%20at%208.34.02%20pm.png)

Low Coupling and High Cohesion: Yin-and-Yang design


###  2.6. <a name='Creator'></a>Creator
####  2.6.1. <a name='Problem:'></a>Problem: 
Who should be responsible for creating a new instance of some class
####  2.6.2. <a name='Example'></a>Example
- It helps to decide which class should be responsible for creating a new instance of a class. 
![](assets/smd/Screen%20Shot%202019-10-25%20at%207.56.39%20pm.png)

In this case, the class Board is the creator of Square
###  2.7. <a name='Solution-1'></a>Solution
Assign class B responsibility to create instance of class A if one of these is true (the more the better):
	- B contains or compositely aggregates A
	- B records A
	- B close uses A 
	- B has the initialising data for A that will be passed to A when it is created. Thus B is an Expert with respect to creating A
If >1 applies choose B which aggregates使聚集/contains A

####  2.7.1. <a name='Sequencediagramanddesigndiagram:'></a>Sequence diagram and design diagram:
![](assets/smd/Screen%20Shot%202019-10-25%20at%208.02.43%20pm.png)
![](assets/smd/Screen%20Shot%202019-10-25%20at%208.03.00%20pm.png)

The black diamond above is composition (or strong aggregation), it basically says the Square don’t exists independently of the Board. The Board needs to know about the Square but the Square doesn’t need to know about the board. 

####  2.7.2. <a name='ContraindicationsWhereyoushouldntapplythepattern'></a>Contraindications (Where you shouldn’t apply the pattern)
- Creation of significant complexity, e.g.
	- recycling instances for performance
	- instances from A1, A2 ... based on property
In these cases delegate to helper class in the form of a Concrete factory or abstract Factory



###  2.8. <a name='InformationExpert'></a>Information Expert
Eg: [Programming, Web and Desktop App Development Source Code Examples](https://www.sourcecodeexamples.net/2018/06/information-expert-grasp-pattern.html)
####  2.8.1. <a name='Problem-1'></a>Problem
What is a general principle of assigning responsibilities to objects?

####  2.8.2. <a name='Solution-1'></a>Solution
Assign responsibility to the information expert — The class that has the information necessary to fulfil the responsibility.
- Start assigning responsibilities by clearly stating the responsibility 
- Look in Domain Model or Design Model?
	- If relevant classes in Design, look there first
	- Otherwise look in Domain, and use or expand to inspire creation of design classes

####  2.8.3. <a name='Contraindications-1'></a>Contraindications
- Suggested solution can result in poor coupling and cohesion
Eg. 
	- need to store objects in a database
	- each class is an expert on what needs to be stored
	- add db handling to each class?
	- No: DB elements and other class elements not cohesive; couples all classes with DB services
	- Separate application logic and DB logic (DB Expert)


###  2.9. <a name='Controller'></a>Controller

###  2.10. <a name='Polymorphism'></a>Polymorphism
####  2.10.1. <a name='Problem-1'></a>Problem
How to handle alternatives based on different types?
	- Fundamental theme in programs
	- Adding new alternatives if using if-then-else or case statement can require mods in many places
How to create pluggable software components? 
	- Client-Server relationship
		- How to replace Server component without affecting Client
####  2.10.2. <a name='Solution-1'></a>Solution
When related alternatives vary by type (class):
	- use operations with the same interface
	- to assign responsibilities for the behaviour
	- to the types for which the behaviour varies
Corollary推论
	- Don’t use conditionals to select the alternative
Polymorphism
	- Giving a single interface to entities of different types

####  2.10.3. <a name='Example:MonopolyGameVersion2'></a>Example: Monopoly Game Version 2
![](assets/smd/Screen%20Shot%202019-10-26%20at%204.37.45%20pm.png)
Use cases, skipped as rules for game known.
SSDs: No update required
Domain Model:
	- Concepts: Square, GoSquare, IncomeTaxSquare, GotoJailSquare
	- Suggests a class hierarchy
![](assets/smd/Screen%20Shot%202019-10-26%20at%204.40.52%20pm.png)

####  2.10.4. <a name='Generalisation-SpecialisationClassHierarchy'></a>Generalisation-Specialisation Class Hierarchy
Generalisation:
	- Identify commonality among concepts
	- Define superclass
	- Define relationships with subclasses
Guideline for creating subclasses:
	- Subclass has additional attributes of interest
	- Subclass has additional associations of interest
	- Subclass is operated on, handled, reacted to, or manipulated differently to the other classes in noteworthy ways
Modelling Guidelines:
	- Declare superclasses abstract
	- Append the superclass name to the subclass

###  2.11. <a name='PureFabrication'></a>Pure Fabrication
####  2.11.1. <a name='Problem-1'></a>Problem 
Which object should have responsibility when solutions offered by (e.g.) Expert violate high Cohesion and Low Coupling 
	- Use domain objects in design to lower representational gap
	- Sometimes using only domain objects in design result in poor coupling, cohesion, or reuse
####  2.11.2. <a name='Solution-1'></a>Solution
Assign a highly cohesive set of responsibilities to a class not in the problem domain
	- Made up to support high cohesion, low coupling, and reuse
	- Fabrication of the imagination, for the purpose of ensuring that the design is very pure 
	- Name is also an English idiom for an International lie, something you do when desperate
*Pattern justifies increasing the representation gap.*

####  2.11.3. <a name='Example:'></a>Example:
![](assets/smd/page26image3802911440.png) 
[version 1 on the left and 2 on the right]

Have reusable dice class and Player: takeTurn method which has player roll and total:
Need to refer back to dice without re-roll
![](assets/smd/Screen%20Shot%202019-10-26%20at%205.03.20%20pm.png)
![](assets/smd/Screen%20Shot%202019-10-26%20at%205.04.42%20pm.png)

####  2.11.4. <a name='Contraindications-1'></a>Contraindications
- Sometimes overused as excuse to add new objects
- Can be driven by behavioural decomposition into functions, resulting in functions just being grouped into objects
- Needs to be balanced with representational decomposition: assigning responsibilities to classes that have the required information 
- Poorly applied, can adversely affect coupling

###  2.12. <a name='Indirection'></a>Indirection间接
####  2.12.1. <a name='Problem-1'></a>Problem
Where to assign a responsibility to avoid direct coupling between two or more s/w elements?
How to de-couple objects so that low coupling is supported and reuse potential remains higher?
![](assets/smd/Screen%20Shot%202019-10-26%20at%205.09.20%20pm.png)

####  2.12.2. <a name='Solution-1'></a>Solution 
Assign the responsibility to an intermediate object to mediate between the other components or services so that they are not directly coupled. 
	- Intermediary creates an *indirection*between the other components. 
![](assets/smd/Screen%20Shot%202019-10-26%20at%205.10.24%20pm.png)

####  2.12.3. <a name='Contraindications-1'></a>Contraindications
Higher complexity in design needs to be justified by the lower coupling


###  2.13. <a name='ProtectedVariations'></a>Protected Variations
####  2.13.1. <a name='Problem-1'></a>Problem
How to design objects, subsystems, and systems so that the variations or instability in these elements doesn’t have an undesirable impact on other elements?
Points of change include:
	- Variation point: variations in existing system or requirements 
	- evolution point: speculative variations that may arise in the future

####  2.13.2. <a name='Solution-1'></a>Solution 
Identify points of known or predicted variation or instability 
Assign responsibilities to create a stable interface around them
*Interface: some design construct that sits between us and the variation*

####  2.13.3. <a name='Open-ClosedPrincipleOCP'></a>Open-Closed Principle (OCP) 
 Modules should be both open (for extension; adaptable) and closed (to modification that affects clients). *– Bertrand Meyer*
(OCP “module” includes **methods**, **classes**, **subsystems**, etc.) 
E.g. A class can be closed w.r.t. attribute access (access methods only – no changes), but open to modification of underlying attributes (+ addition of new methods). 
- OCP and PV are essentially two expressions of the same principle, with different emphasis 

####  2.13.4. <a name='Contraindications-1'></a>Contraindications
- Cost of speculative "future-proofing” at evolution points can outweigh the benefits
	- It may be cheaper/easier to rework a simple “brittle” design
	- Novice designers tend toward brittle designs
	- Intermediate designers ten towards overly general and flexible designs (in ways not used)
	- Expert designers gt the balance right 


###  2.14. <a name='RelationshipsbetweenGRASPprinciples'></a>Relationships between GRASP principles
![](assets/smd/Screen%20Shot%202019-10-26%20at%205.27.48%20pm.png)

##  3. <a name='ApplysomeGoFdesignpatterns'></a>Apply some GoF design patterns 
Recognise GRASP principles (shown above) as a generalisation of other design patterns. 
**GoF** Gang of Four Design patterns, are the four authors of the book - *”Design Patterns: Elements of Reusable Object-Oriented Software”.* 
Three type of pattern:
	- ::Creational patterns::
		- Abstract the object instantiation process
	- ::Structural pattern::
		- Describe how classes and objects can be combined to form larger structures
	- ::Behavioural pattern::
		- Are most specifically concerned with communication between objects
###  3.1. <a name='Adapter'></a>Adapter 
####  3.1.1. <a name='Scenario'></a>Scenario 
POS system needs to support several kinds of external services, including: 
	- Tax calculators
		- e.g., TaxMaster, GoodAsGoldTaxPro 
	- Accounting systems
		- e.g., SAP, GreatNorthern 
	- Credit authorization services 
 Each service has a different API, which cannot be changed. 

####  3.1.2. <a name='Problem-1'></a>Problem
How to resolve incompatible interfaces, or provide a ::stable interface:: to ::similar components:: with ::different interfaces::
####  3.1.3. <a name='Solution-1'></a>Solution
Convert the original interface of a component into another interface, through an intermediate adapter object

####  3.1.4. <a name='Example-1'></a>Example
![](assets/smd/Screen%20Shot%202019-10-26%20at%208.32.44%20pm.png)
![](assets/smd/Screen%20Shot%202019-10-26%20at%208.34.47%20pm.png)
.
####  3.1.5. <a name='AnotherExample:DisneyMadness'></a>Another Example: Disney Madness
![](assets/smd/Screen%20Shot%202019-10-26%20at%208.40.50%20pm.png)

It’s easy to see that the main only need to call the method move() from the adapter and it will operate the appropriate method from its end.
```java
Main (){
	IDisneyAdapter slothAdt = new SlothAdapter(“FlashAdt”);
	IDisneyAdapter ironManAdt = new IronManAdapter(“TonyAdt”);
	slothAdt.move();
	ironManAdt.move();
}
```

####  3.1.6. <a name='WhatGRASPprinciplesareusedbyAdapter'></a>What GRASP principles are used by Adapter?
The Adapter design pattern is a kind of Indirection and a Pure Fabrication, that uses Polymorphism.
![](assets/smd/Screen%20Shot%202019-10-26%20at%208.50.00%20pm.png)

####  3.1.7. <a name='IssuesarisingfromAdapter'></a>Issues arising from Adapter
Who creates the adapters?
Which class of adapter should be created? 
	- Should the Register object creates SAPAccountingAdapter? 
**Partial Answer:**
Separation of Concerns/High Cohesion
	- Creating adapters is not pure application logic
	- Adapter object is not a domain object 
Use GRASP Pure Fabrication pattern 


###  3.2. <a name='ConcreteFactory'></a>(Concrete) Factory
####  3.2.1. <a name='Problem-1'></a>Problem
Who should be responsible for creating objects when there are special considerations, such as complex creation logic, a desire to separate the creation responsibilities for better cohesion, and so forth? 
####  3.2.2. <a name='Solution-1'></a>Solution
Create a Pure Fabrication object called a Factory that handles the creation. 

####  3.2.3. <a name='Factoryclassexample'></a>Factory class example
![](assets/smd/Screen%20Shot%202019-10-26%20at%208.53.07%20pm.png)

####  3.2.4. <a name='CodingExample'></a>Coding Example
Disneyfactory.java
```java
class Disneyfactory(){
	public IDisneyAdapter getDisneyAdapter(String character){
			IDisneyAdapter Adt = null;
			if(character.equals("sloth")){
				adt = new SlothAdapter(name);
			}else if(character.equals("ironman”)){
				adt = new IronManAdapter(“TonyAdt”);
			}
			return add;
	}
}
```
Main.java
```java
Main(){
	Disneyfactory disneyFactory = new Disneyfactory();
	IDisneyAdapter adt = disneyfactory.getDisneyAdapter(“TonyAdt”);
	add.move();
}
```

####  3.2.5. <a name='IssuesarisingfromFactory'></a>Issues arising from Factory
How is Factory accessed?
	- It may need to be called from various places
How to get visibility to this single ServicesFactory instance ?
*Partial Answer:*
	- Only one instance of the factory is needed
	- Where required, pass through to methods or 
		- initialise objects with a ref? *No.*
	- Use ::**Singleton pattern**::to provide a single access point through global visibility 

###  3.3. <a name='SingletonPattern'></a>Singleton Pattern
####  3.3.1. <a name='problem'></a>problem
Exactly one instance of a class is allowed—it is a “singleton.” Objects need a global and single point of access. 
####  3.3.2. <a name='Solution-1'></a>Solution
Define a static method of the class that returns the singleton. 

####  3.3.3. <a name='Example-1'></a>Example
![](assets/smd/Screen%20Shot%202019-10-26%20at%209.03.13%20pm.png)

####  3.3.4. <a name='CodingExample-1'></a>Coding Example
```java
public class Register
{
    public void initialize()
{ 
… do some work … 
    // accessing the singleton Factory via the
getInstance call
accountingAdapter = ServicesFactory.getInstance().getAccountingAdapter(); //… do some work … 
} 
// other methods… 
} // end of class 
```
![](assets/smd/Screen%20Shot%202019-10-26%20at%209.04.48%20pm.png)

####  3.3.5. <a name='Static:Whysomeandnotall'></a>Static: Why some and not all?
Why not aren’t all Singleton service methods *static?*
*E.g.static getAccountingAdapter(): …*
- May want subclasses: static methods are not polymorphic (virtual); no overriding in most languages 
- Most remote communication mechanisms (e.g. Java’s RMI) don’t support remote-enabling of static methods. 
- A class is not always a singleton in all application contexts. 



###  3.4. <a name='Strategy'></a>Strategy
####  3.4.1. <a name='Problem-1'></a>Problem
How to design for varying, but related, ::algorithms or policies::? 
How to design for the ability to change these algorithms or policies? 
####  3.4.2. <a name='Solution-1'></a>Solution
Define each algorithm/policy/strategy in a separate class, with a common interface. 

####  3.4.3. <a name='Example-1'></a>Example
![](assets/smd/Screen%20Shot%202019-10-27%20at%206.46.29%20pm.png)
![](assets/smd/Screen%20Shot%202019-10-27%20at%206.59.47%20pm.png)
![](assets/smd/Screen%20Shot%202019-10-27%20at%207.06.03%20pm.png)

####  3.4.4. <a name='Strategyfactory'></a>Strategy factory
![](assets/smd/Screen%20Shot%202019-10-27%20at%207.07.24%20pm.png)
Strategy not stored. New strategy created for every request. 
PricingStrategyFactory.java
```java
public ISalePricingStrategy getSalePricingStrategy() { String className = System.getProperty( “salepricingstrategy.class.name” ); strategy = (ISalePricingStrategy) Class.forName( className ).newInstance(); return strategy; 
} 
```
Main.java
```java
ISalePricingStrategy  strategy = PricingStrategyFactory.getInstance(). getSalePricingStrategy();
```
![](assets/smd/Screen%20Shot%202019-10-27%20at%207.23.14%20pm.png)

###  3.5. <a name='Composite'></a>Composite 
Conflict resolution strategy: When multiple policies are applicable, how are these policies resolved?
	- Some discounts can’t be combined with others
	- Possible policies: best for customer or Best for store
*E.g. Composite pricing strategy:*
	- Determine which pricing strategies are applicable
	- Apply the relevant conflict resolution strategy 
####  3.5.1. <a name='Problem-1'></a>Problem
How to treat a group or composition structure of objects the same way (polymorphically) as a non-composite (atomic) object? 
####  3.5.2. <a name='Solution-1'></a>Solution 
Define classes for composite and atomic objects so that they implement the same interface. 
![](assets/smd/Screen%20Shot%202019-10-27%20at%207.27.20%20pm.png)

####  3.5.3. <a name='Examples1:Compositeshape'></a>Examples 1: Composite shape
![](assets/smd/Screen%20Shot%202019-10-27%20at%207.27.59%20pm.png)

####  3.5.4. <a name='CodingExample-1'></a>Coding Example
Picture.java
```java
public class Picture extends Shape{ 
ArrayList<Shape> shapes; public Picture() { 
	shapes = new ArrayList<Shape>(); } 
public void addShape(Shape shape) { 
	shapes.add(shape); 
} 
public void draw() { 
	for(Shape s: shapes) { 
		s.draw(); 
		} 
	} 
} 
```

###  3.6. <a name='CompositeStrategies'></a>Composite Strategies
![](assets/smd/Screen%20Shot%202019-10-27%20at%207.31.10%20pm.png)
![](assets/smd/Screen%20Shot%202019-10-27%20at%207.35.09%20pm.png)

	- the *Sale*object treats a Composite Strategy that contains other strategies just like any other *ISalePricingStrategy*
	- **UML**: ::ISalePricingStrategy is an interface, not a class::; this is the way in UML 2 to indicate an object of an unknown class, but that implements this interface 
![](assets/smd/Screen%20Shot%202019-10-27%20at%207.36.22%20pm.png)


###  3.7. <a name='Faade'></a>Façade 
Different companies who wish to purchase the NextGen POS would like to customise its behaviour slightly
E.g. to invalidate an action:
	- paid by a gift card
	- charitable donation sale

This customisation should have ::low impact:: on the existing software components
A “rule engine” subsystem, whise specific implementation is not yet known. It may be implemented with
	- the strategy pattern 
	- free open-source rule interpreters
	- commercial rule interpreters
	- other solutions
####  3.7.1. <a name='problem-1'></a>problem
Require a common, unified interface to a disparate set of implementations or interfaces—such as within a subsystem—is required. There may be undesirable coupling to many things in the subsystem, or the implementation of the subsystem may change. What to do? 
####  3.7.2. <a name='Solution-1'></a>Solution
Define a single point of contact to the subsystem—::a facade object that wraps the subsystem::. This facade object presents a single unified interface and is responsible for collaborating with the subsystem components. 
![](assets/smd/Screen%20Shot%202019-10-27%20at%208.16.36%20pm.png)

####  3.7.3. <a name='UMLpackagediagram:Facade'></a>UML package diagram: Facade
![](assets/smd/Screen%20Shot%202019-10-27%20at%208.17.19%20pm.png)
```java
public class Sale { 	public void makeLineItem( ProductDescription desc, int quantity ) { 
		SalesLineItem sli = new SalesLineItem( desc, quantity ); 		// call to the Facade 		if ( POSRuleEngineFacade.getInstance().isInvalid( sli, this ) ) 
			return; 
		lineItems.add( sli ); 
		} // … 
} 
```

####  3.7.4. <a name='Example:FacadeVs.GRASPController'></a>Example: Facade Vs. GRASP Controller 
![](assets/smd/Screen%20Shot%202019-10-27%20at%208.19.35%20pm.png)

####  3.7.5. <a name='Example:FacadeVs.Adapter'></a>Example: Facade Vs. Adapter
- **Façade**wraps access to a ::subsystem or system:: with ::a single object:: 
- **Adaptor**wraps each API with ::varying interface:: to provide a single interface 


###  3.8. <a name='Observeraka.Publish-Subscribe'></a>Observer (aka. Publish-Subscribe)
####  3.8.1. <a name='Problem-1'></a>Problem
Different kinds of ::subscriber objects:: are interested in the ::state changes or events:: of a ::publisher object::, and ::want to react in their own unique way:: when the ::publisher generates an event::. Moreover, the publisher wants to maintain low coupling to the subscribers. What to do? 

####  3.8.2. <a name='Solution-1'></a>Solution
Define a “subscriber” or “listener” interface. Subscribers implement this interface. The publisher can dynamically register subscribers who are interested in an event and notify them when an event occurs. 
![](assets/smd/Screen%20Shot%202019-10-27%20at%208.23.45%20pm.png)

####  3.8.3. <a name='Example-1'></a>Example 

![](assets/smd/Screen%20Shot%202019-10-27%20at%208.28.08%20pm.png)
![](assets/smd/Screen%20Shot%202019-10-27%20at%208.28.38%20pm.png)

####  3.8.4. <a name='CodingExample-1'></a>Coding Example
ObserverBase.java
```java
Public abstract class ObserverBase{
	public abstract void onEvent(String source, String name, String value); 
}
```
SubjectBase.java
```java
Public abstract class SubjectBase{
		protected ArrayList<ObserverBase> observers; public SubjectBase() { 
			this.observers = new ArrayList<ObserverBase>(); 
		} 
		public void addObserver(ObserverBase observer) {…} // Add an observer
		public void removeObserver(ObserverBase observer) {…} // Remove an observer
		public void publishEvent(String source, String name, String value) { 			for(ObserverBase observer: this.observers) { 
				observer.onEvent(source,name,value);
			} 
		}
}
```

Sale.java
```java
Public class Sale extends SubjectBase {
		public Sale() { 			//Call constructor function in SubjectBase 
			super(); 			//Do something else 
		} 
		public void addItem(SaleLineItem item) { 
			this.saleItems.add(item);
			double preDiscountTotal = getPreDiscountTotal(); 
			publishEvent("Sale","prediscount", Double.toString(preDiscountTotal )); 
		}
} 
```
In this case, when the method addItem been called, it will publish this state, called all the observers to do something.

TotalPriceObserver.java
```java
Public class TotalPriceObserver extends ObserverBase {
		public TotalPriceObserver(SubjectBase subject) {
			//the arg indicates that which subject this observer listen to 			subject.addObserver(this);
		} 
		@Override
		public void onEvent(String source, String name, String value) { 
			//Do something
		}
} 
```

Therefore in the main, everytime init a new Subject, it needs to init a new Observer as well, and it will register the subject as its “listen to” target. Then each time the addItem method in the Subject been called, the observer will get notified and do some operations automatically.

Main.java
```java
Public class Main {
		Sale s = new Sale();
		new TotalPriceObserver(s);
} 
```

####  3.8.5. <a name='Example:AlarmEventsdifferentSubscribers'></a>Example: Alarm Events, different Subscribers
![](assets/smd/Screen%20Shot%202019-10-27%20at%208.44.50%20pm.png)



##  4. <a name='StateMachine'></a>State Machine
A *state machine*describes the behaviour of an object in terms of 
	- *events*that affect the object and
	- the *state*of the object between events. 
###  4.1. <a name='Definitions:'></a>Definitions:
*Event:*
	- a significant or noteworthy occurrence. 
*State:*
	- condition of the object at a moment in time. 
*Transition:*
	- directed relationship between two states such that an event can cause the object to change from the prior state to the subsequent state. 
 *state-dependent object:*
	- Reacts differently to events depending on the object’s state 
*state-independent object:*
	- For all events of interest, an object always reacts to the event the same way 
*state-independent w.r.t. an event:*
	- Always responds to event the same way 

###  4.2. <a name='HOWTOAPPLYSMD'></a>HOW TO APPLY SMD
**Guideline 1:**consider state machines for state- dependent objects with complex behaviour. 
	-  model behaviour of complex reactive objects 

**Guideline 2:**complex state-dependent classes are less common for business information systems, and more common in communications and control applications. 

**Complex Reactive Objects**
	- Physical device controllers
	- Transactions and related Business Objects
	- Role Mutators (objects that change role) 

**Protocols and Legal Sequences**
	- Communications Protocols
	- UI Page/Window Flow, Navigation, or Session
	- Use Case Operation Sequencing 


###  4.3. <a name='TransitionActionandGuardExample'></a>Transition Action and Guard Example
![](assets/smd/E32506F8-DBF1-4F8D-BB3F-D5C8219EEA27.png)
![](assets/smd/Screen%20Shot%202019-10-26%20at%208.03.21%20pm.png)
####  4.3.1. <a name='ChoicePseudo-state'></a>Choice Pseudo-state
![](assets/smd/Screen%20Shot%202019-10-26%20at%208.13.55%20pm.png)
![](assets/smd/Screen%20Shot%202019-10-26%20at%208.14.15%20pm.png)  

Another example:
When a timer reaches 60 seconds, the crossing light becomes “Red”
![](assets/smd/83C10211-0528-4D9E-87B8-0ABA87EAA9BB.png)

###  4.4. <a name='NestedStates'></a>Nested States
![](assets/smd/39F2D23C-F85C-4323-B94C-57C28FAC9721.png)

##  5. <a name='ArchitecturalAnalysisandLogicalArchitecture'></a>Architectural Analysis and Logical Architecture
###  5.1. <a name='SoftwareArchitecture'></a>Software Architecture
- The set of ::significant decisions:: about the ::organisation of a software system::
- the selection of ::the structural elements:: and the ::interfaces by which the system is composed::
- their ::behaviour:: as specified in the collaborations among those elements 
- the composition of these structural and behavioural elements into progressively larger subsystems
- the architectural style that guides this organisation

###  5.2. <a name='ArchitecturalAnalysis'></a>Architectural Analysis
We should do some architectural analysis of the requirements at the beginning to avoid more impact in the future.

- Concerned with identifying and resolving system’s ::non-functional requirements:: in the context of its functional requirements 考虑系统的非功能性需求，联系它的功能性需求
- includes identifying and analysing:
	- architecturally significant requirements
	- variation points
	- potential evolution points
- reduces risk of missing a ::critical factor:: in system design, focuses effort on ::high priority requirements::, and aligns the product with business goals

####  5.2.1. <a name='Examples:SignificantFunctionalrequirements'></a>Examples: Significant Functional requirements
Significant functional requirements 
![](assets/smd/Screen%20Shot%202019-10-28%20at%204.05.30%20pm.png)

####  5.2.2. <a name='Example:SignificantNon-FunctionalRequirements'></a>Example: Significant Non-Functional Requirements
![](assets/smd/Screen%20Shot%202019-10-28%20at%204.07.18%20pm.png)

###  5.3. <a name='IdentificationandResolution'></a>Identification and Resolution
- effect of reliability/fault-tolerance requirements on design?
	- remora service failure r to local?
- effect of re-use components licencing costs on profit?
	- excellent DB server for 2% of sales?
- effect of adaptability/configurability requirements on design? 
	- business rule variations: user customise, or charge them
- effect of brand name and branding on architecture? 
	- protected variation: name, logos, icons, …

###  5.4. <a name='Example:NewLMSRequirenment'></a>Example: New LMS Requirenment
Which of the following requirements for new LMS is architecturally significant?
- The system must record the submission history of each student
- The system must deploy on PC and Linux 
- A list of students will be retrieved from the Uni enrolment system

###  5.5. <a name='CommonSteps'></a>Common Steps
1. Identify/analyse architectural factors: requirements with impact on the architecture (especially non-functional)
	- overlaps with requirements analysis
	- some identified/recorded during inception, now investigated in more detail
2. For the architectural factors, analyse alternatives and create solutions: architectural decisions
	1. E.g. remove requirement
	2. Custom solution
	3. Stop project
	4. Hire expert
###  5.6. <a name='Priorities'></a>Priorities 
1. Inflexible constraints
	1. Safety, security, legal compliance
2. Business goals
	1. Demo for clients, trade-show in 18 months
	2. Competitor-drivers window-of-opportunity
3. Other goals
	1. Requirements all related back to higher-level goals, and eventually to business goals
	2. E.g. extendible -> new release every 6 months

###  5.7. <a name='ArchitectureFactorTable'></a>Architecture Factor Table
A documentation that records ::the influence of the factors, their priorities, and their variability:: (immediate need for flexibility and future evolution) 

![](assets/smd/Screen%20Shot%202019-10-28%20at%204.22.51%20pm.png)
###  5.8. <a name='TechnicalMemo'></a>Technical Memo
A documentation that records ::alternative solutions, decisions, influential factors, and motivations:: for the noteworthy issues and decisions 

![](assets/smd/Screen%20Shot%202019-10-28%20at%204.24.14%20pm.png)
![](assets/smd/Screen%20Shot%202019-10-28%20at%204.24.28%20pm.png)

##  6. <a name='LogicalArchitecture'></a>Logical Architecture
![](assets/smd/Screen%20Shot%202019-10-28%20at%204.27.40%20pm.png)

**Logical architecture:** 
	- The large-scale organisation of the software classes into packages, subsystems and layers
	- Logical: not concerned with networking, physical computers, or operating system processes 
**Layer:**
- Coarse-grained grouping of classes, packages, or subsystems that has cohesive responsibility for a major aspect of the system.

###  6.1. <a name='LayeredArchitecture'></a>Layered Architecture 
- Example layers:
	- **User Interface.** 
	- **Application Logic and Domain Objects**—software objects representing domain concepts (*Sale*class) that full fill application requirements. 
	-  **Technical Services—**general purpose objects and subsystems that provide supporting technical services (e.g., interfaces with DB) 
- **Strict layered architecture:**A layer only calls upon the services of the layer directly below it (e.g., a network protocol stack), not common in information systems 
- **Relaxed layered architecture:**A higher layer calls upon several lower layers. Common in IS. 

####  6.1.1. <a name='Example:UMLPackageDiagramNotations:Layer'></a>Example: UML Package Diagram Notations: Layer
![](assets/smd/Screen%20Shot%202019-10-28%20at%204.31.38%20pm.png)
Use the package to break the responsibilities and achieve high coupling 

####  6.1.2. <a name='Example:Commonlayers'></a>Example: Common layers
![](assets/smd/Screen%20Shot%202019-10-28%20at%204.33.10%20pm.png)

###  6.2. <a name='Guidelines:'></a>Guidelines:
- Organise large-scale logical structure of system into distinct cohesive layers from high application specific to low general services 
	- Maintain separation of concerns, 
	- e.g. No application logic in UI objects 
- Collaboration and coupling from higher layers to lower layers. Lower to higher layer coupling is avoided. 
- Don’t Show External Resources as the Bottom Layer 

####  6.2.1. <a name='MixingViewsofthearchitecture'></a>Mixing Views of the architecture
![](assets/smd/Screen%20Shot%202019-10-28%20at%204.34.41%20pm.png)
####  6.2.2. <a name='SystemSequenceDiagramandLayers'></a>System Sequence Diagram and Layers
![](assets/smd/Screen%20Shot%202019-10-28%20at%204.35.00%20pm.png)
####  6.2.3. <a name='UsingLayersHelpsAddressProblems'></a>Using Layers Helps Address Problems 
- Changes rippling through system due to coupling
- Intertwining of application logic and UI, reducing reuse and restricting distribution options 
- Intertwining of ::general tech. services or business logic:: with application specific logic, reducing reuse, restricting distribution, and complicating replacement 
- ::High coupling:: across areas of concern, impacting division of development work 

##  7. <a name='ModellingandDesignintheSoftwareprocess'></a>Modelling and Design in the Software process
UP - Unified Process
###  7.1. <a name='Schedule-OrientedTermsinUP'></a>Schedule-Oriented Terms in UP
![](assets/smd/Screen%20Shot%202019-10-28%20at%204.43.01%20pm.png)

###  7.2. <a name='Inception'></a>Inception 开始
Initial short project phase answering questions like:
	- What is the vision and business case for this project?
	- Feasible?
	- Buy and/or build?
	- Rough unreliable range of cost: $10K–100K or $xM?
	- Should we proceed or stop? 
####  7.2.1. <a name='Outcome:'></a>Outcome:
	- Common vision and basic scope for the project
	- creation of a business case 
	- analysis of ~10% of use cases
	- analysis of critical non-functional requirements
	- preparation of the development environment
	- prototypes: clarify requirements or technique questions
	- go or no go decision
####  7.2.2. <a name='InceptionArtefactsPartial'></a>Inception Artefacts (Partial) 人工
![](assets/smd/Screen%20Shot%202019-10-28%20at%205.04.36%20pm.png)

###  7.3. <a name='RequirementstoDesign-Iteratively'></a>Requirements to Design - Iteratively
- Iteratively Do the Right Thing, Do the Thing Right
	- Requirements: do the right thing (validation)
	- Design: Do the thing right (verification)
- Provoking Early Change
	- Don’t just passively "embrace change”
- Didn’t all that analysis & modelling take weeks?
	- A few hours or days: use case writing, domain modelling
	- Mixed into a few weeks: proof-of-concept development, finding resources, planning, setting up the environment …. 

####  7.3.1. <a name='SpreadingUseCasesacrossIterations'></a>Spreading Use Cases across Iterations
![](assets/smd/Screen%20Shot%202019-10-28%20at%205.09.54%20pm.png)


###  7.4. <a name='AgileModellingLightweightUMLDrawing'></a>Agile Modelling & Lightweight UML Drawing
- Modelling with other developers
- Static and dynamic models
	- class and interaction diagrams
	- create several models in parallel
- Hand draw
	- White boards, digital captures …
- UML tool
	- IDE integration, reverse or round trip (class and interaction diagrams)

###  7.5. <a name='ObjectDesignSkillvs.UMLDrawingSkill'></a>Object Design Skill vs. UML Drawing Skill
- UML models should reflect decision making about the design
- UML models should use correct notaion as a principle of communication 
- However, of ::greatest importance is object design skill::, not UML drawing skill
- Object design requires knowledge of 
	- principles of responsibility assignment
	- design patterns