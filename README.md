# 🎨 Design Tokens Sync com Figma + GitHub Actions

Este projeto utiliza uma GitHub Action chamada **Generate design tokens**, que automatiza a atualização de design tokens gerados no Figma e os transforma em arquivos `.scss`, `.js` ou `.css`, prontos para serem usados diretamente no código do seu projeto.

A funcionalidade **Design Tokens para Devs** do Figma permite exportar propriedades como cores, tipografia e espaçamentos de forma padronizada. Com o auxílio da biblioteca **[Style Dictionary](https://styledictionary.com/)**, esses tokens são convertidos e organizados em múltiplos formatos compatíveis com diversos ambientes de desenvolvimento.

Essa integração facilita a consistência entre design e código, evita erros manuais e acelera a entrega de interfaces alinhadas com o design system.

![Image](https://github.com/user-attachments/assets/c9068cf2-788e-40ab-bc33-7082c521c839)
---

## ✨ Funcionalidades

- Integração com Figma para exportação de design tokens
- Transformação automática em variáveis CSS e objetos JS
- Criação de Pull Requests automática com os tokens atualizados
- Totalmente configurado com GitHub Actions

## 🛠 Estrutura do Workflow

O workflow principal está em `.github/workflows/update-tokens.yml` e realiza as seguintes etapas:

1. Checkout do repositório
2. Geração do arquivo de tokens no diretório `input/`
3. Execução do `style-dictionary`
4. Criação de Pull Request com as mudanças

## 🧪 Como testar localmente

1. Gere seu arquivo `tokens.json` exportado do Figma
2. Execute localmente com `style-dictionary`:
   ```bash
   npm install
   npx style-dictionary build
