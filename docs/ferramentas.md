# Ferramentas

Digital Manager Guru expõe 95 ferramentas.

### 1. `guru_list_accounts`
**Input**: `account` (opcional)

Lista contas Digital Manager Guru vinculadas a este install — id e apelido.

### 2. `guru_transactions_search`
**Input**: `id` (opcional), `marketplace_name` (opcional), `marketplace_id` (opcional), `sub` (opcional), `ordered_at_ini` (opcional), `ordered_at_end` (opcional), `confirmed_at_ini` (opcional), `confirmed_at_end` (opcional), `transaction_status` (opcional), `product_id` (opcional), `subscription_id` (opcional), `contact_email` (opcional), `contact_doc` (opcional), `contact_name` (opcional), `cursor` (opcional), `account` (opcional), `ids` (opcional), `marketplace_ids` (opcional), `product_ids` (opcional), `subscription_ids` (opcional)

Vendas/transações no Guru (leitura).

### 3. `guru_transactions_get`
**Input**: `id` (opcional), `marketplace_name` (opcional), `marketplace_id` (opcional), `sub` (opcional), `ordered_at_ini` (opcional), `ordered_at_end` (opcional), `confirmed_at_ini` (opcional), `confirmed_at_end` (opcional), `transaction_status` (opcional), `product_id` (opcional), `subscription_id` (opcional), `contact_email` (opcional), `contact_doc` (opcional), `contact_name` (opcional), `cursor` (opcional), `account` (opcional), `ids` (opcional), `marketplace_ids` (opcional), `product_ids` (opcional), `subscription_ids` (opcional)

Vendas/transações no Guru (leitura).

### 4. `guru_transactions_activities`
**Input**: `id` (opcional), `marketplace_name` (opcional), `marketplace_id` (opcional), `sub` (opcional), `ordered_at_ini` (opcional), `ordered_at_end` (opcional), `confirmed_at_ini` (opcional), `confirmed_at_end` (opcional), `transaction_status` (opcional), `product_id` (opcional), `subscription_id` (opcional), `contact_email` (opcional), `contact_doc` (opcional), `contact_name` (opcional), `cursor` (opcional), `account` (opcional), `ids` (opcional), `marketplace_ids` (opcional), `product_ids` (opcional), `subscription_ids` (opcional)

Vendas/transações no Guru (leitura).

### 5. `guru_transactions_order_bumps`
**Input**: `id` (opcional), `marketplace_name` (opcional), `marketplace_id` (opcional), `sub` (opcional), `ordered_at_ini` (opcional), `ordered_at_end` (opcional), `confirmed_at_ini` (opcional), `confirmed_at_end` (opcional), `transaction_status` (opcional), `product_id` (opcional), `subscription_id` (opcional), `contact_email` (opcional), `contact_doc` (opcional), `contact_name` (opcional), `cursor` (opcional), `account` (opcional), `ids` (opcional), `marketplace_ids` (opcional), `product_ids` (opcional), `subscription_ids` (opcional)

Vendas/transações no Guru (leitura).

### 6. `guru_transactions_etickets`
**Input**: `id` (opcional), `marketplace_name` (opcional), `marketplace_id` (opcional), `sub` (opcional), `ordered_at_ini` (opcional), `ordered_at_end` (opcional), `confirmed_at_ini` (opcional), `confirmed_at_end` (opcional), `transaction_status` (opcional), `product_id` (opcional), `subscription_id` (opcional), `contact_email` (opcional), `contact_doc` (opcional), `contact_name` (opcional), `cursor` (opcional), `account` (opcional), `ids` (opcional), `marketplace_ids` (opcional), `product_ids` (opcional), `subscription_ids` (opcional)

Vendas/transações no Guru (leitura).

### 7. `guru_transactions_by_marketplace`
**Input**: `id` (opcional), `marketplace_name` (opcional), `marketplace_id` (opcional), `sub` (opcional), `ordered_at_ini` (opcional), `ordered_at_end` (opcional), `confirmed_at_ini` (opcional), `confirmed_at_end` (opcional), `transaction_status` (opcional), `product_id` (opcional), `subscription_id` (opcional), `contact_email` (opcional), `contact_doc` (opcional), `contact_name` (opcional), `cursor` (opcional), `account` (opcional), `ids` (opcional), `marketplace_ids` (opcional), `product_ids` (opcional), `subscription_ids` (opcional)

Vendas/transações no Guru (leitura).

### 8. `guru_transactions_write_refund`
**Input**: `id`, `data` (opcional), `account` (opcional), `ids` (opcional)

Mutações em transações Guru (mexe em dinheiro, irreversível).

### 9. `guru_transactions_write_chargeback`
**Input**: `id`, `data` (opcional), `account` (opcional), `ids` (opcional)

Mutações em transações Guru (mexe em dinheiro, irreversível).

### 10. `guru_transactions_write_reissue`
**Input**: `id`, `data` (opcional), `account` (opcional), `ids` (opcional)

Mutações em transações Guru (mexe em dinheiro, irreversível).

### 11. `guru_transactions_write_update_buyer`
**Input**: `id`, `data` (opcional), `account` (opcional), `ids` (opcional)

Mutações em transações Guru (mexe em dinheiro, irreversível).

### 12. `guru_transactions_write_generate_invoice`
**Input**: `id`, `data` (opcional), `account` (opcional), `ids` (opcional)

Mutações em transações Guru (mexe em dinheiro, irreversível).

### 13. `guru_subscriptions_search`
**Input**: `id` (opcional), `invoice_code` (opcional), `subscription_status` (opcional), `product_id` (opcional), `contact_email` (opcional), `contact_doc` (opcional), `contact_name` (opcional), `started_at_ini` (opcional), `started_at_end` (opcional), `last_status_at_ini` (opcional), `last_status_at_end` (opcional), `cursor` (opcional), `account` (opcional), `ids` (opcional), `product_ids` (opcional)

Assinaturas no Guru (leitura).

### 14. `guru_subscriptions_get`
**Input**: `id` (opcional), `invoice_code` (opcional), `subscription_status` (opcional), `product_id` (opcional), `contact_email` (opcional), `contact_doc` (opcional), `contact_name` (opcional), `started_at_ini` (opcional), `started_at_end` (opcional), `last_status_at_ini` (opcional), `last_status_at_end` (opcional), `cursor` (opcional), `account` (opcional), `ids` (opcional), `product_ids` (opcional)

Assinaturas no Guru (leitura).

### 15. `guru_subscriptions_activities`
**Input**: `id` (opcional), `invoice_code` (opcional), `subscription_status` (opcional), `product_id` (opcional), `contact_email` (opcional), `contact_doc` (opcional), `contact_name` (opcional), `started_at_ini` (opcional), `started_at_end` (opcional), `last_status_at_ini` (opcional), `last_status_at_end` (opcional), `cursor` (opcional), `account` (opcional), `ids` (opcional), `product_ids` (opcional)

Assinaturas no Guru (leitura).

### 16. `guru_subscriptions_invoices`
**Input**: `id` (opcional), `invoice_code` (opcional), `subscription_status` (opcional), `product_id` (opcional), `contact_email` (opcional), `contact_doc` (opcional), `contact_name` (opcional), `started_at_ini` (opcional), `started_at_end` (opcional), `last_status_at_ini` (opcional), `last_status_at_end` (opcional), `cursor` (opcional), `account` (opcional), `ids` (opcional), `product_ids` (opcional)

Assinaturas no Guru (leitura).

### 17. `guru_subscriptions_invoice`
**Input**: `id` (opcional), `invoice_code` (opcional), `subscription_status` (opcional), `product_id` (opcional), `contact_email` (opcional), `contact_doc` (opcional), `contact_name` (opcional), `started_at_ini` (opcional), `started_at_end` (opcional), `last_status_at_ini` (opcional), `last_status_at_end` (opcional), `cursor` (opcional), `account` (opcional), `ids` (opcional), `product_ids` (opcional)

Assinaturas no Guru (leitura).

### 18. `guru_subscriptions_invoice_transactions`
**Input**: `id` (opcional), `invoice_code` (opcional), `subscription_status` (opcional), `product_id` (opcional), `contact_email` (opcional), `contact_doc` (opcional), `contact_name` (opcional), `started_at_ini` (opcional), `started_at_end` (opcional), `last_status_at_ini` (opcional), `last_status_at_end` (opcional), `cursor` (opcional), `account` (opcional), `ids` (opcional), `product_ids` (opcional)

Assinaturas no Guru (leitura).

### 19. `guru_subscriptions_transactions`
**Input**: `id` (opcional), `invoice_code` (opcional), `subscription_status` (opcional), `product_id` (opcional), `contact_email` (opcional), `contact_doc` (opcional), `contact_name` (opcional), `started_at_ini` (opcional), `started_at_end` (opcional), `last_status_at_ini` (opcional), `last_status_at_end` (opcional), `cursor` (opcional), `account` (opcional), `ids` (opcional), `product_ids` (opcional)

Assinaturas no Guru (leitura).

### 20. `guru_subscriptions_payment_types`
**Input**: `id` (opcional), `invoice_code` (opcional), `subscription_status` (opcional), `product_id` (opcional), `contact_email` (opcional), `contact_doc` (opcional), `contact_name` (opcional), `started_at_ini` (opcional), `started_at_end` (opcional), `last_status_at_ini` (opcional), `last_status_at_end` (opcional), `cursor` (opcional), `account` (opcional), `ids` (opcional), `product_ids` (opcional)

Assinaturas no Guru (leitura).

### 21. `guru_subscriptions_plans_available`
**Input**: `id` (opcional), `invoice_code` (opcional), `subscription_status` (opcional), `product_id` (opcional), `contact_email` (opcional), `contact_doc` (opcional), `contact_name` (opcional), `started_at_ini` (opcional), `started_at_end` (opcional), `last_status_at_ini` (opcional), `last_status_at_end` (opcional), `cursor` (opcional), `account` (opcional), `ids` (opcional), `product_ids` (opcional)

Assinaturas no Guru (leitura).

### 22. `guru_subscriptions_write_cancel`
**Input**: `id`, `data` (opcional), `account` (opcional), `ids` (opcional)

Mutações em assinaturas Guru. Ações: cancel (id, +data opcional); cancel_at_cycle_end (id); add_coupon (id + data); remove_coupon (id); set_current_offer (id + data); set_next_offer (id + data); set_cycle_end_date (id…

### 23. `guru_subscriptions_write_cancel_at_cycle_end`
**Input**: `id`, `data` (opcional), `account` (opcional), `ids` (opcional)

Mutações em assinaturas Guru. Ações: cancel (id, +data opcional); cancel_at_cycle_end (id); add_coupon (id + data); remove_coupon (id); set_current_offer (id + data); set_next_offer (id + data); set_cycle_end_date (id…

### 24. `guru_subscriptions_write_add_coupon`
**Input**: `id`, `data` (opcional), `account` (opcional), `ids` (opcional)

Mutações em assinaturas Guru. Ações: cancel (id, +data opcional); cancel_at_cycle_end (id); add_coupon (id + data); remove_coupon (id); set_current_offer (id + data); set_next_offer (id + data); set_cycle_end_date (id…

### 25. `guru_subscriptions_write_remove_coupon`
**Input**: `id`, `data` (opcional), `account` (opcional), `ids` (opcional)

Mutações em assinaturas Guru. Ações: cancel (id, +data opcional); cancel_at_cycle_end (id); add_coupon (id + data); remove_coupon (id); set_current_offer (id + data); set_next_offer (id + data); set_cycle_end_date (id…

### 26. `guru_subscriptions_write_set_current_offer`
**Input**: `id`, `data` (opcional), `account` (opcional), `ids` (opcional)

Mutações em assinaturas Guru. Ações: cancel (id, +data opcional); cancel_at_cycle_end (id); add_coupon (id + data); remove_coupon (id); set_current_offer (id + data); set_next_offer (id + data); set_cycle_end_date (id…

### 27. `guru_subscriptions_write_set_next_offer`
**Input**: `id`, `data` (opcional), `account` (opcional), `ids` (opcional)

Mutações em assinaturas Guru. Ações: cancel (id, +data opcional); cancel_at_cycle_end (id); add_coupon (id + data); remove_coupon (id); set_current_offer (id + data); set_next_offer (id + data); set_cycle_end_date (id…

### 28. `guru_subscriptions_write_set_cycle_end_date`
**Input**: `id`, `data` (opcional), `account` (opcional), `ids` (opcional)

Mutações em assinaturas Guru. Ações: cancel (id, +data opcional); cancel_at_cycle_end (id); add_coupon (id + data); remove_coupon (id); set_current_offer (id + data); set_next_offer (id + data); set_cycle_end_date (id…

### 29. `guru_subscriptions_write_set_trial_end_date`
**Input**: `id`, `data` (opcional), `account` (opcional), `ids` (opcional)

Mutações em assinaturas Guru. Ações: cancel (id, +data opcional); cancel_at_cycle_end (id); add_coupon (id + data); remove_coupon (id); set_current_offer (id + data); set_next_offer (id + data); set_cycle_end_date (id…

### 30. `guru_subscriptions_write_set_installment`
**Input**: `id`, `data` (opcional), `account` (opcional), `ids` (opcional)

Mutações em assinaturas Guru. Ações: cancel (id, +data opcional); cancel_at_cycle_end (id); add_coupon (id + data); remove_coupon (id); set_current_offer (id + data); set_next_offer (id + data); set_cycle_end_date (id…

### 31. `guru_subscriptions_write_change_plan`
**Input**: `id`, `data` (opcional), `account` (opcional), `ids` (opcional)

Mutações em assinaturas Guru. Ações: cancel (id, +data opcional); cancel_at_cycle_end (id); add_coupon (id + data); remove_coupon (id); set_current_offer (id + data); set_next_offer (id + data); set_cycle_end_date (id…

### 32. `guru_subscriptions_write_simulate_plan`
**Input**: `id`, `data` (opcional), `account` (opcional), `ids` (opcional)

Mutações em assinaturas Guru. Ações: cancel (id, +data opcional); cancel_at_cycle_end (id); add_coupon (id + data); remove_coupon (id); set_current_offer (id + data); set_next_offer (id + data); set_cycle_end_date (id…

### 33. `guru_subscriptions_write_set_payment_types`
**Input**: `id`, `data` (opcional), `account` (opcional), `ids` (opcional)

Mutações em assinaturas Guru. Ações: cancel (id, +data opcional); cancel_at_cycle_end (id); add_coupon (id + data); remove_coupon (id); set_current_offer (id + data); set_next_offer (id + data); set_cycle_end_date (id…

### 34. `guru_subscriptions_write_set_increment_discount`
**Input**: `id`, `data` (opcional), `account` (opcional), `ids` (opcional)

Mutações em assinaturas Guru. Ações: cancel (id, +data opcional); cancel_at_cycle_end (id); add_coupon (id + data); remove_coupon (id); set_current_offer (id + data); set_next_offer (id + data); set_cycle_end_date (id…

### 35. `guru_subscriptions_write_remove_increment_discount`
**Input**: `id`, `data` (opcional), `account` (opcional), `ids` (opcional)

Mutações em assinaturas Guru. Ações: cancel (id, +data opcional); cancel_at_cycle_end (id); add_coupon (id + data); remove_coupon (id); set_current_offer (id + data); set_next_offer (id + data); set_cycle_end_date (id…

### 36. `guru_products_list`
**Input**: `product_id` (opcional), `offer_id` (opcional), `section` (opcional), `name` (opcional), `type` (opcional), `marketplace_id` (opcional), `is_hidden` (opcional), `cursor` (opcional), `account` (opcional), `product_ids` (opcional), `offer_ids` (opcional), `marketplace_ids` (opcional)

Produtos e ofertas no Guru (leitura).

### 37. `guru_products_get`
**Input**: `product_id` (opcional), `offer_id` (opcional), `section` (opcional), `name` (opcional), `type` (opcional), `marketplace_id` (opcional), `is_hidden` (opcional), `cursor` (opcional), `account` (opcional), `product_ids` (opcional), `offer_ids` (opcional), `marketplace_ids` (opcional)

Produtos e ofertas no Guru (leitura).

### 38. `guru_products_subscription_options`
**Input**: `product_id` (opcional), `offer_id` (opcional), `section` (opcional), `name` (opcional), `type` (opcional), `marketplace_id` (opcional), `is_hidden` (opcional), `cursor` (opcional), `account` (opcional), `product_ids` (opcional), `offer_ids` (opcional), `marketplace_ids` (opcional)

Produtos e ofertas no Guru (leitura).

### 39. `guru_products_checkout_options`
**Input**: `product_id` (opcional), `offer_id` (opcional), `section` (opcional), `name` (opcional), `type` (opcional), `marketplace_id` (opcional), `is_hidden` (opcional), `cursor` (opcional), `account` (opcional), `product_ids` (opcional), `offer_ids` (opcional), `marketplace_ids` (opcional)

Produtos e ofertas no Guru (leitura).

### 40. `guru_products_offers`
**Input**: `product_id` (opcional), `offer_id` (opcional), `section` (opcional), `name` (opcional), `type` (opcional), `marketplace_id` (opcional), `is_hidden` (opcional), `cursor` (opcional), `account` (opcional), `product_ids` (opcional), `offer_ids` (opcional), `marketplace_ids` (opcional)

Produtos e ofertas no Guru (leitura).

### 41. `guru_products_offer`
**Input**: `product_id` (opcional), `offer_id` (opcional), `section` (opcional), `name` (opcional), `type` (opcional), `marketplace_id` (opcional), `is_hidden` (opcional), `cursor` (opcional), `account` (opcional), `product_ids` (opcional), `offer_ids` (opcional), `marketplace_ids` (opcional)

Produtos e ofertas no Guru (leitura).

### 42. `guru_products_offer_subscription_options`
**Input**: `product_id` (opcional), `offer_id` (opcional), `section` (opcional), `name` (opcional), `type` (opcional), `marketplace_id` (opcional), `is_hidden` (opcional), `cursor` (opcional), `account` (opcional), `product_ids` (opcional), `offer_ids` (opcional), `marketplace_ids` (opcional)

Produtos e ofertas no Guru (leitura).

### 43. `guru_products_offer_checkout_options`
**Input**: `product_id` (opcional), `offer_id` (opcional), `section` (opcional), `name` (opcional), `type` (opcional), `marketplace_id` (opcional), `is_hidden` (opcional), `cursor` (opcional), `account` (opcional), `product_ids` (opcional), `offer_ids` (opcional), `marketplace_ids` (opcional)

Produtos e ofertas no Guru (leitura).

### 44. `guru_products_write_set_offer_availability`
**Input**: `product_id`, `offer_id`, `data` (opcional), `account` (opcional), `product_ids` (opcional), `offer_ids` (opcional)

Mutações em produtos Guru. Ação: set_offer_availability (product_id + offer_id + data com a disponibilidade). [Flattened action: set_offer_availability] Bulk support: accepts product_ids, offer_ids for batched execution.

### 45. `guru_contacts_search`
**Input**: `id` (opcional), `email` (opcional), `doc` (opcional), `name` (opcional), `created_at_ini` (opcional), `created_at_end` (opcional), `cursor` (opcional), `account` (opcional), `ids` (opcional)

Contatos/clientes no Guru (leitura).

### 46. `guru_contacts_get`
**Input**: `id` (opcional), `email` (opcional), `doc` (opcional), `name` (opcional), `created_at_ini` (opcional), `created_at_end` (opcional), `cursor` (opcional), `account` (opcional), `ids` (opcional)

Contatos/clientes no Guru (leitura).

### 47. `guru_contacts_transactions`
**Input**: `id` (opcional), `email` (opcional), `doc` (opcional), `name` (opcional), `created_at_ini` (opcional), `created_at_end` (opcional), `cursor` (opcional), `account` (opcional), `ids` (opcional)

Contatos/clientes no Guru (leitura).

### 48. `guru_contacts_subscriptions`
**Input**: `id` (opcional), `email` (opcional), `doc` (opcional), `name` (opcional), `created_at_ini` (opcional), `created_at_end` (opcional), `cursor` (opcional), `account` (opcional), `ids` (opcional)

Contatos/clientes no Guru (leitura).

### 49. `guru_contacts_affiliations`
**Input**: `id` (opcional), `email` (opcional), `doc` (opcional), `name` (opcional), `created_at_ini` (opcional), `created_at_end` (opcional), `cursor` (opcional), `account` (opcional), `ids` (opcional)

Contatos/clientes no Guru (leitura).

### 50. `guru_contacts_etickets`
**Input**: `id` (opcional), `email` (opcional), `doc` (opcional), `name` (opcional), `created_at_ini` (opcional), `created_at_end` (opcional), `cursor` (opcional), `account` (opcional), `ids` (opcional)

Contatos/clientes no Guru (leitura).

### 51. `guru_contacts_write_create`
**Input**: `id` (opcional), `data` (opcional), `account` (opcional), `ids` (opcional)

Mutações em contatos Guru. Ações: create (data); update (id + data); anonymize (id, LGPD, irreversível); create_etickets (id + data). [Flattened action: create] Bulk support: accepts ids for batched execution.

### 52. `guru_contacts_write_update`
**Input**: `id` (opcional), `data` (opcional), `account` (opcional), `ids` (opcional)

Mutações em contatos Guru. Ações: create (data); update (id + data); anonymize (id, LGPD, irreversível); create_etickets (id + data). [Flattened action: update] Bulk support: accepts ids for batched execution.

### 53. `guru_contacts_write_anonymize`
**Input**: `id` (opcional), `data` (opcional), `account` (opcional), `ids` (opcional)

Mutações em contatos Guru. Ações: create (data); update (id + data); anonymize (id, LGPD, irreversível); create_etickets (id + data). [Flattened action: anonymize] Bulk support: accepts ids for batched execution.

### 54. `guru_contacts_write_create_etickets`
**Input**: `id` (opcional), `data` (opcional), `account` (opcional), `ids` (opcional)

Mutações em contatos Guru. Ações: create (data); update (id + data); anonymize (id, LGPD, irreversível); create_etickets (id + data). [Flattened action: create_etickets] Bulk support: accepts ids for batched execution.

### 55. `guru_affiliations_list`
**Input**: `id` (opcional), `cursor` (opcional), `account` (opcional), `ids` (opcional)

Afiliações no Guru (leitura). Ações: list (cursor); get (id); assets (id); transactions (id). [Flattened action: list] Bulk support: accepts ids for batched execution.

### 56. `guru_affiliations_get`
**Input**: `id` (opcional), `cursor` (opcional), `account` (opcional), `ids` (opcional)

Afiliações no Guru (leitura). Ações: list (cursor); get (id); assets (id); transactions (id). [Flattened action: get] Bulk support: accepts ids for batched execution.

### 57. `guru_affiliations_assets`
**Input**: `id` (opcional), `cursor` (opcional), `account` (opcional), `ids` (opcional)

Afiliações no Guru (leitura). Ações: list (cursor); get (id); assets (id); transactions (id). [Flattened action: assets] Bulk support: accepts ids for batched execution.

### 58. `guru_affiliations_transactions`
**Input**: `id` (opcional), `cursor` (opcional), `account` (opcional), `ids` (opcional)

Afiliações no Guru (leitura). Ações: list (cursor); get (id); assets (id); transactions (id). [Flattened action: transactions] Bulk support: accepts ids for batched execution.

### 59. `guru_affiliations_write_set_commission`
**Input**: `id`, `data` (opcional), `account` (opcional), `ids` (opcional)

Mutações em afiliações Guru. Ação: set_commission (id + data com a comissão). [Flattened action: set_commission] Bulk support: accepts ids for batched execution.

### 60. `guru_coupons_list`
**Input**: `id` (opcional), `cursor` (opcional), `account` (opcional), `ids` (opcional)

Cupons no Guru (leitura). Ações: list (cursor); get (id); audits (id); transactions (id). [Flattened action: list] Bulk support: accepts ids for batched execution.

### 61. `guru_coupons_get`
**Input**: `id` (opcional), `cursor` (opcional), `account` (opcional), `ids` (opcional)

Cupons no Guru (leitura). Ações: list (cursor); get (id); audits (id); transactions (id). [Flattened action: get] Bulk support: accepts ids for batched execution.

### 62. `guru_coupons_audits`
**Input**: `id` (opcional), `cursor` (opcional), `account` (opcional), `ids` (opcional)

Cupons no Guru (leitura). Ações: list (cursor); get (id); audits (id); transactions (id). [Flattened action: audits] Bulk support: accepts ids for batched execution.

### 63. `guru_coupons_transactions`
**Input**: `id` (opcional), `cursor` (opcional), `account` (opcional), `ids` (opcional)

Cupons no Guru (leitura). Ações: list (cursor); get (id); audits (id); transactions (id). [Flattened action: transactions] Bulk support: accepts ids for batched execution.

### 64. `guru_coupons_write_create`
**Input**: `id` (opcional), `data` (opcional), `account` (opcional), `ids` (opcional)

Mutações em cupons Guru. Ações: create (data); update (id + data); delete (id); duplicate (id); set_activation (id + data, ativa/desativa). [Flattened action: create] Bulk support: accepts ids for batched execution.

### 65. `guru_coupons_write_update`
**Input**: `id` (opcional), `data` (opcional), `account` (opcional), `ids` (opcional)

Mutações em cupons Guru. Ações: create (data); update (id + data); delete (id); duplicate (id); set_activation (id + data, ativa/desativa). [Flattened action: update] Bulk support: accepts ids for batched execution.

### 66. `guru_coupons_write_delete`
**Input**: `id` (opcional), `data` (opcional), `account` (opcional), `ids` (opcional)

Mutações em cupons Guru. Ações: create (data); update (id + data); delete (id); duplicate (id); set_activation (id + data, ativa/desativa). [Flattened action: delete] Bulk support: accepts ids for batched execution.

### 67. `guru_coupons_write_duplicate`
**Input**: `id` (opcional), `data` (opcional), `account` (opcional), `ids` (opcional)

Mutações em cupons Guru. Ações: create (data); update (id + data); delete (id); duplicate (id); set_activation (id + data, ativa/desativa). [Flattened action: duplicate] Bulk support: accepts ids for batched execution.

### 68. `guru_coupons_write_set_activation`
**Input**: `id` (opcional), `data` (opcional), `account` (opcional), `ids` (opcional)

Mutações em cupons Guru. Ações: create (data); update (id + data); delete (id); duplicate (id); set_activation (id + data, ativa/desativa). [Flattened action: set_activation] Bulk support: accepts ids for batched exec…

### 69. `guru_etickets_list`
**Input**: `code` (opcional), `cursor` (opcional), `account` (opcional)

Ingressos (e-tickets) no Guru (leitura).

### 70. `guru_etickets_get`
**Input**: `code` (opcional), `cursor` (opcional), `account` (opcional)

Ingressos (e-tickets) no Guru (leitura).

### 71. `guru_etickets_check_in`
**Input**: `code` (opcional), `cursor` (opcional), `account` (opcional)

Ingressos (e-tickets) no Guru (leitura).

### 72. `guru_etickets_write_do_check_in`
**Input**: `code`, `data` (opcional), `account` (opcional)

Mutações em e-tickets Guru. Ações: do_check_in (code, valida entrada); delete_check_in (code); create_invitations (code + data); delete_invitations (code); delete (code). [Flattened action: do_check_in]

### 73. `guru_etickets_write_delete_check_in`
**Input**: `code`, `data` (opcional), `account` (opcional)

Mutações em e-tickets Guru. Ações: do_check_in (code, valida entrada); delete_check_in (code); create_invitations (code + data); delete_invitations (code); delete (code). [Flattened action: delete_check_in]

### 74. `guru_etickets_write_create_invitations`
**Input**: `code`, `data` (opcional), `account` (opcional)

Mutações em e-tickets Guru. Ações: do_check_in (code, valida entrada); delete_check_in (code); create_invitations (code + data); delete_invitations (code); delete (code). [Flattened action: create_invitations]

### 75. `guru_etickets_write_delete_invitations`
**Input**: `code`, `data` (opcional), `account` (opcional)

Mutações em e-tickets Guru. Ações: do_check_in (code, valida entrada); delete_check_in (code); create_invitations (code + data); delete_invitations (code); delete (code). [Flattened action: delete_invitations]

### 76. `guru_etickets_write_delete`
**Input**: `code`, `data` (opcional), `account` (opcional)

Mutações em e-tickets Guru. Ações: do_check_in (code, valida entrada); delete_check_in (code); create_invitations (code + data); delete_invitations (code); delete (code). [Flattened action: delete]

### 77. `guru_webhooks_list`
**Input**: `id` (opcional), `cursor` (opcional), `account` (opcional), `ids` (opcional)

Webhooks configurados no Guru.

### 78. `guru_webhooks_get`
**Input**: `id` (opcional), `cursor` (opcional), `account` (opcional), `ids` (opcional)

Webhooks configurados no Guru.

### 79. `guru_webhooks_activities`
**Input**: `id` (opcional), `cursor` (opcional), `account` (opcional), `ids` (opcional)

Webhooks configurados no Guru.

### 80. `guru_leads`
**Input**: `cursor` (opcional), `account` (opcional)

Lista leads no Guru (cursor).

### 81. `guru_users_list`
**Input**: `id` (opcional), `cursor` (opcional), `account` (opcional), `ids` (opcional)

Usuários/membros da conta Guru (leitura).

### 82. `guru_users_get`
**Input**: `id` (opcional), `cursor` (opcional), `account` (opcional), `ids` (opcional)

Usuários/membros da conta Guru (leitura).

### 83. `guru_users_activities`
**Input**: `id` (opcional), `cursor` (opcional), `account` (opcional), `ids` (opcional)

Usuários/membros da conta Guru (leitura).

### 84. `guru_users_write_delete`
**Input**: `id`, `account` (opcional), `ids` (opcional)

Mutações em usuários Guru. Ação: delete (id, remove o usuário da conta). [Flattened action: delete] Bulk support: accepts ids for batched execution.

### 85. `guru_blocklists_list`
**Input**: `id` (opcional), `cursor` (opcional), `account` (opcional), `ids` (opcional)

Listas de bloqueio (anti-fraude) no Guru.

### 86. `guru_blocklists_get`
**Input**: `id` (opcional), `cursor` (opcional), `account` (opcional), `ids` (opcional)

Listas de bloqueio (anti-fraude) no Guru.

### 87. `guru_blocklists_write_create`
**Input**: `id` (opcional), `data` (opcional), `account` (opcional), `ids` (opcional)

Mutações em listas de bloqueio Guru.

### 88. `guru_blocklists_write_update`
**Input**: `id` (opcional), `data` (opcional), `account` (opcional), `ids` (opcional)

Mutações em listas de bloqueio Guru.

### 89. `guru_blocklists_write_delete`
**Input**: `id` (opcional), `data` (opcional), `account` (opcional), `ids` (opcional)

Mutações em listas de bloqueio Guru.

### 90. `guru_account`
**Input**: `account_token`, `account` (opcional)

Valida um Account Token do Guru (usado pra verificar origem de webhook).

### 91. `guru_countries_list`
**Input**: `country` (opcional), `zipcode` (opcional), `account` (opcional)

Dados auxiliares de localização do Guru.

### 92. `guru_countries_states`
**Input**: `country` (opcional), `zipcode` (opcional), `account` (opcional)

Dados auxiliares de localização do Guru.

### 93. `guru_countries_address`
**Input**: `country` (opcional), `zipcode` (opcional), `account` (opcional)

Dados auxiliares de localização do Guru.

### 94. `guru_checkout`
**Input**: `data` (opcional), `account` (opcional)

Consulta/configura settings de oferta no checkout do Guru (POST checkout/offers/settings).

### 95. `guru_myorders`
**Input**: `email`, `data` (opcional), `account` (opcional)

Gera link SSO da área de compras (MyOrders) de um comprador pelo email (POST myorders/auth/sso/:email).

## Prompts de exemplo

```
Quais vendas aprovadas tive no Guru nos últimos 7 dias?
Liste minhas assinaturas ativas
Mostre as transações do contato com email X
```
