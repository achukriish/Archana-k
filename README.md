# Archana-k
# Analysis of sceneries using knowledge representation 
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
