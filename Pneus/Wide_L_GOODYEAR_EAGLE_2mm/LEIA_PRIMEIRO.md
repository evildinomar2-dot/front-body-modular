# Pneu Wide L — GOODYEAR / EAGLE, relevo nominal de 2 mm

O pneu enviado foi preservado, com as inscrições adicionadas na lateral frontal (Z positivo): GOODYEAR no arco superior e EAGLE no inferior, seguindo a referência. Entre GOOD e YEAR há um símbolo de pé alado estilizado. A tipografia e o símbolo são uma interpretação da foto, não um logotipo vetorial oficial.

## Relevo e encaixe

As letras acompanham a curvatura real da lateral. O relevo nominal é de 2 mm na direção axial Z, medido a partir da superfície original do pneu, com 0,35 mm de ancoragem para integrar as letras ao corpo. Não é uma placa plana flutuando sobre a lateral. As amostras dos triângulos exportados ficaram entre 1.972 e 2.001 mm; a pequena diferença decorre da triangulação da superfície curva.

Diâmetro máximo original mantido: aproximadamente 77,266 mm. A largura original era 37,130 mm; com o relevo frontal, a largura máxima passa a aproximadamente 39,130 mm. A outra lateral não foi modificada. O encaixe interno, o assento na roda e a banda de rodagem original foram preservados. O modelo não foi redimensionado para adaptar a outra roda.

O STL final é uma única peça fechada, com o texto integrado. O arquivo original foi comparado por diferença de volume e não perdeu material. Não foi acrescentado material à região protegida de raio 29 mm que cobre o encaixe na roda.

## Imprimir

Use STL_IMPRESSAO/Pneu_Wide_L_GOODYEAR_EAGLE_2mm.stl. O pneu está centralizado em X/Y, com a lateral traseira no plano Z=0 e as inscrições voltadas para cima. Confira a orientação e a necessidade de suportes no fatiador. Para um pneu funcional, escolha material flexível adequado ao seu uso e teste uma unidade antes de fazer o jogo completo. Não houve ensaio físico de impressão, encaixe ou rodagem.

As letras amarelas nas imagens são uma indicação de pintura. STL não guarda cores; esse arquivo imprime como uma peça única na cor do filamento. As letras não são peças soltas. Para reproduzir a aparência da referência, pinte o relevo após a impressão ou use seu processo de impressão multicolorido apropriado.

## Referências e reprodução

REFERENCIA/Pneu_Posicao_Original.stl é o mesmo pneu completo nas coordenadas do arquivo de entrada, para comparar no CAD. Não imprima junto com a outra posição; ambos representam a mesma peça.

IMAGENS contém vista frontal, perspectiva, detalhe de relevo e perfil. VALIDACAO.json contém as medidas e verificações. As fontes mantêm as palavras, posicionamento e altura do relevo como parâmetros. A geometria do pneu original continua proveniente de STL, portanto não há um STEP nativo completo neste pacote.

Para reproduzir: use Python 3.12 com FONTES/requirements.txt, coloque seu Wide_Wheel_Tire L.stl junto do script criar_pneu.py e execute-o. O script usa a fonte DejaVu Sans Bold Oblique; em outro sistema, ajuste a variável FONT para a localização do arquivo da fonte. O STL de entrada não é redistribuído separadamente no pacote.
