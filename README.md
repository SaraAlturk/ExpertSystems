Rule-Based Expert System
========================

The ExpertSystem.ipynb File contains an example of tourism activities recommandation system -


Defining expert systems
========================
An expert system is a program capable of pairing up a set of **facts** with a set of **rules** to those facts, and execute some actions based on the matching rules.
facts and rules are fundamental components used to represent knowledge and make decisions within an expert system.

*There are three main components of an expert system*
The KnowledgeEngine, Database and User Interface 

![Structure-of-a-Rule-based-Expert-System](https://github.com/SaraAlturk/ExpertSystems/assets/105989428/d79e1b98-f2d6-47be-978b-b050d4f1e04a)

KnowledgeEngine
---------------
a fundamental class used to define the core of an expert system. 
It is responsible for managing the rules and facts, making inferences, and generating recommendations or decisions based on the available knowledge.

**The Knowledge base:**

   `rules` The @Rule decorator is used to define rules in your expert system. Each rule consists of conditions and actions. IF(condition) THEN (ACTION)
   Conditions are defined using facts and their slots to specify when the rule should be triggered.
   
   For a Rule to be useful, it must be a method of a `KnowledgeEngine` subclass
   
   Rule conditions specify when a rule should be triggered.they're created using logical operators like AND, OR, NOT, and fact instances with   their slots.
   
   Rule actions specify what should happen when a rule is triggered.
   
Database
--------

includes a set of facts used to match against the IF (condition) parts of rules stored in the knowledge base.

`facts`  are used by the system to reason about the problem.

process to execute a KnowledgeEngine.
-------------------------------------
1. The class must be instantiated     engine = name() # Create an instance of the expert system
   
2. The reset method must be called # engine.reset()
   
3. Declare all facts yielded by the methods decorated with @DefFacts. # engine.declare()
   
4. The run method must be called. This starts the cycle of execution. # engine.run()

InferenceEngine
---------------
carries out the reasoning whereby the expert system reaches a solution.
It links the rules in the KB with facts in the DB to make deductions and reach conclusions.

InferenceEngine has two methods for acquiring information from the knowledge base:

(1) Forward chaining 

(2) Back chaining 

UserInterface
---------------
This is the part of the expert system that end users interact with to get an answer to their question or problem.
