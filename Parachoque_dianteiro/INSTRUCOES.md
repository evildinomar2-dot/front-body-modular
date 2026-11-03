# Para-choque dianteiro dividido — chavetas dentro das paredes

O Front_Bumper_V1.stl original foi preservado em ORIGINAL/. O para-choque foi cortado no plano central da largura, sem reescala, e recebeu três alojamentos cegos em cada metade para três chavetas soltas. Não há travessa ou aba atravessando o vão da grade.

## O que imprimir

Na pasta **STL_IMPRESSAO**, imprima uma unidade de cada um dos cinco arquivos:

1. 01_metade_Ypositivo.stl
2. 02_metade_Ynegativo.stl
3. 03_chaveta_A_faixa_central.stl
4. 04_chaveta_B_parede_frontal.stl
5. 05_chaveta_C_parede_traseira.stl

Os STL dessa pasta já estão sobre Z=0. As metades estão com a face da emenda apoiada na mesa; as chavetas estão deitadas para imprimir com a menor altura. As peças foram centralizadas individualmente: arrume-as no fatiador, pois importar todas mantendo suas coordenadas pode sobrepô-las. Você pode imprimir cada metade separadamente.

| Peça | Dimensões na orientação sugerida de impressão (X × Y × Z) |
|---|---|
| Cada metade | aproximadamente 62,20 × 54,80 × 96,35 mm |
| Chaveta A | 4,0 × 14,0 × 2,8 mm |
| Chaveta B | 3,0 × 12,0 × 1,4 mm |
| Chaveta C | 3,0 × 12,0 × 1,2 mm |

A área útil da impressora não foi informada. Essas dimensões permitem conferir se cabe; não foi validado numa impressora específica. A orientação é uma sugestão inicial: confira estabilidade, brim, pontes e suportes no fatiador. A face de corte toca a mesa em regiões separadas, unidas pelo restante do para-choque ao longo da altura. Evite suportes presos dentro dos alojamentos cegos e mantenha a face da emenda limpa. Os encaixes não foram calibrados ou testados fisicamente; confira a folga antes de uma impressão longa.

## Como a emenda funciona

As chavetas entram pelas faces centrais cortadas e ficam no interior da espessura das paredes. Os alojamentos não abrem na superfície externa nem atravessam as paredes para o vão da grade. Uma chaveta alinha a faixa central mais espessa; as outras duas alinham as paredes frontal e traseira. O detalhe fino abaixo do furo central original foi preservado sem inserir uma chaveta nessa região estreita.

| Chaveta | Comprimento transversal × espessura × altura | Alojamento em cada metade |
|---|---|---|
| A | 14,0 × 2,8 × 4,0 mm | profundidade 7,3 mm, seção 3,2 × 4,4 mm |
| B | 12,0 × 1,4 × 3,0 mm | profundidade 6,3 mm, seção 1,8 × 3,4 mm |
| C | 12,0 × 1,2 × 3,0 mm | profundidade 6,3 mm, seção 1,6 × 3,4 mm |

Folga nominal de 0,20 mm por face lateral e 0,30 mm por extremidade. As chavetas têm chanfros de 0,15 mm. Os alojamentos têm seção retangular; os chanfros facilitam a entrada. As dimensões assumem milímetros, pois STL não armazena unidade.

Para montar, apresente as três chavetas nos alojamentos de uma metade e aproxime a outra lateralmente. Não force peças que não entram: ajuste a folga conforme seu processo de impressão. São guias de alinhamento, sem trava elástica; a fixação permanente, caso desejada, precisa de cola adequada ao material ou outra fixação a definir. Não houve ensaio de resistência.

## Arquivos para Fusion e posições de montagem

- `MONTAGEM_PARACHOQUE_DIVIDIDO.step`: montagem CAD com cinco sólidos: duas metades e três chavetas.
- `STEP/`: cinco peças individuais nas posições de montagem.
- `STL_MONTAGEM/`: os mesmos cinco componentes posicionados para montar. Use esta pasta para inspeção/montagem virtual; as coordenadas são diferentes das versões de impressão.
- `STL_IMPRESSAO/`: as cinco peças orientadas e centralizadas individualmente para o fatiador.
- `EXPLODIDO.png`, `MONTADO.png`, `VISTA_INTERNA.png`: imagens reais da geometria STL final.
- `DETALHE_EMENDA.png`: seção central com os alojamentos dentro das paredes e ampliações das três chavetas.
- `validacao.json`, `validacao_step.json`, `validacao_montagem_step.json`: resultados das verificações.
- `FONTES/`: scripts e dependências para reproduzir o projeto.
- `Fusion/GerarF3D/`: conversor opcional executado dentro do Autodesk Fusion.

Extraia o pacote inteiro e importe `MONTAGEM_PARACHOQUE_DIVIDIDO.step` no Fusion para inspecionar ou modificar. Os STEP das metades são BRep facetados, derivados de uma simplificação adicional da malha com tolerância de 0,02 mm. As chavetas STEP são sólidos analíticos chanfrados. Não foi recuperado o histórico paramétrico original do STL. Os STL mantêm a malha original das superfícies externas, com o corte e os novos alojamentos. Não misture versões CAD e STL sem conferir a pequena diferença de aproximação.

O conversor F3D importa os STEP e grava novos arquivos nativos dentro do próprio Fusion. Foi conferido sintaticamente; não foi executado na nuvem, que não tem Autodesk Fusion instalado.

## Validações realizadas

- Reabertura dos cinco STL de montagem e dos cinco STL de impressão: malhas fechadas, orientação consistente e um sólido por arquivo; volumes preservados após orientar para impressão.
- Dez pares verificados quanto a interferência geométrica, dentro de tolerância numérica de 0,0001 mm³.
- Alojamentos inteiramente contidos no material do original: nenhuma perfuração para o vão ou para a superfície externa. A cobertura mínima amostrada na superfície dos alojamentos foi aproximadamente 3,11 mm em A, 0,90 mm em B e 0,97 mm em C. São mínimos amostrados, não valores garantidos de resistência.
- Montagem completa contida no volume de material original: as chavetas não acrescentam material nos vãos livres da grade. Nenhum suporte novo foi acrescentado fora das paredes.
- Aproximação/afastamento lateral de cada metade com as chavetas fixas verificados em cinco posições discretas. Não é uma varredura contínua nem um teste físico.
- Os cinco STEP foram reimportados como sólidos válidos, e a montagem reimportada com cinco sólidos. As verificações CAD foram feitas com CadQuery/OpenCascade; os sólidos geométricos foram verificados com Manifold e Trimesh.

## Escala e orientação

Largura original: aproximadamente 192,70 mm. Cada metade tem aproximadamente 96,35 mm na largura original. Sem alterar o tamanho, foi aplicada uma rotação para Z para cima e uma translação para colocar o meio da largura em Y=0 e a base em Z=0. X novo = -Z original; Y novo = X original menos o centro da largura; Z novo = -Y original menos a menor altura após rotação.

O corte equivale ao meio do eixo X do STL original. As metades de impressão recebem ainda uma rotação para apoiar a face de corte e uma centralização individual. As matrizes estão em validacao.json.

Não houve alinhamento com a carroceria dianteira nem adaptação ao chassi modificado. Os pacotes anteriores da dianteira e traseira foram preservados.
