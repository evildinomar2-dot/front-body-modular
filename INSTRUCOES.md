# Front Body V1 — primeira versão modular para Fusion

O STL original foi preservado em ORIGINAL/. A escala numérica foi mantida (1 unidade = 1 mm, assumido porque STL não registra unidade). Envelope original: largura 197,557 mm, comprimento 237,646 mm, altura 115,154 mm. Não foi adaptado ao novo chassi: seu modelo e pontos de fixação não foram fornecidos.

## Conteúdo

- `MONTAGEM_MODULAR.step`: montagem de oito componentes nomeados, em posição de montagem.
- `STEP/`: oito sólidos CAD individuais. Peças nas mesmas coordenadas da montagem.
- `STL/`: oito malhas fechadas individuais, com maior fidelidade ao arquivo enviado e encaixes integrados.
- `MONTADO.png`, `EXPLODIDO.png`, `ENCAIXES_INTERNOS.png`: imagens obtidas da geometria real dos STL finais. As cores identificam as peças.
- `validacao.json`, `validacao_step.json`, `validacao_step_pares_final.json`, `validacao_montagem_step.json`: verificações da execução atual.
- `Fusion/GerarF3D/`: script opcional para importar os STEP e exportar arquivos F3D dentro do Fusion instalado no seu computador. Não foi executado no Fusion nesta máquina.
- `FONTES/`: scripts utilizados para cortes, encaixes, reparo, conversão e imagens.

## Peças e cores

1. Capô — vermelho. Independente, com os suportes originais do STL e quatro pinos verticais novos.
2. Para-lama Y positivo — azul.
3. Para-lama Y negativo — azul.
4. Painel lateral Y positivo — verde.
5. Painel lateral Y negativo — verde.
6. Painel preenchido do para-brisa — azul claro. Separado; não foi transformado em vidro transparente.
7. Teto — amarelo.
8. Moldura, calha e colunas — roxo, como uma peça de estrutura.

A orientação foi ajustada para Z para cima: X novo = -Z original; Y novo = X original; Z novo = -Y original. Os nomes Y positivo/negativo evitam inverter esquerda/direita. Não há para-choque, grade ou faróis completos neste STL; tais peças não foram inventadas. A moldura/colunas permanece como estrutura única; não é uma desmontagem de cada detalhe da malha.

## Abrir e modificar no Fusion

1. Extraia o ZIP inteiro.
2. Importe `MONTAGEM_MODULAR.step` pelo comando de abrir/carregar arquivo local do Fusion. Para trabalhar apenas numa peça, importe o arquivo correspondente de `STEP/`.
3. Confira a unidade em milímetros: largura original aproximada de 197,56 mm.
4. Os componentes estão independentes. Selecione apenas o componente a modificar. Ative Capturar histórico de projeto para registrar operações novas, se necessário.
5. Salve como projeto Fusion ou exporte como Fusion Archive (.f3d). Opcionalmente, adicione a pasta `Fusion/GerarF3D` em Utilitários → Scripts e complementos → Scripts e execute GerarF3D.

**Os STEP são sólidos BRep FACETADOS, derivados de STL.** Não são superfícies NURBS reconstruídas nem um modelo paramétrico com dimensões originais recuperadas. A conversão reduz a malha inicialmente com tolerância de 0,10 mm e ajusta pequenas regiões de contato entre componentes. Os STL mantêm maior resolução. A edição direta é possível, mas selecionar superfícies curvas compostas de triângulos é menos prático que num CAD desenhado do zero. Aumentar um painel ou alterar sua forma pode exigir cortes, operações novas ou reconstrução daquela região. Não existe parâmetro único para aumentar um para-choque inexistente neste arquivo.

## Encaixes internos — protótipo

- Capô: quatro pinos Ø4,0 mm e quatro alojamentos Ø4,6 mm nos para-lamas; folga nominal de 0,30 mm por lado. Os apoios internos permitem posicionamento e retirada vertical do capô. Não há trava, ímã ou dobradiça.
- Demais uniões: 12 pares de linguetas/guias internas, com folga nominal de 0,30 mm por lado. Os apoios são integrados aos painéis e têm reforços internos onde necessário.
- As guias servem para posicionamento e montagem por colagem ou fixação adicional a projetar. Não são encaixes elásticos certificados nem um kit de travas sem cola.
- O capô está separado para uma futura dobradiça; não está articulado. A dobradiça e seu curso ainda precisam ser projetados conforme chassi, espaço livre e abertura desejada.
- O procedimento físico de montagem e desmontagem, possíveis movimentos simultâneos das peças e acessibilidade dos encaixes ainda não foram validados. Não force encaixes opostos: ajuste guias/sequência no Fusion se necessário.
- As folgas não foram calibradas para sua impressora ou material. Recomenda-se imprimir primeiro um pequeno trecho do encaixe. Não há validação física, de resistência, movimento do capô ou compatibilidade com o chassi modificado.

## Validação e limites

Os STL finais foram reabertos e conferidos quanto a malha fechada, orientação e um único sólido por arquivo. Todos os 28 pares foram verificados por interseção volumétrica; resíduos abaixo de 0,02 mm³ são tolerância numérica e não significam teste físico de encaixe. O reparo da moldura CAD removeu aproximadamente 1.17% de volume nessa peça, sobretudo pequenos contatos defeituosos; não é uma cópia exata da malha de alta resolução. A moldura recebeu folgas locais adicionais no STEP para compensar a simplificação. Assim, STEP e STL não são geometricamente idênticos; use um mesmo formato em todas as peças de uma montagem. Os STEP individuais são exportados e reimportados como sólidos válidos; a montagem é reimportada com oito sólidos. A versão simplificada de CAD também teve os 28 pares verificados antes da conversão BRep.

Os cortes acompanham uma interpretação das linhas dos painéis do STL, não desenhos originais do fabricante. Foram removidos cinco triângulos soltos do arquivo e fragmentos minúsculos de corte, fechadas pequenas falhas e corrigidos contatos numéricos. Isso preserva a forma geral; não equivale a preservar cada triângulo original.

O Autodesk Fusion não está instalado neste ambiente: os testes CAD foram feitos com CadQuery/OpenCascade. O script F3D foi apenas conferido sintaticamente. Os corpos importados não recuperam esboços nem o histórico original.
