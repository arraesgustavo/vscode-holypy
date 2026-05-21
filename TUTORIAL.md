# 📖 Guia Completo: Desenvolvimento e Publicação da HolyPy

Este guia contém todas as informações necessárias para manter, testar e publicar a extensão **HolyPy** no VS Code Marketplace.

---

## 🛠 1. Estrutura do Projeto

*   `package.json`: O coração da extensão. Contém metadados, ícones e declarações de contribuição (linguagens, gramáticas, snippets).
*   `syntaxes/holypy.tmLanguage.json`: Define as regras de destaque de sintaxe (TextMate Grammar).
*   `language-configuration.json`: Define comportamentos do editor como auto-fechamento de parênteses, comentários e indentação.
*   `snippets/holypy.json`: Atalhos de código (ex: digitar `fn` e apertar `tab`).
*   `logos/`: Contém o ícone da extensão (`logo.png`) e o ícone dos arquivos `.hpy` (`logo_vscode.png`).

---

## 🚀 2. Teste Local (Desenvolvimento)

Sempre teste suas alterações antes de publicar.

### Modo de Depuração (Rápido)
1.  Abra a pasta do projeto no VS Code.
2.  Pressione **F5**.
3.  Uma nova janela do VS Code abrirá. Crie ou abra um arquivo `.hpy` para ver a sintaxe e os snippets em ação.

### Instalando como uma Extensão Real (VSIX)
Para usar a extensão no seu VS Code sem depender do modo de depuração:
1.  Instale o empacotador: `npm install -g @vscode/vsce`
2.  Gere o pacote: `vsce package`
3.  No VS Code: Vá em **Extensions** -> `...` (canto superior direito) -> **Install from VSIX...** e selecione o arquivo `.vsix` gerado.

---

## 🌍 3. Publicação no Marketplace (Gratuito)

### Passo 1: Criar uma conta de Publisher
1.  Acesse o [Management Console do Marketplace](https://marketplace.visualstudio.com/manage).
2.  Crie um novo Publisher com o ID: `gustavofernandes`.

### Passo 2: Gerar um Personal Access Token (PAT)
A ferramenta de publicação precisa de uma "chave" para acessar sua conta.
1.  Acesse [dev.azure.com](https://dev.azure.com) e faça login.
2.  No canto superior direito (ícone de usuário), clique em **Personal access tokens**.
3.  Clique em **+ New Token**.
4.  **Configurações importantes:**
    *   **Organization:** `All accessible organizations`.
    *   **Scopes:** Selecione `Custom Defined` -> clique em `Show all scopes` lá embaixo -> Procure por **Marketplace** e marque **Manage**.
5.  Clique em **Create** e **COPIE O TOKEN**. Você não o verá novamente.

### Passo 3: Publicar via Terminal
Abra o terminal na pasta do projeto e execute:

```bash
# 1. Faça login (Cole o Token quando solicitado)
vsce login gustavofernandes

# 2. Publique a extensão
vsce publish
```

---

## 🔄 4. Como Atualizar a Extensão
Quando você fizer melhorias (ex: adicionar novos snippets ou corrigir cores):

1.  Abra o `package.json`.
2.  Aumente o número da versão (ex: de `0.0.1` para `0.0.2`).
3.  Execute `vsce publish` novamente.

---

## 💡 Dicas de Manutenção

*   **Gramática:** Se adicionar uma nova palavra-chave na linguagem, lembre de incluí-la no `syntaxes/holypy.tmLanguage.json`.
*   **README:** O Marketplace usa o seu `README.md` como a página principal da extensão. Mantenha-o atualizado com exemplos de código.
*   **Licença:** É recomendável ter um arquivo chamado `LICENSE` na raiz para que as pessoas saibam como podem usar seu código.

---
*Gerado por Gemini CLI em 21 de Maio de 2026.*
