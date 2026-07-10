# 🏀 Hannah's Basketball

Projeto desenvolvido para a **Week 0** do curso **CS50x - Introduction to Computer Science (Harvard University)**.

O objetivo foi criar um jogo em Scratch aplicando os conceitos básicos de programação apresentados durante a primeira semana do curso.

---

# 🎮 Sobre o jogo

O jogador controla **Hannah**, movimentando-a pelo cenário para coletar diamantes enquanto interage com uma cesta de basquete. Durante o desenvolvimento, o foco não foi apenas terminar o jogo, mas compreender a lógica por trás de cada funcionalidade implementada.

---

# 🛠 Tecnologias

- Scratch
- Piskel (criação de sprites)

---

# 📚 Conceitos utilizados

- Eventos
- Loops (`forever` e `repeat`)
- Condicionais (`if`)
- Variáveis (pontuação)
- Blocos personalizados
- Parâmetros em blocos personalizados
- Colisão entre sprites
- Hitboxes
- Fantasias (Costumes)
- Animações
- Geração aleatória de posições
- Organização modular do código

---

# 📖 Diário de Desenvolvimento

## Planejamento

- Escolha do tema: basquete.
- Utilização da personagem **Hannah** da biblioteca do Scratch.
- Pesquisa sobre sprites e animações.
- Aprendizado sobre criação de sprites utilizando o Piskel.

### Aprendizados

- Diferença entre sprites e costumes.
- Como importar imagens para o Scratch.
- Organização inicial do projeto.

---

## Movimentação

Foi implementada a movimentação utilizando as teclas:

- W
- A
- S
- D

A lógica foi organizada em um bloco personalizado responsável apenas pelo movimento da personagem.

### Problema encontrado

O sprite continuava olhando para apenas um lado.

### Solução

Foi utilizado:

- Rotation Style → Left-Right
- Point in Direction

Assim o sprite passou a inverter corretamente sua direção durante a movimentação.

---

## Sistema de animação

Foi criada uma animação alternando entre duas fantasias da personagem.

Inicialmente a animação era ativada apenas quando alguma tecla era pressionada e posteriormente foi integrada ao sistema de movimentação.

---

## Área da cesta

Para detectar quando a personagem estava próxima da cesta, foi criada uma hitbox utilizando um sprite invisível.

### Problema encontrado

Ao utilizar o bloco `hide`, a colisão deixava de funcionar.

### Solução

O sprite passou a utilizar o efeito **Ghost (100)** em vez do bloco `hide`, permanecendo invisível sem perder a colisão.

### Aprendizados

- Diferença entre esconder um sprite e apenas deixá-lo invisível.
- Funcionamento das hitboxes no Scratch.

---

## Sistema de Spawn

Foi desenvolvido um sistema responsável por gerar diamantes em posições aleatórias.

Inicialmente foi utilizado:

- `go to random position`

### Problema encontrado

O diamante aparecia parcialmente fora da tela.

### Solução

A posição passou a ser controlada manualmente utilizando limites para os eixos X e Y.

---

## Validação do Spawn

Foi criada uma verificação para impedir que o diamante surgisse:

- sobre a personagem;
- sobre a área da cesta.

Durante esse processo foi necessário pensar na lógica de validação em vez de depender apenas da geração aleatória.

---

## Organização do código

O projeto começou com poucas instruções dentro de um único script.

Conforme novas funcionalidades foram adicionadas, a lógica foi dividida em blocos personalizados separados para:

- movimentação;
- animação;
- geração de diamantes;
- validação do spawn.

Isso tornou o projeto mais organizado e facilitou futuras modificações.

---

## Loops e WAIT

Um dos maiores aprendizados da Week 0 aconteceu ao perceber que o bloco:

```scratch
wait
```

interrompia a execução daquele script.

Durante o desenvolvimento foi necessário reorganizar o fluxo do programa para separar responsabilidades e evitar que determinadas ações fossem bloqueadas durante a espera.

Esse comportamento levou ao estudo de conceitos como:

- fluxo de execução;
- sincronismo;
- concorrência de tarefas.

Embora o Scratch simplifique esses conceitos, foi uma primeira experiência importante para compreender como programas executam diferentes tarefas.

---

## Blocos Personalizados

Após revisar os requisitos do projeto do CS50, foi criado um bloco personalizado com parâmetro.

```scratch
spawn diamonds(wait time)
```

O parâmetro permite controlar o tempo entre os spawns, tornando o bloco reutilizável para diferentes situações.

---

# 🚧 Dificuldades encontradas

- Inverter corretamente a direção da personagem.
- Entender a diferença entre `hide` e o efeito `ghost`.
- Criar uma hitbox funcional.
- Limitar o spawn dentro do cenário.
- Evitar spawn em posições inválidas.
- Compreender o funcionamento do bloco `wait`.
- Organizar melhor a lógica do projeto utilizando blocos personalizados.

---

# 💡 Principais aprendizados

Durante o desenvolvimento percebi que criar um jogo envolve muito mais do que utilizar blocos do Scratch.

Foi necessário aprender a dividir problemas em partes menores, organizar responsabilidades, pensar em fluxo de execução e validar diferentes estados do jogo.

Além dos conceitos apresentados nas aulas, o projeto proporcionou um primeiro contato com ideias que posteriormente aparecem em linguagens como C, Java e Python, como modularização, reutilização de código e parâmetros em funções.

---

# 🎯 Próximos passos

Após concluir este projeto, pretendo continuar o curso seguindo para a **Week 1**, onde o Scratch será substituído pela linguagem C, levando comigo os conceitos aprendidos nesta primeira etapa.
