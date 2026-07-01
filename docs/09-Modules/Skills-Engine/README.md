# FORGE

# Skills Engine

**Versão:** 1.0 Alpha

**Status:** Core Module

---

# Índice

1. Visão Geral
2. Objetivos
3. Filosofia
4. Conceitos Fundamentais
5. Arquitetura do Sistema
6. Fluxos do Usuário
7. Estrutura de uma Skill
8. Progressões
9. Regressões
10. Árvore de Skills
11. Sistema de Domínio
12. XP e Evolução
13. Recomendações Inteligentes
14. Integração com IA
15. Integração com Forge DNA
16. Integração com Workout Engine
17. Gamificação
18. Banco de Dados
19. Casos de Erro
20. Critérios de Aceitação
21. Roadmap

---

# 1. Visão Geral

O Skills Engine é responsável por toda a evolução técnica do usuário.

Enquanto o Workout Engine registra os treinos, o Skills Engine acompanha aquilo que o usuário é capaz de executar.

Ele transforma habilidades em uma jornada clara de aprendizado.

---

# 2. Objetivos

- Organizar habilidades por modalidade.
- Guiar progressões.
- Sugerir regressões.
- Medir domínio.
- Acompanhar evolução.
- Motivar o usuário.

---

# 3. Filosofia

Aprender uma skill é um processo.

O Forge nunca mostrará apenas o objetivo final.

Sempre apresentará o próximo passo possível.

O foco é progresso contínuo.

---

# 4. Conceitos Fundamentais

Uma Skill é composta por:

- Nome
- Categoria
- Descrição
- Dificuldade
- Pré-requisitos
- Progressões
- Regressões
- Critérios de domínio
- Exercícios auxiliares
- Tempo estimado
- XP

---

# 5. Arquitetura do Sistema

```

Categoria

↓

Skill

↓

Estágio

↓

Exercícios

↓

Sessões

↓

Domínio

↓

XP

↓

Forge DNA

```

---

# 6. Fluxo do Usuário

Escolher Skill

↓

Ver requisitos

↓

Assistir explicação

↓

Treinar

↓

Registrar tentativa

↓

Receber feedback

↓

Atualizar progresso

↓

Desbloquear próxima etapa

---

# 7. Estrutura de uma Skill

Cada Skill possui:

- Nome
- Ícone
- Descrição
- Objetivo
- Nível
- Categoria
- Tempo médio de aprendizagem
- Equipamentos
- Vídeos
- GIFs
- Exercícios relacionados
- Músculos envolvidos
- Cuidados
- Erros comuns

---

# 8. Progressões

Cada habilidade possui uma árvore de evolução.

Exemplo:

Dead Hang

↓

Scapular Pull-up

↓

Negative Pull-up

↓

Pull-up

↓

Chest-to-Bar

↓

Muscle-up

Outro exemplo:

Frog Stand

↓

Crow

↓

Tuck Planche

↓

Advanced Tuck

↓

Straddle

↓

Full Planche

---

# 9. Regressões

Caso o usuário encontre dificuldades, o Forge recomenda versões mais acessíveis do movimento.

Exemplo:

Pull-up

↓

Band Assisted Pull-up

↓

Australian Pull-up

↓

Dead Hang

---

# 10. Árvore de Skills

As habilidades serão organizadas em um grafo navegável.

Categorias iniciais:

- Pull
- Push
- Core
- Hand Balance
- Levers
- Flags
- Mobility
- Rings
- Freestyle

Cada nó exibe:

- Estado (bloqueado, disponível, dominado)
- XP
- Pré-requisitos
- Próximas habilidades

---

# 11. Sistema de Domínio

Cada Skill possui um nível de domínio.

Exemplo:

0% — Não iniciado

25% — Aprendendo

50% — Intermediário

75% — Consistente

100% — Dominado

A progressão é baseada em:

- Frequência de treino
- Execuções registradas
- Qualidade da execução (futuro)
- Feedback da IA
- Autoavaliação do usuário

---

# 12. XP e Evolução

Treinar Skills concede XP específico.

O XP influencia:

- Nível da Skill
- Conquistas
- Desafios
- Forge DNA

Cada Skill mantém um histórico de evolução.

---

# 13. Recomendações Inteligentes

O sistema poderá recomendar:

- próxima Skill;
- exercícios auxiliares;
- mobilidade necessária;
- dias ideais de prática;
- recuperação.

As recomendações levam em conta:

- Forge DNA;
- Workout Engine;
- disponibilidade;
- equipamentos.

---

# 14. Integração com IA

A IA poderá:

- explicar uma Skill;
- sugerir correções;
- responder dúvidas;
- criar planos de progressão;
- adaptar o ritmo de aprendizado.

---

# 15. Integração com Forge DNA

As Skills influenciam atributos como:

- Técnica
- Controle corporal
- Mobilidade
- Força relativa

O DNA utiliza essas informações para atualizar o perfil do usuário.

---

# 16. Integração com Workout Engine

Ao registrar uma sessão de treino, exercícios relacionados a Skills atualizam automaticamente o progresso quando apropriado.

---

# 17. Gamificação

O módulo suporta:

- XP por Skill
- Medalhas
- Títulos
- Missões
- Sequências de treino
- Conquistas especiais por domínio

---

# 18. Banco de Dados

Entidades principais:

- Skill
- SkillStage
- SkillProgress
- SkillAttempt
- SkillRecommendation

Cada tentativa registrada fica armazenada para análise futura.

---

# 19. Casos de Erro

- Usuário tenta desbloquear Skill sem pré-requisitos.
- Dados offline ainda não sincronizados.
- Vídeo da Skill indisponível.
- Equipamento necessário não cadastrado.

O sistema deve orientar o usuário e permitir continuar utilizando os recursos disponíveis.

---

# 20. Critérios de Aceitação

- Todas as Skills possuem progressões definidas.
- O progresso é salvo automaticamente.
- Recomendações são personalizadas.
- O módulo funciona offline para consulta e registro.
- Integração correta com Workout Engine e Forge DNA.

---

# 21. Roadmap

## MVP

- Biblioteca de Skills.
- Progressões e regressões.
- Registro de tentativas.
- XP por Skill.

## Futuro

- Análise por vídeo.
- Comparação com execuções anteriores.
- Recomendações em tempo real.
- Comunidade para compartilhamento de progresso.
