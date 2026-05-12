# Fluxo de Trabalho do Git (Git Workflow)

Este documento define o padrão obrigatório para enviar alterações para o repositório. **Nenhum membro da equipe deve fazer commits diretamente na branch `main`.** Todo o trabalho deve ser feito em branches (ramificações) isoladas e integrado via Pull Request (PR).

## Passo a Passo para Contribuir

### 1. Atualize seu repositório local
Antes de começar qualquer tarefa do Kanban, garanta que você tem a versão mais recente do código para evitar conflitos (Merge Conflicts).
```bash
git checkout main
git pull origin main
```

### 2. Crie uma nova Branch
Crie uma branch específica para a tarefa que você vai executar. Use prefixos para identificar o tipo de trabalho:
- `feature/`: Para novos conteúdos, playbooks ou novas telas.
- `fix/`: Para correção de erros, bugs ou links quebrados.
- `docs/`: Para alterar documentações internas.

```bash
git checkout -b feature/nome-da-sua-tarefa
```

### 3. Salve suas alterações (Stage)
Trabalhe nos seus arquivos. Quando terminar uma etapa lógica, adicione as mudanças ao "palco" (stage) do Git para prepará-las.
```bash
git add caminho/do/arquivo.md
# Ou, para adicionar todas as alterações de uma vez:
git add .
```

### 4. Crie o Commit
Registre a alteração com uma mensagem clara, objetiva e em português, explicando *o que* foi feito.
```bash
git commit -m "feat: adiciona o playbook do modulo 1 de windows"
```

### 5. Envie para o GitHub (Push)
Envie a sua branch local para o servidor remoto no GitHub.
```bash
git push origin feature/nome-da-sua-tarefa
```

### 6. Abra o Pull Request (PR)
1. Vá até a página do repositório no GitHub pelo navegador.
2. Você verá um aviso amarelo/verde sugerindo a sua branch recém-enviada. Clique em **"Compare & pull request"**.
3. Preencha a descrição explicando o que você alterou.
4. Aguarde a revisão de pelo menos um colega da equipe antes que o código seja aprovado e mesclado (merged) na `main`.
