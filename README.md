# ToDoList (Compose)

Aplicativo Android de lista de tarefas feito com Kotlin, Jetpack Compose e Material 3.

## Funcionalidades

- Criar conta, login e logout
- Criar, editar, concluir/desfazer e excluir tarefas
- Lista com estado vazio e contagem de concluídas / total
- Interface reativa baseada em estado (atualiza automaticamente quando os dados mudam)

## Telas

- Login
- Criar conta
- Lista de tarefas
- Adicionar/Editar tarefa

## Decisões de arquitetura

- UI (Compose)
    - Telas e componentes `@Composable` focados em renderização e eventos
    - Componentes reutilizáveis para itens da lista

- ViewModel
    - Mantém o estado das telas e processa ações do usuário
    - Expõe dados via `StateFlow` e emite eventos de UI (ex.: navegação)

- Repositórios
    - Camada de acesso a dados para autenticação e tarefas
    - Implementações concretas encapsulam detalhes do backend

- AppContainer
    - Ponto central para obter dependências, mantendo o projeto simples sem framework de DI

- Navegação
    - Rotas organizadas por feature, com suporte a parâmetros (ex.: edição por id)
