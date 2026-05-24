Explicação Completa do Projeto Snake em C# WPF

EXPLICAÇÃO COMPLETA DO JOGO SNAKE EM C# WPF

1. MAINWINDOW.XAML
Esse arquivo monta a interface visual do jogo.
Define:
- janela
- grid
- textos
- overlay
- aparência

<Window ... >
Define que essa janela pertence à classe MainWindow.

Configurações:
- Title = título da janela
- Height/Width = tamanho
- MinWidth/MinHeight = tamanho mínimo
- Background/Foreground = cores
- WindowStartupLocation = centraliza a janela
- Icon = ícone da aplicação

Eventos:
- PreviewKeyDown = captura tecla antes do processamento
- KeyDown = captura teclas normais

Viewbox:
Permite redimensionamento automático.

Grid:
Layout principal.

RowDefinition:
Cria linhas no layout.

ScoreText:
Mostra a pontuação.

GridBorder:
Borda do jogo.

GameGrid:
Grade do jogo.

Overlay:
Tela escura inicial/game over.

OverlayText:
Texto da tela.

2. GAMESTATE.CS
Responsável pela lógica do jogo.

Propriedades:
- Rows/Cols = tamanho do mapa
- Grid = matriz do jogo
- Dir = direção atual
- Score = pontuação
- GameOver = fim do jogo

Listas:
- dirChanges = fila de direções
- snakePositions = posições da cobra

Construtor:
Inicializa jogo, cobra e comida.

Funções:

AddSnake()
Cria a cobra inicial.

EmptyPositions()
Retorna posições vazias.

AddFood()
Adiciona comida aleatória.

HeadPosition()
Retorna cabeça.

TailPosition()
Retorna cauda.

SnakePositions()
Retorna posições da cobra.

AddHead()
Adiciona nova cabeça.

RemoveTail()
Remove cauda.

GetLastDirection()
Retorna última direção.

CanChangeDirection()
Impede movimentos inválidos.

ChangeDirection()
Muda direção.

OutsideGrid()
Verifica se saiu do mapa.

WillHit()
Verifica colisão.

Move()
Função principal:
- move cobra
- detecta colisão
- adiciona comida
- aumenta score
- detecta game over

3. MAINWINDOW.XAML.CS
Controla interface e renderização.

Dicionários:
- gridValToImage = imagens do grid
- dirToRotation = rotação da cabeça

Variáveis:
- rows/cols = tamanho do mapa
- gridImages = imagens da tela
- gameState = estado do jogo
- gameRunning = evita múltiplos jogos

Funções:

MainWindow()
Inicializa janela.

RunGame()
Executa o jogo.

Window_PreviewKeyDown()
Inicia jogo.

Window_KeyDown()
Controla teclas.

GameLoop()
Loop principal.

SetupGrid()
Cria grade visual.

Draw()
Atualiza tela.

DrawGrid()
Desenha grade.

DrawSnakeHead()
Desenha cabeça.

DrawDeadSnake()
Animação de morte.

ShowCountDown()
Mostra 3,2,1.

ShowGameOver()
Mostra game over.

RESUMO:
- XAML = interface visual
- GameState.cs = lógica
- MainWindow.xaml.cs = controle visual e teclado

