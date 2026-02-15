# 📚 Anotações de Estudo: HTML5 e CSS3

## 📑 Módulo 1: Fundamentos da Web e Estrutura

### 🌐 A Internet e Conexão
* **Origem:** Surgiu através da **ARPANET**, uma rede desenvolvida pelos militares durante a Guerra Fria.
* **Conexão Cliente/Servidor:** A conexão ocorre via solicitação direta ao servidor. 
* **TCP/IP:** Utiliza este protocolo para fragmentar a mensagem em pacotes menores por diversas rotas até o cliente. Isso evita travamentos e lentidão. O TCP/IP do aparelho receptor junta todos os pacotes e exibe a informação.



### 🛠️ Pilares do Desenvolvimento
* **HTML (Conteúdo):** Focado no que o site diz (Texto, Imagem, Vídeo, Tabela).
* **CSS (Design):** Focado na aparência (Cores, Sombras, Tamanhos, Posicionamentos).
* **JS (Interações):** Focado no comportamento (Menus, Animações, Pop-ups, Validações).

---

### 🏷️ Tags HTML: Dicionário e Semântica

#### Estrutura Básica e Texto
* `h1` até `h6`: **Heading** - São os títulos. Vão do nível 1 (mais importante) até o 6.
* `p`: Parágrafo comum.
* `hr`: **Horizontal row** - Cria uma linha horizontal divisória.
* `br`: Quebra de linha manual.
* `b`: Negrito (apenas visual, sem semântica).
* `strong`: Destaque (com semântica para buscadores).
* `i`: Itálico (apenas visual).
* `em`: Ênfase (com semântica).
* `mark`: Efeito de marca-texto.
* `big`: Letra grande (Tag obsoleta).
* `small`: Letra pequena.
* `del`: Texto excluído (riscado no meio).
* `ins`: Texto inserido (sublinhado).
* `sup` / `sub`: Texto sobrescrito e subscrito (ex: potências ou fórmulas químicas).

#### Citações e Códigos
* `code`: Usado para exibir trechos de códigos de programação.
* `pre`: Mantém a indentação e os espaços exatamente como estão digitados no documento original.
* `q`: Citação curta (insere aspas automaticamente).
* `blockquote cite='...'`: Serve para citações longas (blocos de texto).
* `abbr title='...'`: Informa ao que se refere uma abreviação (exibe legenda ao passar o mouse).

#### Listas
* `ol`: Lista Ordenada (possui atributos `type` e `start`).
* `ul`: Lista Não Ordenada (possui atributo `type`).
* `li`: **List Item** - O item individual de qualquer lista.
* `dl`: **Descriptive list** - Lista de descrição (usa `dt` para o termo e `dd` para a descrição).

#### Links e Mídias
* `a`: Âncora para links. 
    * `target=”_blank”`: Abre o link em outra aba.
    * `rel=”external”`: Indica link para site externo.
* `audio`: Serve para adicionar áudio. Usar parâmetros `controls` e `autoplay`.
* `img`: Adiciona imagens (links internos, pastas ou URLs externas).

#### Imagens Responsivas (Tag `<picture>`)
Serve para alternar imagens conforme o tamanho da tela. Colocar sempre do menor para o maior padrão:
```html
<picture>
    <source media="(max-width: 750px)" srcset="pequena.png" type="image/png">
    <source media="(max-width: 1050px)" srcset="media.png" type="image/png">
    <img src="grande.png" alt="Imagem flexível">
</picture>

```

## 🎨 Módulo 2: Estilização, Cores e Tipografia

### 🖌️ CSS: Seletores e Regras de Prioridade
* **Regra Global**: `@charset "UTF-8";` (deve ser a primeira linha do CSS).
* **Seletores**:
    * O `id` no HTML é chamado com `#` no CSS.
    * A `class` no HTML é chamada com `.` no CSS.
* **Prioridade de Estilo**: No mesmo arquivo, a prioridade segue a ordem: `Inline > Local (Interno) > Externo`.
* **Pseudo-classes (:)**:
    * `:hover`: Ativa ao passar o mouse por cima.
    * `:visited`: Personaliza um link já visitado.
    * `:active`: Cor do link ativo (quando está clicado).
* **Pseudo-elementos**: São chamados com `::`.
* **Hierarquia**: `div > p` indica que a estilização afeta apenas os parágrafos que são filhos diretos da div.

### 🎨 Representação e Harmonia de Cores
#### Maneiras de representar cores no CSS:
* **Nomes**: `color: blue; white;`.
* **RGB (Red, Green, Blue)**: `background-color: rgb(0, 0, 255);`.
* **HSL (Hue, Saturation, Luminosity)**: `background-color: hsl(240, 100%, 50%);`.
* **Dica**: No VS Code, é possível usar o atalho visual para escolher cores.

#### Harmonia das Cores:
* **Cores**: Primárias (Amarelo, Vermelho, Azul), Secundárias (Laranja, Violeta, Verde) e Terciárias (Mistura de primária + secundária).
* **Paleta**: De 3 a 5 cores + preto e branco.
* **Complementares**: Cor extrema oposta no círculo cromático (alto contraste).
* **Análogas**: Cores vizinhas que não possuem contraste tão forte.
* **Análogas Relacionadas**: Duas cores vizinhas, pula uma e pega a terceira.
* **Intercaladas**: Escolhe uma, pula uma ou duas (seguindo o padrão) e escolhe a próxima.
* **Tetrádicas**: Formam um tetraedro no círculo.
* **Monocromia**: Alteração da saturação e luminosidade da cor escolhida.
* **Degradê**: `background-image: linear-gradient(direção, cor1, cor2);`. Pode-se usar graus (`45deg`) ou formas (`circle`).



### 📦 Modelo de Caixas (Box Model)
Toda caixa é composta por: **Conteúdo (Content) -> Padding -> Border -> Outline -> Margin**.



* **box-level**: Ocupam a linha toda (Ex: `div`, `h1-h6`, `main`, `header`, `footer`).
* **inline-level**: Ocupam apenas o espaço do conteúdo (Ex: `span`, `a`, `code`, `strong`, `button`).
* **Shorthand Padding/Margin**: `padding: cima direita baixo esquerda;` (sentido horário). Ex: `padding: 10px 20px;` (10px cima/baixo e 20px laterais).
* **Centralizar caixa**: Use `margin: auto;` (a caixa precisa ser `display: block`).
* **Borda Arredondada**: `border-radius: 10px;`. Para fazer um círculo: `width` e `height` iguais + `border-radius: 50%`.
* **Sombra (Box-shadow)**: `box-shadow: deslocamento_H deslocamento_V blur espalhamento cor;`.

### 🖋️ Tipografia e Medidas
* **Medidas Absolutas**: `cm, mm, in, px, pt, pc`.
* **Medidas Relativas**:
    * `em`: Relativa ao tamanho atual da fonte.
    * `rem`: Relativa à fonte root (body).
    * `vw/vh`: Relativa à largura ou altura da tela (viewport).
* **Shorthand para Fontes**: `font: style weight size family;`. Ex: `font: italic bolder 2em sans-serif;`.
* **Formatos de Fontes**: `otf`, `ttf`, `embedded-opentype`, `truetype-aat`, `svg`.