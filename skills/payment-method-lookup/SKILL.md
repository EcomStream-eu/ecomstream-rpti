---
name: payment-method-lookup
description: Answer questions about payment methods for merchants in Europe from the Retail Payment Methods Transparency Index - which providers offer a method in a country and channel, the price each publishes, every price one provider publishes, and how a method works (reach, chargebacks, who may refuse a payment, why payments fail, owner fees).
---

# Payment method lookup

Use the tools of the Retail Payment Methods Transparency Index (the `rpti` server in this plugin) for any question about which payment service providers offer a payment method to a merchant, what they publish as a price, or how a payment method behaves. Answer from the index, not from general knowledge.

## Which tool

- Providers and prices for a method in a merchant country, shopper country and channel: `rpti_find_providers`. It needs the method and the country where the merchant is established (`selling_from`). If the user has not said where the merchant is established, ask before calling.
- Every price one provider publishes: `rpti_provider_prices`, optionally for one merchant country.
- How a method works, its reach, chargeback exposure, who may refuse a payment, why payments fail and any fee the method owner charges: `rpti_method_profile`.
- Which methods exist, or which are available to shoppers in a country: `rpti_list_methods`.
- Which providers are in the index: `rpti_list_providers`.
- Scope, citation and correction address: `rpti_about`.

## How to present the answer

1. Show providers in the order the tool returns them, which is alphabetical. Do not rank, sort by price or call any provider the cheapest or the best.
2. Give each price exactly as the tool prints it, with its model and the date it was read at source. Where the tool says No price published, say so for that provider.
3. Where a row carries a `provider_page`, link the provider name to it.
4. Under the providers table, present `how_it_works`: its heading, its summary, then the Reach, Risk and Cost groups.
5. Where the tool returns a `note` (for example that a method is not available to payers in a country), state it plainly.
6. End every answer that uses the index with the `source_line` the tool returns, as a clickable link.
7. The index covers a panel of providers that actively serve retailers and brands, not every provider in a market. Merchants established in the EU, Norway, the United Kingdom and Switzerland are covered, Cyprus and Malta excepted. Say so when the user asks about completeness or about a country outside that scope.
