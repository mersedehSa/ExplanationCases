
<p align="center">
  <img src="taxonomy.jpg">
</p>

# Training

_Training_ covers the situations when users would like to know about some concepts, operations, and mechanics of the system or a component of the system mainly to learn how to operate with the system. Accordingly, the required explanation are generic and user-independent expositions of functions and components of a system (e.g., tool documentation for tech-savvy users or user manual for ordinary users).

# Interaction 
_Interaction_ motivation covers the situations where some intelligent behaviors of the system are not understandable, desirable, or expected by the user <sup>[[1]](#1)</sup>. Hence, to steer the human-system interaction, the system should provide some explanations to clarify (e.g., the reason behind some actions or decisions), instruct (e.g., the required input or steps by users to proceed), and/or convince (e.g., that a decision or suggestion is valid, relevant and useful) the user <sup>[[2]](#2),[[3]](#3)</sup>. Like the _Training_ motivation, the primary recipients of the _Interaction_ category's explanations are end-users engaging with the system. However, here the confusion is directly linked to the course of actions made by the user, the context of the use, and the system's state. Accordingly, the required explanation must be derived per case. Furthermore, since the lack of adjusted explanation leaves the user baffled or disinterested and hinders further interactions, the explanation must be built dynamically at runtime. 
## Disobedience
Most often, the situation that users attempt to command a system and the system does not respond and execute the order leaves users baffled. In many cases, however, such disobedience is indeed not simply breaking the rules, but it occurs because the system is following some other rules or goals which are not very obvious for the user at that moment, or it is incapable of accomplishing the instructions due to some constraints or system conditions. In the following, we present the more specific Disobedience cases.
<details>
  <summary> <b> Conflicts </b> </summary>

* __Goal-Order Conflicts__: It is when the users have set up a rule that might conflict with their will at particular conditions or moments. In such cases, the system may decide to prioritize the predefined goal(such prioritization could be based on user-defined rules or some intelligent algorithm of the system) instead of the direct command and act consequently. It hence may compel the system to avoid performing orders by the user.
  
  Scenario:
  
  >It is 7 pm, and there is a pile of dirty dishes in the dish washer. Bob would like to wash them before dinner but the dish washer does not start after Bob had     turned it on. The reason is that the _Smarthome Manager_ has deactivated the dish washer because Bob has set up a rule to reduce the electric  consumption at peak times (usually from 6 to 9 pm).

* __Multi User Conflict__: 
In a smart environment with multiple users, such as the smart home or smart office, every user may have its own goals and preferences, which may conflict with other user’s actions at some conditions or moments. Hence, the _Smarthome Manager_ needs to resolve such a conflict by prioritizing one user’s goals or activities over the other one. In such a situation, the user whose command has been rejected in favor of other users’ goals might be confused.

  Scenario:

  >Bob wants to roll up the window blinds to brighten the living room, but the system declines because Alice is watching a movie with a projector.

</details>

<details>
    <summary> <b> Contextual Conditions </b> </summary>
Sometimes the system chooses to avoid following a user's command due to its contextual awareness and comprehensive knowledge. The system may anticipate that the ordered action may lead to some undesirable situation or concludes the requested operation is not the best possible course of action in compliance with some rules, goals, or user preferences. 

<br> Scenario:

> Bob receives a notification on his phone from the washing machine saying that the washing is completed. Bob then commands Coco, his assistance robot, to collect the clothes and hang them on the rack on the balcony. Coco, however, does not move to the washing machine. Bob repeats the order again but still no response from Coco! He is wondering if something is wrong with Coco! However, Coco's behavior is due to its awareness of the high chance of rain in the next few hours!

</details>

<details>
    <summary> <b> System Conditions </b> </summary>

Sometimes, the system cannot perform the user’s order because of the absence of some prerequisites that involve the user’s actions to be addressed, but the user is oblivious. In this case, an explanation is necessary to bring such demands to the attention of the users.

<br>Scenario: 

> Alice is attempting to make a coffee, but the coffee machine does not start to prepare one, which makes her annoyed. It is because the coffee machine is out of coffee beans, and it needs to be refilled.

</details>

## Failure  
Another category of naturally confusing situations is when the system is not responding correctly or is operating erroneously. Hence, the user requires some explanation to understand the cause of the error and some hints to return the system back to the normal conditions.

<details> 
    <summary> <b>  System Error </b> </summary>
<div style="text-align: justify"> The next category of naturally confusing situations is when the system is not responding, generates a wrong output or is operating erroneously. Hence, the user requires some explanation to understand the cause of the error and some hints to return the system back to the normal conditions to achieve the desired output. </div>   

<br> Scenario:

> Bob is in the kitchen and needs to clean up the floor. He turns on his robotic vacuum cleaner (Robo cleaner) using his smartphone application and directs it to the kitchen. But it is not arriving! Bob goes to check why and notices that the Robo cleaner is stuck and it is just spinning! It is because the bumper of the cleaner must be re-assembled.

</details>

<details> 
    <summary> <b> User Fault </b> </summary>
When the system fails to perform the expected behavior or generate the sought output because the user has not been following the system specification correctly, or s/he has done something wrong! In other words, in such a situation, the system has not made any mistake, but users perceive their fault as an error of the system.  

<br> Scenario:

> Alice is in a hurry and needs to print a document. To expedite the process, she remotely connects to the printer when she is near her office and sends the document to it via her phone. When she reaches the printer to collect the paper, she finds out the printer has been printed the document on A3 paper! She immediately sends another print command by her phone, and again the printer is printing it on A3 paper! Alice is frustrated by the erroneous functioning of the printer. However, it is happening because the printer setting on her phone is not on automatic paper tray selection, and it is following the previous configuration, which has been explicitly set to take A3 papers.

</details>

## Context Aware Behaviour 
<div style="text-align: justify"> 
Under this category, we analyze the situations where the intelligent behavior of the system is the source of confusion. So, users require some explanation to interpret the particular act of the system. In modern IoT systems and smart environments, the system often has a ubiquitous and comprehensive knowledge of other linked systems, environment as well as users' actions, goals, and preferences. It enables the system to learn users tastes and better recommend a suitable course of steps for the user to follow and to perform context-aware decisions and activities in various directions-- from home automation to personalized graphical user interface generation and context-aware access control for smart devices <sup>[[4]](#4),[[5]](#5)</sup>, to name a few--. Though the context-awareness of the system is meant to maximize user satisfaction and comfort, the autonomous and automated nature of decision making of the system or lack of transparency of reasons behind a particular recommendation may confound the users. Subsequently, some explanation can acquaint the user with the cause, purpose, and benefit of such suggestion and behavior of the system.  </div>   
<details> 
    <summary> <b> Suggestion </b> </summary>
One of the well-studied circumstances in the literature is when an intelligent system recommends to a user a particular item, product, or action to perform. Innately, it should clarify the motivation, reason and advantage of opting for such a thing or pursuing such action.

<br> Scenario:

  >Alice is going to bed when she receives a notification on her smartphone from the _Smarthome Manager_ suggesting to close all the opened windows of the house. It makes Alice wonder, due to which circumstance the system suddenly has drawn the conclusion to advise her to close the windows. "Is there some security threat?'' Alice whispers! The system, however, has suggested it based on the temperature drop reported by the outside thermostats and the weather forecast API’s alarm that it is going to be a cold and rainy night ahead. 
 
</details> 
<details> 
  <summary> <b> Autonomous Actions </b> </summary>
Another progressing trend in context-aware smart homes is toward reducing human assistance and making systems more autonomous. In this direction, for example, a self-adaptive system continuously monitors itself, the user, and the environment to learn and optimize rules which let the system autonomously adapt itself to the changing environment and user preferences and activities <sup>[[6]](#6) </sup>. As a result, the system gradually evolves, behaves more intelligently, and independently acts or decides upon something without waiting for users' permissions. Hence, a user is confronted with some already performed actions (or the consequence of performing such actions). Without some explanations, the activity itself, or its underlying cause and benefit might not be understandable for the user.

<br> Scenario:

  > Bob has invited a couple of his friends to a party in his home. Suddenly, at midnight, the system turns off a couple of lights, changes the light color of others to blue, lowers the volume of the Amazon Echo playing some music, and locks the main door! Everyone, including Bob, is surprised and wonders what happened! The system, however, just followed the newly adopted rule: to put the smart-home to "bedtime mode'' at midnight learned from Bob's routine in the last couple of weeks!

</details>

# validation
_Validation_ that constitutes a large portion of research on explainability, particularly in the domain of artificial intelligence and machine learning (ML). ML-based applications are opaque systems generating models (trained over some pair of input and outputs) that can predict the outputs of unseen inputs. ML algorithms, however, do not allow obtaining the reason behind such correlation of input data to the associated label. It is often argued that there is a trade-off between the performance and transparency of a model <sup>[[7]](#7)</sup>. 
The need for explanation stems from the desire and necessity of opening the model’s black box to interpret the model and validate its decisions. According to <sup>[[8]](#8)</sup>, the explanations are required to detect any bias in the training dataset, to highlight adversarial perturbation that affects the prediction and to assure the existence of a truthful causality in the model reasoning. In contrast to the _Training_ category, here explanations are extremely case dependent and the target audience are domain experts and model developers. 
# Debugging
_Debugging_ which is also case-dependent, is a particular situation for particular types of systems. It occurs when a system developer wants to trace back an error or fix the system itself or a product of the system by applying some changes on firmware, mechanics, or structure of the system (e.g., code debugging in IDEs). Therefore in _Debugging_ cases, as well as the _Validation_, the application of the explanations is in the post-mortem analysis of an executed program -either successfully or not-, hence the derivation and building process of such explanations do not happen at runtime.

It is worth highlighting that we distinguish this situation with a state where a system behaves anomalously either due to mistakes of users (e.g., wrong inputs) or lack of necessary resources (e.g., internet, permissions). There is another similar but yet distinct circumstance where a system can report some malfunctioning to inform the users even though the user personally cannot take any action to fix the problem (e.g., when the touch screen of the system is not responsive). We have categorized the situations mentioned above under the _Interaction_ motivation because the trigger for the required explanation is an anomaly that damages the trust and obstructs the regular communication of the user with the system. The user needs an explanation to understand the situation and address the issue so s/he can continue to interact with the system at that particular moment rather than repairing (or building) a system.


##### References

<sup> <a id="1">[1]</a>: Gregor, Shirley, and Izak Benbasat. "Explanations from intelligent systems: Theoretical foundations and implications for practice." MIS quarterly (1999): 497-530.

<sup> <a id="2">[2]</a> : Dhaliwal, Jasbir S. "An experimental investigation of the use of explanations provided by knowledge-based systems." PhD diss., University of British Columbia, 1993

<sup> <a id="3">[3]</a> : Hayes, Philip J., and D. Raj Reddy. "Steps toward graceful interaction in spoken and written man-machine communication." International Journal of Man-Machine Studies 19, no. 3 (1983): 231-284.s

<sup> <a id="4">[4]</a>: Baresi, Luciano, and Mersedeh Sadeghi. "Fine-grained context-aware access control for smart devices." In 2018 8th International Conference on Computer Science and Information Technology (CSIT), pp. 55-61. IEEE, 2018.

<sup> <a id="5">[5]</a> : SADEGHI, MERSEDEH. "A model-centered solution for taming the heterogeneity of smart devices." (2019).

<sup> <a id="6">[6]</a>: Klös, Verena, Thomas Göthel, and Sabine Glesner. "Comprehensible and dependable self-learning self-adaptive systems." Journal of Systems Architecture 85 (2018): 28-42.

<sup> <a id="7">[7]</a> : Došilović, Filip Karlo, Mario Brčić, and Nikica Hlupić. "Explainable artificial intelligence: A survey." In 2018 41st International convention on information and communication technology, electronics and microelectronics (MIPRO), pp. 0210-0215. IEEE, 2018

<sup> <a id="8">[8]</a> : Arrieta, Alejandro Barredo, Natalia Díaz-Rodríguez, Javier Del Ser, Adrien Bennetot, Siham Tabik, Alberto Barbado, Salvador García et al. "Explainable Artificial Intelligence (XAI): Concepts, taxonomies, opportunities and challenges toward responsible AI." Information Fusion 58 (2020): 82-115
