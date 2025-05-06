# Guia de Contribuição - Clone TabNews

Este documento contém regras e diretrizes para o desenvolvimento e manutenção do projeto "Clone TabNews". Estas regras podem e devem ser aprimoradas ao longo do tempo.

## Tecnologias Utilizadas

- **Next.js**: versão 13.1.6
- **React**: versão 18.2.0
- **Node.js**: LTS/Hydrogen
- **JavaScript**: ECMAScript moderno

## Estrutura do Projeto

### Organização de Diretórios

- `/pages`: Contém as rotas da aplicação (padrão Next.js)
  - `/api`: Endpoints da API REST
  - `/[username]`: Páginas de perfil de usuário
  - `/[username]/[slug]`: Páginas de conteúdo específico
- `/components`: Componentes React reutilizáveis
  - `/ui`: Componentes de UI básicos (botões, inputs, etc.)
  - `/layout`: Componentes de layout (header, footer, etc.)
  - `/features`: Componentes específicos de features
- `/styles`: Arquivos de estilo globais e variáveis
- `/public`: Arquivos estáticos
- `/lib`: Funções utilitárias e lógica de negócios
- `/models`: Modelos de dados e interação com banco de dados
- `/tests`: Testes automatizados
  - `/unit`: Testes unitários
  - `/integration`: Testes de integração
  - `/e2e`: Testes end-to-end

### Convenções de Nomenclatura

- **Arquivos e Diretórios**: Use kebab-case para arquivos e diretórios (`user-profile.js`)
- **Componentes React**: Use PascalCase para componentes (`UserProfile.jsx`)
- **Funções e Variáveis**: Use camelCase (`getUserData()`)
- **Constantes**: Use UPPER_SNAKE_CASE para constantes globais (`MAX_USERNAME_LENGTH`)
- **Arquivos de Testes**: Nomeie como `[nome-do-arquivo].test.js` ou `[nome-do-arquivo].spec.js`

## Padrões de Código

### Estilos de Código

- Usar 2 espaços para indentação
- Usar ponto e vírgula ao final das instruções
- Usar aspas simples para strings
- Manter linhas com no máximo 100 caracteres
- Adicionar espaço entre operadores

### Boas Práticas JavaScript/React

- Preferir funções de componente com hooks ao invés de componentes de classe
- Usar desestruturação para props e state
- Evitar uso excessivo de estados globais
- Utilizar React.memo() para componentes que não precisam re-renderizar frequentemente
- Usar nomes descritivos para variáveis e funções

### Importações

- Agrupar importações na seguinte ordem:
  1. Bibliotecas externas (React, Next.js, etc.)
  2. Componentes internos
  3. Utilitários, hooks, etc.
  4. Estilos e assets

## Controle de Versão

### Commits

- Usar commits atômicos (cada commit deve representar uma única alteração lógica)
- Seguir o padrão Conventional Commits:
  - `feat`: Nova feature
  - `fix`: Correção de bug
  - `docs`: Alteração na documentação
  - `style`: Alterações que não afetam o significado do código (espaço em branco, formatação, etc.)
  - `refactor`: Refatoração de código
  - `test`: Adição ou correção de testes
  - `chore`: Alterações em processos de build ou ferramentas auxiliares

### Branches

- `main`: Branch principal, sempre estável
- `develop`: Branch de desenvolvimento
- `feature/[nome-da-feature]`: Para desenvolvimento de novas features
- `fix/[nome-do-bug]`: Para correção de bugs
- `refactor/[nome-da-refatoração]`: Para refatorações de código

## Testes

- Escrever testes para novas funcionalidades
- Manter cobertura de testes acima de 70%
- Testes devem ser independentes entre si
- Usar mocks quando necessário para isolar componentes
- Utilizar Jest como framework de testes

## Documentação

- Comentar código complexo ou não óbvio
- Documentar APIs e componentes públicos
- Manter README atualizado com:
  - Descrição do projeto
  - Como instalar e executar
  - Como contribuir
  - Como reportar bugs

## Ferramentas de Qualidade

### Implementadas
- .nvmrc para controle de versão do Node.js

### Sugestões para Implementação Futura
- ESLint para análise estática de código
- Prettier para formatação consistente
- Husky para git hooks (pre-commit, pre-push)
- Jest para testes unitários e de integração
- Cypress para testes end-to-end
- GitHub Actions para CI/CD

## Acessibilidade

- Todos os componentes de UI devem ser acessíveis
- Seguir as diretrizes WCAG 2.1 nível AA
- Garantir navegação por teclado
- Fornecer textos alternativos para imagens

## Performance

- Otimizar imagens e assets
- Implementar lazy loading para componentes pesados
- Monitorar e otimizar renderizações desnecessárias
- Usar Server-Side Rendering (SSR) ou Static Site Generation (SSG) quando apropriado

## Fluxo de Desenvolvimento

1. Criar uma branch a partir da `develop` seguindo a convenção de nomenclatura
2. Desenvolver a feature/correção
3. Escrever/atualizar testes
4. Certificar-se de que todos os testes passam
5. Atualizar documentação se necessário
6. Fazer commit seguindo o padrão Conventional Commits
7. Abrir um Pull Request para a branch `develop`
8. Aguardar revisão e aprovação

---

Este documento é vivo e deve evoluir com o projeto. Sugestões de melhorias são sempre bem-vindas!
