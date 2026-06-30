# FORGE

# UI Components Specification

Version: 1.0 Alpha

Status: Draft

---

# Índice

1. Objetivo
2. Filosofia
3. Estrutura dos Componentes
4. Componentes Base
5. Componentes Compostos
6. Componentes de Layout
7. Componentes de Navegação
8. Componentes de Dados
9. Componentes de Feedback
10. Componentes Específicos do Forge
11. Convenções
12. Checklist

---

# 1. Objetivo

Este documento define o comportamento funcional de todos os componentes visuais do Forge.

Enquanto o Design System define aparência e identidade visual, este documento estabelece regras de uso, estados, propriedades, acessibilidade e padrões de implementação.

---

# 2. Filosofia

Todo componente deve ser:

- reutilizável;
- previsível;
- acessível;
- documentado;
- independente;
- testável.

---

# 3. Estrutura dos Componentes

Todo componente deve possuir:

## Objetivo

O problema que resolve.

## Quando usar

Situações recomendadas.

## Quando não usar

Casos em que outro componente é mais apropriado.

## Props

Lista completa das propriedades.

## Estados

Loading

Disabled

Hover

Focus

Error

Success

Selected

Offline (quando aplicável)

## Variantes

Visual.

## Acessibilidade

ARIA.

Teclado.

Leitores de tela.

## Exemplos

Código.

Capturas.

Boas práticas.

---

# 4. Componentes Base

## ForgeButton

Variantes

- Primary
- Secondary
- Ghost
- Outline
- Danger
- Success
- Link

Tamanhos

- XS
- SM
- MD
- LG
- XL

Estados

- Loading
- Disabled
- Hover
- Focus
- Pressed

---

## ForgeInput

Tipos

- Text
- Number
- Email
- Password
- Search

Recursos

- Máscaras
- Validação
- Ícones
- Mensagens de erro
- Contador de caracteres

---

## ForgeSelect

- Pesquisa
- Seleção única
- Seleção múltipla
- Agrupamento
- Virtualização para listas longas

---

## ForgeCheckbox

- Estado marcado
- Desmarcado
- Indeterminado

---

## ForgeSwitch

Utilizado para configurações.

---

## ForgeSlider

Para metas, intensidade e volume.

---

## ForgeProgress

Exibe progresso em:

- XP
- Objetivos
- Treinos
- Desafios

---

# 5. Componentes Compostos

## WorkoutCard

Exibe:

- Nome do treino
- Exercícios
- Volume
- Duração
- Última execução

Ações:

- Iniciar
- Editar
- Duplicar
- Excluir

---

## ExerciseCard

Mostra:

- Nome
- Grupo muscular
- Dificuldade
- Equipamentos
- GIF/Vídeo

---

## SkillCard

Exibe:

- Skill
- XP
- Nível
- Domínio
- Próxima progressão

---

## AchievementCard

- Medalha
- XP
- Data
- Descrição

---

## ChallengeCard

- Meta
- Prazo
- Progresso
- Recompensas

---

# 6. Componentes de Layout

ForgeContainer

ForgeGrid

ForgeStack

ForgeDivider

ForgeSection

ForgePageHeader

ForgeEmptyState

---

# 7. Navegação

ForgeSidebar

ForgeTopBar

ForgeBottomNavigation

ForgeBreadcrumb

ForgeSearch

ForgeCommandPalette

---

# 8. Dados

ForgeTable

ForgeChart

ForgeTimeline

ForgeCalendar

ForgeStatistics

ForgeHistory

---

# 9. Feedback

ForgeToast

ForgeSnackbar

ForgeAlert

ForgeDialog

ForgeModal

ForgeTooltip

ForgePopover

ForgeSkeleton

ForgeSpinner

---

# 10. Componentes Específicos

ForgeWorkoutTimer

ForgeExerciseViewer

ForgeSkillTree

ForgeXPBar

ForgeStreakCounter

ForgeHeatmap

ForgeAIChat

ForgeVideoAnalysis

ForgeLeaderboard

ForgeWorkoutRecorder

---

# 11. Convenções

Todos os componentes devem:

- aceitar className;
- aceitar children quando aplicável;
- ser tipados em TypeScript;
- possuir documentação;
- possuir testes;
- seguir acessibilidade;
- utilizar Design Tokens.

---

# 12. Checklist

Antes de criar um componente:

- Existe componente semelhante?
- É reutilizável?
- Está documentado?
- Está acessível?
- Está testado?
- Segue o Design System?
- Possui exemplos?
