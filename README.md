# Projeto-da-loja-Virtual
Um projeto desenvolvido para criar um site baseado em uma loja virtual, usando html e css. - Vitor
Projeto Final (Prof. Vitor) PPS
Tema:  Desenvolver um site de uma loja de eletrônicos.

Uma loja virtual completa de artigos nerds, RPG e periféricos gamers de alto desempenho desenvolvida **exclusivamente com HTML5 e CSS3**, sem nenhuma linha de JavaScript ou linguagens de programação.

Este projeto demonstra a potência máxima e flexibilidade das especificações modernas de CSS3, utilizando técnicas clássicas de formulários (Checkbox Hack, Radio Button Hack) e pseudo-classes nativas do HTML5 (`:target`, `:checked`, `:hover`, `~`, `+`) para entregar uma experiência de e-commerce totalmente funcional, rica, dinâmica e responsiva.

---

## 📋 Estrutura de Pastas Implementada (Seguindo a Imagem 1)

O projeto foi estruturado exatamente conforme as diretrizes acadêmicas:

```
projeto-loja/
├── index.html        # Página inicial (Hero banner, mundos de categorias, destaques)
├── sobre.html        # Página sobre a guilda e Painel Administrativo de Mestre
├── produtos.html     # Catálogo completo com filtros CSS, modais :target e checkout de pagamento
├── contato.html      # Central de atendimento com mapa rúnico e acordeão FAQ (details & summary)
├── css/
│   └── style.css     # Estilos centralizados e lógicas de interatividade CSS-only
└── img/              # Banco de imagens mockadas e geradas por inteligência artificial
    ├── notebook.jpg  # Laptop gamer premium (Exigido)
    ├── mouse.jpg     # Mouse gamer ergonômico RGB (Exigido)
    ├── headset.jpg   # Headset surround wireless (Exigido)
    ├── dados.jpg     # Dados místicos de RPG (Poliédricos Obsidian)
    ├── camisa.jpg    # Camiseta geek vaporwave arcade
    └── jogo.jpg      # Jogo de tabuleiro medieval estratégico
```

---

## 🛠️ Comandos e Elementos Utilizados (Seguindo a Imagem 2)

Para garantir nota máxima na avaliação, os elementos do HTML5 e propriedades de CSS3 exigidos no escopo foram implementados de forma orgânica e natural em todo o projeto. Veja onde encontrá-los na folha de estilos `css/style.css`:

### Elementos HTML
*   **`body`**: Estilizado com plano de fundo escuro profundo e fontes modernas importadas do Google Fonts (`style.css: Linhas 20-27`).
*   **`header`**: Menu superior fixo (`position: sticky`) com efeito de vidro translúcido (`backdrop-filter`) e distribuição flexível (`style.css: Linhas 29-41`).
*   **`nav`**: Contém os links de navegação com efeitos de hover com linhas expansivas (`style.css: Linhas 43-47`).
*   **`main`**: Centraliza e define larguras máximas com espaçamentos elegantes para o conteúdo (`style.css: Linhas 77-82`).
*   **`article`**: Usado para cards de produtos e blocos informativos, com animações tridimensionais no hover (`style.css: Linhas 84-96`).
*   **`form`**: Utilizado em modais de login, caixas de checkout e caixa de missivas (`style.css: Linhas 98-106`).
*   **`a href`**: Links de navegação e botões estilizados, com transições graduais (`style.css: Linhas 49-65`).
*   **`img`**: Ajuste responsivo de imagens, mantendo proporções sem distorções no grid (`style.css: Linhas 67-75`).

### Propriedades CSS
*   **`display: flex`**: Alinhamento de cabeçalho, cart, formulários e abas (`style.css: Linhas 38, 44, 99...`).
*   **`justify-content`**: Distribuição espacial de elementos (`style.css: Linhas 40, 104...`).
*   **`padding`**: Espaçamentos internos consistentes nos cards e containers (`style.css: Linhas 26, 41, 56, 102...`).
*   **`margin`**: Margens externas para afastar seções de forma respirável (`style.css: Linhas 25, 80...`).
*   **`font-family`**: Fontes premium *Outfit* e *Inter* do Google Fonts (`style.css: Linhas 23`).
*   **`background-color`**: Paleta dark premium baseada em tons espaciais e luzes neon (`style.css: Linhas 21, 22...`).
*   **`width` & `height`**: Dimensionamento rígido do cabeçalho, modais e carrinho deslizante (`style.css: Linhas 39, 40, 245...`).
*   **`border`**: Linhas delimitadoras sutis e acentos de cores neon em focos e botões (`style.css: Linhas 31, 86, 101...`).
*   **`position`, `relative` & `absolute`**: Utilizados no posicionamento de badges de loots, overlays de modais e carrinho lateral (`style.css: Linhas 32, 57, 58...`).
*   **`transition` & `hover`**: Micro-interações suaves para dar vida ao site com luzes de neon quando o mouse passa por cima (`style.css: Linhas 54, 61, 74, 91...`).

---

## 🔮 Como Funciona a Interatividade Avançada Sem JavaScript?

O grande diferencial técnico deste e-commerce é a implementação de recursos dinâmicos complexos usando exclusivamente as regras estruturais e de estilização da W3C:

### 1. 🛒 Carrinho de Compras Lateral
*   **Como funciona**: Um elemento `<input type="checkbox" id="cart-toggle">` fica oculto no topo da página. Ao clicar nos ícones da loja ou no botão fechar (que são `<label for="cart-toggle">`), o estado `:checked` é alterado.
*   **CSS Hack**: Usando o seletor irmão geral (`~`), quando o rádio está ativado, o painel do carrinho muda de `right: -450px` (escondido) para `right: 0` com uma transição suave.
    ```css
    #cart-toggle:checked ~ .cart-sidebar { right: 0; }
    ```

### 2. 👤 Autenticação de Usuário (Modais de Login/Registro)
*   **Como funciona**: De forma parecida com o carrinho, ao clicar no ícone de perfil (uma label), ativa-se o `#auth-toggle`. A sobreposição do modal (`.modal-overlay`) muda de `display: none` para `display: flex`.
*   **Abas Internas**: Dentro do modal, rádios de input controlam a exibição do formulário de Login ou Registro usando `#auth-tab-login:checked ~ .form-login { display: flex; }`.

### 3. 🛍️ Catálogo de Produtos e Filtros Dinâmicos
*   **Como funciona**: No topo da página de catálogo (`produtos.html`), há 5 rádio-botões para representar as categorias. Os botões laterais de filtro são apenas `labels` que selecionam esses rádios.
*   **CSS Hack**: Usamos seletores de negação `:not()` combinados com `:checked` para sumir com os cards que não batem com a categoria ativa!
    ```css
    #filter-rpg:checked ~ .catalog-layout .products-grid .product-card:not(.cat-rpg) { display: none; }
    ```

### 4. 🔍 Modais :target para Detalhes do Produto
*   **Como funciona**: Em vez de checkboxes, cada card tem um link direto para a ID de um modal (ex: `<a href="#detail-dados">`).
*   **CSS Hack**: O navegador suporta nativamente focar em âncoras na URL. Usamos a pseudo-classe `:target` para exibir o modal ativo. Clicar no botão Fechar apenas redireciona para `#` (limpando o foco e ocultando o modal).
    ```css
    .detail-modal:target { display: flex; }
    ```

### 5. ⭐ Avaliações Estrela Interativas
*   **Como funciona**: No formulário de review dentro do modal de detalhes, cinco rádios invisíveis representam notas de 1 a 5 estrelas. Eles são declarados em ordem inversa no HTML.
*   **CSS Hack**: Usando o seletor irmão geral (`~`), iluminamos a estrela selecionada e todas as anteriores a ela ao mesmo tempo ao passar o mouse ou clicar!
    ```css
    .interactive-stars label:hover,
    .interactive-stars label:hover ~ label,
    .interactive-stars input:checked ~ label { color: #ffb800; }
    ```

### 6. 💳 Seleção de Pagamento no Checkout
*   **Como funciona**: Rádios controlam se o cliente seleciona Cartão de Crédito, Pix ou Boleto.
*   **CSS Hack**: Quando um método está ativo, o formulário específico dele fica visível: `#pay-pix:checked ~ .payment-details-pix { display: block; }`, enquanto os outros permanecem ocultos.

### 7. 📊 Painel Administrativo com Gráficos Customizados
*   **Como funciona**: Na aba "Sobre Nós", há uma área restrita (Painel do Mestre). Nele, você pode alternar entre abas de estatísticas, inventário e upload usando rádios de abas.
*   **CSS Chart**: O gráfico semanal é desenhado com colunas flexíveis de alturas absolutas. Cada coluna possui um atributo `data-value` que gera uma legenda tooltip em flutuação ao passar o mouse via seletores `::after`.

---

## 🚀 Como Visualizar o Projeto Localmente

Como o projeto é estritamente estático (HTML/CSS puro), você **não precisa de servidores complexos, bancos de dados, node ou npm**. 

Basta seguir um dos passos abaixo:

### Método 1: Abertura Direta (Mais Simples)
1.  Navegue até a pasta `projeto-loja/`.
2.  Dê um clique duplo em `index.html`.
3.  O site se abrirá diretamente em seu navegador padrão com todos os links, interatividades e imagens funcionando perfeitamente!

### Método 2: Servidor Estático Simples (Recomendado para Devs)
Se você estiver utilizando o VS Code ou outro editor, pode utilizar uma extensão como o **Live Server** ou rodar um servidor em Python na raiz da pasta `projeto-loja/`:
```bash
python -m http.server 8000
```
Depois, acesse `http://localhost:8000` em seu navegador.

---

**Desenvolvido com carinho, criatividade e paixão pela cultura geek e boas práticas de CSS!** 🎲🧙‍♂️👾


