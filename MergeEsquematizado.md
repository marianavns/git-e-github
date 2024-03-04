# Merge Esquematizado

## Cenário 1

Duas frentes, EquipeA e EquipeB, estão desenvolvendo a funcionalidadeA e a funcionalidadeB, respectivamente.


|     Tarefa     |     Comando     | 
|----------|----------|
| Equipe A faz uma branch a partir da main    | entrar na branch main e `git checkout -b funcionalidadeA`   | 
| Equipe B faz uma branch a partir da main    | entrar na branch main e `git checkout -b funcionalidadeB`   | 
| Equipe A desenvolve seu código    | ``` main main featA featA```  | 
| Equipe B desenvolve seu código    | ``` main main featB featB```  | 
| A funcionalidade A faz o merge da sua funcionalidade na main.   | entrar na branch main e `git merge funcionalidadeA`   | ``` main main featA featA```
| A funcionalidade B faz o merge em seguida, **mas precisa que o código da funcionalidade A não se perca**.    | entrar na branch main e `git checkout -b funcionalidadeB`   | 




 

