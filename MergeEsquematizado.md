# Merge Esquematizado

## Cenário 1

Duas frentes, EquipeA e EquipeB, estão desenvolvendo a funcionalidadeA e a funcionalidadeB, respectivamente.


|     Tarefa     |     Comando     | 
|----------|----------|
| A equipe funcionalidade A faz uma branch a partir da main    | entrar na branch main e `git checkout -b funcionalidadeA`   | 
| A equipe funcionalidade B faz uma branch a partir da main    | entrar na branch main e `git checkout -b funcionalidadeB`   | 
| A equipe funcionalidade A desenvolve seu código    |    | 
| A equipe funcionalidade B desenvolve seu código    |    | 
| A funcionalidade A faz o merge da sua funcionalidade na main.   | entrar na branch main e `git merge funcionalidadeA`   | 
| A funcionalidade B faz o merge em seguida, **mas precisa que o código da funcionalidade A não se perca**.    | entrar na branch main e `git checkout -b funcionalidadeB`   | 




 

