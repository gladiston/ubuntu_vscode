
# Configurar o Visual Studio Code como Editor Padrão

Este documento fornece orientações para configurar o Visual Studio Code como editor padrão para arquivos de programação e arquivos no formato `.md`.

---

## 1. Associar Arquivos no Gerenciador de Arquivos
1. **Clique com o botão direito** no arquivo que deseja associar (.md ou arquivos de programação, como .js, .py, etc.).
2. Escolha **Propriedades** ou **Abrir com**.
3. Selecione o **Visual Studio Code** e clique em **Definir como padrão**.

---

## 2. Usar a Linha de Comando
Você pode definir o Visual Studio Code como editor padrão usando os seguintes comandos no terminal:

### 2.1. Configurar o MIME para o VS Code
```bash
xdg-mime default code.desktop text/markdown
xdg-mime default code.desktop text/x-python
xdg-mime default code.desktop text/x-shellscript
```

Substitua os tipos MIME conforme necessário para outros arquivos.

### 2.2. Verificar a Associação
Para confirmar que o VS Code foi configurado corretamente como editor padrão, use:
```bash
xdg-mime query default text/markdown
```

---

## 3. Configurar como Editor Padrão no Terminal
Se você deseja configurar o VS Code como editor padrão para abrir arquivos via terminal:

1. Adicione o VS Code como uma alternativa de editor:
   ```bash
   sudo update-alternatives --install /usr/bin/editor editor /usr/bin/code 1
   ```

2. Configure-o como editor padrão:
   ```bash
   sudo update-alternatives --config editor
   ```

---

## 4. Configuração no Próprio VS Code
1. Abra o **Visual Studio Code**.
2. Vá para **File > Preferences > Settings** ou use `Ctrl + ,`.
3. Configure os arquivos para abrir com extensões apropriadas ou instale as extensões necessárias no Marketplace do VS Code (por exemplo, extensões para Markdown ou Python).

---

## 5. Testar a Configuração
Teste abrindo um arquivo pelo terminal:
```bash
code arquivo.md
```

Se o comando `code` não funcionar, verifique se ele está no PATH usando:
```bash
code --version
```

---

## Referências
- Documentação oficial do Visual Studio Code: https://code.visualstudio.com/docs
- Guia sobre MIME types no Linux.

---

Autor: Gladiston Santana  
Data: 2025-01-02
