1.	Explique as três áreas do Git e diga qual comando move um arquivo entre cada par delas.

O Git possui três áreas: Working Directory, onde os arquivos são modificados; Staging Area, onde são selecionadas as alterações que irão para o commit; e Repository, onde ficam armazenados os commits. O comando “git add” move as alterações do Working Directory para a Staging Area. O comando “git commit” move as alterações da Staging Area para o Repository.

2.	Reescreva as mensagens de commit a seguir de modo que sirvam a quem lê o histórico: «ajustes», «agora foi», «correções diversas».

- «ajustes» → Ajusta validação do formulário de cadastro.
- «agora foi» → Corrige erro no cálculo do total.
- «correções diversas» → Corrige problemas na tela de login e no menu.

3.	Um colega pergunta por que não pode simplesmente fazer um commit por dia com tudo o que mexeu. Responda em cinco linhas.

Fazer um único commit por dia pode juntar várias alterações diferentes e dificultar o entendimento do histórico.
Commits menores facilitam identificar o que foi alterado.
Também fica mais fácil descobrir quando surgiu um problema.
Além disso, é possível voltar para uma versão anterior com mais facilidade.
Por isso, o ideal é fazer commits pequenos, frequentes e com mensagens claras.

4.	Explique por que ocorre um conflito, o que significa cada um dos três delimitadores inseridos pelo Git e quais passos resolvem a situação.

Um conflito ocorre quando duas alterações diferentes são feitas na mesma parte de um arquivo e o Git não consegue decidir automaticamente qual deve permanecer. O “<<<<<<< HEAD” indica o início da versão atual, o “=======” separa as duas versões e o “>>>>>>>” indica o fim da outra versão. Para resolver, é preciso abrir o arquivo, escolher ou combinar as alterações, remover os delimitadores, salvar o arquivo, executar “git add” e depois fazer o “git commit”.

5.	Liste cinco tipos de arquivo que não devem ser versionados e explique o risco específico de cada um.

- “.env” — pode conter senhas, tokens e chaves de API.
- Arquivos de senhas — podem expor credenciais de acesso.
- Chaves privadas (“.pem”, “.key”) — podem permitir acesso não autorizado a sistemas.
- Arquivos de banco de dados locais — podem conter dados pessoais ou informações sensíveis.
- Arquivos temporários e logs — podem expor informações desnecessárias e deixar o repositório desorganizado.

6.	Uma credencial foi commitada por engano e removida no commit seguinte. Explique por que isso não é suficiente e o que deve ser feito.

Remover a credencial no commit seguinte não é suficiente porque ela continua registrada no histórico do Git e pode ser recuperada. Primeiro, a credencial deve ser revogada ou substituída, pois deve ser considerada comprometida. Depois, é necessário remover o segredo do histórico do repositório com uma ferramenta apropriada, como “git filter-repo”.

7.	Explique por que gestão de configuração é pré-requisito para testes automatizados e para qualquer forma de auditoria.

A gestão de configuração permite controlar e identificar as versões do código, arquivos e configurações utilizadas. Isso é importante para testes automatizados porque permite reproduzir os testes em uma versão conhecida do sistema. Sem esse controle, os resultados podem mudar devido a alterações não registradas. Para auditorias, também é necessário saber quem fez uma alteração, quando ela ocorreu e qual era a versão anterior. Por isso, a gestão de configuração garante rastreabilidade e controle das mudanças.
