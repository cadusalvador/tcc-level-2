# ANXIA QUESTS
Plataforma gamificada para auxiliar pessoas jovens no combate ao sedentarismo e problemas com ansiedade.

# 🤯 O problema 

O comportamento sedentário atinge cerca de 60% dos jovens e este estilo de vida ocioso vem aumentando com o uso e auxilio das tecnologias como computadores, smartphones, tablets, reduzindo momentos de lazer com práticas de atividades físicas. Este comportamento pode potencializar a experimentação dos aspectos negativos da ansiedade, causando prejuizos fisicos e mentais para os adolescentes. O que nos leva a dois pontos:

- Como incentivar jovens a terem uma rotina de vida mais saudável?
- Como adequar o cérebro para manter-se nessa rotina?

# 💡 Proposta de Solução
### Visão Geral🧐

Jane McGonigal desenvolveu uma técnica para “gamificar” seu cotidiano de fisioterapia e recuperação: criou uma espécie de sistemas de pontos e premiação para se auto motivar a melhorar e cumprir as tarefas que eram sugeridas pelos médicos.
Os jogadores completam missões, derrotam bandidos, recrutam aliados e alcançam vitórias épicas relacionadas à saúde mental, bem-estar e outros objetivos de vida. A nossa proposta é criar um sistema equivalente ao que foi descrito no livro de Jane, trazendo mais interatividade para os players, mais organização nas tarefas e trazer formas de lidar com problemas de saúde de uma forma divertida.

# 🔌Integração
A integração ocorrerá via banco de dados. Será recebido uma carga de dados de:

### Pessoa/Usuario
- desafios
- amigos

# ⚙️ Funcionalidades 

## A pessoa faz cadastro (Must Have).

- Apelido
- Nome Completo
- Email
- Senha

## A pessoa faz login(Must Have).

- Email
- Senha

## A pessoa pode ver suas tarefas diárias(Must Have).

Um painel deve mostrar 5 tarefas diárias em niveis diferentes de dificuldade, podendo variar entre fácil, média e difícil [enum].

A pessoa poderá escolher a tarefa que quer realizar naquele momento 

No próximo dia, as tarefas serão diferentes

## A pessoa pode marcar uma quest como concluida(Must Have).

O usuário pode marcar uma quest como concluida recebendo uma quantidade de resiliência (pontos).

## A pessoa vai ser recompensada com pontos para concluir tarefas(Must Have).

A quantidade de resiliência recompensada depende da dificuldade da tarefa.

- Fácil: 20 pts de resiliência
- Médio: 50 pts de resiliência
- Difícil: 100 pts de resiliência.

## A pessoa pode ver sua evolução(Must Have).

Um histórico de atividades será salvo para cada usuário e ao ser consultado mostra um resumo com base num prazo definido.

Dados do resumo:
- Pontos de resiliência ganhos
- Quantidade de missões realizadas

## A pessoa poderá se juntar a outros amigos e aliados para realizar missões(Must Have).

O usuário pesquisa dentro da aplicação o apelido de um amigo para que eles possam
realizar atividades juntos.

O auto-relacionamento se dará por uma tabela "amizade", com o usuário solicitante
e o usuário que recebe a solicitação.

A amizade possui dois estados correspondentes a um enum na entidade: SOLICITADA ou ATIVA.

O usuário pode responder aceitando ou não a amizade; caso sim, elas podem compartilhar
atividades juntas, sendo bonificadas com maior pontuação por isso.

## A pessoa poderá se comunicar por chat(Must Have).  

Haverá um chat para que as pessoas possam compartilhar suas experiências durante o uso da aplicação

O chat não salvará o histórico da conversa entre as pessoas

O chat utilizará o websocket Socket.io

# 💾 Backlog

## A pessoa poderá capacidade de adicionar seus próprios power-ups e missões(Nice to Have).

Conforme a criatidade e as necessidades do usuário, ele mesmo pode definir
novos power-ups e missões que queira realizar, utilizando os dados aos responder um formulário:

- Título [String]
- Descrição da atividade [String/Text area no Front]
- Nível de dificuldade (no caso da missão) [enum]

## Impulso

A pessoa escreve algo específico que ela espera nos próximos dias ou semanas. Não precisa estar relacionado ao seu desafio ou Vitória Épica – qualquer coisa que ela esteja esperando conta.
- Título [String]
- Descrição do que ela aguarda[String/Text area no Front]

