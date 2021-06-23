
# Training

_Training_ covers the situations when users would like to know about some concepts, operations, and mechanics of the system or a component of the system mainly to learn how to operate with the system. Accordingly, the required explanation are generic and user-independent expositions of functions and components of a system (e.g., tool documentation for tech-savvy users or user manual for ordinary users).

# Interaction 
_Interaction_ motivation covers the situations where some intelligent behaviors of the system are not understandable, desirable, or expected by the user. Hence, to steer the human-system interaction, the system should provide some explanations to clarify (e.g., the reason behind some actions or decisions), instruct (e.g., the required input or steps by users to proceed), and/or convince (e.g., that a decision or suggestion is valid, relevant and useful) the user. Like the _Training_ motivation, the primary recipients of the _Interaction_ category's explanations are end-users engaging with the system. However, here the confusion is directly linked to the course of actions made by the user, the context of the use, and the system's state. Accordingly, the required explanation must be derived per case. Furthermore, since the lack of adjusted explanation leaves the user baffled or disinterested and hinders further interactions, the explanation must be built dynamically at runtime. 
<details>
    <summary> Disobedience </summary>
    

  #### [Conflicts](Conflicts.md)
   - [Goal Order Conflict](Goal_Order_Conflict.md)
   - [Multi User Conflict](Multi_User_Conflict.md)

  #### [Contextual Conditions](Contextual_Conditions.md)

  #### [System Conditions](System_Conditions.md)
  
</details>

<details>
    <summary> <a href="Failure.md">Failure</a> </summary>
  
  [more](Failure.md)
  #### [System Error](System_Error.md)
  
  #### [User Fault](User_Fault.md)
  
</details>

<details>
    <summary> Context Aware Behaviour </summary>
    
## [Context Aware Behaviour](Context_Aware_Behaviour.md)
### [Suggestion](Suggestion.md)
  
### [Autonomous Actions](Autonomous_Actions.md)
</details>

# validation
_Validation_ that constitutes a large portion of research on explainability, particularly in the domain of artificial intelligence and machine learning (ML). ML-based applications are opaque systems generating models (trained over some pair of input and outputs) that can predict the outputs of unseen inputs. ML algorithms, however, do not allow obtaining the reason behind such correlation of input data to the associated label. It is often argued that there is a trade-off between the performance and transparency of a model~\cite{dovsilovic2018explainable}. 
The need for explanation stems from the desire and necessity of opening the model’s black box to interpret the model and validate its decisions. According to~\cite{arrieta2020explainable} the explanations are required to detect any bias in the training dataset, to highlight adversarial perturbation that affects the prediction and to assure the existence of a truthful causality in the model reasoning. In contrast to the \emph{Training} category, here explanations are extremely case dependent and the target audience are domain experts and model developers. 
# Debugging
_Debugging_ which is also case-dependent, is a particular situation for particular types of systems. It occurs when a system developer wants to trace back an error or fix the system itself or a product of the system by applying some changes on firmware, mechanics, or structure of the system (e.g., code debugging in IDEs). Therefore in \emph{Debugging} cases, as well as the \emph{Validation}, the application of the explanations is in the post-mortem analysis of an executed program -either successfully or not-, hence the derivation and building process of such explanations do not happen at runtime.

It is worth highlighting that we distinguish this situation with a state where a system behaves anomalously either due to mistakes of users (e.g., wrong inputs) or lack of necessary resources (e.g., internet, permissions). There is another similar but yet distinct circumstance where a system can report some malfunctioning to inform the users even though the user personally cannot take any action to fix the problem (e.g., when the touch screen of the system is not responsive). We have categorized the situations mentioned above under the \emph{Interaction} motivation because the trigger for the required explanation is an anomaly that damages the trust and obstructs the regular communication of the user with the system. The user needs an explanation to understand the situation and address the issue so s//he can continue to interact with the system at that particular moment rather than repairing (or building) a system.
