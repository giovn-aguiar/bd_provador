# Banco de Dados "Provador"

## Objetivo

Este banco de dados foi projetado para gerenciar informações sobre empresas, lojas, sensores, provadores e os registros de uso dos provadores.

## Estrutura

O banco de dados é composto pelas seguintes tabelas:

1. **Empresa**: Armazena informações das empresas, como CNPJ, e-mail e senha.
2. **Sensor**: Armazena informações sobre os sensores usados nos provadores, incluindo número de série e status.
3. **Loja**: Armazena informações das lojas, incluindo endereço e o nome da unidade, e está associada a uma empresa.
4. **Provador**: Relaciona os sensores aos provadores em cada loja.
5. **Registro**: Registra os usos dos provadores, com a data/hora e o status de uso.

## Relacionamentos

- **Empresa ↔ Loja**: Cada loja pertence a uma empresa.
- **Loja ↔ Provador**: Cada loja pode ter múltiplos provadores.
- **Provador ↔ Sensor**: Cada provador é associado a um sensor.
- **Provador ↔ Registro**: Cada uso de provador é registrado.

## Restrições

- Chaves primárias e estrangeiras garantem a integridade dos dados.
- Verificação de formato de e-mail na tabela **Empresa**.
- Status dos sensores deve ser "Ativo" ou "Inativo".

Este banco de dados facilita o gerenciamento e controle de provadores em lojas, garantindo dados consistentes e integrados.
