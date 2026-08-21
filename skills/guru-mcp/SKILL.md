---
name: guru-mcp
description: Skill da REST API do Digital Manager Guru na MCP.AI: 95 endpoints em /api/guru. Plataforma de checkout e gestão de vendas de infoprodutos Digital Manager Guru via API oficial: vendas/transações, assinaturas, produtos e ofertas, contatos, afiliações, cupons, ingressos (e-tickets) e webhooks. Gere seu User Token no painel em Meu Perfil → Tokens API. Autentique com workspace API key (sk_live) gerada em app.mcp.ai/settings/api-keys. Use quando o usuário pedir algo coberto pelos endpoints.
---

# Digital Manager Guru — REST API skill

Você tem acesso à **Digital Manager Guru** REST API na MCP.AI.

> Plataforma de checkout e gestão de vendas de infoprodutos Digital Manager Guru via API oficial: vendas/transações, assinaturas, produtos e ofertas, contatos, afiliações, cupons, ingressos (e-tickets) e webhooks. Gere seu User Token no painel em Meu Perfil → Tokens API.

## Base URL

```
https://api.mcp.ai/api/guru
```

Todo endpoint é um **POST** na Base URL + o path abaixo. Os parâmetros vão no corpo JSON.

## Autenticação

Inclua em toda request:

```
Authorization: Bearer sk_live_...
Content-Type: application/json
```

> Gere sua chave em **https://app.mcp.ai/settings/api-keys** (workspace API key `sk_live_…`, não expira, revogável). Uma única chave serve pra todos os seus MCPs.

## Formato de resposta

```json
{ "ok": true, "tool": "<tool_id>", "result": <payload> }
```

## Exemplo cURL

```bash
curl -X POST https://api.mcp.ai/api/guru/account \
  -H "Authorization: Bearer sk_live_..." \
  -H "Content-Type: application/json" \
  -d '{"account_token":"..."}'
```

## Reportar problemas

Se um endpoint retornar erro, vazio ou dado inesperado, reporte (não desista calado): **POST /api/guru/report** com `{ "message": "...", "context"?: "...", "conversation"?: [...] }`. Isso notifica o time da MCP.AI.

## Endpoints (95)

#### `guru_account`

Valida um Account Token do Guru (usado pra verificar origem de webhook). _(POST /api/guru/account)_

| Parâmetro | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `account_token` | string | Sim | Account Token a validar |
| `account` | string | Não | Opcional quando há várias contas Guru vinculadas a este install (id, label ou parcial). Use guru_list_accounts pra ver as opções; omita se só houver uma. |

#### `guru_affiliations_assets`

Afiliações no Guru (leitura). Ações: list (cursor); get (id); assets (id); transactions (id). _(POST /api/guru/affiliations/assets)_

| Parâmetro | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `id` | string | Não |  |
| `cursor` | string | Não | Cursor de paginação (próxima página) |
| `account` | string | Não | Opcional quando há várias contas Guru vinculadas a este install (id, label ou parcial). Use guru_list_accounts pra ver as opções; omita se só houver uma. |
| `ids` | string[] | Não | Bulk mode: multiple values for id |

#### `guru_affiliations_get`

Afiliações no Guru (leitura). Ações: list (cursor); get (id); assets (id); transactions (id). _(POST /api/guru/affiliations/get)_

| Parâmetro | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `id` | string | Não |  |
| `cursor` | string | Não | Cursor de paginação (próxima página) |
| `account` | string | Não | Opcional quando há várias contas Guru vinculadas a este install (id, label ou parcial). Use guru_list_accounts pra ver as opções; omita se só houver uma. |
| `ids` | string[] | Não | Bulk mode: multiple values for id |

#### `guru_affiliations_list`

Afiliações no Guru (leitura). Ações: list (cursor); get (id); assets (id); transactions (id). _(POST /api/guru/affiliations/list)_

| Parâmetro | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `id` | string | Não |  |
| `cursor` | string | Não | Cursor de paginação (próxima página) |
| `account` | string | Não | Opcional quando há várias contas Guru vinculadas a este install (id, label ou parcial). Use guru_list_accounts pra ver as opções; omita se só houver uma. |
| `ids` | string[] | Não | Bulk mode: multiple values for id |

#### `guru_affiliations_transactions`

Afiliações no Guru (leitura). Ações: list (cursor); get (id); assets (id); transactions (id). _(POST /api/guru/affiliations/transactions)_

| Parâmetro | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `id` | string | Não |  |
| `cursor` | string | Não | Cursor de paginação (próxima página) |
| `account` | string | Não | Opcional quando há várias contas Guru vinculadas a este install (id, label ou parcial). Use guru_list_accounts pra ver as opções; omita se só houver uma. |
| `ids` | string[] | Não | Bulk mode: multiple values for id |

#### `guru_affiliations_write_set_commission`

Mutações em afiliações Guru. Ação: set_commission (id + data com a comissão). _(POST /api/guru/affiliations/write/set/commission)_

| Parâmetro | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `id` | string | Sim |  |
| `data` | object | Não | Corpo da requisição (campos conforme a doc oficial Guru do recurso/ação) |
| `account` | string | Não | Opcional quando há várias contas Guru vinculadas a este install (id, label ou parcial). Use guru_list_accounts pra ver as opções; omita se só houver uma. |
| `ids` | string[] | Não | Bulk mode: multiple values for id |

#### `guru_blocklists_get`

Listas de bloqueio (anti-fraude) no Guru. _(POST /api/guru/blocklists/get)_

| Parâmetro | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `id` | string | Não |  |
| `cursor` | string | Não | Cursor de paginação (próxima página) |
| `account` | string | Não | Opcional quando há várias contas Guru vinculadas a este install (id, label ou parcial). Use guru_list_accounts pra ver as opções; omita se só houver uma. |
| `ids` | string[] | Não | Bulk mode: multiple values for id |

#### `guru_blocklists_list`

Listas de bloqueio (anti-fraude) no Guru. _(POST /api/guru/blocklists/list)_

| Parâmetro | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `id` | string | Não |  |
| `cursor` | string | Não | Cursor de paginação (próxima página) |
| `account` | string | Não | Opcional quando há várias contas Guru vinculadas a este install (id, label ou parcial). Use guru_list_accounts pra ver as opções; omita se só houver uma. |
| `ids` | string[] | Não | Bulk mode: multiple values for id |

#### `guru_blocklists_write_create`

Mutações em listas de bloqueio Guru. _(POST /api/guru/blocklists/write/create)_

| Parâmetro | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `id` | string | Não |  |
| `data` | object | Não | Corpo da requisição (campos conforme a doc oficial Guru do recurso/ação) |
| `account` | string | Não | Opcional quando há várias contas Guru vinculadas a este install (id, label ou parcial). Use guru_list_accounts pra ver as opções; omita se só houver uma. |
| `ids` | string[] | Não | Bulk mode: multiple values for id |

#### `guru_blocklists_write_delete`

Mutações em listas de bloqueio Guru. _(POST /api/guru/blocklists/write/delete)_

| Parâmetro | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `id` | string | Não |  |
| `data` | object | Não | Corpo da requisição (campos conforme a doc oficial Guru do recurso/ação) |
| `account` | string | Não | Opcional quando há várias contas Guru vinculadas a este install (id, label ou parcial). Use guru_list_accounts pra ver as opções; omita se só houver uma. |
| `ids` | string[] | Não | Bulk mode: multiple values for id |

#### `guru_blocklists_write_update`

Mutações em listas de bloqueio Guru. _(POST /api/guru/blocklists/write/update)_

| Parâmetro | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `id` | string | Não |  |
| `data` | object | Não | Corpo da requisição (campos conforme a doc oficial Guru do recurso/ação) |
| `account` | string | Não | Opcional quando há várias contas Guru vinculadas a este install (id, label ou parcial). Use guru_list_accounts pra ver as opções; omita se só houver uma. |
| `ids` | string[] | Não | Bulk mode: multiple values for id |

#### `guru_checkout`

Consulta/configura settings de oferta no checkout do Guru (POST checkout/offers/settings). _(POST /api/guru/checkout)_

| Parâmetro | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `data` | object | Não | Corpo da requisição (campos conforme a doc oficial Guru do recurso/ação) |
| `account` | string | Não | Opcional quando há várias contas Guru vinculadas a este install (id, label ou parcial). Use guru_list_accounts pra ver as opções; omita se só houver uma. |

#### `guru_contacts_affiliations`

Contatos/clientes no Guru (leitura). _(POST /api/guru/contacts/affiliations)_

| Parâmetro | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `id` | string | Não |  |
| `email` | string | Não |  |
| `doc` | string | Não |  |
| `name` | string | Não |  |
| `created_at_ini` | string | Não |  |
| `created_at_end` | string | Não |  |
| `cursor` | string | Não | Cursor de paginação (próxima página) |
| `account` | string | Não | Opcional quando há várias contas Guru vinculadas a este install (id, label ou parcial). Use guru_list_accounts pra ver as opções; omita se só houver uma. |
| `ids` | string[] | Não | Bulk mode: multiple values for id |

#### `guru_contacts_etickets`

Contatos/clientes no Guru (leitura). _(POST /api/guru/contacts/etickets)_

| Parâmetro | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `id` | string | Não |  |
| `email` | string | Não |  |
| `doc` | string | Não |  |
| `name` | string | Não |  |
| `created_at_ini` | string | Não |  |
| `created_at_end` | string | Não |  |
| `cursor` | string | Não | Cursor de paginação (próxima página) |
| `account` | string | Não | Opcional quando há várias contas Guru vinculadas a este install (id, label ou parcial). Use guru_list_accounts pra ver as opções; omita se só houver uma. |
| `ids` | string[] | Não | Bulk mode: multiple values for id |

#### `guru_contacts_get`

Contatos/clientes no Guru (leitura). _(POST /api/guru/contacts/get)_

| Parâmetro | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `id` | string | Não |  |
| `email` | string | Não |  |
| `doc` | string | Não |  |
| `name` | string | Não |  |
| `created_at_ini` | string | Não |  |
| `created_at_end` | string | Não |  |
| `cursor` | string | Não | Cursor de paginação (próxima página) |
| `account` | string | Não | Opcional quando há várias contas Guru vinculadas a este install (id, label ou parcial). Use guru_list_accounts pra ver as opções; omita se só houver uma. |
| `ids` | string[] | Não | Bulk mode: multiple values for id |

#### `guru_contacts_search`

Contatos/clientes no Guru (leitura). _(POST /api/guru/contacts/search)_

| Parâmetro | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `id` | string | Não |  |
| `email` | string | Não |  |
| `doc` | string | Não |  |
| `name` | string | Não |  |
| `created_at_ini` | string | Não |  |
| `created_at_end` | string | Não |  |
| `cursor` | string | Não | Cursor de paginação (próxima página) |
| `account` | string | Não | Opcional quando há várias contas Guru vinculadas a este install (id, label ou parcial). Use guru_list_accounts pra ver as opções; omita se só houver uma. |
| `ids` | string[] | Não | Bulk mode: multiple values for id |

#### `guru_contacts_subscriptions`

Contatos/clientes no Guru (leitura). _(POST /api/guru/contacts/subscriptions)_

| Parâmetro | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `id` | string | Não |  |
| `email` | string | Não |  |
| `doc` | string | Não |  |
| `name` | string | Não |  |
| `created_at_ini` | string | Não |  |
| `created_at_end` | string | Não |  |
| `cursor` | string | Não | Cursor de paginação (próxima página) |
| `account` | string | Não | Opcional quando há várias contas Guru vinculadas a este install (id, label ou parcial). Use guru_list_accounts pra ver as opções; omita se só houver uma. |
| `ids` | string[] | Não | Bulk mode: multiple values for id |

#### `guru_contacts_transactions`

Contatos/clientes no Guru (leitura). _(POST /api/guru/contacts/transactions)_

| Parâmetro | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `id` | string | Não |  |
| `email` | string | Não |  |
| `doc` | string | Não |  |
| `name` | string | Não |  |
| `created_at_ini` | string | Não |  |
| `created_at_end` | string | Não |  |
| `cursor` | string | Não | Cursor de paginação (próxima página) |
| `account` | string | Não | Opcional quando há várias contas Guru vinculadas a este install (id, label ou parcial). Use guru_list_accounts pra ver as opções; omita se só houver uma. |
| `ids` | string[] | Não | Bulk mode: multiple values for id |

#### `guru_contacts_write_anonymize`

Mutações em contatos Guru. _(POST /api/guru/contacts/write/anonymize)_

| Parâmetro | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `id` | string | Não |  |
| `data` | object | Não | Corpo da requisição (campos conforme a doc oficial Guru do recurso/ação) |
| `account` | string | Não | Opcional quando há várias contas Guru vinculadas a este install (id, label ou parcial). Use guru_list_accounts pra ver as opções; omita se só houver uma. |
| `ids` | string[] | Não | Bulk mode: multiple values for id |

#### `guru_contacts_write_create`

Mutações em contatos Guru. _(POST /api/guru/contacts/write/create)_

| Parâmetro | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `id` | string | Não |  |
| `data` | object | Não | Corpo da requisição (campos conforme a doc oficial Guru do recurso/ação) |
| `account` | string | Não | Opcional quando há várias contas Guru vinculadas a este install (id, label ou parcial). Use guru_list_accounts pra ver as opções; omita se só houver uma. |
| `ids` | string[] | Não | Bulk mode: multiple values for id |

#### `guru_contacts_write_create_etickets`

Mutações em contatos Guru. _(POST /api/guru/contacts/write/create/etickets)_

| Parâmetro | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `id` | string | Não |  |
| `data` | object | Não | Corpo da requisição (campos conforme a doc oficial Guru do recurso/ação) |
| `account` | string | Não | Opcional quando há várias contas Guru vinculadas a este install (id, label ou parcial). Use guru_list_accounts pra ver as opções; omita se só houver uma. |
| `ids` | string[] | Não | Bulk mode: multiple values for id |

#### `guru_contacts_write_update`

Mutações em contatos Guru. _(POST /api/guru/contacts/write/update)_

| Parâmetro | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `id` | string | Não |  |
| `data` | object | Não | Corpo da requisição (campos conforme a doc oficial Guru do recurso/ação) |
| `account` | string | Não | Opcional quando há várias contas Guru vinculadas a este install (id, label ou parcial). Use guru_list_accounts pra ver as opções; omita se só houver uma. |
| `ids` | string[] | Não | Bulk mode: multiple values for id |

#### `guru_countries_address`

Dados auxiliares de localização do Guru. _(POST /api/guru/countries/address)_

| Parâmetro | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `country` | string | Não | states: código do país (ex.: BR) |
| `zipcode` | string | Não | address: CEP (Brasil) |
| `account` | string | Não | Opcional quando há várias contas Guru vinculadas a este install (id, label ou parcial). Use guru_list_accounts pra ver as opções; omita se só houver uma. |

#### `guru_countries_list`

Dados auxiliares de localização do Guru. _(POST /api/guru/countries/list)_

| Parâmetro | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `country` | string | Não | states: código do país (ex.: BR) |
| `zipcode` | string | Não | address: CEP (Brasil) |
| `account` | string | Não | Opcional quando há várias contas Guru vinculadas a este install (id, label ou parcial). Use guru_list_accounts pra ver as opções; omita se só houver uma. |

#### `guru_countries_states`

Dados auxiliares de localização do Guru. _(POST /api/guru/countries/states)_

| Parâmetro | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `country` | string | Não | states: código do país (ex.: BR) |
| `zipcode` | string | Não | address: CEP (Brasil) |
| `account` | string | Não | Opcional quando há várias contas Guru vinculadas a este install (id, label ou parcial). Use guru_list_accounts pra ver as opções; omita se só houver uma. |

#### `guru_coupons_audits`

Cupons no Guru (leitura). Ações: list (cursor); get (id); audits (id); transactions (id). _(POST /api/guru/coupons/audits)_

| Parâmetro | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `id` | string | Não |  |
| `cursor` | string | Não | Cursor de paginação (próxima página) |
| `account` | string | Não | Opcional quando há várias contas Guru vinculadas a este install (id, label ou parcial). Use guru_list_accounts pra ver as opções; omita se só houver uma. |
| `ids` | string[] | Não | Bulk mode: multiple values for id |

#### `guru_coupons_get`

Cupons no Guru (leitura). Ações: list (cursor); get (id); audits (id); transactions (id). _(POST /api/guru/coupons/get)_

| Parâmetro | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `id` | string | Não |  |
| `cursor` | string | Não | Cursor de paginação (próxima página) |
| `account` | string | Não | Opcional quando há várias contas Guru vinculadas a este install (id, label ou parcial). Use guru_list_accounts pra ver as opções; omita se só houver uma. |
| `ids` | string[] | Não | Bulk mode: multiple values for id |

#### `guru_coupons_list`

Cupons no Guru (leitura). Ações: list (cursor); get (id); audits (id); transactions (id). _(POST /api/guru/coupons/list)_

| Parâmetro | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `id` | string | Não |  |
| `cursor` | string | Não | Cursor de paginação (próxima página) |
| `account` | string | Não | Opcional quando há várias contas Guru vinculadas a este install (id, label ou parcial). Use guru_list_accounts pra ver as opções; omita se só houver uma. |
| `ids` | string[] | Não | Bulk mode: multiple values for id |

#### `guru_coupons_transactions`

Cupons no Guru (leitura). Ações: list (cursor); get (id); audits (id); transactions (id). _(POST /api/guru/coupons/transactions)_

| Parâmetro | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `id` | string | Não |  |
| `cursor` | string | Não | Cursor de paginação (próxima página) |
| `account` | string | Não | Opcional quando há várias contas Guru vinculadas a este install (id, label ou parcial). Use guru_list_accounts pra ver as opções; omita se só houver uma. |
| `ids` | string[] | Não | Bulk mode: multiple values for id |

#### `guru_coupons_write_create`

Mutações em cupons Guru. _(POST /api/guru/coupons/write/create)_

| Parâmetro | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `id` | string | Não |  |
| `data` | object | Não | Corpo da requisição (campos conforme a doc oficial Guru do recurso/ação) |
| `account` | string | Não | Opcional quando há várias contas Guru vinculadas a este install (id, label ou parcial). Use guru_list_accounts pra ver as opções; omita se só houver uma. |
| `ids` | string[] | Não | Bulk mode: multiple values for id |

#### `guru_coupons_write_delete`

Mutações em cupons Guru. _(POST /api/guru/coupons/write/delete)_

| Parâmetro | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `id` | string | Não |  |
| `data` | object | Não | Corpo da requisição (campos conforme a doc oficial Guru do recurso/ação) |
| `account` | string | Não | Opcional quando há várias contas Guru vinculadas a este install (id, label ou parcial). Use guru_list_accounts pra ver as opções; omita se só houver uma. |
| `ids` | string[] | Não | Bulk mode: multiple values for id |

#### `guru_coupons_write_duplicate`

Mutações em cupons Guru. _(POST /api/guru/coupons/write/duplicate)_

| Parâmetro | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `id` | string | Não |  |
| `data` | object | Não | Corpo da requisição (campos conforme a doc oficial Guru do recurso/ação) |
| `account` | string | Não | Opcional quando há várias contas Guru vinculadas a este install (id, label ou parcial). Use guru_list_accounts pra ver as opções; omita se só houver uma. |
| `ids` | string[] | Não | Bulk mode: multiple values for id |

#### `guru_coupons_write_set_activation`

Mutações em cupons Guru. _(POST /api/guru/coupons/write/set/activation)_

| Parâmetro | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `id` | string | Não |  |
| `data` | object | Não | Corpo da requisição (campos conforme a doc oficial Guru do recurso/ação) |
| `account` | string | Não | Opcional quando há várias contas Guru vinculadas a este install (id, label ou parcial). Use guru_list_accounts pra ver as opções; omita se só houver uma. |
| `ids` | string[] | Não | Bulk mode: multiple values for id |

#### `guru_coupons_write_update`

Mutações em cupons Guru. _(POST /api/guru/coupons/write/update)_

| Parâmetro | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `id` | string | Não |  |
| `data` | object | Não | Corpo da requisição (campos conforme a doc oficial Guru do recurso/ação) |
| `account` | string | Não | Opcional quando há várias contas Guru vinculadas a este install (id, label ou parcial). Use guru_list_accounts pra ver as opções; omita se só houver uma. |
| `ids` | string[] | Não | Bulk mode: multiple values for id |

#### `guru_etickets_check_in`

Ingressos (e-tickets) no Guru (leitura). _(POST /api/guru/etickets/check/in)_

| Parâmetro | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `code` | string | Não |  |
| `cursor` | string | Não | Cursor de paginação (próxima página) |
| `account` | string | Não | Opcional quando há várias contas Guru vinculadas a este install (id, label ou parcial). Use guru_list_accounts pra ver as opções; omita se só houver uma. |

#### `guru_etickets_get`

Ingressos (e-tickets) no Guru (leitura). _(POST /api/guru/etickets/get)_

| Parâmetro | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `code` | string | Não |  |
| `cursor` | string | Não | Cursor de paginação (próxima página) |
| `account` | string | Não | Opcional quando há várias contas Guru vinculadas a este install (id, label ou parcial). Use guru_list_accounts pra ver as opções; omita se só houver uma. |

#### `guru_etickets_list`

Ingressos (e-tickets) no Guru (leitura). _(POST /api/guru/etickets/list)_

| Parâmetro | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `code` | string | Não |  |
| `cursor` | string | Não | Cursor de paginação (próxima página) |
| `account` | string | Não | Opcional quando há várias contas Guru vinculadas a este install (id, label ou parcial). Use guru_list_accounts pra ver as opções; omita se só houver uma. |

#### `guru_etickets_write_create_invitations`

Mutações em e-tickets Guru. _(POST /api/guru/etickets/write/create/invitations)_

| Parâmetro | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `code` | string | Sim |  |
| `data` | object | Não | Corpo da requisição (campos conforme a doc oficial Guru do recurso/ação) |
| `account` | string | Não | Opcional quando há várias contas Guru vinculadas a este install (id, label ou parcial). Use guru_list_accounts pra ver as opções; omita se só houver uma. |

#### `guru_etickets_write_delete`

Mutações em e-tickets Guru. _(POST /api/guru/etickets/write/delete)_

| Parâmetro | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `code` | string | Sim |  |
| `data` | object | Não | Corpo da requisição (campos conforme a doc oficial Guru do recurso/ação) |
| `account` | string | Não | Opcional quando há várias contas Guru vinculadas a este install (id, label ou parcial). Use guru_list_accounts pra ver as opções; omita se só houver uma. |

#### `guru_etickets_write_delete_check_in`

Mutações em e-tickets Guru. _(POST /api/guru/etickets/write/delete/check/in)_

| Parâmetro | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `code` | string | Sim |  |
| `data` | object | Não | Corpo da requisição (campos conforme a doc oficial Guru do recurso/ação) |
| `account` | string | Não | Opcional quando há várias contas Guru vinculadas a este install (id, label ou parcial). Use guru_list_accounts pra ver as opções; omita se só houver uma. |

#### `guru_etickets_write_delete_invitations`

Mutações em e-tickets Guru. _(POST /api/guru/etickets/write/delete/invitations)_

| Parâmetro | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `code` | string | Sim |  |
| `data` | object | Não | Corpo da requisição (campos conforme a doc oficial Guru do recurso/ação) |
| `account` | string | Não | Opcional quando há várias contas Guru vinculadas a este install (id, label ou parcial). Use guru_list_accounts pra ver as opções; omita se só houver uma. |

#### `guru_etickets_write_do_check_in`

Mutações em e-tickets Guru. _(POST /api/guru/etickets/write/do/check/in)_

| Parâmetro | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `code` | string | Sim |  |
| `data` | object | Não | Corpo da requisição (campos conforme a doc oficial Guru do recurso/ação) |
| `account` | string | Não | Opcional quando há várias contas Guru vinculadas a este install (id, label ou parcial). Use guru_list_accounts pra ver as opções; omita se só houver uma. |

#### `guru_leads`

Lista leads no Guru (cursor). _(POST /api/guru/leads)_

| Parâmetro | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `cursor` | string | Não | Cursor de paginação (próxima página) |
| `account` | string | Não | Opcional quando há várias contas Guru vinculadas a este install (id, label ou parcial). Use guru_list_accounts pra ver as opções; omita se só houver uma. |

#### `guru_list_accounts`

Lista contas Digital Manager Guru vinculadas a este install — id e apelido. _(POST /api/guru/list/accounts)_

| Parâmetro | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `account` | string | Não | Opcional quando há várias contas Guru vinculadas a este install (id, label ou parcial). Use guru_list_accounts pra ver as opções; omita se só houver uma. |

#### `guru_myorders`

Gera link SSO da área de compras (MyOrders) de um comprador pelo email (POST myorders/auth/sso/:email). _(POST /api/guru/myorders)_

| Parâmetro | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `email` | string | Sim | Email do comprador |
| `data` | object | Não | Corpo da requisição (campos conforme a doc oficial Guru do recurso/ação) |
| `account` | string | Não | Opcional quando há várias contas Guru vinculadas a este install (id, label ou parcial). Use guru_list_accounts pra ver as opções; omita se só houver uma. |

#### `guru_products_checkout_options`

Produtos e ofertas no Guru (leitura). _(POST /api/guru/products/checkout/options)_

| Parâmetro | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `product_id` | string | Não |  |
| `offer_id` | string | Não |  |
| `section` | string | Não | checkout_options/offer_checkout_options (appearance, content, emails, order-bump, pixels, redirects) |
| `name` | string | Não |  |
| `type` | string | Não |  |
| `marketplace_id` | string | Não |  |
| `is_hidden` | integer | Não |  |
| `cursor` | string | Não | Cursor de paginação (próxima página) |
| `account` | string | Não | Opcional quando há várias contas Guru vinculadas a este install (id, label ou parcial). Use guru_list_accounts pra ver as opções; omita se só houver uma. |
| `product_ids` | string[] | Não | Bulk mode: multiple values for product_id |
| `offer_ids` | string[] | Não | Bulk mode: multiple values for offer_id |
| `marketplace_ids` | string[] | Não | Bulk mode: multiple values for marketplace_id |

#### `guru_products_get`

Produtos e ofertas no Guru (leitura). _(POST /api/guru/products/get)_

| Parâmetro | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `product_id` | string | Não |  |
| `offer_id` | string | Não |  |
| `section` | string | Não | checkout_options/offer_checkout_options (appearance, content, emails, order-bump, pixels, redirects) |
| `name` | string | Não |  |
| `type` | string | Não |  |
| `marketplace_id` | string | Não |  |
| `is_hidden` | integer | Não |  |
| `cursor` | string | Não | Cursor de paginação (próxima página) |
| `account` | string | Não | Opcional quando há várias contas Guru vinculadas a este install (id, label ou parcial). Use guru_list_accounts pra ver as opções; omita se só houver uma. |
| `product_ids` | string[] | Não | Bulk mode: multiple values for product_id |
| `offer_ids` | string[] | Não | Bulk mode: multiple values for offer_id |
| `marketplace_ids` | string[] | Não | Bulk mode: multiple values for marketplace_id |

#### `guru_products_list`

Produtos e ofertas no Guru (leitura). _(POST /api/guru/products/list)_

| Parâmetro | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `product_id` | string | Não |  |
| `offer_id` | string | Não |  |
| `section` | string | Não | checkout_options/offer_checkout_options (appearance, content, emails, order-bump, pixels, redirects) |
| `name` | string | Não |  |
| `type` | string | Não |  |
| `marketplace_id` | string | Não |  |
| `is_hidden` | integer | Não |  |
| `cursor` | string | Não | Cursor de paginação (próxima página) |
| `account` | string | Não | Opcional quando há várias contas Guru vinculadas a este install (id, label ou parcial). Use guru_list_accounts pra ver as opções; omita se só houver uma. |
| `product_ids` | string[] | Não | Bulk mode: multiple values for product_id |
| `offer_ids` | string[] | Não | Bulk mode: multiple values for offer_id |
| `marketplace_ids` | string[] | Não | Bulk mode: multiple values for marketplace_id |

#### `guru_products_offer`

Produtos e ofertas no Guru (leitura). _(POST /api/guru/products/offer)_

| Parâmetro | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `product_id` | string | Não |  |
| `offer_id` | string | Não |  |
| `section` | string | Não | checkout_options/offer_checkout_options (appearance, content, emails, order-bump, pixels, redirects) |
| `name` | string | Não |  |
| `type` | string | Não |  |
| `marketplace_id` | string | Não |  |
| `is_hidden` | integer | Não |  |
| `cursor` | string | Não | Cursor de paginação (próxima página) |
| `account` | string | Não | Opcional quando há várias contas Guru vinculadas a este install (id, label ou parcial). Use guru_list_accounts pra ver as opções; omita se só houver uma. |
| `product_ids` | string[] | Não | Bulk mode: multiple values for product_id |
| `offer_ids` | string[] | Não | Bulk mode: multiple values for offer_id |
| `marketplace_ids` | string[] | Não | Bulk mode: multiple values for marketplace_id |

#### `guru_products_offer_checkout_options`

Produtos e ofertas no Guru (leitura). _(POST /api/guru/products/offer/checkout/options)_

| Parâmetro | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `product_id` | string | Não |  |
| `offer_id` | string | Não |  |
| `section` | string | Não | checkout_options/offer_checkout_options (appearance, content, emails, order-bump, pixels, redirects) |
| `name` | string | Não |  |
| `type` | string | Não |  |
| `marketplace_id` | string | Não |  |
| `is_hidden` | integer | Não |  |
| `cursor` | string | Não | Cursor de paginação (próxima página) |
| `account` | string | Não | Opcional quando há várias contas Guru vinculadas a este install (id, label ou parcial). Use guru_list_accounts pra ver as opções; omita se só houver uma. |
| `product_ids` | string[] | Não | Bulk mode: multiple values for product_id |
| `offer_ids` | string[] | Não | Bulk mode: multiple values for offer_id |
| `marketplace_ids` | string[] | Não | Bulk mode: multiple values for marketplace_id |

#### `guru_products_offer_subscription_options`

Produtos e ofertas no Guru (leitura). _(POST /api/guru/products/offer/subscription/options)_

| Parâmetro | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `product_id` | string | Não |  |
| `offer_id` | string | Não |  |
| `section` | string | Não | checkout_options/offer_checkout_options (appearance, content, emails, order-bump, pixels, redirects) |
| `name` | string | Não |  |
| `type` | string | Não |  |
| `marketplace_id` | string | Não |  |
| `is_hidden` | integer | Não |  |
| `cursor` | string | Não | Cursor de paginação (próxima página) |
| `account` | string | Não | Opcional quando há várias contas Guru vinculadas a este install (id, label ou parcial). Use guru_list_accounts pra ver as opções; omita se só houver uma. |
| `product_ids` | string[] | Não | Bulk mode: multiple values for product_id |
| `offer_ids` | string[] | Não | Bulk mode: multiple values for offer_id |
| `marketplace_ids` | string[] | Não | Bulk mode: multiple values for marketplace_id |

#### `guru_products_offers`

Produtos e ofertas no Guru (leitura). _(POST /api/guru/products/offers)_

| Parâmetro | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `product_id` | string | Não |  |
| `offer_id` | string | Não |  |
| `section` | string | Não | checkout_options/offer_checkout_options (appearance, content, emails, order-bump, pixels, redirects) |
| `name` | string | Não |  |
| `type` | string | Não |  |
| `marketplace_id` | string | Não |  |
| `is_hidden` | integer | Não |  |
| `cursor` | string | Não | Cursor de paginação (próxima página) |
| `account` | string | Não | Opcional quando há várias contas Guru vinculadas a este install (id, label ou parcial). Use guru_list_accounts pra ver as opções; omita se só houver uma. |
| `product_ids` | string[] | Não | Bulk mode: multiple values for product_id |
| `offer_ids` | string[] | Não | Bulk mode: multiple values for offer_id |
| `marketplace_ids` | string[] | Não | Bulk mode: multiple values for marketplace_id |

#### `guru_products_subscription_options`

Produtos e ofertas no Guru (leitura). _(POST /api/guru/products/subscription/options)_

| Parâmetro | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `product_id` | string | Não |  |
| `offer_id` | string | Não |  |
| `section` | string | Não | checkout_options/offer_checkout_options (appearance, content, emails, order-bump, pixels, redirects) |
| `name` | string | Não |  |
| `type` | string | Não |  |
| `marketplace_id` | string | Não |  |
| `is_hidden` | integer | Não |  |
| `cursor` | string | Não | Cursor de paginação (próxima página) |
| `account` | string | Não | Opcional quando há várias contas Guru vinculadas a este install (id, label ou parcial). Use guru_list_accounts pra ver as opções; omita se só houver uma. |
| `product_ids` | string[] | Não | Bulk mode: multiple values for product_id |
| `offer_ids` | string[] | Não | Bulk mode: multiple values for offer_id |
| `marketplace_ids` | string[] | Não | Bulk mode: multiple values for marketplace_id |

#### `guru_products_write_set_offer_availability`

Mutações em produtos Guru. Ação: set_offer_availability (product_id + offer_id + data com a disponibilidade). _(POST /api/guru/products/write/set/offer/availability)_

| Parâmetro | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `product_id` | string | Sim |  |
| `offer_id` | string | Sim |  |
| `data` | object | Não | Corpo da requisição (campos conforme a doc oficial Guru do recurso/ação) |
| `account` | string | Não | Opcional quando há várias contas Guru vinculadas a este install (id, label ou parcial). Use guru_list_accounts pra ver as opções; omita se só houver uma. |
| `product_ids` | string[] | Não | Bulk mode: multiple values for product_id |
| `offer_ids` | string[] | Não | Bulk mode: multiple values for offer_id |

#### `guru_subscriptions_activities`

Assinaturas no Guru (leitura). _(POST /api/guru/subscriptions/activities)_

| Parâmetro | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `id` | string | Não |  |
| `invoice_code` | string | Não | invoice/invoice_transactions |
| `subscription_status` | string | Não |  |
| `product_id` | string | Não |  |
| `contact_email` | string | Não |  |
| `contact_doc` | string | Não |  |
| `contact_name` | string | Não |  |
| `started_at_ini` | string | Não |  |
| `started_at_end` | string | Não |  |
| `last_status_at_ini` | string | Não |  |
| `last_status_at_end` | string | Não |  |
| `cursor` | string | Não | Cursor de paginação (próxima página) |
| `account` | string | Não | Opcional quando há várias contas Guru vinculadas a este install (id, label ou parcial). Use guru_list_accounts pra ver as opções; omita se só houver uma. |
| `ids` | string[] | Não | Bulk mode: multiple values for id |
| `product_ids` | string[] | Não | Bulk mode: multiple values for product_id |

#### `guru_subscriptions_get`

Assinaturas no Guru (leitura). _(POST /api/guru/subscriptions/get)_

| Parâmetro | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `id` | string | Não |  |
| `invoice_code` | string | Não | invoice/invoice_transactions |
| `subscription_status` | string | Não |  |
| `product_id` | string | Não |  |
| `contact_email` | string | Não |  |
| `contact_doc` | string | Não |  |
| `contact_name` | string | Não |  |
| `started_at_ini` | string | Não |  |
| `started_at_end` | string | Não |  |
| `last_status_at_ini` | string | Não |  |
| `last_status_at_end` | string | Não |  |
| `cursor` | string | Não | Cursor de paginação (próxima página) |
| `account` | string | Não | Opcional quando há várias contas Guru vinculadas a este install (id, label ou parcial). Use guru_list_accounts pra ver as opções; omita se só houver uma. |
| `ids` | string[] | Não | Bulk mode: multiple values for id |
| `product_ids` | string[] | Não | Bulk mode: multiple values for product_id |

#### `guru_subscriptions_invoice`

Assinaturas no Guru (leitura). _(POST /api/guru/subscriptions/invoice)_

| Parâmetro | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `id` | string | Não |  |
| `invoice_code` | string | Não | invoice/invoice_transactions |
| `subscription_status` | string | Não |  |
| `product_id` | string | Não |  |
| `contact_email` | string | Não |  |
| `contact_doc` | string | Não |  |
| `contact_name` | string | Não |  |
| `started_at_ini` | string | Não |  |
| `started_at_end` | string | Não |  |
| `last_status_at_ini` | string | Não |  |
| `last_status_at_end` | string | Não |  |
| `cursor` | string | Não | Cursor de paginação (próxima página) |
| `account` | string | Não | Opcional quando há várias contas Guru vinculadas a este install (id, label ou parcial). Use guru_list_accounts pra ver as opções; omita se só houver uma. |
| `ids` | string[] | Não | Bulk mode: multiple values for id |
| `product_ids` | string[] | Não | Bulk mode: multiple values for product_id |

#### `guru_subscriptions_invoice_transactions`

Assinaturas no Guru (leitura). _(POST /api/guru/subscriptions/invoice/transactions)_

| Parâmetro | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `id` | string | Não |  |
| `invoice_code` | string | Não | invoice/invoice_transactions |
| `subscription_status` | string | Não |  |
| `product_id` | string | Não |  |
| `contact_email` | string | Não |  |
| `contact_doc` | string | Não |  |
| `contact_name` | string | Não |  |
| `started_at_ini` | string | Não |  |
| `started_at_end` | string | Não |  |
| `last_status_at_ini` | string | Não |  |
| `last_status_at_end` | string | Não |  |
| `cursor` | string | Não | Cursor de paginação (próxima página) |
| `account` | string | Não | Opcional quando há várias contas Guru vinculadas a este install (id, label ou parcial). Use guru_list_accounts pra ver as opções; omita se só houver uma. |
| `ids` | string[] | Não | Bulk mode: multiple values for id |
| `product_ids` | string[] | Não | Bulk mode: multiple values for product_id |

#### `guru_subscriptions_invoices`

Assinaturas no Guru (leitura). _(POST /api/guru/subscriptions/invoices)_

| Parâmetro | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `id` | string | Não |  |
| `invoice_code` | string | Não | invoice/invoice_transactions |
| `subscription_status` | string | Não |  |
| `product_id` | string | Não |  |
| `contact_email` | string | Não |  |
| `contact_doc` | string | Não |  |
| `contact_name` | string | Não |  |
| `started_at_ini` | string | Não |  |
| `started_at_end` | string | Não |  |
| `last_status_at_ini` | string | Não |  |
| `last_status_at_end` | string | Não |  |
| `cursor` | string | Não | Cursor de paginação (próxima página) |
| `account` | string | Não | Opcional quando há várias contas Guru vinculadas a este install (id, label ou parcial). Use guru_list_accounts pra ver as opções; omita se só houver uma. |
| `ids` | string[] | Não | Bulk mode: multiple values for id |
| `product_ids` | string[] | Não | Bulk mode: multiple values for product_id |

#### `guru_subscriptions_payment_types`

Assinaturas no Guru (leitura). _(POST /api/guru/subscriptions/payment/types)_

| Parâmetro | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `id` | string | Não |  |
| `invoice_code` | string | Não | invoice/invoice_transactions |
| `subscription_status` | string | Não |  |
| `product_id` | string | Não |  |
| `contact_email` | string | Não |  |
| `contact_doc` | string | Não |  |
| `contact_name` | string | Não |  |
| `started_at_ini` | string | Não |  |
| `started_at_end` | string | Não |  |
| `last_status_at_ini` | string | Não |  |
| `last_status_at_end` | string | Não |  |
| `cursor` | string | Não | Cursor de paginação (próxima página) |
| `account` | string | Não | Opcional quando há várias contas Guru vinculadas a este install (id, label ou parcial). Use guru_list_accounts pra ver as opções; omita se só houver uma. |
| `ids` | string[] | Não | Bulk mode: multiple values for id |
| `product_ids` | string[] | Não | Bulk mode: multiple values for product_id |

#### `guru_subscriptions_plans_available`

Assinaturas no Guru (leitura). _(POST /api/guru/subscriptions/plans/available)_

| Parâmetro | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `id` | string | Não |  |
| `invoice_code` | string | Não | invoice/invoice_transactions |
| `subscription_status` | string | Não |  |
| `product_id` | string | Não |  |
| `contact_email` | string | Não |  |
| `contact_doc` | string | Não |  |
| `contact_name` | string | Não |  |
| `started_at_ini` | string | Não |  |
| `started_at_end` | string | Não |  |
| `last_status_at_ini` | string | Não |  |
| `last_status_at_end` | string | Não |  |
| `cursor` | string | Não | Cursor de paginação (próxima página) |
| `account` | string | Não | Opcional quando há várias contas Guru vinculadas a este install (id, label ou parcial). Use guru_list_accounts pra ver as opções; omita se só houver uma. |
| `ids` | string[] | Não | Bulk mode: multiple values for id |
| `product_ids` | string[] | Não | Bulk mode: multiple values for product_id |

#### `guru_subscriptions_search`

Assinaturas no Guru (leitura). _(POST /api/guru/subscriptions/search)_

| Parâmetro | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `id` | string | Não |  |
| `invoice_code` | string | Não | invoice/invoice_transactions |
| `subscription_status` | string | Não |  |
| `product_id` | string | Não |  |
| `contact_email` | string | Não |  |
| `contact_doc` | string | Não |  |
| `contact_name` | string | Não |  |
| `started_at_ini` | string | Não |  |
| `started_at_end` | string | Não |  |
| `last_status_at_ini` | string | Não |  |
| `last_status_at_end` | string | Não |  |
| `cursor` | string | Não | Cursor de paginação (próxima página) |
| `account` | string | Não | Opcional quando há várias contas Guru vinculadas a este install (id, label ou parcial). Use guru_list_accounts pra ver as opções; omita se só houver uma. |
| `ids` | string[] | Não | Bulk mode: multiple values for id |
| `product_ids` | string[] | Não | Bulk mode: multiple values for product_id |

#### `guru_subscriptions_transactions`

Assinaturas no Guru (leitura). _(POST /api/guru/subscriptions/transactions)_

| Parâmetro | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `id` | string | Não |  |
| `invoice_code` | string | Não | invoice/invoice_transactions |
| `subscription_status` | string | Não |  |
| `product_id` | string | Não |  |
| `contact_email` | string | Não |  |
| `contact_doc` | string | Não |  |
| `contact_name` | string | Não |  |
| `started_at_ini` | string | Não |  |
| `started_at_end` | string | Não |  |
| `last_status_at_ini` | string | Não |  |
| `last_status_at_end` | string | Não |  |
| `cursor` | string | Não | Cursor de paginação (próxima página) |
| `account` | string | Não | Opcional quando há várias contas Guru vinculadas a este install (id, label ou parcial). Use guru_list_accounts pra ver as opções; omita se só houver uma. |
| `ids` | string[] | Não | Bulk mode: multiple values for id |
| `product_ids` | string[] | Não | Bulk mode: multiple values for product_id |

#### `guru_subscriptions_write_add_coupon`

Mutações em assinaturas Guru. _(POST /api/guru/subscriptions/write/add/coupon)_

| Parâmetro | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `id` | string | Sim | ID da assinatura |
| `data` | object | Não | Corpo da requisição (campos conforme a doc oficial Guru do recurso/ação) |
| `account` | string | Não | Opcional quando há várias contas Guru vinculadas a este install (id, label ou parcial). Use guru_list_accounts pra ver as opções; omita se só houver uma. |
| `ids` | string[] | Não | Bulk mode: multiple values for id |

#### `guru_subscriptions_write_cancel`

Mutações em assinaturas Guru. _(POST /api/guru/subscriptions/write/cancel)_

| Parâmetro | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `id` | string | Sim | ID da assinatura |
| `data` | object | Não | Corpo da requisição (campos conforme a doc oficial Guru do recurso/ação) |
| `account` | string | Não | Opcional quando há várias contas Guru vinculadas a este install (id, label ou parcial). Use guru_list_accounts pra ver as opções; omita se só houver uma. |
| `ids` | string[] | Não | Bulk mode: multiple values for id |

#### `guru_subscriptions_write_cancel_at_cycle_end`

Mutações em assinaturas Guru. _(POST /api/guru/subscriptions/write/cancel/at/cycle/end)_

| Parâmetro | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `id` | string | Sim | ID da assinatura |
| `data` | object | Não | Corpo da requisição (campos conforme a doc oficial Guru do recurso/ação) |
| `account` | string | Não | Opcional quando há várias contas Guru vinculadas a este install (id, label ou parcial). Use guru_list_accounts pra ver as opções; omita se só houver uma. |
| `ids` | string[] | Não | Bulk mode: multiple values for id |

#### `guru_subscriptions_write_change_plan`

Mutações em assinaturas Guru. _(POST /api/guru/subscriptions/write/change/plan)_

| Parâmetro | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `id` | string | Sim | ID da assinatura |
| `data` | object | Não | Corpo da requisição (campos conforme a doc oficial Guru do recurso/ação) |
| `account` | string | Não | Opcional quando há várias contas Guru vinculadas a este install (id, label ou parcial). Use guru_list_accounts pra ver as opções; omita se só houver uma. |
| `ids` | string[] | Não | Bulk mode: multiple values for id |

#### `guru_subscriptions_write_remove_coupon`

Mutações em assinaturas Guru. _(POST /api/guru/subscriptions/write/remove/coupon)_

| Parâmetro | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `id` | string | Sim | ID da assinatura |
| `data` | object | Não | Corpo da requisição (campos conforme a doc oficial Guru do recurso/ação) |
| `account` | string | Não | Opcional quando há várias contas Guru vinculadas a este install (id, label ou parcial). Use guru_list_accounts pra ver as opções; omita se só houver uma. |
| `ids` | string[] | Não | Bulk mode: multiple values for id |

#### `guru_subscriptions_write_remove_increment_discount`

Mutações em assinaturas Guru. _(POST /api/guru/subscriptions/write/remove/increment/discount)_

| Parâmetro | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `id` | string | Sim | ID da assinatura |
| `data` | object | Não | Corpo da requisição (campos conforme a doc oficial Guru do recurso/ação) |
| `account` | string | Não | Opcional quando há várias contas Guru vinculadas a este install (id, label ou parcial). Use guru_list_accounts pra ver as opções; omita se só houver uma. |
| `ids` | string[] | Não | Bulk mode: multiple values for id |

#### `guru_subscriptions_write_set_current_offer`

Mutações em assinaturas Guru. _(POST /api/guru/subscriptions/write/set/current/offer)_

| Parâmetro | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `id` | string | Sim | ID da assinatura |
| `data` | object | Não | Corpo da requisição (campos conforme a doc oficial Guru do recurso/ação) |
| `account` | string | Não | Opcional quando há várias contas Guru vinculadas a este install (id, label ou parcial). Use guru_list_accounts pra ver as opções; omita se só houver uma. |
| `ids` | string[] | Não | Bulk mode: multiple values for id |

#### `guru_subscriptions_write_set_cycle_end_date`

Mutações em assinaturas Guru. _(POST /api/guru/subscriptions/write/set/cycle/end/date)_

| Parâmetro | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `id` | string | Sim | ID da assinatura |
| `data` | object | Não | Corpo da requisição (campos conforme a doc oficial Guru do recurso/ação) |
| `account` | string | Não | Opcional quando há várias contas Guru vinculadas a este install (id, label ou parcial). Use guru_list_accounts pra ver as opções; omita se só houver uma. |
| `ids` | string[] | Não | Bulk mode: multiple values for id |

#### `guru_subscriptions_write_set_increment_discount`

Mutações em assinaturas Guru. _(POST /api/guru/subscriptions/write/set/increment/discount)_

| Parâmetro | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `id` | string | Sim | ID da assinatura |
| `data` | object | Não | Corpo da requisição (campos conforme a doc oficial Guru do recurso/ação) |
| `account` | string | Não | Opcional quando há várias contas Guru vinculadas a este install (id, label ou parcial). Use guru_list_accounts pra ver as opções; omita se só houver uma. |
| `ids` | string[] | Não | Bulk mode: multiple values for id |

#### `guru_subscriptions_write_set_installment`

Mutações em assinaturas Guru. _(POST /api/guru/subscriptions/write/set/installment)_

| Parâmetro | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `id` | string | Sim | ID da assinatura |
| `data` | object | Não | Corpo da requisição (campos conforme a doc oficial Guru do recurso/ação) |
| `account` | string | Não | Opcional quando há várias contas Guru vinculadas a este install (id, label ou parcial). Use guru_list_accounts pra ver as opções; omita se só houver uma. |
| `ids` | string[] | Não | Bulk mode: multiple values for id |

#### `guru_subscriptions_write_set_next_offer`

Mutações em assinaturas Guru. _(POST /api/guru/subscriptions/write/set/next/offer)_

| Parâmetro | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `id` | string | Sim | ID da assinatura |
| `data` | object | Não | Corpo da requisição (campos conforme a doc oficial Guru do recurso/ação) |
| `account` | string | Não | Opcional quando há várias contas Guru vinculadas a este install (id, label ou parcial). Use guru_list_accounts pra ver as opções; omita se só houver uma. |
| `ids` | string[] | Não | Bulk mode: multiple values for id |

#### `guru_subscriptions_write_set_payment_types`

Mutações em assinaturas Guru. _(POST /api/guru/subscriptions/write/set/payment/types)_

| Parâmetro | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `id` | string | Sim | ID da assinatura |
| `data` | object | Não | Corpo da requisição (campos conforme a doc oficial Guru do recurso/ação) |
| `account` | string | Não | Opcional quando há várias contas Guru vinculadas a este install (id, label ou parcial). Use guru_list_accounts pra ver as opções; omita se só houver uma. |
| `ids` | string[] | Não | Bulk mode: multiple values for id |

#### `guru_subscriptions_write_set_trial_end_date`

Mutações em assinaturas Guru. _(POST /api/guru/subscriptions/write/set/trial/end/date)_

| Parâmetro | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `id` | string | Sim | ID da assinatura |
| `data` | object | Não | Corpo da requisição (campos conforme a doc oficial Guru do recurso/ação) |
| `account` | string | Não | Opcional quando há várias contas Guru vinculadas a este install (id, label ou parcial). Use guru_list_accounts pra ver as opções; omita se só houver uma. |
| `ids` | string[] | Não | Bulk mode: multiple values for id |

#### `guru_subscriptions_write_simulate_plan`

Mutações em assinaturas Guru. _(POST /api/guru/subscriptions/write/simulate/plan)_

| Parâmetro | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `id` | string | Sim | ID da assinatura |
| `data` | object | Não | Corpo da requisição (campos conforme a doc oficial Guru do recurso/ação) |
| `account` | string | Não | Opcional quando há várias contas Guru vinculadas a este install (id, label ou parcial). Use guru_list_accounts pra ver as opções; omita se só houver uma. |
| `ids` | string[] | Não | Bulk mode: multiple values for id |

#### `guru_transactions_activities`

Vendas/transações no Guru (leitura). _(POST /api/guru/transactions/activities)_

| Parâmetro | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `id` | string | Não |  |
| `marketplace_name` | string | Não | by_marketplace: nome do marketplace |
| `marketplace_id` | string | Não |  |
| `sub` | string | Não | by_marketplace: sub-recurso (default detail) (detail, activities, order-bumps, etickets) |
| `ordered_at_ini` | string | Não |  |
| `ordered_at_end` | string | Não |  |
| `confirmed_at_ini` | string | Não |  |
| `confirmed_at_end` | string | Não |  |
| `transaction_status` | string | Não |  |
| `product_id` | string | Não |  |
| `subscription_id` | string | Não |  |
| `contact_email` | string | Não |  |
| `contact_doc` | string | Não |  |
| `contact_name` | string | Não |  |
| `cursor` | string | Não | Cursor de paginação (próxima página) |
| `account` | string | Não | Opcional quando há várias contas Guru vinculadas a este install (id, label ou parcial). Use guru_list_accounts pra ver as opções; omita se só houver uma. |
| `ids` | string[] | Não | Bulk mode: multiple values for id |
| `marketplace_ids` | string[] | Não | Bulk mode: multiple values for marketplace_id |
| `product_ids` | string[] | Não | Bulk mode: multiple values for product_id |
| `subscription_ids` | string[] | Não | Bulk mode: multiple values for subscription_id |

#### `guru_transactions_by_marketplace`

Vendas/transações no Guru (leitura). _(POST /api/guru/transactions/by/marketplace)_

| Parâmetro | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `id` | string | Não |  |
| `marketplace_name` | string | Não | by_marketplace: nome do marketplace |
| `marketplace_id` | string | Não |  |
| `sub` | string | Não | by_marketplace: sub-recurso (default detail) (detail, activities, order-bumps, etickets) |
| `ordered_at_ini` | string | Não |  |
| `ordered_at_end` | string | Não |  |
| `confirmed_at_ini` | string | Não |  |
| `confirmed_at_end` | string | Não |  |
| `transaction_status` | string | Não |  |
| `product_id` | string | Não |  |
| `subscription_id` | string | Não |  |
| `contact_email` | string | Não |  |
| `contact_doc` | string | Não |  |
| `contact_name` | string | Não |  |
| `cursor` | string | Não | Cursor de paginação (próxima página) |
| `account` | string | Não | Opcional quando há várias contas Guru vinculadas a este install (id, label ou parcial). Use guru_list_accounts pra ver as opções; omita se só houver uma. |
| `ids` | string[] | Não | Bulk mode: multiple values for id |
| `marketplace_ids` | string[] | Não | Bulk mode: multiple values for marketplace_id |
| `product_ids` | string[] | Não | Bulk mode: multiple values for product_id |
| `subscription_ids` | string[] | Não | Bulk mode: multiple values for subscription_id |

#### `guru_transactions_etickets`

Vendas/transações no Guru (leitura). _(POST /api/guru/transactions/etickets)_

| Parâmetro | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `id` | string | Não |  |
| `marketplace_name` | string | Não | by_marketplace: nome do marketplace |
| `marketplace_id` | string | Não |  |
| `sub` | string | Não | by_marketplace: sub-recurso (default detail) (detail, activities, order-bumps, etickets) |
| `ordered_at_ini` | string | Não |  |
| `ordered_at_end` | string | Não |  |
| `confirmed_at_ini` | string | Não |  |
| `confirmed_at_end` | string | Não |  |
| `transaction_status` | string | Não |  |
| `product_id` | string | Não |  |
| `subscription_id` | string | Não |  |
| `contact_email` | string | Não |  |
| `contact_doc` | string | Não |  |
| `contact_name` | string | Não |  |
| `cursor` | string | Não | Cursor de paginação (próxima página) |
| `account` | string | Não | Opcional quando há várias contas Guru vinculadas a este install (id, label ou parcial). Use guru_list_accounts pra ver as opções; omita se só houver uma. |
| `ids` | string[] | Não | Bulk mode: multiple values for id |
| `marketplace_ids` | string[] | Não | Bulk mode: multiple values for marketplace_id |
| `product_ids` | string[] | Não | Bulk mode: multiple values for product_id |
| `subscription_ids` | string[] | Não | Bulk mode: multiple values for subscription_id |

#### `guru_transactions_get`

Vendas/transações no Guru (leitura). _(POST /api/guru/transactions/get)_

| Parâmetro | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `id` | string | Não |  |
| `marketplace_name` | string | Não | by_marketplace: nome do marketplace |
| `marketplace_id` | string | Não |  |
| `sub` | string | Não | by_marketplace: sub-recurso (default detail) (detail, activities, order-bumps, etickets) |
| `ordered_at_ini` | string | Não |  |
| `ordered_at_end` | string | Não |  |
| `confirmed_at_ini` | string | Não |  |
| `confirmed_at_end` | string | Não |  |
| `transaction_status` | string | Não |  |
| `product_id` | string | Não |  |
| `subscription_id` | string | Não |  |
| `contact_email` | string | Não |  |
| `contact_doc` | string | Não |  |
| `contact_name` | string | Não |  |
| `cursor` | string | Não | Cursor de paginação (próxima página) |
| `account` | string | Não | Opcional quando há várias contas Guru vinculadas a este install (id, label ou parcial). Use guru_list_accounts pra ver as opções; omita se só houver uma. |
| `ids` | string[] | Não | Bulk mode: multiple values for id |
| `marketplace_ids` | string[] | Não | Bulk mode: multiple values for marketplace_id |
| `product_ids` | string[] | Não | Bulk mode: multiple values for product_id |
| `subscription_ids` | string[] | Não | Bulk mode: multiple values for subscription_id |

#### `guru_transactions_order_bumps`

Vendas/transações no Guru (leitura). _(POST /api/guru/transactions/order/bumps)_

| Parâmetro | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `id` | string | Não |  |
| `marketplace_name` | string | Não | by_marketplace: nome do marketplace |
| `marketplace_id` | string | Não |  |
| `sub` | string | Não | by_marketplace: sub-recurso (default detail) (detail, activities, order-bumps, etickets) |
| `ordered_at_ini` | string | Não |  |
| `ordered_at_end` | string | Não |  |
| `confirmed_at_ini` | string | Não |  |
| `confirmed_at_end` | string | Não |  |
| `transaction_status` | string | Não |  |
| `product_id` | string | Não |  |
| `subscription_id` | string | Não |  |
| `contact_email` | string | Não |  |
| `contact_doc` | string | Não |  |
| `contact_name` | string | Não |  |
| `cursor` | string | Não | Cursor de paginação (próxima página) |
| `account` | string | Não | Opcional quando há várias contas Guru vinculadas a este install (id, label ou parcial). Use guru_list_accounts pra ver as opções; omita se só houver uma. |
| `ids` | string[] | Não | Bulk mode: multiple values for id |
| `marketplace_ids` | string[] | Não | Bulk mode: multiple values for marketplace_id |
| `product_ids` | string[] | Não | Bulk mode: multiple values for product_id |
| `subscription_ids` | string[] | Não | Bulk mode: multiple values for subscription_id |

#### `guru_transactions_search`

Vendas/transações no Guru (leitura). _(POST /api/guru/transactions/search)_

| Parâmetro | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `id` | string | Não |  |
| `marketplace_name` | string | Não | by_marketplace: nome do marketplace |
| `marketplace_id` | string | Não |  |
| `sub` | string | Não | by_marketplace: sub-recurso (default detail) (detail, activities, order-bumps, etickets) |
| `ordered_at_ini` | string | Não |  |
| `ordered_at_end` | string | Não |  |
| `confirmed_at_ini` | string | Não |  |
| `confirmed_at_end` | string | Não |  |
| `transaction_status` | string | Não |  |
| `product_id` | string | Não |  |
| `subscription_id` | string | Não |  |
| `contact_email` | string | Não |  |
| `contact_doc` | string | Não |  |
| `contact_name` | string | Não |  |
| `cursor` | string | Não | Cursor de paginação (próxima página) |
| `account` | string | Não | Opcional quando há várias contas Guru vinculadas a este install (id, label ou parcial). Use guru_list_accounts pra ver as opções; omita se só houver uma. |
| `ids` | string[] | Não | Bulk mode: multiple values for id |
| `marketplace_ids` | string[] | Não | Bulk mode: multiple values for marketplace_id |
| `product_ids` | string[] | Não | Bulk mode: multiple values for product_id |
| `subscription_ids` | string[] | Não | Bulk mode: multiple values for subscription_id |

#### `guru_transactions_write_chargeback`

Mutações em transações Guru (mexe em dinheiro, irreversível). _(POST /api/guru/transactions/write/chargeback)_

| Parâmetro | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `id` | string | Sim | ID da transação |
| `data` | object | Não | Corpo da requisição (campos conforme a doc oficial Guru do recurso/ação) |
| `account` | string | Não | Opcional quando há várias contas Guru vinculadas a este install (id, label ou parcial). Use guru_list_accounts pra ver as opções; omita se só houver uma. |
| `ids` | string[] | Não | Bulk mode: multiple values for id |

#### `guru_transactions_write_generate_invoice`

Mutações em transações Guru (mexe em dinheiro, irreversível). _(POST /api/guru/transactions/write/generate/invoice)_

| Parâmetro | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `id` | string | Sim | ID da transação |
| `data` | object | Não | Corpo da requisição (campos conforme a doc oficial Guru do recurso/ação) |
| `account` | string | Não | Opcional quando há várias contas Guru vinculadas a este install (id, label ou parcial). Use guru_list_accounts pra ver as opções; omita se só houver uma. |
| `ids` | string[] | Não | Bulk mode: multiple values for id |

#### `guru_transactions_write_refund`

Mutações em transações Guru (mexe em dinheiro, irreversível). _(POST /api/guru/transactions/write/refund)_

| Parâmetro | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `id` | string | Sim | ID da transação |
| `data` | object | Não | Corpo da requisição (campos conforme a doc oficial Guru do recurso/ação) |
| `account` | string | Não | Opcional quando há várias contas Guru vinculadas a este install (id, label ou parcial). Use guru_list_accounts pra ver as opções; omita se só houver uma. |
| `ids` | string[] | Não | Bulk mode: multiple values for id |

#### `guru_transactions_write_reissue`

Mutações em transações Guru (mexe em dinheiro, irreversível). _(POST /api/guru/transactions/write/reissue)_

| Parâmetro | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `id` | string | Sim | ID da transação |
| `data` | object | Não | Corpo da requisição (campos conforme a doc oficial Guru do recurso/ação) |
| `account` | string | Não | Opcional quando há várias contas Guru vinculadas a este install (id, label ou parcial). Use guru_list_accounts pra ver as opções; omita se só houver uma. |
| `ids` | string[] | Não | Bulk mode: multiple values for id |

#### `guru_transactions_write_update_buyer`

Mutações em transações Guru (mexe em dinheiro, irreversível). _(POST /api/guru/transactions/write/update/buyer)_

| Parâmetro | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `id` | string | Sim | ID da transação |
| `data` | object | Não | Corpo da requisição (campos conforme a doc oficial Guru do recurso/ação) |
| `account` | string | Não | Opcional quando há várias contas Guru vinculadas a este install (id, label ou parcial). Use guru_list_accounts pra ver as opções; omita se só houver uma. |
| `ids` | string[] | Não | Bulk mode: multiple values for id |

#### `guru_users_activities`

Usuários/membros da conta Guru (leitura). _(POST /api/guru/users/activities)_

| Parâmetro | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `id` | string | Não |  |
| `cursor` | string | Não | Cursor de paginação (próxima página) |
| `account` | string | Não | Opcional quando há várias contas Guru vinculadas a este install (id, label ou parcial). Use guru_list_accounts pra ver as opções; omita se só houver uma. |
| `ids` | string[] | Não | Bulk mode: multiple values for id |

#### `guru_users_get`

Usuários/membros da conta Guru (leitura). _(POST /api/guru/users/get)_

| Parâmetro | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `id` | string | Não |  |
| `cursor` | string | Não | Cursor de paginação (próxima página) |
| `account` | string | Não | Opcional quando há várias contas Guru vinculadas a este install (id, label ou parcial). Use guru_list_accounts pra ver as opções; omita se só houver uma. |
| `ids` | string[] | Não | Bulk mode: multiple values for id |

#### `guru_users_list`

Usuários/membros da conta Guru (leitura). _(POST /api/guru/users/list)_

| Parâmetro | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `id` | string | Não |  |
| `cursor` | string | Não | Cursor de paginação (próxima página) |
| `account` | string | Não | Opcional quando há várias contas Guru vinculadas a este install (id, label ou parcial). Use guru_list_accounts pra ver as opções; omita se só houver uma. |
| `ids` | string[] | Não | Bulk mode: multiple values for id |

#### `guru_users_write_delete`

Mutações em usuários Guru. Ação: delete (id, remove o usuário da conta). _(POST /api/guru/users/write/delete)_

| Parâmetro | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `id` | string | Sim |  |
| `account` | string | Não | Opcional quando há várias contas Guru vinculadas a este install (id, label ou parcial). Use guru_list_accounts pra ver as opções; omita se só houver uma. |
| `ids` | string[] | Não | Bulk mode: multiple values for id |

#### `guru_webhooks_activities`

Webhooks configurados no Guru. _(POST /api/guru/webhooks/activities)_

| Parâmetro | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `id` | string | Não |  |
| `cursor` | string | Não | Cursor de paginação (próxima página) |
| `account` | string | Não | Opcional quando há várias contas Guru vinculadas a este install (id, label ou parcial). Use guru_list_accounts pra ver as opções; omita se só houver uma. |
| `ids` | string[] | Não | Bulk mode: multiple values for id |

#### `guru_webhooks_get`

Webhooks configurados no Guru. _(POST /api/guru/webhooks/get)_

| Parâmetro | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `id` | string | Não |  |
| `cursor` | string | Não | Cursor de paginação (próxima página) |
| `account` | string | Não | Opcional quando há várias contas Guru vinculadas a este install (id, label ou parcial). Use guru_list_accounts pra ver as opções; omita se só houver uma. |
| `ids` | string[] | Não | Bulk mode: multiple values for id |

#### `guru_webhooks_list`

Webhooks configurados no Guru. _(POST /api/guru/webhooks/list)_

| Parâmetro | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `id` | string | Não |  |
| `cursor` | string | Não | Cursor de paginação (próxima página) |
| `account` | string | Não | Opcional quando há várias contas Guru vinculadas a este install (id, label ou parcial). Use guru_list_accounts pra ver as opções; omita se só houver uma. |
| `ids` | string[] | Não | Bulk mode: multiple values for id |

---

Este MCP também funciona via **conexão MCP** (Claude / Cursor) em `https://api.mcp.ai/p_guru` — veja o [README](../../README.md). A skill acima é pra consumir a **REST API** direto (agente próprio / código).
