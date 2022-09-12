# Code Review
O code review é uma cultura de revisões, análise e constante evolução do código. Há inúmeros benefícios em adotar essa prática, como:  ter uma segunda visão sobre seu código, fazer o compartilhamento de features, bug fix e lógica usada. 

É interessante que o code review seja uma implementação fixa e constante, adotando como uma rotina permanente de evolução, Assim compartilhando conhecimento e entendendo o profissional que trabalha ao seu lado.

# Responsabilidades em um Code Review

## Autor

Aquele que escreve o código

- Escrever uma boa ChangeLog, com clareza e objetividade
- Commitar de maneira eficiente, pragmática e seguir algum tipo de [Flow](https://www.atlassian.com/br/git/tutorials/comparing-workflows/gitflow-workflow)
- Utilizar Git squash e rebase para uma melhor organização do fluxo de commits:
    - [https://medium.com/cwi-software/utilizando-rebase-e-squash-para-melhorar-o-histórico-do-git-fdb2d952c09c](https://medium.com/cwi-software/utilizando-rebase-e-squash-para-melhorar-o-hist%C3%B3rico-do-git-fdb2d952c09c)
    - [http://blog.abraseucodigo.com.br/git-squash-wtf.html](http://blog.abraseucodigo.com.br/git-squash-wtf.html)

## Revisor:

Responsável por analisar e sugerir melhorias 

- Fazer feedbacks colaborativos e principalmente construtivos
- Entender o Design do codigo: o processo pelo qual um agente desenvolve um código de modo a atender o requisito funcional também fazendo com que este mesmo código seja possível de ser mantido com o mínimo de dificuldade pelo próximo agente.
- Funcionalidade: certificar que o código se comporta da maneira exata que o autor afirmou
- Complexidade: entender se o código pode ter sua implementação de maneira mais simples, para outros devs que trabalhem usando esse código irão possam entender e fazer modificações no futuro
- Testes: garantir que o código é seguro

# ****Mensagens de commit****

Prefixe suas mensagens de confirmação com comandos imperativos como: `fix`, `refactor`, `add`e`remove`

Objetos gerais da mensagem em um commit:

- informar a outros desenvolvedores o que fará
- Introduzir o entendimento do que foi feito no código
- Transmitir uma mensagem sem exceder 50 caracteres.

Dentro de seus commits, você pode incluir uma descrição do commit, permitindo-nos adicionar ainda mais detalhes/contexto sobre o que você fez.

# E****stratégia de commit****

- ****Fazer commits pequenos e específicos:**** Commits menores facilitam a reversão do código para um estado anterior se houver um problema. Se o seu commit afetar muitas áreas, reverter pode significar perder muito código.

# P****ull Requests eficientes****

Alguns cuidados para que o objetivo da PR seja cumprido da melhor maneira possível: 

- enviar assim que o recurso ou bug atual estiver concluído.
- manter seus PR's pequenos, contendo apenas commits relacionados.
- commits que estão relacionados ao mesmo componente, é recomendável reuni-los em um PR.
- **Não deve** ir no mesmo PR quando há muita coisa acontecendo. Devem ser agrupados em vários PR's contendo commits relevantes no momento.
- Sempre mantenha seus PR's pequenos. Ninguém quer abrir caminho através de uma solicitação de pull de mais de 50 arquivos.

# ****Como revisar uma PR****

- O código segue as diretrizes de codificação da sua equipe?
- O código atende aos seus objetivos/critérios de aceitação?
- O código é legível e é fácil de entender o que está fazendo sem a necessidade de comentários/documentação pesados? (Este para mim é um dos mais importantes, pois sou um grande fã de funções descritivas e nomes de variáveis.)
- O código precisa de alguma refatoração, considerando segurança, desempenho ou simplesmente facilidade de leitura?
- O código segue padrões/princípios de design simples, como responsabilidade única, abstração, encapsulamento e assim por diante? Se não, você pode fazer sugestões sobre como isso pode ser alcançado ou talvez ensinar àqueles que não estão familiarizados com isso o que isso significa e os benefícios.
- Existem "números/strings mágicos" que seriam melhor servidos como uma constante ou variável nomeada?

## Não perca tempo em PRs

- Embora você não deva necessariamente se sentir obrigado a olhar para um PR imediatamente, também não deixe o autor pendurado.
- Fazer uma call e passar pelo PR juntos pode acelerar o processo e reduzir o tempo de espera.
- leia cada arquivo e altere com cuidado
- Você pode utilizar a [extensão](https://marketplace.visualstudio.com/items?itemName=GitHub.vscode-pull-request-github) para visualizar solicitações de pull e visualizar comentários enquanto verifica a PR tudo dentro do próprio VS Code.
- Um pull request não é um exame, também não é uma oportunidade para você criticar duramente o trabalho de alguém. É uma oportunidade de aprendizado e uma chance de garantir que o melhor código chegue ao branch principal.
- Como você está criticando um trabalho em que alguém provavelmente se esforçou muito, um comentário PR é o oposto de uma mensagem git commit. Não usamos mais a voz imperativa. Não os ordene a fazer mudanças, mas faça sugestões mais suaves usando o modo [subjuntivo](https://www.grammar-monster.com/glossary/subjunctive_mood.htm) .

## Sugestão de melhorias

- A maioria dos sistemas Git permite que você clique na linha que deseja alterar e adicione um comentário,
- Provedores de hospedagem, como o GitHub, têm um recurso de "sugestão" que permite adicionar uma sugestão de código diretamente no comentário, que pode ser instantaneamente aceita e confirmada a partir do PR.
- Lembre-se de um PR é uma discussão. É um processo de mão dupla, dando a você a oportunidade de defender seu código e explicar com mais contexto o que você estava pensando.
- Não tenha medo de oferecer contra-argumentos, mas esteja pronto com um raciocínio válido, se você realmente acredita em sua solução.
## artigos de referência
- [Git Best Practices – How to Write Meaningful Commits, Effective Pull Requests, and Code Reviews](https://www.freecodecamp.org/news/git-best-practices-commits-and-code-reviews/)
- [Como fazer um git squash para melhorar seu histórico de commits.](https://blog.novatics.com.br/como-fazer-um-git-squash-para-melhorar-seu-hist%C3%B3rico-de-commits-2a93835bfe8f)
- [Git smash](http://blog.abraseucodigo.com.br/git-squash-wtf.html)
