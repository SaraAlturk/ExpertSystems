Expert Systems 
==========

The ExpertSystem.ipynb File contains an example of tourism activities recommandation system 


Defining expert systems
========================
An expert system is a program capable of pairing up a set of **facts** with a set of **rules** to those facts, and execute some actions based on the matching rules.
facts and rules are fundamental components used to represent knowledge and make decisions within an expert system.

KnowledgeEngine
---------------
a fundamental class used to define the core of an expert system. 
It is responsible for managing the rules and facts, making inferences, and generating recommendations or decisions based on the available knowledge.

1. `facts`  used by the system to reason about the problem.
2. `rules` The @Rule decorator is used to define rules in your expert system. Each rule consists of conditions and actions.
   Conditions are defined using facts and their slots to specify when the rule should be triggered.
   
   For a Rule to be useful, it must be a method of a `KnowledgeEngine` subclass
   
   Rule conditions specify when a rule should be triggered.they're created using logical operators like AND, OR, NOT, and fact instances with   their slots.
   
   Rule actions specify what should happen when a rule is triggered.
3. 

process to execute a KnowledgeEngine.
-------------------------------------
1. The class must be instantiated     engine = name() # Create an instance of the expert system
2. The reset method must be called # engine.reset()
4. Declare all facts yielded by the methods decorated with @DefFacts. # engine.declare()
5.The run method must be called. This starts the cycle of execution. # engine.run()

