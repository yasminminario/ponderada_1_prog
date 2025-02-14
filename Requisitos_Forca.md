# Jogo da Forca

**Nome:** Yasmin Ingrid Silva Minário <br>
**Data:** 13 de fevereiro de 2025  <br>
**Turma:** T13 <br>
**Professor:** Jefferson de Oliveira Silva <br>
**Matéria:** Programação

## Contexto do Jogo
&nbsp;&nbsp;&nbsp;&nbsp;O jogo será em uma plataforma online onde os jogadores se conectarão remotamente e jogarão em tempo real. Um dos jogadores criará uma sala virtual que produzirá um código, e os outros jogadores inserirão essa chave para entrar na aplicação. O jogador que criar a sala (host) escolherá uma palavra, iniciando a seção de adivinhação dos outros jogadores. Haverá um sorteio para determinar a ordem em que os jogadores falarão as letras. Cada jogador digitará uma letra por rodada. Em um canto da tela principal, haverá um chat que permitirá fazer chutes da palavra. Cada jogador terá direito a três chutes por rodada. Caso ninguém acerte com apenas uma letra por jogador por rodada, os jogadores poderão chutar mais uma letra cada, na mesma ordem do primeiro chute. O jogador que ganhar acumulará pontos inversamente proporcionais ao número de letras que precisou para acertar. Após o término de uma sessão, os jogadores poderão escolher se querem participar de outra. Cada sessão terá no máximo 10 jogadores, incluindo o host.

## Requisitos Funcionais
- **RF01:** Os jogadores se conectarão remotamente e jogarão em tempo real.
  - **Descrição:** O jogo será totalmente online, permitindo que jogadores participem remotamente de uma mesma sessão de jogo. Para isso, o sistema disponibilizará a criação de salas privadas, onde um jogador atuará como host e compartilhará um código único para que os outros participantes ingressem. Esse recurso garante que apenas jogadores autorizados participem da sessão, evitando interferências externas.
  - **CA01:** O sistema deve permitir a criação de salas privadas e a entrada de jogadores por meio de um código único.
- **RF02:** O jogo terá uma interface intuitiva e fácil de usar, com botões de informação para grande parte dos botões da tela, além de contar com um tutorial no início.
  - **Descrição:** A experiência do usuário será uma prioridade no desenvolvimento do jogo. Para isso, haverá um tutorial interativo que será exibido na primeira vez que um usuário acessar o jogo. Além disso, botões de informação estarão disponíveis para esclarecer funcionalidades específicas da interface.
  - **CA02:** O tutorial deve ser exibido na primeira vez que o usuário acessar o jogo e poder ser reativado a qualquer momento.
- **RF03:** O jogo terá uma interface acessível.
  - **Descrição:** Para garantir que todos os jogadores possam aproveitar a experiência, a interface será projetada com suporte a tecnologias assistivas. O jogo será compatível com leitores de tela, oferecerá atalhos de teclado para navegação e permitirá ajustes de contraste e tamanho de fonte. Isso acaba tornando o jogo inclusivo.
  - **CA03:** Deve suportar leitores de tela e atalhos de teclado para facilitar a navegação.
  - **CA04:** Deve permitir ajuste do contraste e tamanho da fonte para usuários com problemas visuais.
- **RF04:** O jogo será responsivo.
  - **Descrição:** A plataforma será projetada para oferecer uma experiência otimizada independentemente do dispositivo utilizado pelo jogador. A interface se adaptará automaticamente a diferentes tamanhos de tela, garantindo que o jogo funcione sem problemas em desktops, tablets e smartphones.
  - **CA05:** A interface deve se adaptar corretamente a diferentes tamanhos de tela (desktop, tablet e celular).
- **RF05:** O jogo terá um sistema de ranking para mostrar os melhores jogadores ao final da partida.
  - **Descrição:** Para incentivar a competitividade e engajamento entre os participantes, o jogo contará com um ranking que exibirá os melhores jogadores de cada sessão. A pontuação será calculada de forma inversamente proporcional ao número de letras necessárias para acertar a palavra.
  - **CA06:** O ranking deve exibir os jogadores daquela partida da ordem da maior pontuação para a menor.
- **RF06:** O jogo terá notificações para informar os jogadores sobre eventos importantes durante a partida.
  - **Descrição:** Para manter todos os jogadores informados e garantir fluidez na experiência, o jogo contará com notificações em tempo real que alertarão os jogadores quando for sua vez de jogar, indicarão o fim de uma rodada e exibirão mensagens enviadas no chat.
  - **CA07:** O sistema deve exibir notificações para avisar sobre a vez de um jogador, fim de rodada e mensagens do chat.

## Requisitos Não Funcionais
- **RNF01:** O sistema deve ser escalável para suportar um grande número de jogadores simultâneos.
  - **Descrição:** A arquitetura do sistema deve ser projetada para escalar conforme a demanda, evitando atrasos ou falhas durante as partidas. Para garantir essa robustez, testes de carga serão realizados para verificar o número máximo de jogadores simultâneos que o sistema suporta.
  - **CA01:** Testes de carga devem comprovar que o sistema suporta pelo menos X jogadores simultâneos sem queda de desempenho.
- **RNF02:** O tempo de resposta do sistema deve ser inferior a 2 segundos para qualquer ação do usuário.
  - ** Descrição:** Qualquer ação do jogador, como chutar uma letra, enviar mensagens no chat ou atualizar o ranking, deve ser processada rapidamente. Um tempo de resposta inferior a 2 segundos evita frustrações e garante que a interação com o jogo seja dinâmica.
  - **CA02:** Nenhuma ação do usuário (chutar uma letra, enviar mensagem no chat, atualizar ranking) deve demorar mais que 2 segundos para refletir na interface.
  - **CA03:** Testes de desempenho devem comprovar que o tempo de resposta médio está abaixo desse limite.
- **RNF03:** O sistema deve ser compatível com os principais navegadores (Chrome, Firefox, Safari, Edge).
  - **Descrição:** Para garantir acessibilidade a um público amplo, o jogo será desenvolvido de forma a ser compatível com os navegadores mais utilizados. Isso evita problemas de compatibilidade que poderiam impedir certos jogadores de acessar a plataforma.
  - **CA04:** O jogo deve funcionar sem erros em todos os navegadores suportados.
  - **CA05:** Testes de compatibilidade devem ser realizados antes do lançamento.
- **RNF04:** O sistema deve passar por testes para garantir a ausência de bugs críticos antes do lançamento.
  - **Descrição:** Terá testes unitários, de integração e de aceitação para identificar e corrigir possíveis bugs. Esse processo garante que o jogo funcione conforme esperado e evita problemas que possam comprometer a experiência do usuário.
  - **CA06:** Deve haver um plano de testes abrangente, incluindo testes unitários, integração e aceitação.
- **RNF05:** O sistema deve ter alta disponibilidade.
  - **Descrição:** O tempo de inatividade planejado não deve ultrapassar 0,1% do tempo total de operação, garantindo que os usuários possam acessar o jogo sempre que quiserem. Além disso, um plano de recuperação será implementado para lidar rapidamente com falhas inesperadas, minimizando o impacto de eventuais problemas técnicos.
  - **CA08:** O tempo de inatividade planejado não deve ultrapassar 0,1% do tempo total de operação.
  - **CA09:** O sistema deve contar com um plano de recuperação em caso de falha.

Fontes: [Games of Codes - Requisitos Corrigido](https://memoria.ifrn.edu.br/bitstream/handle/1044/2060/Games_of_Codes-Requisitos-Corrigido.pdf?sequence=1&isAllowed=y)

Além disso, foi utilizado o Copilot para ajuda com a definição de Critérios de Aceite dos Requisitos Não Funcionais e correção gramatical do texto.