# FORGE

# Design System

**Versão:** 1.0 Alpha

**Status:** Em desenvolvimento

---

# Índice

1. Objetivo
2. Filosofia de Design
3. Inspirações
4. Design Tokens
5. Cores
6. Tipografia
7. Grid
8. Espaçamento
9. Bordas
10. Sombras
11. Elevação
12. Ícones
13. Ilustrações
14. Componentes
15. Layout
16. Navegação
17. Estados
18. Animações
19. Acessibilidade
20. Responsividade
21. Componentes do Forge UI
22. Convenções
23. Evolução

---

# 1. Objetivo

O Design System do Forge estabelece todos os padrões visuais e de interação da plataforma.

Seu propósito é garantir consistência, acessibilidade, qualidade visual e facilidade de manutenção.

Todo componente criado para o Forge deve seguir este documento.

---

# 2. Filosofia de Design

O Forge deve transmitir:

- confiança;
- precisão;
- tecnologia;
- disciplina;
- simplicidade;
- evolução.

A interface nunca deve parecer exagerada.

Menos elementos.

Mais significado.

---

# 3. Inspirações

O Forge não copia interfaces.

Ele se inspira em soluções consolidadas.

### Apple

- Espaçamento
- Clareza
- Minimalismo

### GitHub

- Organização
- Legibilidade
- Navegação

### Notion

- Simplicidade
- Conteúdo

### Discord

- Comunidade
- Chats
- Layout

### Material Design 3

- Componentização
- Acessibilidade

---

# 4. Design Tokens

Todo valor visual deve existir como token.

Nunca utilizar valores "soltos".

Exemplo:

Primary Color

Background Color

Surface Color

Border Radius

Spacing

Typography

Animation Duration

Shadow

Z-Index

---

# 5. Paleta de Cores

## Primary

Neon Green

Representa evolução.

---

## Secondary

Blue

Representa tecnologia.

---

## Neutral

Preto

Grafite

Cinza

Branco

---

## Success

Verde.

---

## Warning

Amarelo.

---

## Error

Vermelho.

---

## Info

Azul.

---

## Background

Background Principal

Background Elevado

Background Cards

Background Hover

---

# 6. Tipografia

Fonte principal

Inter

Fonte para código

JetBrains Mono

Escala tipográfica

Display

Heading

Title

Subtitle

Body

Caption

Overline

Todo texto deve possuir hierarquia clara.

---

# 7. Grid

Sistema baseado em 8 pixels.

Todos os componentes devem respeitar o grid.

---

# 8. Espaçamento

4

8

12

16

24

32

40

48

64

96

128

Nunca utilizar espaçamentos aleatórios.

---

# 9. Bordas

Pequeno

Médio

Grande

Circular

---

# 10. Sombras

Shadow XS

Shadow Small

Shadow Medium

Shadow Large

Shadow Floating

Utilizar sombras apenas quando necessário.

---

# 11. Elevação

Background

↓

Card

↓

Modal

↓

Drawer

↓

Tooltip

↓

Toast

↓

Dialog

---

# 12. Ícones

Biblioteca

Lucide

Tamanho

16

20

24

32

48

Ícones devem possuir peso consistente.

---

# 13. Ilustrações

Minimalistas.

Poucas cores.

Sem excesso de detalhes.

---

# 14. Componentes

Botão

Input

Select

Checkbox

Switch

Slider

Card

Avatar

Badge

Tag

Progress

Tabs

Accordion

Toast

Tooltip

Dialog

Drawer

Sidebar

Navbar

Breadcrumb

Table

Chart

Calendar

Timer

Workout Card

Exercise Card

Skill Card

Achievement Card

User Card

Challenge Card

---

Cada componente deve possuir

Objetivo

Quando usar

Quando não usar

Estados

Variantes

Exemplos

Boas práticas

---

# 15. Layout

Desktop

Tablet

Mobile

Sidebar

Topbar

Content

Footer

Cada tela deverá seguir a mesma estrutura.

---

# 16. Navegação

Sidebar

Desktop

Bottom Navigation

Mobile

Breadcrumb

Desktop

---

# 17. Estados

Loading

Empty

Error

Success

Offline

Disabled

Hover

Focus

Pressed

Selected

Todos os estados devem ser desenhados.

---

# 18. Motion Design

Animações rápidas.

Nunca exageradas.

Duração

100 ms

150 ms

200 ms

250 ms

300 ms

Curvas suaves.

Framer Motion será utilizado.

---

# 19. Acessibilidade

Contraste AA.

Suporte a teclado.

Focus visível.

ARIA Labels.

Navegação por teclado.

Leitores de tela.

---

# 20. Responsividade

Mobile First.

Breakpoints

sm

md

lg

xl

2xl

Todos os componentes devem ser responsivos.

---

# 21. Forge UI

O Forge possuirá uma biblioteca própria de componentes.

Exemplo

ForgeButton

ForgeInput

ForgeCard

ForgeDialog

ForgeChart

ForgeAvatar

ForgeSidebar

ForgeCalendar

ForgeWorkoutCard

ForgeExerciseCard

ForgeSkillTree

ForgeProgressChart

Todos reutilizáveis.

---

# 22. Convenções

Nunca utilizar cores diretamente.

Sempre utilizar tokens.

Nunca utilizar fontes diferentes.

Nunca alterar componentes base.

Novos componentes devem ser documentados.

---

# 23. Evolução

O Design System deverá crescer junto com o produto.

Toda nova funcionalidade deverá atualizar este documento antes da implementação.
