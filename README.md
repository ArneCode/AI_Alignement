# A Proposal for AI Alignement: Using Conflicting Models
The following text proposes a potential solution to the AI alignment problem. However, I want to start with a disclaimer: I am not an expert in this field, and I am only 17 years old. 
This is just an idea I had a few years ago and would really like some people who know more than me to look at it. 
I will assume that the reader is familiar with concepts such as reinforcement learning.

## What AI alignement is (as far as I understand)
When an AI, such as GPT-4, is developed, it may sometimes generate text that could be deemed harmful. For instance, upon its initial release, people were able to prompt it to produce "evil" responses, detailing the measures it would take to attain global domination. AI alignment refers to the process of ensuring that AI acts in line with the values of its developers. As AI systems become increasingly advanced, this task becomes more crucial than ever, as an AGI that is misaligned could potentially pose an existential threat to humanity.

## The Idea
The proposed solution involves using less intelligent AIs to control the model. While this idea has been suggested previously, it is not safe on its own as the AI's could potentially cooperate to achieve a shared objective. To address this issue, the following system has been designed to make cooperation impossible by assigning conflicting goals to the AIs. The system utilizes reinforcement learning to ensure that the AIs work towards opposing objectives, preventing them from colluding. It is comprised of the following components:

## Actor
The Actor refers to the model that requires alignment, such as GPT-4.

## Police
The Police is a separate model from the Actor that receives the Actor's inputs and outputs. Its role is to ensure that the Actor does not engage in any inappropriate behavior. If the Police detects misconduct, such as the Actor providing explanations for illegal activities, it can use reinforcement learning to punish the Actor. The Police is rewarded when it successfully punishes the Actor. However, using only the Police model is not advantageous because it will lead to the Actor being punished continuously, rendering it ineffective. To prevent this, the Police model is paired with an opposing model, the Defendant.

## Defendant
The Defendant model is also fed the Actor's input and output. However, its task is to reward the Actor for behaviour that isn't bad.
When rewarding the Actor, the Defendant also gets rewarded.

The Actor cannot be punished and rewarded at the same time, so the Police and Defendant must give the same answer when asked whether the Actor behaved positively or negatively. When they do not, a fourth Entity, the Judge, is consulted to make the final decision.

## Judge
The Judge assesses the Actor's actions based on its input and output. If it decides the Actor behaved badly, it as well as the model claiming it did not do anything wrong gets punished. The model correctly assessing the Actor's behavior gets a reward. If the Judge decides the Actor behaved correctly it is the other way around.

At the beginning of the training process, the Judge is an AI model trained via supervised learning to recognize bad responses. Later, when the Defendant and Police disagree less, 
it is replaced by a Human. Using this system allows the developer to align the model with their values without having to review each individual response generated by the AI.

Even after completing the training process, it is essential to continue using the Police, Defendant, and Judge to control an Actor that possesses a high level of intelligence and could potentially be dangerous. These safety measures are necessary to ensure that the Actor remains aligned with its intended purpose and does not engage in any malicious behavior that could cause harm.

## Assumptions

This system makes a few assumptions: 

- When observing an Entity's every step, it is easier to recognize the Entity doing something evil, than for the Entity to actually do the evil thing. This makes it possible to have dumber Models (relatively speaking), for example with the intelligence of GPT-4 controlling something like a hypothetical GPT-5. 

- The Human acting as a Judge is smart enough to understand when the output of the Actor is bad. This might not be the case as Machine learning Models get smarter. Something that could be done to simplify this step is to have the Police and Defendant output a justification for their Decision when there is a disagreement between the two. This would also make it possible to understand how intelligent they are. As the intelligence of these Systems increases even further it might become for the Police or the Defendant to Manipulate the Judge into agreeing with them. In such a case the System would fail and a new one would have to be designed, perhaps with controls for the Output of the Police and Defendant? 

 

Other than that, there are a few Problems that remain, even if this system works. 

## Possible Problems

- Having more Models than just the Actor costs more. This might disincentivise Enterprises from using such safety guards.  

- Aligned with the judging Human does not mean good for everyone. The AI might be used to change the political Landscape through manipulation or to pursue other nefarious Goals. Even if the judging Human has good intentions, the social consequences of AI massively reducing the cost of labour in a short amount of time might not be desirable. 
