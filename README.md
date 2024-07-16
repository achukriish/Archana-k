# Archana-k
# Analysis of sceneries using knowledge representation 
# INTRODUCTION:
# In Artificial Intelligence our focus is to make a machine intelligent. If we want a machine to be intelligent enough to have a dialogue with us in natural language, then first the machine needs to become knowledgeable about the real world. AI can enable a machine to be knowledgeable through propositional logic.
# However, a machine can’t understand our language, so the knowledge of the real world needs to be represented to the machine in the right manner that is readable to a computer system. Propositional logic is one of the simplest methods of knowledge representation to a machine.
# Propositional logic in Artificial Intelligence is one of the many methods of how knowledge is represented to a machine so that its automatic learning capacity can be enhanced. Knowledge Representation and Logic are imperative for building smart machines that can perform tasks that typically require human intelligence. We will implement the proposition logic in python to solve the problem.

# EXAMPLE PROBLEM:
# Consider the following sentences:
# 1. If it didn’t rain, Harry visited Hagrid today.
# 2. Harry visited Hagrid or Dumbledore today, but not both.
# 3. Harry visited Dumbledore today.

# Based on these three sentences, we can answer the question “did it rain today?”, even though none of the individual sentences tell us anything about whether it is raining today. Here is how we can go about it: looking at sentence 3, we know Harry visited Dumbledore. Looking at sentence 2, we know Harry visited either Dumbledore or Hagrid, and thus we can conclude that,
# 4. Harry did not visit Hagrid.

# PYTHON CODE TO BE IMPLEMENTED:
from logic import *   
rain = Symbol("rain")
hagrid = Symbol("hagrid")  
dumbledore = Symbol("dumpledore")
logical_sentence = And(rain, hagrid) 
print(logical_sentence.formula())     
implication_logic = Implication(Not(rain), hagrid) 
print(implication_logic.formula())
knowledge_base = And(Implication(Not(rain), hagrid),

   Or(hagrid, dumbledore),

   Not(And(hagrid,dumbldore)),hagrid)
print(knowledge_base.formula())

print(model_check(knowledge_base, rain))
 
# CONCLUSION  :
# We can develop our AI agent by implementing the code given above.AI agents will take the natural language as text and will generate new knowledge without being explicitly programmed.  
