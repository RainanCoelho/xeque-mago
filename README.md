# Xeque-Mago

Estratégia de turnos em voxel: cada jogador tem um **Mago**, que é o rei, e um exército de bonecos.
Derrube o Mago inimigo para vencer, sem perder o seu.

![Arena](imagens/02_arena.png)

## Baixar e jogar (Windows)

1. Abra a aba **[Releases](../../releases/latest)** e baixe `XequeMago-v0.4-windows.zip`.
2. Extraia o zip numa pasta.
3. Rode `XequeMago.exe`. Os dois arquivos (`.exe` e `.pck`) precisam ficar na mesma pasta.

Se o Windows mostrar "O Windows protegeu o computador", clique em **Mais informações → Executar assim mesmo**
(o jogo ainda não é assinado digitalmente).

Requisitos: Windows 10 ou 11 (64 bits) e placa de vídeo com Vulkan.

## Modos

- **Tutorial**: ensina a andar, atacar, quebrar a torre do escudo e derrubar o Mago, passo a passo
- **Contra a CPU**
- **Dois jogadores** no mesmo computador, passando a vez

## Tutorial

![Tutorial](imagens/09_tutorial.png)

## Como funciona

![Guarda do Mago](imagens/03_guarda_do_mago.png)

- **Guarda do Mago.** Cada Mago começa dentro de uma cúpula de energia, atrás de 5 pilares de cristal.
  Com a guarda de pé, ele não ataca, mas os poderes de suporte (cura, escudo, potencializar, mudar o
  terreno) alcançam a arena inteira. Quebre um pilar e a guarda desmorona: o Mago passa a atacar.
- **Totens de flanco.** Enquanto os dois totens de um lado estão de pé, o Mago desse lado não leva dano.
  Para vencer, é preciso ir pelos flancos.
- **Santuários.** O boneco que chega a um santuário dourado escolhe uma bênção que vale até o fim da partida:
  **Ataque** (+2 de dano), **Defesa** (defende com 3 a menos no dado) ou **Velocidade** (+1 casa por movimento).
  Cada boneco recebe uma bênção por partida.
- **Dado de 20 lados.** Todo ataque rola um d20 contra um mínimo calculado pelos atributos; o alvo rola a defesa.

![Duelo de dados](imagens/04_duelo_de_dados.png)

## Classes

Cada boneco tem **1 golpe de dano** (fraco e com condição), **4 golpes de efeito** e **uma passiva**.

| Classe | Bonecos | Papel |
|---|---|---|
| Tanque | Golem, Minotauro, Yeti, Titã de Lava | Aguenta golpes, segura a linha, protege |
| Assassino | Lobo Sombrio, Salamandra, Verme das Dunas | Entra pelos flancos e finaliza |
| Atirador | Arqueira Élfica, Goblin Catapulta | Age de longe e muda o terreno |
| Suporte | Árvore Anciã, Fantasma, Geomante, Maga das Marés | Cura, fortalece e controla |

![Classes e golpes](imagens/05_classes_e_golpes.png)

Na escolha do exército, o botão **!** ao lado de cada boneco abre a ficha dele: classe, passiva, atributos e golpes.

![Ficha do boneco](imagens/10_ficha.png)

## Mapas e eventos aleatórios

Cinco mapas, cada um com 3 eventos. Cada evento é anunciado uma rodada antes num cartaz no meio da tela, com as casas
atingidas marcadas em vermelho; quando acontece, aparece o efeito no tabuleiro (chuva, neve, areia, pedras caindo...)
e, se durar mais de uma rodada, um aviso no canto mostra quantas rodadas faltam:

| Mapa | Eventos |
|---|---|
| Floresta Antiga | Névoa Fina, Raízes Vivas, Chuva de Verão |
| Dunas de Âmbar | Tempestade de Areia, Sol a Pino, Areia Movediça |
| Pântano Sombrio | Maré Cheia, Névoa do Brejo, Esporos |
| Picos Gelados | Nevasca, Geada, Avalanche |
| Caverna Cristalina | Desabamento, Cristal Ressonante, Escuridão |

![Evento: névoa](imagens/06_evento_nevoa.png)

![Lago](imagens/08_lago.png)

## Controles

- **W A S D**: mover a câmera
- **Botão esquerdo + arrastar**: girar
- **Roda do mouse**: aproximar
- **Botão direito**: voltar um passo
- **Esc**: menu

## Feedback

Jogou? Conte o que achou na aba **[Issues](../../issues)**: o que ficou confuso, o que está forte ou fraco demais,
bugs e ideias. Prints ajudam muito.

---

Versão 0.4 (protótipo). Feito com Godot 4.5. Este repositório traz apenas o jogo para download;
o código-fonte não está público.
