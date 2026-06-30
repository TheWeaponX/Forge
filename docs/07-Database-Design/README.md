# FORGE

# Database Design

**Versão:** 1.0 Alpha

**Status:** Em desenvolvimento

---

# Índice

1. Objetivo
2. Filosofia de Dados
3. Tecnologias
4. Estratégia Offline First
5. Arquitetura Geral
6. Domínios do Banco
7. Modelo Conceitual
8. Entidades
9. Relacionamentos
10. Índices
11. Auditoria
12. Sincronização
13. Versionamento
14. Escalabilidade
15. Segurança
16. Convenções
17. Próximos Passos

---

# 1. Objetivo

Este documento define a arquitetura de dados do Forge.

Ele estabelece as entidades, relacionamentos, regras de persistência, sincronização e princípios que deverão ser seguidos durante todo o desenvolvimento.

O banco de dados deve ser preparado para milhões de usuários sem necessidade de reestruturações profundas.

---

# 2. Filosofia de Dados

Os dados são o ativo mais importante da plataforma.

O modelo de dados deve ser:

- Consistente
- Escalável
- Auditável
- Offline First
- Seguro
- Extensível
- Independente da interface

---

# 3. Tecnologias

## Banco Principal

PostgreSQL

Responsável por armazenar todos os dados oficiais da plataforma.

---

## Banco Local

SQLite

Responsável pelo funcionamento offline.

Sempre que possível, todas as operações devem ser executadas primeiro localmente.

---

## ORM

Prisma

Será utilizado para acesso ao PostgreSQL.

---

# 4. Estratégia Offline First

Fluxo padrão:

Usuário

↓

SQLite

↓

Fila de sincronização

↓

API

↓

PostgreSQL

↓

Confirmação

↓

Atualização Local

Caso não exista internet, o usuário continua utilizando normalmente o aplicativo.

---

# 5. Arquitetura Geral

O banco será dividido em domínios independentes.

Domínios:

- Users
- Workouts
- Exercises
- Skills
- Progress
- Nutrition
- Community
- Challenges
- AI
- Notifications
- Settings
- Analytics

Cada domínio poderá evoluir sem impactar os demais.

---

# 6. Modelo Conceitual

User

↓

Workout

↓

Workout Session

↓

Exercise

↓

Exercise Set

↓

Statistics

↓

Achievements

---

# 7. Entidades

## User

Representa um usuário da plataforma.

Campos principais:

- id
- name
- email
- username
- avatar
- birthDate
- gender
- height
- weight
- createdAt
- updatedAt

---

## Workout

Modelo de treino.

Campos:

- id
- userId
- title
- description
- category
- visibility
- createdAt
- updatedAt

---

## WorkoutSession

Execução real de um treino.

Campos:

- id
- workoutId
- startedAt
- finishedAt
- duration
- calories
- notes

---

## Exercise

Biblioteca de exercícios.

Campos:

- id
- name
- description
- muscleGroup
- equipment
- difficulty
- instructions
- video
- gif

---

## ExerciseSet

Cada série realizada.

Campos:

- id
- workoutSessionId
- exerciseId
- repetitions
- weight
- duration
- distance
- restTime
- rpe
- completed

---

## Skill

Skill de calistenia.

Campos:

- id
- name
- category
- difficulty
- xpRequired
- description

---

## SkillProgress

Progresso individual.

Campos:

- userId
- skillId
- level
- xp
- mastery
- totalTrainingTime

---

## Achievement

Conquistas.

Campos:

- id
- title
- description
- icon
- xpReward

---

## UserAchievement

Relaciona usuário e conquista.

---

## Challenge

Desafios.

Campos:

- title
- objective
- xpReward
- deadline

---

## UserChallenge

Relacionamento entre usuário e desafio.

---

## Progress

Medições corporais.

Campos:

- weight
- bodyFat
- chest
- waist
- hips
- arm
- forearm
- thigh
- calf

---

## NutritionLog

Registro alimentar.

Campos:

- meal
- calories
- protein
- carbs
- fats
- fiber
- water

---

## SleepLog

Registro de sono.

Campos:

- bedtime
- wakeTime
- duration
- quality

---

## Habit

Hábitos.

Campos:

- title
- frequency
- streak
- completed

---

## Notification

Notificações.

---

## Conversation

Conversas da IA.

---

## AIMessage

Histórico do assistente.

---

## Group

Comunidades.

---

## Post

Publicações.

---

## Comment

Comentários.

---

## Like

Curtidas.

---

## Ranking

Pontuações.

---

# 8. Relacionamentos

User

↓

Workouts

↓

Workout Sessions

↓

Exercise Sets

Exercise

↓

Exercise Sets

User

↓

Progress

↓

Measurements

User

↓

Skills

↓

Skill Progress

User

↓

Groups

↓

Posts

↓

Comments

---

# 9. Índices

Criar índices para:

- email
- username
- createdAt
- userId
- workoutId
- exerciseId
- skillId

Todos os índices devem ser analisados durante a implementação para evitar consultas desnecessárias.

---

# 10. Auditoria

Todas as tabelas principais deverão possuir:

- createdAt
- updatedAt

Sempre que necessário:

- deletedAt

O Forge utilizará exclusão lógica (soft delete) para preservar histórico.

---

# 11. Sincronização

Cada registro sincronizável deverá possuir:

- syncStatus
- localId
- serverId
- version
- lastSyncAt
- updatedLocally

Estados possíveis:

- pending
- synced
- conflict
- failed

---

# 12. Versionamento

Toda entidade sincronizada possuirá um campo de versão para auxiliar na resolução de conflitos entre dispositivos.

---

# 13. Escalabilidade

O banco deverá suportar:

- milhões de usuários;
- múltiplos dispositivos por usuário;
- sincronização simultânea;
- expansão para novos módulos sem alterações destrutivas.

---

# 14. Segurança

Os dados sensíveis deverão ser protegidos conforme as boas práticas de segurança.

Nunca armazenar senhas em texto.

Utilizar hash forte para autenticação.

Aplicar o princípio do menor privilégio nas permissões de acesso.

---

# 15. Convenções

Nomes de tabelas:

snake_case

Exemplo:

workout_sessions

Campos:

camelCase no código.

snake_case no banco.

UUID como chave primária.

Relacionamentos explícitos.

Nunca utilizar nomes ambíguos.

---

# 16. Próximos Passos

Após a aprovação deste documento serão elaborados:

- Modelo lógico.
- Modelo físico.
- Diagrama Entidade-Relacionamento (ERD).
- Esquema Prisma.
- Estratégias de migração.
- Estratégias de backup.
