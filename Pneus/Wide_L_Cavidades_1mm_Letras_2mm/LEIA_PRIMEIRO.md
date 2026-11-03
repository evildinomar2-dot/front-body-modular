# Pneu com baixo relevo de 1 mm e letras soltas de 2 mm

Nova variante para imprimir o pneu numa cor e as inscrições em outra, depois encaixar e colar. A versão anterior com relevo integrado continua salva separadamente.

## O que imprimir

1. O pneu: STL_PNEU/Pneu_Wide_L_BaixoRelevo_1mm.stl, uma unidade na cor/material do pneu.
2. As letras: TODAS_AS_LETRAS_2mm.stl, uma unidade na cor das letras. Esse arquivo contém 14 peças separadas, organizadas em duas filas: GOODYEAR e o símbolo na superior; EAGLE na inferior.

LETRAS_INDIVIDUAIS oferece os mesmos 14 componentes, um arquivo por peça, para reimprimir somente alguma letra. Escolha a bandeja completa OU os arquivos individuais: não precisa imprimir os dois conjuntos.

## Faça primeiro o teste pequeno

Imprima uma unidade de TESTE_ENCAIXE/TESTE_CAVIDADE_O.stl no mesmo material do pneu e uma de TESTE_ENCAIXE/TESTE_LETRA_O_2mm.stl no material das letras. O teste repete o alojamento e a letra O do conjunto. Ele permite conferir ajuste, orientação, perfil de impressão e aderência da cola antes de imprimir tudo.

Ensaie a seco antes de usar cola. Se estiver apertado, confira compensação de furos/expansão horizontal, fluxo e acabamento das costas da letra, e repita o teste. Não escale o pneu inteiro para acertar apenas o encaixe das letras.

## Geometria do encaixe

- Baixo relevo no pneu: profundidade nominal de 1,00 mm a partir da lateral original, acompanhando sua curvatura.
- Letras e símbolo: espessura nominal de 2,00 mm, também seguindo a curvatura.
- Folga lateral: 0,15 mm por face entre letra e alojamento.
- Reserva no fundo para película de cola: 0,05 mm.
- Saliência após encaixar: aproximadamente 1 mm (nominalmente 1,05 mm considerando essa reserva).

A altura visual das letras é a mesma: 4,8 mm no GOODYEAR e símbolo, 4,2 mm no EAGLE. O espaçamento do arco superior foi aberto ligeiramente para dar folga aos alojamentos e manter cada cavidade independente.

O pneu sem as letras mantém as dimensões do arquivo original: aproximadamente 77,266 mm de diâmetro máximo e 37,130 mm de largura. O encaixe da roda, a banda de rodagem e a outra lateral foram preservados. Somente as cavidades das inscrições foram retiradas da lateral frontal.

## Orientação e curvatura das letras

O pneu está apoiado pela lateral traseira em Z=0, com os alojamentos voltados para cima. Confira a necessidade de suportes e o perfil do seu material no fatiador.

As letras são pequenas peças curvas que combinam com a lateral do pneu. Foram orientadas com as costas de colagem aproximadamente tangentes à mesa. Revise suportes leves nas costas e/ou brim para estabilizar as peças, conforme o fatiador indicar. Remova suportes e resíduos antes de colar.

A espessura é de 2 mm; a altura total da caixa envolvente no fatiador pode chegar a cerca de 2.57 mm por causa da curvatura. Não force a dimensão Z para 2 mm usando escala: isso alteraria o encaixe. A bandeja ocupa aproximadamente 57.3 × 19.5 mm na mesa.

## Colagem

Separe e identifique as peças antes de misturar as duas filas. Os alojamentos indicam a posição e a orientação. GOODYEAR fica em cima; EAGLE fica no arco inferior, com a mesma orientação da referência enviada.

Limpe e seque as superfícies. Aplique uma película pequena de cola nas costas da letra ou no fundo do alojamento, encaixe sem forçar e aguarde a cura indicada pelo fabricante. Evite encher as cavidades de cola.

Pode usar a Super Bonder se ela aderir aos filamentos escolhidos: teste primeiro no O fornecido. A aderência depende da combinação de cola e materiais, especialmente em TPU. O projeto não inclui teste físico de colagem, impressão, encaixe ou uso.

## Referências e validação

IMAGENS mostra o pneu vazio, as letras separadas e a montagem ilustrada em amarelo. A cor é apenas uma representação: você escolhe os filamentos de cada impressão.

VALIDACAO.json registra as verificações: pneu e peças individuais fechados; 14 sólidos na bandeja; cavidades de aproximadamente 1 mm; espessura das letras de aproximadamente 2 mm; encaixe da roda preservado; ausência de interpenetração das letras com o pneu na posição final. Não houve ensaio físico.

FONTES contém o script. Para reproduzir, use Python 3.12 e requirements.txt, coloque seu Wide_Wheel_Tire L.stl junto do script e ajuste FONT para o caminho da fonte DejaVu Sans Bold Oblique no seu sistema. O STL de entrada não está redistribuído separadamente neste pacote.
