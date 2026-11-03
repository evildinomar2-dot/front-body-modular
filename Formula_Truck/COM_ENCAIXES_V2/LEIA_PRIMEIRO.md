# Caminhão Formula Truck — V2 com encaixes para colar

Use esta revisão no lugar dos painéis do pacote anterior. Os 47 painéis foram revisados para receber as chavetas. Não misture painéis antigos com chavetas novas.

## Conteúdo

- 47 peças da carroceria/cabine com alojamentos e reforços internos.
- 84 chavetas para a carroceria e 13 chavetas para os vidros/faixas opcionais: 97 no total.
- 8 peças opcionais de vidros/faixas com seus alojamentos.
- Montagem STEP com 152 sólidos independentes, CAD individual e STL individual.
- Teste de encaixe, lista das peças, mapa das uniões e fontes reproduzíveis.

As chavetas são pontes internas com dois pinos retangulares, um em cada peça. São uniões para alinhar e COLAR, sem travas de pressão. Não há necessidade de parafusos M3 nessas uniões. Emblema e espelhos usam seus pinos/hastes redondos originais, também colados.

## Primeiro: teste a folga

Na pasta TESTE_ENCAIXE, imprima:

1. TESTE_ALOJAMENTO_IMPRIMIR_2X.stl: duas unidades.
2. TESTE_CHAVETA_IMPRIMIR_1X.stl: uma unidade.

O teste repete a geometria funcional dos encaixes: pino 3,2 × 5,2 mm; alojamento 3,6 × 5,6 mm; folga 0,2 mm por face; inserção útil 4 mm; fundo livre 0,5 mm. Teste SEM COLA, com o mesmo filamento e perfil que usará no caminhão. O pino deve entrar sem forçar e deixar espaço para a cola. Se não entrar, corrija primeiro a compensação de furos/fluxo no fatiador e repita o teste. Não reduza ou aumente o caminhão inteiro para ajustar a folga.

Este projeto foi conferido digitalmente; encaixe físico e resistência ainda não foram testados.

## Arquivos para imprimir e editar

- STL_IMPRESSAO: arquivos individuais apoiados em Z=0 e orientados para caber no envelope de 218 × 218 × 248 mm, dentro da sua impressora 220 × 220 × 250 mm. As chavetas ficam com a ponte na mesa e os pinos para cima.
- STL_MONTAGEM: mesmas peças nas coordenadas de montagem. Não mande essa pasta inteira ao fatiador para imprimir de uma vez.
- STEP_PECAS / STEP_CHAVETAS / STEP_VIDROS_OPCIONAIS: CAD individual editável.
- MONTAGEM_COM_ENCAIXES.step: montagem de referência com peças e chavetas nomeadas.
- LISTA_PECAS.csv: dimensões e quantidades. Os oito vidros/faixas e suas 13 chavetas são opcionais.
- MAPA_UNIOES.csv: para cada CHxxx, indica as duas peças que ela une.
- MAPA_UNIOES.json: inclui pontos de encaixe e direção de inserção nas coordenadas da montagem STEP.

Identifique as peças com etiquetas de papel pelos nomes dos arquivos antes de retirar várias da mesa. Os códigos CHxxx estão nos nomes dos arquivos e no mapa; não estão gravados fisicamente nas chavetas.

A orientação dos painéis busca caber na mesa; confira suportes no fatiador para os reforços e saliências. Comece com camada de 0,2 mm, quatro paredes e preenchimento de 40% como ponto de partida; confirme o resultado no teste. As chavetas pequenas podem usar preenchimento de 100%.

## Montagem sugerida

1. Ensaie as uniões a seco. As chavetas entram pelos alojamentos internos; alinhe as bordas externas dos painéis antes de colar.
2. Una as subdivisões da frente, traseira e laterais da cabine. Deixe o teto e os vidros fora para acessar os encaixes internos.
3. Monte o teto em quatro peças separadamente. Una a cabine por dentro e coloque o teto só depois de conferir o acesso às chavetas de canto. A cabine deve estar fora do chassi nessa etapa.
4. Monte a lâmina inferior, as seções do para-choque, as metades dos para-lamas e as carenagens seguindo o mapa. Depois una esses conjuntos à cabine e entre si.
5. Coloque grades e telas usando suas chavetas internas. Os alojamentos ficam nos contornos das peças; as aberturas principais permanecem livres.
6. Cole as hastes dos espelhos e os três pinos do emblema nos furos correspondentes. As folgas radiais nominais são 0,25 mm nos espelhos e 0,2 mm no emblema.
7. Coloque os vidros/faixas opcionais por último, utilizando suas chavetas. Seus contornos foram reduzidos para aliviar o ajuste nas aberturas.
8. Só depois adapte a carroceria ao seu chassi, como combinado.

Aplique uma pequena quantidade de cola compatível com o filamento, sem encher o fundo dos alojamentos. A folga não é uma trava: a fixação definitiva depende da cola. Aguarde a cura antes de manusear o conjunto.

## Verificações e limites

Todos os STEP individuais foram reimportados e têm um sólido CAD válido. Todos os STL são fechados e cabem no envelope informado. Foram verificadas 194 cavidades de encaixe abertas. A montagem completa foi reimportada com 152 sólidos independentes. A conferência de colisões usou malhas de desvio absoluto de 0,025 mm e não encontrou interpenetrações acima de 0,15 mm³ nem invasão dos quatro pneus de referência de 200 mm. Não foram usados reparos de malha no pacote final.

Entre-eixos de referência: 500 mm. Largura externa dos pneus: 400 mm. A largura individual de pneu de 52 mm permanece uma referência visual e não uma medida confirmada do seu chassi. Os espelhos passam da largura de 400 mm. Fixações ao chassi, resistência a impactos e folgas da sua impressora precisam da adaptação/ensaio físico. As imagens de detalhe mostram recortes do CAD real para facilitar a visualização das uniões.
