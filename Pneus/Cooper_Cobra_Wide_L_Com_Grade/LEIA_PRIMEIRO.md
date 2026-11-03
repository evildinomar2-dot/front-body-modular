# Pneu COOPER / COBRA — baixo relevo de 1 mm e letras de 2 mm em grades curvas

Projeto independente COOPER / COBRA, usando a mesma base funcional e o sistema de encaixes do kit anterior. As letras agora ficam presas em duas armações curvas: uma para COOPER, outra para COBRA. As grades mantêm as letras na posição e curvatura corretas dos alojamentos durante o manuseio e a instalação. Depois da cura da cola, corte as pontinhas e retire as grades.

## Pneu e letras

Use o pneu desta versão, com rebaixos específicos para COOPER / COBRA: STL_PNEU/Pneu_COOPER_COBRA_BaixoRelevo_1mm.stl. O corpo, a banda de rodagem e o encaixe na roda mantêm a base original enviada. A versão GOODYEAR permanece salva separadamente.

As letras continuam com espessura nominal de 2 mm, folga lateral de 0,15 mm por face e reserva de 0,05 mm no fundo para cola. Depois de encaixadas, ficam aproximadamente 1 mm para fora. As letras seguem os arcos da lateral, com COOPER em cima e COBRA embaixo. As grades e suas ligações temporárias seguram as letras na posição correta. A prévia branca é uma indicação de cor de filamento; o STL não armazena cores. A tipografia é uma interpretação dos nomes COOPER / COBRA, sem símbolo de cobra ou logotipo oficial.

## Arquivos para imprimir

- DUAS_GRADES_PARA_IMPRIMIR.stl: imprime as duas palavras juntas no mesmo trabalho, como dois conjuntos separados. Ocupa aproximadamente 37.5 × 29.5 mm na mesa.
- GRADES_IMPRESSAO/Grade_COOPER_Letras_2mm.stl: opção para imprimir apenas o conjunto superior.
- GRADES_IMPRESSAO/Grade_COBRA_Letras_2mm.stl: opção para imprimir apenas o conjunto inferior.

Escolha o arquivo das duas grades OU os arquivos individuais. Grade e letras são impressas juntas na mesma cor. Não precisa imprimir as três opções como peças adicionais.

Os arquivos estão orientados com as costas das letras aproximadamente voltadas para a mesa e Z mínimo zero. As formas curvas e as armações exigem revisar suportes e brim no fatiador, principalmente sob os arcos e as costas das letras. A altura do conjunto pode chegar a aproximadamente 4,9 mm por incluir a armação; as letras em si continuam com 2 mm de espessura. Não altere a escala Z para tentar limitar o conjunto a 2 mm.

## Teste pequeno primeiro

TESTE_ENCAIXE/TESTE_CAVIDADE_O.stl é um alojamento de teste desta versão COOPER / COBRA. TESTE_ENCAIXE/TESTE_O_COM_GRADE.stl é a letra O com uma pequena armação e a mesma pontinha de corte usada nas grades completas. Imprima ambos com os materiais pretendidos para testar o encaixe, a cola e o corte antes de fazer o jogo completo. Use o alojamento O fornecido nesta versão para o teste.

## Instalação e corte

1. Remova os suportes gerados pelo fatiador, mantendo intactos os arcos, as hastes e as pequenas ligações às letras.
2. Posicione cada palavra inteira no pneu, ainda presa à grade, e confira o encaixe a seco. COOPER vai no arco superior; COBRA no inferior, como na referência.
3. Limpe e seque as superfícies. Aplique uma película pequena de cola nas costas das letras ou no fundo dos alojamentos, e assente as letras sem forçar. A grade permanece afastada do pneu e serve de gabarito de posição.
4. Aguarde a cura indicada pelo fabricante da cola, mantendo as letras assentadas. A Super Bonder deve ser testada nos filamentos escolhidos; aderência e flexibilidade dependem dos materiais, especialmente em TPU.
5. Com alicate de corte rente/fino, apoie cada letra e corte a ligação pequena junto ao contorno da letra. A seção nominal de cada pontinha é 0,8 × 0,6 mm. Retire a armação depois de cortar todas as ligações e faça acabamento leve nos pontos de corte, se necessário.

As pontinhas estão nas laterais externas das letras, acima da superfície do pneu e abaixo da face visível da letra, para deixar a região de colagem livre. Não cole os arcos nem as hastes no pneu.

## Verificação e limites

Cada palavra com sua grade é um sólido fechado conectado; o arquivo duplo contém dois conjuntos. As estruturas STEP foram reimportadas válidas. As letras das grades mantêm a geometria e posição dos respectivos alojamentos COOPER / COBRA. A verificação digital não encontrou interpenetração da grade ou das letras com o pneu na posição de montagem. O arquivo do pneu do pacote foi conferido como idêntico ao pneu COOPER / COBRA validado na geração dos rebaixos.

Não houve ensaio físico de impressão, resistência das pontinhas, encaixe ou colagem. Por isso foi incluído o teste O com grade.

IMAGENS mostra a instalação com as grades, as grades separadas, a disposição na mesa e o detalhe da ligação cortável. As grades são temporárias e devem ser retiradas após a colagem.

CAD_ESTRUTURA contém somente os arcos e ligações em STEP, sem as letras. Os STL de impressão contêm os conjuntos completos. FONTES permite reproduzir as grades em Python 3.12 com requirements.txt e os dados de entrada fornecidos. O script usa o pneu da pasta STL_PNEU e o alojamento O da pasta TESTE_ENCAIXE deste pacote; mantenha a organização das pastas ao executar. O script opcional criar_pneu_cooper.py regenera também o pneu e os caracteres; para ele, forneça seu Wide_Wheel_Tire L.stl ao lado do script e ajuste o caminho da fonte DejaVu Sans Bold Oblique no seu sistema.
