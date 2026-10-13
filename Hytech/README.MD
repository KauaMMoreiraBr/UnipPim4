# HyTech — Relatório de Atualização

**Data:** 13/10/2026
**Escopo desta atualização:** ilustrações e ícones da **área do aluno**. A home recebeu o mascote da HyTech.

Este documento compara o `index.html` anterior com a versão atual (`hytech.rar`) e descreve o que mudou.

---

## 1. Resumo

Os emojis usados como ícones e ilustrações foram substituídos por **imagens PNG e WebP**, organizadas em uma nova pasta `assets/`. O `index.html` passou a carregar essas imagens, e o projeto agora precisa da pasta `assets/` ao lado dele para funcionar.

| | Antes | Agora |
|---|---|---|
| `index.html` | 6.099 linhas | 6.171 linhas |
| Ícones e ilustrações | Emojis no código | 38 imagens em `assets/` (cerca de 690 KB) |
| Imagens soltas | Pasta `banco de imagens/` | Pasta `assets/social/` |

---

## 2. Estrutura de pastas

```
hytech/
├── index.html
├── assets/
│   ├── badges/
│   │   ├── conquistas/    8 imagens (.webp, 192×192)
│   │   └── niveis/        5 imagens (.webp, 256×256)
│   ├── icons/
│   │   ├── atalho/        conteudo.webp, desafio.webp
│   │   ├── desafio/       sem-desafio.webp
│   │   ├── menu/          inicio, modulos, jogar, desafios, ranking, configuracoes, ticket-suporte (.png, 52×52)
│   │   ├── perfil/        chave, fases, fases-concluidas, ranking, ver-perfil (.png)
│   │   ├── ticket/        ticket.png, chat.png
│   │   └── trilha/        alerta.png
│   ├── mascote/           mascote-home.webp (900×900, fundo transparente)
│   ├── materias/          programacao, design, banco-de-dados, redes (.webp, 320×320)
│   └── social/            instagram-white.png, facebook-white.png
└── originais/             arquivos originais (badges, icons, materias)
```

---

## 3. O que mudou, por tela

### Home (página pública)
- **Mascote da HyTech** no lugar do emoji de computador (🖥️) do destaque principal.
  - Imagem: `assets/mascote/mascote-home.webp`.
  - Tamanho maior (440×440 px, antes a caixa era 260×200), com brilho lavanda atrás para destacar do fundo roxo e uma animação leve de flutuação, que é desativada para quem prefere menos movimento.
  - No celular (até 768 px) o mascote agora aparece, com 260×260 px, abaixo do texto. Antes a imagem ficava escondida.
- **Redes sociais do rodapé:** os ícones passaram de `banco de imagens/instagramWhite.png` e `facebookWhite.png` para `assets/social/instagram-white.png` e `facebook-white.png`, com texto alternativo.

### Menu lateral (todas as páginas do aluno)
- Os 7 itens trocaram emoji por ícone PNG: Início, Acessar módulo, Jogar agora, Desafios, Ranking, Configurações e Ticket de suporte (`assets/icons/menu/`).
- **Ilustração do topo da sidebar** passou a ser uma imagem em cada página:

| Página | Antes | Agora |
|---|---|---|
| Início | 🖥️ | ícone de início (casinha) |
| Acessar módulo | 🖥️ | imagem da matéria selecionada |
| Jogar agora | 🧭 | imagem da matéria selecionada |
| Desafios | 🎯 | ícone de desafios |
| Ranking | 🏆 | ícone de medalha |
| Configurações | 👤 | ícone de ver perfil (branco) |
| Ticket de suporte | 🎫 | ícone de ticket |

- **Sidebar padronizada:** o menu mudava de posição ao navegar entre as páginas, porque o topo tinha alturas diferentes. Agora a área da ilustração tem altura fixa (96 px) em Início, Acessar módulo, Desafios, Ranking, Configurações e Ticket de suporte. Em Acessar módulo a imagem da matéria ficou em 64 px. A página Jogar agora manteve o tamanho próprio (104 px).

### Painel do perfil (menu do avatar)
- Chaves, posição no ranking e fases agora usam ícones (`chave`, `ranking`, `fases`) em vez de 🗝️ 🏆 ▶️.
- Botões "Editar perfil" e "Ver perfil" ficaram sem emoji.

### Início (dashboard)
- Cards de atalho "Conteúdo" e "Desafio" com imagens WebP (`assets/icons/atalho/`), no lugar de 📖 e 🎮.

### Acessar módulo (Hub de aulas)
- Lista de matérias com a imagem de cada matéria (Programação, Design, Banco de Dados e Redes), no lugar de 💻 🎨 🗄️ 🌐.
- Selos "Vale 3 Chaves" e "Vale 5 Chaves" com o ícone de chave em imagem.

### Jogar agora (Trilhas)
- Sidebar com as imagens das matérias.
- Tela "Conclua os Tópicos Primeiro!": o emoji 📚 foi trocado pelo ícone de alerta (`assets/icons/trilha/alerta.png`, 56 px).
- Cards de questão com o ícone de chave em imagem.

### Desafios
- Título "Desafios" sem emoji.
- Abas de filtro (Todas, Programação, Design, Banco de Dados, Redes) sem emoji, com a imagem de cada matéria.
- Tela sem desafios com a ilustração `sem-desafio.webp`, no lugar do 🎯.

### Ranking
- **Níveis:** os 5 níveis (Iniciante, Explorador, Aprendiz, Desenvolvedor e Mestre Python) agora têm imagem própria, no lugar de 🥚 🌱 ⚡ 🔥 🐍.
- **Conquistas:** as 8 conquistas têm imagem própria (Primeiro Passo, Leitor, Coletor, Desafiante, Desbravador, Certificado I, All Star e Pythonista). As ainda bloqueadas aparecem esmaecidas em tons de cinza. Antes elas mostravam um 🔒.
- **Progresso por matéria:** ícones de matéria em imagem.
- **Títulos sem emoji:** "Progresso Geral", "Progresso por Matéria" e "Conquistas".
- O texto do próximo nível ("Explorador (19 chaves)") usa o ícone de chave em imagem.

### Configurações (perfil)
- Resumo do perfil (chaves, posição no ranking e fases concluídas) com ícones em imagem.
- Campos do formulário sem os ícones de emoji.

### Ticket de suporte
- Ícones de ticket e de chat em imagem (`assets/icons/ticket/`).
- Botão "Enviar Ticket" sem emoji.
- Mensagem de "nenhum ticket aberto" com o ícone em imagem.

---

## 4. Mudanças técnicas no `index.html`

**CSS**
- Nova seção `ÍCONES E IMAGENS (pasta assets/)`, com a classe base `.ico` e as classes `.ico-inicio`, `.ico-modulos`, `.ico-jogar`, `.ico-desafios`, `.ico-ranking`, `.ico-config`, `.ico-ticket`, `.ico-chave`, `.ico-medalha`, `.ico-fases`, `.ico-play` e `.ico-user`.
- Classes de tamanho para as imagens: `.mat-ico*`, `.chave-ico`, `.nivel-img`, `.conq-img`, `.es-img`, `.tv-img` e `.acao-card-img img`.
- `.hero-imagem` reescrita para o mascote (brilho, sombra, animação e versão para celular).
- Regras da sidebar padronizada, aplicadas só às páginas do aluno, exceto Jogar agora.

**JavaScript**
- Novas constantes e funções: `MAT_IMG`, `matImg()`, `CHAVE_IMG`, `IMG_NIVEIS`, `IMG_CONQUISTAS`, `_setNivelBadge()`, `_setMascoteMateria()` e `_esc()`.
- Os dados de `NIVEIS` e `CONQUISTAS_DEF` passaram de um campo `icone` (emoji) para um campo `img` (nome do arquivo).
- `renderHub()` e `renderTrilha()` atualizam a imagem da matéria na sidebar.

**Correção**
- O id da aba "Banco de Dados" em Desafios era `dab-aluno-BancoDeDados`. O JavaScript monta o id removendo os espaços do nome da matéria, que resulta em `BancodeDados`. O id foi ajustado para esse valor, e a aba passa a ficar destacada ao ser clicada.

---

## 5. Verificação
- As 38 imagens referenciadas no código existem em `assets/`, e nenhum arquivo da pasta ficou sem uso.
- O `index.html` não tem mais referências à pasta `banco de imagens/`.
