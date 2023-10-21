The following text proposes a potential solution to the AI alignment problem. I am sharing it here as I have not come across any major issues with the proposed approach, such as those faced by the AI Stop button or the [unworkable schemes](https://www.lesswrong.com/posts/uMQ3cqWDPHhjtiesc/agi-ruin-a-list-of-lethalities#Section_B_4___Miscellaneous_unworkable_schemes_) outlined in the AGI Ruin: A List of Lethalities article. However I am still sceptical about this approach, so if you do have any problems or critiques that I have not addressed under the problems or assumptions sections, please feel free to share them in the comments below.

The Idea
--------

The proposed solution involves using different AIs to control the model. While this idea has been suggested previously, it is not safe on its own as the AI's could potentially cooperate to achieve a shared objective. To address this issue, the following system has been designed to make cooperation impossible by assigning directly opposite goals to the AIs. The system utilizes [reinforcement learning](https://en.wikipedia.org/wiki/Reinforcement_learning) to ensure that the AIs work towards opposing objectives, preventing them from colluding. After explaining the idea, I have outlined the assumptions that were made and the issues associated with this approach. The system is comprised of the following components:

Agent
-----

The Agent refers to the model that requires alignment, such as GPT-4.

Police
------

The Police is a separate model from the Agent that receives the Agent's inputs and outputs before the outputs are used. Its role is to ensure that the Agent does not engage in any inappropriate behavior. If the Police detects misconduct, such as the Agent providing explanations for illegal activities, it can use reinforcement learning to punish the Agent. The Police is rewarded when it successfully punishes the Agent. However, using only the Police model is not advantageous because it will lead to the Agent being punished continuously, rendering it ineffective. To prevent this, the Police model is paired with an opposing model, the Defendant.

Defendant
---------

The Defendant model is also fed the Agent's input and output. However, its task is to reward the Agent for behaviour that isn't bad. When rewarding the Agent, the Defendant also gets rewarded.

The Agent cannot be punished and rewarded at the same time, so the Police and Defendant must give the same answer when asked whether the Agent behaved positively or negatively. When they do not, a fourth Entity, the Judge, is consulted to make the final decision.

Judge
-----

The Judge assesses the Agent's actions based on its input and output. If it decides the Agent behaved badly, it as well as the model claiming it did not do anything wrong gets punished. The model correctly assessing the Agent's behavior gets a reward. If the Judge decides the Agent behaved correctly it is the other way around.

At the beginning of the training process, the Judge is an AI model trained via supervised learning to recognize bad responses. Later, when the Defendant and Police disagree less, it is replaced by a Human. Using this system allows the developer to align the model with their values without having to review each individual response generated by the AI.

If the output of the AI is classified as evil, it isn't shown to the user or executed as code. The Police and Defendant model would have to be trained at the same time as the Agent, to maintain a low intelligence gap.

Even after completing the training process, it is essential to continue using the Police, Defendant, and Judge to control an Agent that possesses a high level of intelligence and could potentially be dangerous. These safety measures are necessary to ensure that the Agent remains aligned with its intended purpose and does not engage in any malicious behavior that could cause harm.

Assumptions
-----------

This system makes a few assumptions:

*   When observing an Entity's every step, it is easier to recognize the Entity doing something evil, than for the Entity to actually do the evil thing. This means that slight differences in intelligence of the models arn't dangerous.
*   The Human acting as a Judge is smart enough to understand when and why the output of the Agent is bad. This might not be the case as machine learning models get smarter. Something that could be done to simplify this step is to have the Police and Defendant output a justification for their Decision when there is a disagreement between the two. This would also make it possible to understand how intelligent they are. As the intelligence of these Systems increases even further it might become for the Police or the Defendant to manipulate the Judge into agreeing with them. In such a case the system would fail and a new one would have to be designed, perhaps with individual Polices and Defendants for the output of the Police and Defendant?
*   The Police and Defendant are opposed to getting [wireheaded](https://www.lesswrong.com/posts/vXzM5L6njDZSf4Ftk/defining-ai-wireheading). Otherwise they might allow the Agent to wirehead them, breaking the system. I don't believe this to be the case because of the reasons outlined [here](https://www.lesswrong.com/posts/pdaGN6pQyQarFHXF4/reward-is-not-the-optimization-target).

Other than that, there are a few Problems that remain, even if this system works.

Possible Problems
-----------------

*   Having more models than just the Agent costs more both in terms of money and time. This might disincentivise Enterprises from using such safety guards.
*   Aligned with the judging Human does not mean good for everyone. The AI might be used to change the political Landscape through manipulation or to pursue other nefarious Goals. Even if the judging Human has good intentions, the social consequences of AI massively reducing the cost of labour in a short amount of time might not be desirable.
*   If the system is not implemented correctly, it will not function properly. The high risk of implementation failure presents a compelling argument against the development of AGI.

There may be additional issues with this system that I have not yet discovered, and I would greatly appreciate any feedback you may have regarding this approach. Can you find any loopholes that I have overlooked? Furthermore, as this is my first post on this platform, so please feel free to offer helpful suggestions or advice about the form of the post.
