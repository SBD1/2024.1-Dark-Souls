# Dicionário de dados



## Histórico de versões

| Versão |    Data    | Descrição               |     
| :----: | :--------: | ----------------------- |
| `1.0`  | 20/05/2024 | Primeira versão do dicionário de dados |


### Tabela: PC

| Nome | Descrição | Tipo de Dado | Valores permitidos | Chave | Restrições de domínio |
| --- | --- | --- | --- | --- | --- |
| id_personagem | Código identificador único de um jogador | int | 1-5000 | pk | not null |
| Nome | Identifica o tipo de personagem | varchar[30] | a-z, A-Z | | not null |
| Vida | Vida que o personagem possui no momento | int | 1-100 | | not null |
| Resistência | Defesa que um determinado do status,  de 0 até 100 | int | 0 até 100 | | not null |
| Status | Relação se está vivo ou morto |  | de 0 a 1 | | enum |
| Vigor | Status da vida | int | | | not null |
| Destreza | Velocidade de ataque | int | 0 até 100 | | not null |
| Força | Poder de ataque | int | 0 até 100 | | not null |
| Nível |  nível do jogador | int | 0 até 1000 | FK | not null |
| Stamina | Tempo em ação do personagem | int | 0 até 100 | | not null |
| Vitalidade | Vida do personagem | int | 0 até 100 | | not null |
| Classe  | classe do jogador | int |  | FK | not null |



### Tabela: MAGIA

| Nome | Descrição | Tipo de Dado | Valores permitidos | Chave | Restrições de domínio |
| --- | --- | --- | --- | --- | --- |
| id_magia  | Identifica o tipo de magia | int |  | PK | not null |
| Quantidade  | Quantidade da magia disponibilizada no inventário | int | | | not null |
| Tipo  | Identifica o tipo de magia | int |  | | not null |
| Nome  | Identifica o nome da magia | varchar[30] | a-z, A-Z | | not null |
| Descrição  | Identifica o tipo de personagem | varchar[255] | a-z, A-Z | | not null |
| Efeito  | Identifica o que ocorre ao personagem | varchar[30] | a-z, A-Z | | not null |
| Requisitos  | Identifica o tipo de personagem | int | a-z, A-Z | | not null |

### Tabela: FALA

| Nome | Descrição | Tipo de Dado | Valores permitidos | Chave | Restrições de domínio |
| --- | --- | --- | --- | --- | --- |
| id_fala  | Identifica o tipo de fala do personagem | int |  | PK | not null |
| Fala  | o diálogo do personagem | varchar[30] | a-z, A-Z | | not null |


### Tabela: NPCFALA

| Nome | Descrição | Tipo de Dado | Valores permitidos | Chave | Restrições de domínio |
| --- | --- | --- | --- | --- | --- |
| id_fala  | Identifica o tipo de fala do personagem | int |  | PK, FK | not null |
| id_personagem  | Identifica o tipo de personagem | int |  | PK, FK | not null |

### Tabela: INIMIGO

| Nome | Descrição | Tipo de Dado | Valores permitidos | Chave | Restrições de domínio |
| --- | --- | --- | --- | --- | --- |
| id_personagem  | Identifica o tipo de personagem | int |  | PK, FK | not null |
| Nome  | Identifica o nome de personagem | varchar[30] | a-z, A-Z | | not null |
| Vida  | Identifica a vida de personagem | int | 0 a 100 | | not null |
| Defesa  | Identifica a defesa de personagem | int | 0 a 100 | | not null |
| Status  | Identifica o tipo de status do personagem | int |  | | enum |
| Função  | Identifica a função de personagem | int | | | not null |
| Fraqueza  | Identifica o ponto fraco  de personagem | int | | | not null |
| Resistência  | Identifica a resistência de personagem | int | | | not null |
| Ataque  | Identifica o pode de ataque do personagem | int | 0 a 100 | | not null |

### Tabela: BOSS

| Nome | Descrição | Tipo de Dado | Valores permitidos | Chave | Restrições de domínio |
| --- | --- | --- | --- | --- | --- |
| id_personagem  | Identifica o tipo de personagem | int |  | PK, FK | not null |
| Nome  | Identifica o nome de personagem | varchar[30] | a-z, A-Z | | not null |
| Vida  | Identifica a vida de personagem | int | 0 a 100 | | not null |
| Defesa  | Identifica a defesa de personagem | int | 0 a 100 | | not null |
| Status  | Identifica o tipo de status do personagem | int |  | | enum |
| Função  | Identifica a função de personagem | int | | | not null |
| Fraqueza  | Identifica o ponto fraco  de personagem | int | | | not null |
| Resistência  | Identifica a resistência de personagem | int | | | not null |
| Ataque  | Identifica o pode de ataque do personagem | int | 0 a 100 | | not null |

### Tabela: FIRE KEEPER

| Nome | Descrição | Tipo de Dado | Valores permitidos | Chave | Restrições de domínio |
| --- | --- | --- | --- | --- | --- |
| id_personagem  | Identifica o tipo de personagem | varchar[30] | a-z, A-Z | | not null |
| Nome  | Identifica o tipo de personagem | varchar[30] | a-z, A-Z | | not null |
| Vida  | Identifica o tipo de personagem | varchar[30] | a-z, A-Z | | not null |
| Defesa  | Identifica o tipo de personagem | varchar[30] | a-z, A-Z | | not null |
| Status  | Identifica o tipo de personagem | varchar[30] | a-z, A-Z | | not null |
| Função  | Identifica o tipo de personagem | varchar[30] | a-z, A-Z | | not null |
| Fraqueza  | Identifica o tipo de personagem | varchar[30] | a-z, A-Z | | not null |
| Resistência  | Identifica o tipo de personagem | varchar[30] | a-z, A-Z | | not null |

### Tabela: AMIGO

| Nome | Descrição | Tipo de Dado | Valores permitidos | Chave | Restrições de domínio |
| --- | --- | --- | --- | --- | --- |
| id_personagem  | Identifica o tipo de personagem | varchar[30] | a-z, A-Z | | not null |
| Nome  | Identifica o tipo de personagem | varchar[30] | a-z, A-Z | | not null |
| Vida  | Identifica o tipo de personagem | varchar[30] | a-z, A-Z | | not null |
| Defesa  | Identifica o tipo de personagem | varchar[30] | a-z, A-Z | | not null |
| Status  | Identifica o tipo de personagem | varchar[30] | a-z, A-Z | | not null |
| Função  | Identifica o tipo de personagem | varchar[30] | a-z, A-Z | | not null |
| Fraqueza  | Identifica o tipo de personagem | varchar[30] | a-z, A-Z | | not null |
| Resistência  | Identifica o tipo de personagem | varchar[30] | a-z, A-Z | | not null |

### Tabela: ÁREA

| Nome | Descrição | Tipo de Dado | Valores permitidos | Chave | Restrições de domínio |
| --- | --- | --- | --- | --- | --- |
| id_area  | Identifica o tipo de personagem | varchar[30] | a-z, A-Z | | not null |
| Nome  | Identifica o tipo de personagem | varchar[30] | a-z, A-Z | | not null |
| Região  | Identifica o tipo de personagem | varchar[30] | a-z, A-Z | | not null |

### Tabela: REGIÃO

| Nome | Descrição | Tipo de Dado | Valores permitidos | Chave | Restrições de domínio |
| --- | --- | --- | --- | --- | --- |
| id_regiao  | Identifica o tipo de personagem | varchar[30] | a-z, A-Z | | not null |
| Nome  | Identifica o tipo de personagem | varchar[30] | a-z, A-Z | | not null |