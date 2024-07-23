# Dicionário de dados



## Histórico de versões

| Versão |    Data    | Descrição               |     
| :----: | :--------: | ----------------------- |
| `1.0`  | 20/05/2024 | Primeira versão do dicionário de dados |


### Tabela: PC

| Nome | Descrição | Tipo de Dado | Valores permitidos | Chave | Restrições de domínio |
| --- | --- | --- | --- | --- | --- |
| id_personagem | Código identificador único de um jogador | int | 1-5000 | pk | not null |
| Nome | Identifica o tipo de personagem | vachar[30] | a-z, A-Z | | not null |
| Vida | Vida que o personagem possui no momento | int | 1-100 | | not null |
| Resistência | Defesa que um determinado do status,  de 0 até 100 | int | 0 até 100 | | not null |
| Status | Relação se está vivo ou morto |  | de 0 a 1 | | enum |
| Vigor | Status da vida | int | | | not null |
| Destreza | Identifica o tipo de personagem | vachar[30] | a-z, A-Z | | not null |
| Força | Identifica o tipo de personagem | vachar[30] | a-z, A-Z | | not null |
| Nível | Identifica o tipo de personagem | vachar[30] | a-z, A-Z | | not null |
| Stamina | Identifica o tipo de personagem | vachar[30] | a-z, A-Z | | not null |
| Vitalidade | Identifica o tipo de personagem | vachar[30] | a-z, A-Z | | not null |
| Classe  | Identifica o tipo de personagem | vachar[30] | a-z, A-Z | | not null |



### Tabela: MAGIA

| Nome | Descrição | Tipo de Dado | Valores permitidos | Chave | Restrições de domínio |
| --- | --- | --- | --- | --- | --- |
| id_magia  | Identifica o tipo de personagem | vachar[30] | a-z, A-Z | | not null |
| Quantidade  | Identifica o tipo de personagem | vachar[30] | a-z, A-Z | | not null |
| Tipo  | Identifica o tipo de personagem | vachar[30] | a-z, A-Z | | not null |
| Nome  | Identifica o tipo de personagem | vachar[30] | a-z, A-Z | | not null |
| Descrição  | Identifica o tipo de personagem | vachar[30] | a-z, A-Z | | not null |
| Efeito  | Identifica o tipo de personagem | vachar[30] | a-z, A-Z | | not null |
| Requisitos  | Identifica o tipo de personagem | vachar[30] | a-z, A-Z | | not null |

### Tabela: FALA

| Nome | Descrição | Tipo de Dado | Valores permitidos | Chave | Restrições de domínio |
| --- | --- | --- | --- | --- | --- |
| id_fala  | Identifica o tipo de personagem | vachar[30] | a-z, A-Z | | not null |
| Fala  | Identifica o tipo de personagem | vachar[30] | a-z, A-Z | | not null |


### Tabela: NPCFALA

| Nome | Descrição | Tipo de Dado | Valores permitidos | Chave | Restrições de domínio |
| --- | --- | --- | --- | --- | --- |
| id_fala  | Identifica o tipo de personagem | vachar[30] | a-z, A-Z | | not null |
| id_personagem  | Identifica o tipo de personagem | vachar[30] | a-z, A-Z | | not null |

### Tabela: INIMIGO

| Nome | Descrição | Tipo de Dado | Valores permitidos | Chave | Restrições de domínio |
| --- | --- | --- | --- | --- | --- |
| id_personagem  | Identifica o tipo de personagem | vachar[30] | a-z, A-Z | | not null |
| Nome  | Identifica o tipo de personagem | vachar[30] | a-z, A-Z | | not null |
| Vida  | Identifica o tipo de personagem | vachar[30] | a-z, A-Z | | not null |
| Defesa  | Identifica o tipo de personagem | vachar[30] | a-z, A-Z | | not null |
| Status  | Identifica o tipo de personagem | vachar[30] | a-z, A-Z | | not null |
| Função  | Identifica o tipo de personagem | vachar[30] | a-z, A-Z | | not null |
| Fraqueza  | Identifica o tipo de personagem | vachar[30] | a-z, A-Z | | not null |
| Resistência  | Identifica o tipo de personagem | vachar[30] | a-z, A-Z | | not null |
| Ataque  | Identifica o tipo de personagem | vachar[30] | a-z, A-Z | | not null |

### Tabela: BOSS

| Nome | Descrição | Tipo de Dado | Valores permitidos | Chave | Restrições de domínio |
| --- | --- | --- | --- | --- | --- |
| id_personagem  | Identifica o tipo de personagem | vachar[30] | a-z, A-Z | | not null |
| Nome  | Identifica o tipo de personagem | vachar[30] | a-z, A-Z | | not null |
| Vida  | Identifica o tipo de personagem | vachar[30] | a-z, A-Z | | not null |
| Defesa  | Identifica o tipo de personagem | vachar[30] | a-z, A-Z | | not null |
| Status  | Identifica o tipo de personagem | vachar[30] | a-z, A-Z | | not null |
| Função  | Identifica o tipo de personagem | vachar[30] | a-z, A-Z | | not null |
| Fraqueza  | Identifica o tipo de personagem | vachar[30] | a-z, A-Z | | not null |
| Resistência  | Identifica o tipo de personagem | vachar[30] | a-z, A-Z | | not null |
| Ataque  | Identifica o tipo de personagem | vachar[30] | a-z, A-Z | | not null |

### Tabela: FIRE KEEPER

| Nome | Descrição | Tipo de Dado | Valores permitidos | Chave | Restrições de domínio |
| --- | --- | --- | --- | --- | --- |
| id_personagem  | Identifica o tipo de personagem | vachar[30] | a-z, A-Z | | not null |
| Nome  | Identifica o tipo de personagem | vachar[30] | a-z, A-Z | | not null |
| Vida  | Identifica o tipo de personagem | vachar[30] | a-z, A-Z | | not null |
| Defesa  | Identifica o tipo de personagem | vachar[30] | a-z, A-Z | | not null |
| Status  | Identifica o tipo de personagem | vachar[30] | a-z, A-Z | | not null |
| Função  | Identifica o tipo de personagem | vachar[30] | a-z, A-Z | | not null |
| Fraqueza  | Identifica o tipo de personagem | vachar[30] | a-z, A-Z | | not null |
| Resistência  | Identifica o tipo de personagem | vachar[30] | a-z, A-Z | | not null |

### Tabela: AMIGO

| Nome | Descrição | Tipo de Dado | Valores permitidos | Chave | Restrições de domínio |
| --- | --- | --- | --- | --- | --- |
| id_personagem  | Identifica o tipo de personagem | vachar[30] | a-z, A-Z | | not null |
| Nome  | Identifica o tipo de personagem | vachar[30] | a-z, A-Z | | not null |
| Vida  | Identifica o tipo de personagem | vachar[30] | a-z, A-Z | | not null |
| Defesa  | Identifica o tipo de personagem | vachar[30] | a-z, A-Z | | not null |
| Status  | Identifica o tipo de personagem | vachar[30] | a-z, A-Z | | not null |
| Função  | Identifica o tipo de personagem | vachar[30] | a-z, A-Z | | not null |
| Fraqueza  | Identifica o tipo de personagem | vachar[30] | a-z, A-Z | | not null |
| Resistência  | Identifica o tipo de personagem | vachar[30] | a-z, A-Z | | not null |

### Tabela: ÁREA

| Nome | Descrição | Tipo de Dado | Valores permitidos | Chave | Restrições de domínio |
| --- | --- | --- | --- | --- | --- |
| id_area  | Identifica o tipo de personagem | vachar[30] | a-z, A-Z | | not null |
| Nome  | Identifica o tipo de personagem | vachar[30] | a-z, A-Z | | not null |
| Região  | Identifica o tipo de personagem | vachar[30] | a-z, A-Z | | not null |

### Tabela: REGIÃO

| Nome | Descrição | Tipo de Dado | Valores permitidos | Chave | Restrições de domínio |
| --- | --- | --- | --- | --- | --- |
| id_regiao  | Identifica o tipo de personagem | vachar[30] | a-z, A-Z | | not null |
| Nome  | Identifica o tipo de personagem | vachar[30] | a-z, A-Z | | not null |