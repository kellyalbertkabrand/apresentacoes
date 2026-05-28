# CLAUDE.md — Instruções do projeto

## Gatilho: "MODELO YUFIL" / "modelo Base Estratégica"

Quando o usuário pedir para **gerar uma apresentação no "MODELO YUFIL"** (ou
"modelo Base Estratégica"), ele quer um `.pptx` seguindo EXATAMENTE o padrão
visual documentado neste repositório. Não invente outro estilo.

### Como executar o pedido
1. Leia o padrão completo em **`MODELO-APRESENTACAO-YUFIL.md`** (formato, paleta,
   tipografia, arquétipos de slide e roteiro de seções).
2. Use **`gerar-modelo.py`** como base — ele já contém os helpers e os 10
   arquétipos de slide com o padrão visual aplicado. Adapte o conteúdo
   (textos, marca, seções) ao que o usuário enviar e gere o `.pptx`.
3. Reaproveite os assets em **`assets/`** (`textura-papel.jpeg` = fundo cinza).
4. Salve o resultado como `.pptx`, faça commit no branch de trabalho e
   entregue o arquivo ao usuário com `SendUserFile`.

### Regras visuais inegociáveis (já validadas com o usuário)
- Formato 16:9 (20" × 11,25").
- **Fundo CINZA** (textura `assets/textura-papel.jpeg`, ~#EAEAEA) **somente** na
  **capa, no sumário e nas páginas que separam grandes temas** (divisores).
  Todos os demais slides: **fundo gelo liso `#F6F5F0`**.
- **Sem rodapé** (não escrever "BASE ESTRATÉGICA…") e **sem logotipo**.
- **Fonte única: Outfit** (todos os textos). Nada de Calibri/Playfair/IBM Plex.
- Paleta: títulos `#1A1A1A`/`#000000`, corpo `#7A7A72`, acento areia `#C8BFA8`,
  blocos `#E8E4D8`/`#D4D9CB`, branco sobre blocos escuros, vermelho `#FF3131`
  só para ênfase pontual.
- Capa: título em duas linhas a 75pt. Divisor de tema: título ~100pt.
  Título de slide de conteúdo: 39pt. Eyebrow/kicker: 16,5pt caixa alta `#7A7A72`.

### O que pedir ao usuário (se faltar)
Marca/título, mês-ano, lista de seções (= divisores), o texto de cada slide e
eventuais imagens/fotos.

### Observação de ambiente
LibreOffice não funciona aqui, então não tente renderizar prévia em imagem;
entregue o `.pptx` e peça feedback visual ao usuário.
