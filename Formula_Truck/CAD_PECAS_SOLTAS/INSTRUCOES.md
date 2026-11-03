# Formula Truck 400 mm — CAD base com todas as peças separadas

Entrega do modelo aprovado pelo usuário para edição no Fusion e adaptação ao próprio chassi. O desenho é inspirado na fotografia enviada; não é uma réplica dimensional certificada do caminhão real. A adaptação ao chassi foi deixada com o usuário, conforme solicitado.

## Abrir no Fusion

1. Extraia o ZIP inteiro.
2. Abra `MONTAGEM_TRUCK_CARROCERIA.step`: 47 componentes de carroceria separados e nomeados.
3. Para visualizar também as peças opcionais de vidro/faixas, abra `MONTAGEM_TRUCK_COM_VIDROS.step`: 55 componentes.
4. Para modificar uma única peça, abra seu arquivo individual em `STEP_PECAS/` ou `STEP_VIDROS_OPCIONAIS/`.

Cada arquivo individual contém um sólido CAD. As montagens preservam os corpos em posições de montagem, sem fundi-los num corpo único. Os STEP foram gerados em CAD com lofts e formas analíticas; as superfícies não foram convertidas a partir de STL. O histórico de operações do CadQuery não é transferido para a linha do tempo do Fusion: os STEP fornecem os sólidos e as superfícies para edição direta. As fontes Python também acompanham o pacote.

Para salvar em F3D, importe no próprio Fusion e use seu salvamento/exportação. O script opcional `Fusion/GerarF3D` importa a montagem de carroceria e os 47 STEP de carroceria, exportando arquivos F3D em uma nova pasta. O script foi conferido sintaticamente, mas não foi executado no Fusion nesta máquina.

## Todas as peças soltas

- **20 painéis de cabine:** teto em quatro; frente em quatro; painel traseiro em quatro; laterais em oito.
- **4 seções de para-choque:** as regiões superior e inferior da seção central estão em arquivos separados porque são corpos fisicamente desconectados nessa subdivisão.
- **3 seções da lâmina inferior.**
- **8 metades de para-lamas:** cada um dos quatro para-lamas foi cortado em duas partes.
- **4 carenagens laterais.**
- **2 partes da grade**, **3 telas dos dutos**, **1 emblema** e **2 espelhos**.
- **8 peças opcionais de vidros/faixas**, em pasta própria. São formas CAD de referência para a transparência; não são vidros comerciais especificados. Pode preferir usar acetato ou ajustar esses corpos antes de fabricar.

Rodas e pneus mostrados na imagem são apenas referências de proporção: não há projeto de roda/pneu funcional para imprimir neste pacote. O usuário já tem o conjunto rodante.

A lista de arquivos, quantidades e dimensões está em `LISTA_PECAS.csv`. Os nomes Ypositivo/Ynegativo ou sufixos 1/-1 representam o lado do eixo transversal, evitando confundir esquerda/direita pela direção de observação.

## Pastas de STL

Embora a entrega principal seja CAD, também foram incluídos STL:

- `STL_PECAS/`: 47 peças da carroceria nas posições de montagem.
- `STL_VIDROS_OPCIONAIS/`: 8 peças opcionais nas posições de montagem.
- `STL_IMPRESSAO/`: os mesmos 55 componentes girados individualmente para uma orientação que cabe na impressora e colocados em Z=0. Os nomes que começam com vidro_opcional não são obrigatórios.

Todas as peças foram verificadas contra um envelope de **218 × 218 × 248 mm**, dentro da impressora informada de **220 × 220 × 250 mm**. Isso confere as caixas dimensionais em uma orientação possível, não prova a adequação de suportes, brim ou adesão na sua impressora. Confira a orientação no fatiador antes de imprimir; superfícies curvas e molduras podem precisar de suportes. Arquivos de impressão foram posicionados individualmente: arrume-os no fatiador ao importar vários juntos.

A malha STL usa tolerância nominal de tesselação de 0,03 mm. Os arquivos CAD STEP são a referência de superfícies. Os STL foram reabertos como malhas fechadas e orientadas; volumes foram preservados ao girá-los para impressão.

## Medidas adotadas

- Entre-eixos: **500 mm**.
- Diâmetro externo dos pneus de referência: **200 mm**.
- Largura externa total de referência dos pneus: **400 mm**.
- Largura nominal máxima de carroceria: **400 mm**, desconsiderando os espelhos.
- Cabine: aproximadamente 376 mm na base, estreitando para o teto.
- Altura do teto a partir do chão de referência: aproximadamente 450 mm, estimada visualmente.
- Rodas de referência: eixos longitudinais X=185 e X=685 mm, Z=100 mm.

A largura individual dos pneus não foi informada; o desenho visual usou pneus de referência com 52 mm de largura. Os espelhos ultrapassam a largura nominal de 400 mm. Alturas, balanços, contornos e detalhes não dimensionados na foto foram estimados para formar o modelo aprovado, e podem ser alterados no CAD.

## Montagem e adaptação

**As peças estão separadas por cortes; esta entrega não inclui travas, dobradiças, encaixes mecânicos finais ou suportes específicos para o chassi.** Não há alegação de kit de encaixe sem cola. As uniões entre painéis podem receber colagem ou detalhes de fixação que o usuário definir no Fusion. Os recortes não têm uma folga de montagem calibrada para uma impressora/material específico. A adaptação ao chassi e a escolha das uniões estruturais ficam com o usuário, conforme o escopo aceito para esta entrega CAD.

Não foram feitos testes físicos, ensaios de resistência, calibração de impressão, verificação completa de todas as interferências, simulação da suspensão/direção ou validação do encaixe no chassi real. Esses limites não devem ser confundidos com a validade geométrica dos sólidos.

## Validação CAD realizada

- 47 STEP de carroceria e 8 STEP opcionais reimportados como sólidos válidos, um por arquivo.
- Montagem de carroceria reimportada com 47 sólidos e montagem com vidros reimportada com 55 sólidos.
- Volumes comparados entre os sólidos exportados e reimportados.
- STL individuais e orientados reabertos como malhas fechadas; rotação para impressão sem espelhamento e com volume preservado.
- Dimensões orientadas conferidas dentro de 218 × 218 × 248 mm.

Os resultados estão em `validacao_pecas.json`. As verificações CAD foram feitas com CadQuery/OpenCascade e Trimesh. O Autodesk Fusion não foi executado no ambiente de geração.

## Fontes

FONTES contém o desenho CadQuery, parâmetros do estudo e os scripts de subdivisão/exportação. Algumas dimensões estão no JSON e outras diretamente no código; o JSON não controla todos os detalhes. O projeto utiliza milímetros.

Os arquivos anteriores do carro, traseira e para-choque continuam preservados no repositório. A prévia inicial do caminhão também foi mantida em sua pasta de estudo.
