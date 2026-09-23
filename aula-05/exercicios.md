 **1. Descreva os cinco passos do fluxo de contribuição, do clone ao merge, indicando o artefato produzido em cada um.**
   
Resposta:  
•	Clone: baixa o repositório para a máquina local.  
Artefato: uma cópia local do repositório.  
•	Branch: cria uma branch para trabalhar sem alterar diretamente a main.
Artefato: uma nova branch.  
•	Commit e push: faz as alterações, registra com commits e envia a branch para o GitHub.  
Artefato: commits publicados no repositório remoto.  
•	Pull Request: abre um PR para solicitar que as alterações sejam revisadas e incorporadas à branch principal.  
Artefato: Pull Request.  
•	Revisão e merge: outras pessoas revisam o código e, se estiver tudo certo, o PR é integrado à main.  
Artefato: código integrado na branch principal.  
 
**2. Um pull request tem título «alterações», nenhuma descrição e 38 arquivos alterados. Liste o que falta para torná-lo revisável e explique o risco de aprová-lo assim.**
   
Resposta:  
Falta um título mais específico, uma descrição explicando o que foi alterado e por quê, informações sobre como testar, e, se necessário, indicar issues relacionadas. Também seria importante verificar se os 38 arquivos realmente precisam fazer parte do mesmo PR.
Aprovar dessa forma é arriscado porque o revisor pode não entender o objetivo das alterações nem conseguir verificar facilmente se elas estão corretas. Além disso, um PR muito grande e sem contexto aumenta a chance de algum problema passar despercebido.
 
**3. Escreva um comentário de revisão adequado para um trecho que ignora o caso de lista vazia, indicando se é bloqueante ou sugestão.**
   
Resposta:  
Bloqueante: Este trecho não trata o caso em que a lista está vazia. Isso pode causar um erro durante a execução. Sugiro verificar se a lista possui elementos antes de acessar o primeiro item.  
É bloqueante porque o problema pode fazer o programa falhar em uma situação válida.
 
**4. Justifique cada uma das quatro regras de proteção da branch principal em termos do problema que ela evita.**
   
Resposta:  
•	Exigir Pull Request: evita alterações diretas na main sem revisão.  
•	Exigir aprovação de revisão: evita que alterações com problemas sejam integradas sem que outra pessoa as analise.  
•	Exigir verificações/status checks: evita integrar código que não passou pelos testes ou pelas verificações automáticas.  
•	Exigir branch atualizada antes do merge: evita integrar uma alteração baseada em uma versão antiga da main, reduzindo problemas de conflito ou incompatibilidade. 
 
**5. Traduza para comandos gh as seguintes ações: criar issue, abrir PR, trazer PR do colega para a máquina e aprovar a revisão.**
   
Resposta:  
Criar uma issue:
gh issue create
Abrir um Pull Request:
gh pr create
Trazer o PR do colega para a máquina:
gh pr checkout NUMERO_DO_PR
Aprovar a revisão:
gh pr review NUMERO_DO_PR --approve
 
**6. Compare GitHub Flow, Git Flow e trunk-based indicando em que contexto cada um é adequado.**
   
Resposta:  
•	GitHub Flow: utiliza branches curtas e Pull Requests. É adequado para projetos que fazem mudanças frequentes e usam revisão de código antes do merge.  
•	Git Flow: possui várias branches, como develop, feature e release. É adequado para projetos que possuem ciclos de lançamento mais definidos e precisam organizar versões.  
•	Trunk-based: os desenvolvedores trabalham em branches muito curtas ou diretamente próximas da branch principal, integrando alterações frequentemente. É adequado para equipes que fazem integração contínua e possuem bons testes automatizados. 
 
**7. Explique por que revisão por pares é considerada uma prática de qualidade e não um mecanismo de controle sobre as pessoas.**
   
Resposta:  
A revisão por pares tem como objetivo melhorar a qualidade do código e do projeto, identificando erros, problemas de segurança, dificuldades de manutenção e possíveis melhorias antes que as alterações sejam integradas. O foco está no trabalho produzido, e não em controlar ou julgar a pessoa que escreveu o código. Além disso, a revisão permite que os integrantes compartilhem conhecimento e aprendam uns com os outros.
