# Rear Body V1 — traseira modular para Fusion

O arquivo original está preservado em ORIGINAL/Rear_Body_V1.stl. Não foi aplicado fator de escala. STL não registra unidade: adotamos 1 unidade = 1 mm, como na dianteira. Envelope original aproximado: largura 200,696 mm, comprimento 223,754 mm, altura 120,228 mm.

## Arquivos

- `MONTAGEM_TRASEIRA_MODULAR.step`: oito componentes nomeados, posicionados na montagem traseira.
- `STEP/`: oito sólidos individuais, nas coordenadas da montagem.
- `STL/`: oito malhas fechadas com guias e pinos integrados, na mesma geometria-base usada no CAD.
- `MONTADO.png`, `EXPLODIDO.png`, `ENCAIXES_INTERNOS.png`: imagens produzidas das peças finais reais.
- `validacao.json`: fechamento dos STL, contagem de sólidos, 28 pares de interseção e teste da tampa em seis posições discretas.
- `validacao_step.json` e `validacao_montagem_step.json`: exportação e reimportação dos sólidos CAD e da montagem.
- `Fusion/GerarF3D/`: conversão opcional de STEP para F3D, executada no Fusion instalado no seu computador. O script não foi executado na nuvem.
- `FONTES/`: scripts da preparação, com dependências e instruções para reprodução.

## Oito componentes

1. Tampa do porta-malas — vermelho. Inclui os suportes de fixação originais e quatro pinos de posicionamento novos.
2. Painel traseiro com arco de roda, Y positivo — azul.
3. Painel traseiro com arco de roda, Y negativo — azul.
4. Trecho lateral dianteiro, Y positivo — verde.
5. Trecho lateral dianteiro, Y negativo — verde.
6. Painel preenchido do vidro traseiro — azul claro. Não foi criado vidro transparente.
7. Teto com antena integrada — amarelo.
8. Moldura e colunas traseiras — roxo, como uma peça estrutural.

Y positivo/negativo evita inverter esquerda/direita. Antena e detalhes integrados de cada painel permanecem com seu painel; não há um arquivo individual para cada pequeno relevo. O STL não contém para-choque traseiro e lanternas completos; essas peças não foram inventadas.

## Abrir no Fusion

Extraia o ZIP inteiro e abra/importe `MONTAGEM_TRASEIRA_MODULAR.step` como arquivo local. Para trabalhar apenas numa peça, abra o STEP correspondente. Confira milímetros e largura aproximada de 200,70 mm. Salve o projeto no Fusion ou exporte como Fusion Archive (.f3d).

Opcionalmente, no Fusion, abra Utilitários → Scripts e complementos → Scripts, adicione a pasta Fusion/GerarF3D e execute GerarF3D. O script importa os oito STEP e a montagem e exporta F3D numa pasta nova, sem substituir arquivos antigos. Ele foi conferido sintaticamente, mas não testado no Fusion.

**Os STEP são sólidos BRep FACETADOS, derivados de STL.** Não são superfícies NURBS reconstruídas nem CAD com o histórico paramétrico original. A malha-base foi simplificada com tolerância de 0,06 mm antes de separar os painéis; os cortes acompanham uma interpretação das linhas existentes. Não houve reescala. Foram desconsiderados dois triângulos soltos do STL e removidos fragmentos minúsculos de corte menores que 1 mm³. Triângulos muito estreitos em regiões quase planas foram retriangulados com tolerância local de 0,0001 mm e diferença de volume conferida abaixo de 0,02 mm³. Os novos cortes, pinos e guias alteram regiões locais da geometria para torná-la modular. A conversão não recupera esboços ou parâmetros perdidos no STL. Para alterar curvas de forma ampla, pode ser necessário reconstruir a região no Fusion.

## Encaixes — primeira versão

- Tampa removível: quatro pinos Ø4,0 mm com alojamentos Ø4,6 mm, folga nominal de 0,30 mm por lado. Pinos novos curtos, com comprimento aproximado de 4,25 mm; não confundir com os suportes antigos que já existiam no STL.
- Demais uniões: 12 pares de linguetas/guias internas, folga nominal de 0,30 mm por lado, com reforços ligados aos próprios painéis. As guias nas colunas C foram deslocadas mais para dentro para evitar saliência externa.
- São guias de posicionamento para colagem ou fixação adicional a projetar. Não são travas elásticas certificadas nem encaixes sem cola validados fisicamente.
- A tampa não tem dobradiça, ímã ou fecho. O teste de retirada avalia deslocamento vertical em posições discretas, não uma articulação nem uma varredura contínua.
- A sequência física de montagem, acesso às guias e eventuais movimentos simultâneos ainda precisam ser conferidos. Não force encaixes opostos.
- Imprima primeiro uma pequena região de encaixe para calibrar a folga para sua impressora/material. Não houve ensaio físico, de resistência ou de impressão.

## Validação e limites

Os oito STL foram reabertos e verificados quanto a fechamento, orientação e um único sólido por peça. Os 28 pares foram avaliados por interseção volumétrica nos dois sentidos; adotou-se limite numérico de 0,02 mm³. Resíduos abaixo desse limite não equivalem a um teste físico de encaixe. A tampa foi testada em elevações de 0,5, 2, 5, 10, 20 e 40 mm, com o mesmo limite, sem alegar varredura contínua.

Os oito STEP foram exportados e reimportados como sólidos válidos, com volumes conferidos em relação às malhas correspondentes. A montagem foi reimportada com oito sólidos válidos. As verificações foram feitas com CadQuery/OpenCascade e Manifold; o Autodesk Fusion não está instalado neste ambiente.

A orientação local foi ajustada para Z para cima: X novo = -Z original; Y novo = X original; Z novo = -Y original. A traseira não foi posicionada nem unida à dianteira para formar um veículo completo. Não foram projetadas novas uniões entre os dois módulos nem suportes para o chassi modificado: faltam o modelo do chassi e as referências de alinhamento. Os arquivos e o pacote da dianteira permanecem preservados.
