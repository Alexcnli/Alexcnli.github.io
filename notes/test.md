Checking Liveness Properties of PR Systems  

Let 𝐶∥𝑈𝑛 be the PR system with controller process 𝐶and 𝑛user processes 𝑈  
Let 𝑓 be a liveness property of 𝐶and 𝐴¬𝑓an automaton that accepts all runs that do not satisfy 𝑓  
Let 𝑉𝐴𝑆𝑆(𝐶,𝑈𝑖,𝐴¬𝑓)be the configuration space of the VASS constructed from 𝐶,𝑈 and 𝐴¬𝑓, with 𝑖explicit copies of 𝑈. We call a configuration of this VASS an accepting configuration if it contains an accepting state of 𝐴¬𝑓  

Lemma:  
There is an 𝑛∈ℕand a run of 𝐶∥𝑈𝑛that does not satisfy 𝑓iff 𝑉𝐴𝑆𝑆𝐶,𝑈0,𝐴¬𝑓has an infinite run that contains infinitely many accepting configurations.  

Proof idea:  
⇒: follows from the ability of the VASS to „load“ a system of size 𝑛and correctly simulate the run  
⇐: follows from the fact that the VASS has to „load“ a system of some size 𝑛and then correctly simulates a run (and from the properties of 𝐴¬𝑓  

Lemma:  
𝑉𝐴𝑆𝑆(𝐶,𝑈𝑖,𝐴) has an infinite run with infinitely many accepting configurations iff it has a finite path of the form 𝛼𝛽with the following properties:  
1. 𝛼 starts in the initial configuration  
2. 𝛽 is a cycle, i.e., it starts and ends in the same configuration  
3. except for the first configuration of 𝛽, no configuration appears more than once on 𝛼𝛽  
4. a final configuration appears in 𝛽  
   
Proof idea:  
follows from the fact that there are only finitely many accepting states of 𝐴, and, even though 𝑉𝐴𝑆𝑆(𝐶,𝑈𝑖,𝐴) is an infinite state system, after the initialization it simulates asystem of fixed size 𝑛.
Therefore, any infinite run must contain repetitions, and any run that visits infinitely many accepting configurations can be partitioned into the form 𝛼𝛽𝜔with the properties above.  

Let 𝑝 = |(𝑄𝐶 ∪ {𝑞𝑖𝑛𝑖𝑡}) × (𝑄𝑈)^𝑖 × 𝑄𝐴| and 𝑚= |𝑄_𝑈|  

Lemma:  
There exists a finite path of 𝑉𝐴𝑆𝑆𝐶,𝑈𝑖,𝐴of the form 𝛼𝛽with the properties from the preceding Lemma iff there exists such a path of length at most 2^(𝑘⋅𝑝⋅log𝑝⋅2^(𝑘⋅𝑚⋅log𝑚)), for some constant 𝑘  
(length of the path follows from how many configurations we can see without a repetition)  

Theorem:  
The PMCP for PR systems with finite state processes and properties defined as Büchi automata is decidable (in time exponential in 𝑄𝐶and 𝐴and doubly exponential in 𝑄𝑈  

Corollary:  
There exists a cutoff for the PMCP of PR systems and properties defined by a Büchi automaton 𝐴, where 𝑈,𝐶 and 𝐴are of bounded size.  
(or, alternatively: the cutoff depends on the size of 𝑈,𝐶 and 𝐴)  
