# Retail Payment Methods Transparency Index for Claude

This plugin connects Claude to the [Retail Payment Methods Transparency Index](https://www.ecomstream.eu/payment-methods-transparency-index/), published by EcomStream. It answers which payment service providers offer a payment method to a merchant established in a European country, selling to shoppers in a given country online, in-store or both, and the price each provider publishes for it, as printed at source, with the pricing model and the date it was read. It also describes how a payment method works: where shoppers pay with it, chargeback exposure, who may refuse a payment, why a payment can fail, and any fee the method owner charges directly.

Merchants established in the EU, Norway, the United Kingdom and Switzerland are covered, Cyprus and Malta excepted. The index covers a panel of providers that actively serve retailers and brands, not every provider in a market. Providers are always listed alphabetically.

## What the plugin contains

- `.mcp.json`: one remote MCP server, `rpti`, at `https://www.ecomstream.eu/wp-json/ecomstream-mcp/v1/mcp`. Read-only, no account and no authentication.
- `skills/payment-method-lookup/SKILL.md`: instructions for Claude on which tool to use and how to present prices, the method profile and the source line.

The plugin runs no local code, installs no packages and uses no hooks.

## What is sent where

Every tool call goes to the server above on ecomstream.eu and carries only the payment method, provider, countries and channel asked about, never the conversation or any document. EcomStream keeps a daily count per type of query with those details and nothing else, deleted after 90 days. To limit excessive use, the client address is held in hashed form for up to two minutes and then deleted. See the [privacy policy](https://www.ecomstream.eu/privacy-policy/) and the [connector documentation](https://www.ecomstream.eu/payment-methods-transparency-index/connector/).

## Example questions

- Which providers offer iDEAL to a merchant in the Netherlands selling online, and what price does each publish?
- What does Stripe publish for merchants in Germany?
- Who can refuse a Bancontact payment, and can a shopper reverse it?

## Citation and licence

Answers carry the citation line: EcomStream, Retail Payment Methods Transparency Index, ecomstream.eu/payment-methods-transparency-index. The index data is published under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/). The plugin files are under the MIT licence.

## Support and corrections

index@ecomstream.nl. A provider that believes a row is wrong can write to that address; every reported correction is checked at the source.
