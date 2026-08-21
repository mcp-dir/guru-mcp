# Digital Manager Guru

### Digital Manager Guru for Claude, ChatGPT and AI agents

Digital Manager Guru checkout and sales-management platform for digital products via the official API: sales/transactions, subscriptions, products and offers, contacts, affiliations, coupons, e-tickets and webhooks. Generate your User Token in the dashboard under My Profile → API Tokens.

- 📊 **95 tools**
- ✏️ **Read and write**
- 💬 **Works with any MCP client**: Claude Desktop, Cursor, VS Code, Cline, Continue
- 🔑 **Magic-link login (no password)**

[Portuguese version](README.md) · [Full docs (PT-BR)](docs/)

---

## One-click install

### Claude (Web and Desktop)

[➕ Open in Claude and connect](https://claude.ai/new?modal=add-custom-connector#settings/customize-connectors)

Manual: [claude.ai/customize/connectors](https://claude.ai/customize/connectors?surface=cowork) → **+** → **Add custom connector** → name `Digital Manager Guru`, URL `https://api.mcp.ai/p_guru`.

### Cursor

[➕ Install in Cursor](cursor://anysphere.cursor-deeplink/mcp/install?name=guru&config=eyJ1cmwiOiJodHRwczovL2FwaS5tY3AuYWkvcF9ndXJ1In0=)

### VS Code (Copilot Chat)

[➕ Install in VS Code](vscode:mcp/install?name=guru&config=%7B%22type%22%3A%22http%22%2C%22url%22%3A%22https%3A%2F%2Fapi.mcp.ai%2Fp_guru%22%7D)

### Any other MCP-over-HTTP client

```
https://api.mcp.ai/p_guru
```

---

## 95 tools

| Tool | Description |
|---|---|
| `guru_list_accounts` | Lista contas Digital Manager Guru vinculadas a este install — id e apelido. |
| `guru_transactions_search` | Vendas/transações no Guru (leitura). |
| `guru_transactions_get` | Vendas/transações no Guru (leitura). |
| `guru_transactions_activities` | Vendas/transações no Guru (leitura). |
| `guru_transactions_order_bumps` | Vendas/transações no Guru (leitura). |
| `guru_transactions_etickets` | Vendas/transações no Guru (leitura). |
| `guru_transactions_by_marketplace` | Vendas/transações no Guru (leitura). |
| `guru_transactions_write_refund` | Mutações em transações Guru (mexe em dinheiro, irreversível). |
| `guru_transactions_write_chargeback` | Mutações em transações Guru (mexe em dinheiro, irreversível). |
| `guru_transactions_write_reissue` | Mutações em transações Guru (mexe em dinheiro, irreversível). |
| `guru_transactions_write_update_buyer` | Mutações em transações Guru (mexe em dinheiro, irreversível). |
| `guru_transactions_write_generate_invoice` | Mutações em transações Guru (mexe em dinheiro, irreversível). |
| `guru_subscriptions_search` | Assinaturas no Guru (leitura). |
| `guru_subscriptions_get` | Assinaturas no Guru (leitura). |
| `guru_subscriptions_activities` | Assinaturas no Guru (leitura). |
| `guru_subscriptions_invoices` | Assinaturas no Guru (leitura). |
| `guru_subscriptions_invoice` | Assinaturas no Guru (leitura). |
| `guru_subscriptions_invoice_transactions` | Assinaturas no Guru (leitura). |
| `guru_subscriptions_transactions` | Assinaturas no Guru (leitura). |
| `guru_subscriptions_payment_types` | Assinaturas no Guru (leitura). |
| `guru_subscriptions_plans_available` | Assinaturas no Guru (leitura). |
| `guru_subscriptions_write_cancel` | Mutações em assinaturas Guru. Ações: cancel (id, +data opcional); cancel_at_cycle_end (id); add_coupon (id + data); remove_coupon (id); set_current_offer (id + data); set_next_offer (id + data); set_cycle_end_date (id… |
| `guru_subscriptions_write_cancel_at_cycle_end` | Mutações em assinaturas Guru. Ações: cancel (id, +data opcional); cancel_at_cycle_end (id); add_coupon (id + data); remove_coupon (id); set_current_offer (id + data); set_next_offer (id + data); set_cycle_end_date (id… |
| `guru_subscriptions_write_add_coupon` | Mutações em assinaturas Guru. Ações: cancel (id, +data opcional); cancel_at_cycle_end (id); add_coupon (id + data); remove_coupon (id); set_current_offer (id + data); set_next_offer (id + data); set_cycle_end_date (id… |
| `guru_subscriptions_write_remove_coupon` | Mutações em assinaturas Guru. Ações: cancel (id, +data opcional); cancel_at_cycle_end (id); add_coupon (id + data); remove_coupon (id); set_current_offer (id + data); set_next_offer (id + data); set_cycle_end_date (id… |
| `guru_subscriptions_write_set_current_offer` | Mutações em assinaturas Guru. Ações: cancel (id, +data opcional); cancel_at_cycle_end (id); add_coupon (id + data); remove_coupon (id); set_current_offer (id + data); set_next_offer (id + data); set_cycle_end_date (id… |
| `guru_subscriptions_write_set_next_offer` | Mutações em assinaturas Guru. Ações: cancel (id, +data opcional); cancel_at_cycle_end (id); add_coupon (id + data); remove_coupon (id); set_current_offer (id + data); set_next_offer (id + data); set_cycle_end_date (id… |
| `guru_subscriptions_write_set_cycle_end_date` | Mutações em assinaturas Guru. Ações: cancel (id, +data opcional); cancel_at_cycle_end (id); add_coupon (id + data); remove_coupon (id); set_current_offer (id + data); set_next_offer (id + data); set_cycle_end_date (id… |
| `guru_subscriptions_write_set_trial_end_date` | Mutações em assinaturas Guru. Ações: cancel (id, +data opcional); cancel_at_cycle_end (id); add_coupon (id + data); remove_coupon (id); set_current_offer (id + data); set_next_offer (id + data); set_cycle_end_date (id… |
| `guru_subscriptions_write_set_installment` | Mutações em assinaturas Guru. Ações: cancel (id, +data opcional); cancel_at_cycle_end (id); add_coupon (id + data); remove_coupon (id); set_current_offer (id + data); set_next_offer (id + data); set_cycle_end_date (id… |
| `guru_subscriptions_write_change_plan` | Mutações em assinaturas Guru. Ações: cancel (id, +data opcional); cancel_at_cycle_end (id); add_coupon (id + data); remove_coupon (id); set_current_offer (id + data); set_next_offer (id + data); set_cycle_end_date (id… |
| `guru_subscriptions_write_simulate_plan` | Mutações em assinaturas Guru. Ações: cancel (id, +data opcional); cancel_at_cycle_end (id); add_coupon (id + data); remove_coupon (id); set_current_offer (id + data); set_next_offer (id + data); set_cycle_end_date (id… |
| `guru_subscriptions_write_set_payment_types` | Mutações em assinaturas Guru. Ações: cancel (id, +data opcional); cancel_at_cycle_end (id); add_coupon (id + data); remove_coupon (id); set_current_offer (id + data); set_next_offer (id + data); set_cycle_end_date (id… |
| `guru_subscriptions_write_set_increment_discount` | Mutações em assinaturas Guru. Ações: cancel (id, +data opcional); cancel_at_cycle_end (id); add_coupon (id + data); remove_coupon (id); set_current_offer (id + data); set_next_offer (id + data); set_cycle_end_date (id… |
| `guru_subscriptions_write_remove_increment_discount` | Mutações em assinaturas Guru. Ações: cancel (id, +data opcional); cancel_at_cycle_end (id); add_coupon (id + data); remove_coupon (id); set_current_offer (id + data); set_next_offer (id + data); set_cycle_end_date (id… |
| `guru_products_list` | Produtos e ofertas no Guru (leitura). |
| `guru_products_get` | Produtos e ofertas no Guru (leitura). |
| `guru_products_subscription_options` | Produtos e ofertas no Guru (leitura). |
| `guru_products_checkout_options` | Produtos e ofertas no Guru (leitura). |
| `guru_products_offers` | Produtos e ofertas no Guru (leitura). |
| `guru_products_offer` | Produtos e ofertas no Guru (leitura). |
| `guru_products_offer_subscription_options` | Produtos e ofertas no Guru (leitura). |
| `guru_products_offer_checkout_options` | Produtos e ofertas no Guru (leitura). |
| `guru_products_write_set_offer_availability` | Mutações em produtos Guru. Ação: set_offer_availability (product_id + offer_id + data com a disponibilidade). [Flattened action: set_offer_availability] Bulk support: accepts product_ids, offer_ids for batched execution. |
| `guru_contacts_search` | Contatos/clientes no Guru (leitura). |
| `guru_contacts_get` | Contatos/clientes no Guru (leitura). |
| `guru_contacts_transactions` | Contatos/clientes no Guru (leitura). |
| `guru_contacts_subscriptions` | Contatos/clientes no Guru (leitura). |
| `guru_contacts_affiliations` | Contatos/clientes no Guru (leitura). |
| `guru_contacts_etickets` | Contatos/clientes no Guru (leitura). |
| `guru_contacts_write_create` | Mutações em contatos Guru. Ações: create (data); update (id + data); anonymize (id, LGPD, irreversível); create_etickets (id + data). [Flattened action: create] Bulk support: accepts ids for batched execution. |
| `guru_contacts_write_update` | Mutações em contatos Guru. Ações: create (data); update (id + data); anonymize (id, LGPD, irreversível); create_etickets (id + data). [Flattened action: update] Bulk support: accepts ids for batched execution. |
| `guru_contacts_write_anonymize` | Mutações em contatos Guru. Ações: create (data); update (id + data); anonymize (id, LGPD, irreversível); create_etickets (id + data). [Flattened action: anonymize] Bulk support: accepts ids for batched execution. |
| `guru_contacts_write_create_etickets` | Mutações em contatos Guru. Ações: create (data); update (id + data); anonymize (id, LGPD, irreversível); create_etickets (id + data). [Flattened action: create_etickets] Bulk support: accepts ids for batched execution. |
| `guru_affiliations_list` | Afiliações no Guru (leitura). Ações: list (cursor); get (id); assets (id); transactions (id). [Flattened action: list] Bulk support: accepts ids for batched execution. |
| `guru_affiliations_get` | Afiliações no Guru (leitura). Ações: list (cursor); get (id); assets (id); transactions (id). [Flattened action: get] Bulk support: accepts ids for batched execution. |
| `guru_affiliations_assets` | Afiliações no Guru (leitura). Ações: list (cursor); get (id); assets (id); transactions (id). [Flattened action: assets] Bulk support: accepts ids for batched execution. |
| `guru_affiliations_transactions` | Afiliações no Guru (leitura). Ações: list (cursor); get (id); assets (id); transactions (id). [Flattened action: transactions] Bulk support: accepts ids for batched execution. |
| `guru_affiliations_write_set_commission` | Mutações em afiliações Guru. Ação: set_commission (id + data com a comissão). [Flattened action: set_commission] Bulk support: accepts ids for batched execution. |
| `guru_coupons_list` | Cupons no Guru (leitura). Ações: list (cursor); get (id); audits (id); transactions (id). [Flattened action: list] Bulk support: accepts ids for batched execution. |
| `guru_coupons_get` | Cupons no Guru (leitura). Ações: list (cursor); get (id); audits (id); transactions (id). [Flattened action: get] Bulk support: accepts ids for batched execution. |
| `guru_coupons_audits` | Cupons no Guru (leitura). Ações: list (cursor); get (id); audits (id); transactions (id). [Flattened action: audits] Bulk support: accepts ids for batched execution. |
| `guru_coupons_transactions` | Cupons no Guru (leitura). Ações: list (cursor); get (id); audits (id); transactions (id). [Flattened action: transactions] Bulk support: accepts ids for batched execution. |
| `guru_coupons_write_create` | Mutações em cupons Guru. Ações: create (data); update (id + data); delete (id); duplicate (id); set_activation (id + data, ativa/desativa). [Flattened action: create] Bulk support: accepts ids for batched execution. |
| `guru_coupons_write_update` | Mutações em cupons Guru. Ações: create (data); update (id + data); delete (id); duplicate (id); set_activation (id + data, ativa/desativa). [Flattened action: update] Bulk support: accepts ids for batched execution. |
| `guru_coupons_write_delete` | Mutações em cupons Guru. Ações: create (data); update (id + data); delete (id); duplicate (id); set_activation (id + data, ativa/desativa). [Flattened action: delete] Bulk support: accepts ids for batched execution. |
| `guru_coupons_write_duplicate` | Mutações em cupons Guru. Ações: create (data); update (id + data); delete (id); duplicate (id); set_activation (id + data, ativa/desativa). [Flattened action: duplicate] Bulk support: accepts ids for batched execution. |
| `guru_coupons_write_set_activation` | Mutações em cupons Guru. Ações: create (data); update (id + data); delete (id); duplicate (id); set_activation (id + data, ativa/desativa). [Flattened action: set_activation] Bulk support: accepts ids for batched exec… |
| `guru_etickets_list` | Ingressos (e-tickets) no Guru (leitura). |
| `guru_etickets_get` | Ingressos (e-tickets) no Guru (leitura). |
| `guru_etickets_check_in` | Ingressos (e-tickets) no Guru (leitura). |
| `guru_etickets_write_do_check_in` | Mutações em e-tickets Guru. Ações: do_check_in (code, valida entrada); delete_check_in (code); create_invitations (code + data); delete_invitations (code); delete (code). [Flattened action: do_check_in] |
| `guru_etickets_write_delete_check_in` | Mutações em e-tickets Guru. Ações: do_check_in (code, valida entrada); delete_check_in (code); create_invitations (code + data); delete_invitations (code); delete (code). [Flattened action: delete_check_in] |
| `guru_etickets_write_create_invitations` | Mutações em e-tickets Guru. Ações: do_check_in (code, valida entrada); delete_check_in (code); create_invitations (code + data); delete_invitations (code); delete (code). [Flattened action: create_invitations] |
| `guru_etickets_write_delete_invitations` | Mutações em e-tickets Guru. Ações: do_check_in (code, valida entrada); delete_check_in (code); create_invitations (code + data); delete_invitations (code); delete (code). [Flattened action: delete_invitations] |
| `guru_etickets_write_delete` | Mutações em e-tickets Guru. Ações: do_check_in (code, valida entrada); delete_check_in (code); create_invitations (code + data); delete_invitations (code); delete (code). [Flattened action: delete] |
| `guru_webhooks_list` | Webhooks configurados no Guru. |
| `guru_webhooks_get` | Webhooks configurados no Guru. |
| `guru_webhooks_activities` | Webhooks configurados no Guru. |
| `guru_leads` | Lista leads no Guru (cursor). |
| `guru_users_list` | Usuários/membros da conta Guru (leitura). |
| `guru_users_get` | Usuários/membros da conta Guru (leitura). |
| `guru_users_activities` | Usuários/membros da conta Guru (leitura). |
| `guru_users_write_delete` | Mutações em usuários Guru. Ação: delete (id, remove o usuário da conta). [Flattened action: delete] Bulk support: accepts ids for batched execution. |
| `guru_blocklists_list` | Listas de bloqueio (anti-fraude) no Guru. |
| `guru_blocklists_get` | Listas de bloqueio (anti-fraude) no Guru. |
| `guru_blocklists_write_create` | Mutações em listas de bloqueio Guru. |
| `guru_blocklists_write_update` | Mutações em listas de bloqueio Guru. |
| `guru_blocklists_write_delete` | Mutações em listas de bloqueio Guru. |
| `guru_account` | Valida um Account Token do Guru (usado pra verificar origem de webhook). |
| `guru_countries_list` | Dados auxiliares de localização do Guru. |
| `guru_countries_states` | Dados auxiliares de localização do Guru. |
| `guru_countries_address` | Dados auxiliares de localização do Guru. |
| `guru_checkout` | Consulta/configura settings de oferta no checkout do Guru (POST checkout/offers/settings). |
| `guru_myorders` | Gera link SSO da área de compras (MyOrders) de um comprador pelo email (POST myorders/auth/sso/:email). |

---

## Pricing

See [docs/precos.md](docs/precos.md) (PT-BR).

---

## License

MIT — see [LICENSE](LICENSE). The MCP server at `api.mcp.ai/p_guru` is proprietary (hosted); this repo (manifests, docs, skills) is MIT.
