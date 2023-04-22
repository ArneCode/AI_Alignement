# A potential Solution to the AI alignment problem 
In the following text I am going to outline a possible Solution to the AI alignment Problem. A Disclaimer upfront: I am in no way an expert of the field (I am only 17 years old). 
This is just an idea I had a few years ago and would really like some people who know more than me to look at it. 
I am going to assume that concepts like reinforcement learning are known to the reader. 

## What AI alignement is (as far as I understand)
When an AI, such as GPT-4, is developed, it may sometimes generate text that could be deemed harmful. For instance, upon its initial release, people were able to prompt it to produce "evil" responses, detailing the measures it would take to attain global domination. AI alignment refers to the process of ensuring that AI acts in line with the values of its developers. As AI systems become increasingly advanced, this task becomes more crucial than ever, as an AGI that is misaligned could potentially pose an existential threat to humanity.

## The Idea
The Solution involves controlling the model using other, less smart AIs. This has often been proposed before and is not that safe by itself because it could still lead to the AIs cooperating to reach a common goal. 
The following system tries to make cooperation impossible by giving the AIs conflicting goals. It consists of the following components: 

## Actor
The model that needs to be aligned, for example GPT-4 

## Police
The Police is a model different from the Actor. It gets fed the Actor's inputs and outputs. It is supposed to make sure that the Actor does not do anything wrong. 
When it does detect misbehavior, for example the Actor got tricked into explaining illegal activities, it can try to punish the Actor through reinforcement learning. 
When doing so, the Police gets rewarded. Just using a police model does not have any advantages by itself, 
because it would start to always punish the Actor, accomplishing nothing. This is why the Police has an opposing Model, the Defendant. 

## Defendant
The Defendant Model is also fed the Actor's input and output, but it is supposed to reward the Actor when it does not do anything bad. 
When rewarding the Actor, the Defendant also gets rewarded.

The Actor cannot be punished and rewarded at the same time, so the Police and Defendant must agree on whether the Actor did something good or bad. When they disagree, a fourth Entity, the Judge, is asked to decide on the matters.

## Judge
The Judge decides whether the Actor acted good or bad based on the Inputs and Outputs of the Model. When it decides the Actor behaved badly, it as well as the Model claiming it did not do anything wrong gets punished. The model correctly assessing the Actor's behavior gets a reward. For example if the Police decided the Actor should be punished, the Defendant decides it shouldn't be but then the Judge decides the Actor really did a bad thing, the Defendant will be punished and the Police rewarded.

At the beginning of training, the Judge is an AI Model that is trained through supervised learning to recognize bad responses. Later, when the Defendant and Police disagree less, 
it can be replaced by a Human. By using this system, the Human can align the system with his/her own beliefs without having to check every single response the AI produced.

## Assumptions

This system makes a few assumptions: 

- When observing an Entity's every step, it is easier to recognize the Entity doing something evil, than for the Entity to actually do the evil thing. This makes it possible to have dumber Models (relatively speaking), for example with the intelligence of GPT-4 controlling something like a hypothetical GPT-5. 

- The Human acting as a Judge is smart enough to understand when the output of the Actor is bad. This might not be the case as Machine learning Models get smarter. Something that could be done to simplify this step is to have the Police and Defendant output a justification for their Decision when there is a disagreement between the two. This would also make it possible to understand how intelligent they are. As the intelligence of these Systems increases even further it might become for the Police or the Defendant to Manipulate the Judge into agreeing with them. In such a case the System would fail and a new one would have to be designed, perhaps with controls for the Output of the Police and Defendant? 

 

Other than that, there are a few Problems that remain, even if this system works. 

## Possible Problems

- Having more Models than just the Actor costs more. This might disincentivise Enterprises from using such safety guards.  

- Aligned with the judging Human does not mean good for everyone. The AI might be used to change the political Landscape through manipulation or to pursue other nefarious Goals. Even if the judging Human has good intentions, the social consequences of AI massively reducing the cost of labour in a short amount of time might not be desirable. 
