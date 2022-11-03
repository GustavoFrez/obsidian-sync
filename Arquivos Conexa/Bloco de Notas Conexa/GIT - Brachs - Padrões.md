1 - Fazer a tarefa
2 - Abrir um PR pra master e um PR pra qa
3 - Enviar o PR da master pra Code Review
4 - Com Code Review aprovado, faz o merge do PR de qa e roda a pipeline
5 - Quando a tarefa passar pelo QA e for a deploy, enviar PR pro Tech Lead|

feat: (novo recurso para o usuário, não um novo recurso para script de compilação)
fix: (correção de bug para o usuário, não uma correção para um script de compilação)
docs: (alterações na documentação)
style: (formatação, falta de ponto e vírgula, etc; sem alteração do código de produção)
refactor: (refatorando o código de produção, por exemplo, renomeando uma variável)
test: (adicionando testes ausentes, testes de refatoração; nenhuma alteração no código de produção)
chore: (atualizando tarefas grunt etc; sem alteração de código de produção)

[prefixos para branches e commits]

feat, fix, chore, style, refactor e test

[padrões de nome de branch]

(prefixo)/(card da tarefa)-(nome)

ex:

feat/PA-1221-new-signup-form

chore/MS-2223-lint-configuration

[padrões de commit]


(prefixo): (mensagem)

ex:

style: removing TODO comments

feat: adding new input icon

refactor: changing Input made 

test: implement modal tests 