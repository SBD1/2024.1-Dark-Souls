# Dicionário de dados



## Histórico de versões

| Versão |    Data    | Descrição               |     
| :----: | :--------: | ----------------------- |
| `1.0`  | 20/05/2024 | Primeira versão do dicionário de dados |


### Tabela: PC

| Nome | Descrição | Tipo de Dado | Valores permitidos | Chave | Restrições de domínio |
| --- | --- | --- | --- | --- | --- |
| id_personagem | Identifica o personagem | int | 1-5000 | PK | not null, unique |
| Nome | Nome do personagem | varchar[30] | a-z, A-Z | | not null |
| Vida | Vida que o personagem possui no momento | int | 1-100 | | not null |
| Resistência | Defesa que um determinado do status,  de 0-100 | int | 0-100 | | not null |
| Status | Relação se está vivo ou morto | enum(Vivo, Morto) | Vivo ou Morto | | not null |
| Vigor | Status da vida | int | 0-100 | | not null |
| Destreza | Velocidade de ataque | int | 0-100 | | not null |
| Força | Poder de ataque | int | 0-100 | | not null |
| Nível |  nível do jogador | int | 0-1000 | FK | not null |
| Stamina | Tempo em ação do personagem | int | 0-100 | | not null |
| Vitalidade | Vida do personagem | int | 0-100 | | not null |



### Tabela: MAGIA

| Nome | Descrição | Tipo de Dado | Valores permitidos | Chave | Restrições de domínio |
| --- | --- | --- | --- | --- | --- |
| id_magia  | Identifica a magia | int | 1-40 | PK | not null, unique |
| Quantidade  | Quantidade da magia disponibilizada no inventário | int | 1-20 | | not null |
| Tipo  | Identifica o tipo de magia | enum(Piromancia, Arcano, Milagre) | Piromancia, Arcano, Milagre | | not null |
| Nome  | Identifica o nome da magia | varchar[30] | a-z, A-Z | | not null |
| Descrição  | Descreve a magia | varchar[255] | a-z, A-Z | | not null |
| Efeito  | Identifica o que ocorre ao personagem | varchar[30] | a-z, A-Z | | not null |
| Requisitos  | Requisitos para usar a magia | int | 1-99 | | not null |

### Tabela: FALA

| Nome | Descrição | Tipo de Dado | Valores permitidos | Chave | Restrições de domínio |
| --- | --- | --- | --- | --- | --- |
| id_fala  | Identifica a fala do personagem | int | 1-9999 | PK | not null |
| Fala  | A fala em si do personagem | varchar[255] | a-z, A-Z | | not null |


### Tabela: NPCFALA

| Nome | Descrição | Tipo de Dado | Valores permitidos | Chave | Restrições de domínio |
| --- | --- | --- | --- | --- | --- |
| id_fala  | Identifica a fala do personagem | int | 1-9999 | PK, FK | not null |
| id_personagem  | Identifica o personagem | int | 1-5000 | PK, FK | not null |

### Tabela: INIMIGO

| Nome | Descrição | Tipo de Dado | Valores permitidos | Chave | Restrições de domínio |
| --- | --- | --- | --- | --- | --- |
| id_personagem  | Identifica o inimigo | int | 1-5000 | PK, FK | not null |
| Nome  | Identifica o nome de inimigo | varchar[30] | a-z, A-Z | | not null |
| Vida  | Identifica a vida de inimigo | int | 0-100 | | not null |
| Defesa  | Identifica a defesa de inimigo | int | 0-100 | | not null |
| Status  | Identifica o status do inimigo | enum(Vivo, Morto) | Vivo, Morto | | not null |
| Função  | Identifica a função de inimigo | enum(Passivo, Ativo) | Passivo, Ativo | | not null |
| Fraqueza  | Identifica o ponto fraco  de inimigo | enum(Elétrico, Fogo, Escuridão) | Elétrico, Fogo, Escuridão | | nullable |
| Resistência  | Identifica a resistência de inimigo | enum(Elétrico, Fogo, Escuridão) | Elétrico, Fogo, Escuridão | | nullable |
| Ataque  | Identifica o poder de ataque do inimigo | int | 0-100 | | not null |

### Tabela: BOSS

| Nome | Descrição | Tipo de Dado | Valores permitidos | Chave | Restrições de domínio |
| --- | --- | --- | --- | --- | --- |
| id_personagem  | Identifica o boss | int | 1-5000 | PK, FK | not null |
| Nome  | Identifica o nome do boss | varchar[30] | a-z, A-Z | | not null |
| Vida  | Identifica a vida do boss | int | 0-100 | | not null |
| Defesa  | Identifica a defesa do boss | int | 0-100 | | not null |
| Status  | Identifica o tipo de status do boss | enum(Vivo, Morto) | Vivo, Morto | | not null |
| Função  | Identifica a função do boss | not(Passivo, Ativo) | Passivo, Ativo | | not null |
| Fraqueza  | Identifica o ponto fraco  do boss | enum(Elétrico, Fogo, Escuridão) | Elétrico, Fogo, Escuridão | | nullable |
| Resistência  | Identifica a resistência do boss | enum(Elétrico, Fogo, Escuridão) | Elétrico, Fogo, Escuridão | | nullable |
| Ataque  | Identifica o pode de ataque do boss | int | 0-100 | | not null |

### Tabela: FIRE KEEPER

| Nome | Descrição | Tipo de Dado | Valores permitidos | Chave | Restrições de domínio |
| --- | --- | --- | --- | --- | --- |
| id_personagem  | Código identificador único de um personagem | int | 1-5000 | PK | not null |
| Nome  | Identifica o fire keeper | int | 1-5000 | | not null |
| Vida  | Vida que o fire keeper possui no momento	 | int | 1-100 | | not null |
| Defesa  | Identifica a defesa do fire keeper	 | int | 0-100 | | not null |
| Status  | Identifica o status do fire keeper | enum(Vivo, Morto) | Vivo, Morto | | not null |
| Função  | Identifica a função do fire keeper	 | enum(upar pc, upar poçao)	 | upar pc, upar poçao | | not null |
| Resistência  | Identifica a resistência do fire keeper	 | int	 | 0-100 | | not null |

### Tabela: AMIGO

| Nome | Descrição | Tipo de Dado | Valores permitidos | Chave | Restrições de domínio |
| --- | --- | --- | --- | --- | --- |
| id_personagem  | Código identificador único de um personagem | int | 1-5000 | PK | not null |
| Nome  | Identifica o amigo |  | 1-5000 | | not null |
| Vida  | Vida que o amigo possui no momento	 | int | 1-100 | | not null |
| Defesa  | Identifica a defesa do amigo	 | int | 0-100 | | not null |
| Status  | Identifica o tipo de status do amigo | int |  | | enum |
| Função  | Identifica a função do amigo	 | int	 |  | | not null |
| Fraqueza  | Identifica o ponto fraco do amigo | int	 |  | | not null |
| Resistência  | Identifica a resistência do amigo	 | int	 | 0-100 | | not null |

### Tabela: ÁREA

| Nome | Descrição | Tipo de Dado | Valores permitidos | Chave | Restrições de domínio |
| --- | --- | --- | --- | --- | --- |
| id_area  | Identifica o tipo de área  | int | 1-100 | pk | not null |
| Nome  | Identifica o nome da área | varchar[50] | a-z, A-Z | | not null |
| Região  | Lugar no Mapa | int | 1-30 | fk | not null |

### Tabela: REGIÃO

| Nome | Descrição | Tipo de Dado | Valores permitidos | Chave | Restrições de domínio |
| --- | --- | --- | --- | --- | --- |
| id_regiao  | Identifica a região | int | 1-30 | pk | not null |
| Nome  | Identifica o nome da região | varchar[50] | a-z, A-Z | | not null |

### Tabela: Inventario 

| Nome | Descrição | Tipo de Dado | Valores permitidos | Chave | Restrições de domínio |
| --- | --- | --- | --- | --- | --- |
| id_player | Identificador do jogador | int | 1-5000 | pk/fk | not null |
| Slot_ID | Espaço de armazenar item | int | 1-500 | | not null |
| Item | Identificador da instancia | int | 1-5000 | | not null |

### Instância_de_Item

| Nome | Descrição | Tipo de Dado | Valores permitidos | Chave | Restrições de domínio |
| --- | --- | --- | --- | --- | --- |
| id_instancia | Código identificador a instancia de um item | int | 1-5000 | pk | not null |
| id_item | Identifica o item | int | 1-5000 | | not null |
| id_area | identifica a area | int | 1-100 | | not null |


### Tabela: Armadura

| Nome | Descrição | Tipo de Dado | Valores permitidos | Chave | Restrições de domínio |
| --- | --- | --- | --- | --- | --- |
| id_item | Identifica o item | int | 1-5000 | pk | not null |
| Valor | Indentifica o preço do item | int | 1-99999 | | not null |
| Peso | Indentifica o peso do item | int | 0-100 | | not null |
| Nome | Nome do item| varchar[30] |  a-z, A-Z | | not null |
| Descrição | Descrição do item | varchar[255] | a-z, A-Z | | Not null |
| Requisitos | Requisitos de habilidades para usar um item | int |0-99 | | not null |
| Nível |  nível do equipamento | int | 0-10 |  | not null |
| Durabilidade | condição do equipamento | int | 0-100 | | not null |
| Resistencia | Redução de dano | int | 0-100 | | not null |


### Tabela: Arma

| Nome | Descrição | Tipo de Dado | Valores permitidos | Chave | Restrições de domínio |
| --- | --- | --- | --- | --- | --- |
| id_item | Identifica o item | int | 1-5000 | pk | not null |
| Valor | Indentifica o preço do item | int | 1-99999 | | not null |
| Peso | Indentifica o peso do item | int | 0-100 | | not null |
| Nome | Nome do item| varchar[30] |  a-z, A-Z | | not null |
| Descrição | Descrição do item | varchar[255] | a-z, A-Z | | Not null |
| Requisitos | Requisitos de habilidades para usar um item | int |0-99 | | not null |
| Nível |  nível do equipamento | int | 0-10 |  | not null |
| Durabilidade | condição do equipamento | int | 0-100 | | not null |
| Dano | Dano causado pela arma | int | 1-9999 | | not null |


### Tabela: Poção

| Nome | Descrição | Tipo de Dado | Valores permitidos | Chave | Restrições de domínio |
| --- | --- | --- | --- | --- | --- |
| id_item | Identifica o item | int | 1-5000 | pk | not null |
| Valor | Indentifica o preço do item | int | 1-99999 | | not null |
| Peso | Indentifica o peso do item | int | 0-100 | | not null |
| Nome | Nome do item| varchar[30] |  a-z, A-Z | | not null |
| Descrição | Descrição do item | varchar[255] | a-z, A-Z | | Not null |
| Requisitos | Requisitos de habilidades para usar um item | int |0-99 | | not null |
| Destreza | Velocidade de ataque | int | 0-100 | | not null |
| Nível |  nível do equipamento | int | 0-10 |  | not null |
| Efeito |  Efeito da poção no jogador | varchar[30] | a-z, A-Z |  | not null |
| Quantidade |  Quantidade de poção no inventario | int | 0-30 |  | not null |


### Tabela: Impulso

| Nome | Descrição | Tipo de Dado | Valores permitidos | Chave | Restrições de domínio |
| --- | --- | --- | --- | --- | --- |
| id_item | Identifica o item | int | 1-5000 | pk | not null |
| Valor | Indentifica o preço do item | int | 1-99999 | | not null |
| Peso | Indentifica o peso do item | int | 0-100 | | not null |
| Nome | Nome do item| varchar[30] |  a-z, A-Z | | not null |
| Descrição | Descrição do item | varchar[255] | a-z, A-Z | | Not null |
| Requisitos | Requisitos de habilidades para usar um item | int |0-99 | | not null |
| Destreza | Velocidade de ataque | int | 0-100 | | not null |
| Nível |  nível do equipamento | int | 0-10 |  | not null |
| Efeito |  Efeito da poção no jogador | varchar[30] | a-z, A-Z |  | not null |
| Quantidade |  Quantidade de poção no inventario | int | 0-30 |  | not null |
| Tipo |  Tipo de efeito no jogador | varchar[30] |  a-z, A-Z |  | not null |



