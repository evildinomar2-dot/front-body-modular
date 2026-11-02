# Front Body V1 modular para Fusion

[**BAIXAR O PACOTE COMPLETO — ZIP, aproximadamente 44 MB**](https://github.com/evildinomar2-dot/front-body-modular/raw/refs/heads/main/Pacote_completo_Fusion.zip)

Extraia o ZIP inteiro e abra `MONTAGEM_MODULAR.step` no Autodesk Fusion. O pacote também contém oito STEP individuais, oito STL, imagens, instruções, fontes e o STL original preservado. Não requer instalar Python para abrir os STEP.

![Vista explodida dos STL finais](EXPLODIDO.png)

## Peças

Capô, dois para-lamas, dois painéis laterais, painel do para-brisa, teto e moldura/calha/colunas. Escala numérica original mantida; unidade assumida: milímetro. Largura original aproximada de 197,56 mm.

## Encaixes e edição

O capô tem quatro pinos removíveis de Ø4,0 mm e alojamentos de Ø4,6 mm nos para-lamas. As demais peças têm guias internas de posicionamento para colagem ou fixação adicional a projetar, com folga nominal de 0,30 mm por lado. O capô não tem dobradiça e os encaixes não foram testados fisicamente. A adaptação ao chassi modificado ainda não foi feita.

Os STEP são sólidos BRep **facetados, derivados do STL**, sem recuperação de superfícies NURBS ou histórico paramétrico original. A versão CAD foi simplificada e teve ajustes locais; não misture STEP e STL ao montar um mesmo conjunto sem conferir os contatos. Não há para-choque completo no arquivo de origem.

A montagem STEP foi exportada e reimportada com oito sólidos válidos. Os arquivos individuais também foram reabertos; os pares foram verificados por interseção volumétrica com tolerância numérica. Esses testes foram feitos com CadQuery/OpenCascade; a importação no Fusion e a impressão física ainda não foram testadas.

Leia [as instruções completas](INSTRUCOES.md) antes de modificar ou imprimir. O pacote inclui um script opcional de conversão para F3D que deve ser executado dentro do Fusion; ele não foi executado na nuvem.

![Encaixes internos dos STL](ENCAIXES_INTERNOS.png)
