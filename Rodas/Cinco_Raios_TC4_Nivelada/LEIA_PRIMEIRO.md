# Roda de cinco raios estilo TC4 — NIVELADA COM A BORDA EXTERNA ORIGINAL

Desenho de cinco raios largos inspirado na fotografia da TC4, sem logotipos ou inscrições. Não é uma réplica medida do produto da foto.

Esta variante usa a borda externa original do aro, em Z=-2,30 mm, como referência. Os raios, o miolo e a tampa ficam nesse mesmo plano. A versão aprovada de sete raios continua salva separadamente. A cor grafite nas imagens é somente uma representação; use o filamento/cor de sua preferência.

## Medidas e verificações

Diâmetro máximo: 56,5955 mm, incluindo os detalhes originais de retenção do pneu. Largura axial final: 26,00 mm. Os 0,55 mm de diferença em relação às opções anteriores vêm da retirada da saliência frontal; o assento externo do pneu, o encaixe traseiro e a posição de apoio do parafuso não foram deslocados.

Furo de eixo original: 4 mm. Hexágono traseiro: 12,4 mm entre faces. Entrada do hexágono em Z=-17,30 mm e fundo em Z=-12,30 mm. A geometria original do cubo até Z=-10,301 mm foi comparada por diferença de volumes: resultado zero.

O nivelamento foi medido nas próprias superfícies do STL final, no miolo, em dois pontos dos raios, na borda original e na tampa. Todos ficaram em Z=-2,30 mm, dentro da tolerância numérica de 0,001 mm. VALIDACAO.json contém os resultados. PERFIL_NIVELAMENTO.png mostra uma seção do STL com a linha de referência.

## Impressão e fixação

Imprima STL_IMPRESSAO/Roda_TC4_Nivelada.stl. É uma peça única e fechada, centralizada e com a borda traseira em Z=0. Ela precisa de suportes sob o miolo/raios; confira no fatiador e evite suportes aderidos ao hexágono e ao furo central.

O acesso ao parafuso tem 10 mm de diâmetro acima do apoio original. A tampa central é opcional e vem separada: STL_IMPRESSAO/Tampa_Central_Opcional.stl. Sua face lisa fica na mesa e o anel para cima. Na montagem, ela fica nivelada com a borda. A folga radial nominal é de 0,2 mm. Teste antes de aplicar uma pequena quantidade de adesivo removível somente nas bordas, mantendo o acesso ao parafuso.

Imprima e teste uma roda antes do jogo completo. As unidades foram interpretadas como milímetros. Não houve teste físico de encaixe, impressão, resistência ou rodagem.

## CAD e referência

CAD/Face_TC4_CAD_Nativo.step é somente a nova face, não a roda completa nem um aplique para encaixar na roda antiga. A base funcional continua derivada da malha original. CAD/Tampa_Central_Opcional.step contém a tampa completa.

REFERENCIA/Roda_TC4_Posicao_Original.stl contém a mesma roda completa nas coordenadas do STL original para comparação no CAD. Não imprima junto com a outra posição da roda.

IMAGENS contém vistas do CAD final, comparação com a opção aprovada de sete raios e corte de perfil. A tampa é mostrada nivelada na posição de montagem.

FONTES contém o script e requirements.txt. Em Python 3.12, instale as dependências, coloque seu Standar_Wheel.stl junto do script e execute criar_tc4.py. O STL de entrada não é redistribuído neste pacote.
