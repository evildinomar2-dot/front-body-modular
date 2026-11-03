# Letras de 2 mm em grades curvas para imprimir, posicionar e colar

Revisão do kit de pneu com baixo relevo de 1 mm. As letras agora ficam presas em duas armações curvas: uma para GOODYEAR e símbolo, outra para EAGLE. As grades mantêm as letras na posição e curvatura corretas dos alojamentos durante o manuseio e a instalação. Depois da cura da cola, corte as pontinhas e retire as grades.

## Pneu e letras

O pneu é exatamente o mesmo arquivo com rebaixos de 1 mm do kit anterior, incluído em STL_PNEU/Pneu_Wide_L_BaixoRelevo_1mm.stl. Se já imprimiu esse pneu, pode aproveitar a peça.

As letras continuam com espessura nominal de 2 mm, folga lateral de 0,15 mm por face e reserva de 0,05 mm no fundo para cola. Depois de encaixadas, ficam aproximadamente 1 mm para fora. O tamanho e a posição das letras foram mantidos. A alteração foi somente a adição das grades e suas ligações temporárias.

## Arquivos para imprimir

- DUAS_GRADES_PARA_IMPRIMIR.stl: imprime as duas palavras juntas no mesmo trabalho, como dois conjuntos separados. Ocupa aproximadamente 54.0 × 34.2 mm na mesa.
- GRADES_IMPRESSAO/Grade_GOODYEAR_Letras_2mm.stl: opção para imprimir apenas o conjunto superior.
- GRADES_IMPRESSAO/Grade_EAGLE_Letras_2mm.stl: opção para imprimir apenas o conjunto inferior.

Escolha o arquivo das duas grades OU os arquivos individuais. Grade e letras são impressas juntas na mesma cor. Não precisa imprimir as três opções como peças adicionais.

Os arquivos estão orientados com as costas das letras aproximadamente voltadas para a mesa e Z mínimo zero. As formas curvas e as armações exigem revisar suportes e brim no fatiador, principalmente sob os arcos e as costas das letras. A altura do conjunto pode chegar a aproximadamente 4,9 mm por incluir a armação; as letras em si continuam com 2 mm de espessura. Não altere a escala Z para tentar limitar o conjunto a 2 mm.

## Teste pequeno primeiro

TESTE_ENCAIXE/TESTE_CAVIDADE_O.stl é o mesmo alojamento de teste anterior. TESTE_ENCAIXE/TESTE_O_COM_GRADE.stl é a letra O com uma pequena armação e a mesma pontinha de corte usada nas grades completas. Imprima ambos com os materiais pretendidos para testar o encaixe, a cola e o corte antes de fazer o jogo completo. Se já tem o alojamento O anterior, ele pode ser reutilizado.

## Instalação e corte

1. Remova os suportes gerados pelo fatiador, mantendo intactos os arcos, as hastes e as pequenas ligações às letras.
2. Posicione cada palavra inteira no pneu, ainda presa à grade, e confira o encaixe a seco. GOODYEAR vai no arco superior; EAGLE no inferior, como na referência.
3. Limpe e seque as superfícies. Aplique uma película pequena de cola nas costas das letras ou no fundo dos alojamentos, e assente as letras sem forçar. A grade permanece afastada do pneu e serve de gabarito de posição.
4. Aguarde a cura indicada pelo fabricante da cola, mantendo as letras assentadas. A Super Bonder deve ser testada nos filamentos escolhidos; aderência e flexibilidade dependem dos materiais, especialmente em TPU.
5. Com alicate de corte rente/fino, apoie cada letra e corte a ligação pequena junto ao contorno da letra. A seção nominal de cada pontinha é 0,8 × 0,6 mm. Retire a armação depois de cortar todas as ligações e faça acabamento leve nos pontos de corte, se necessário.

As pontinhas estão nas laterais externas das letras, acima da superfície do pneu e abaixo da face visível da letra, para deixar a região de colagem livre. Não cole os arcos nem as hastes no pneu.

## Verificação e limites

Cada palavra com sua grade é um sólido fechado conectado; o arquivo duplo contém dois conjuntos. As estruturas STEP foram reimportadas válidas. As letras mantêm a geometria e posição do kit anterior. A verificação digital não encontrou interpenetração da grade ou das letras com o pneu na posição de montagem. O arquivo do pneu foi conferido como idêntico ao anterior.

Não houve ensaio físico de impressão, resistência das pontinhas, encaixe ou colagem. Por isso foi incluído o teste O com grade.

IMAGENS mostra a instalação com as grades, as grades separadas, a disposição na mesa e o detalhe da ligação cortável. As grades são temporárias e devem ser retiradas após a colagem.

CAD_ESTRUTURA contém somente os arcos e ligações em STEP, sem as letras. Os STL de impressão contêm os conjuntos completos. FONTES permite reproduzir as grades em Python 3.12 com requirements.txt e os dados de entrada fornecidos. O script usa o pneu da pasta STL_PNEU e o alojamento O da pasta TESTE_ENCAIXE deste pacote; mantenha a organização das pastas ao executar.
