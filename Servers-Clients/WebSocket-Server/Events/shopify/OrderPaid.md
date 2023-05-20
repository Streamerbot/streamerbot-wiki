---
title: OrderPaid
description: Websocket Events Reference - shopify
published: true
date: 2023-02-12T03:23:35.752Z
tags: 
editor: markdown
dateCreated: 2023-02-12T03:23:33.909Z
---

```json
{
  "created_at": "2022-11-15T00:23:09+01:00",
  "event": "orders/paid",
  "id": 820982911946154500,
  "email": "jon@doe.ca",
  "closed_at": null,
  "updated_at": "2022-11-15T00:23:09+01:00",
  "number": 234,
  "note": null,
  "total_price": "254.98",
  "subtotal_price": "244.98",
  "currency": "EUR",
  "financial_status": "voided",
  "confirmed": false,
  "total_discounts": "5.00",
  "total_line_items_price": "249.98",
  "buyer_accepts_marketing": true,
  "name": "#9999",
  "referring_site": null,
  "landing_site": null,
  "total_price_usd": null,
  "order_number": 1234,
  "line_items": [
    {
      "id": 487817672276298560,
      "variant_id": null,
      "title": "Aviator sunglasses",
      "quantity": 1,
      "sku": "SKU2006-001",
      "variant_title": null,
      "vendor": null,
      "fulfillment_service": "manual",
      "product_id": 788032119674292900,
      "requires_shipping": true,
      "taxable": true,
      "gift_card": false,
      "name": "Aviator sunglasses",
      "variant_inventory_management": null,
      "properties": [],
      "product_exists": true,
      "fulfillable_quantity": 1,
      "grams": 100,
      "price": "89.99",
      "total_discount": "0.00",
      "fulfillment_status": null,
      "price_set": {
        "shop_money": {
          "amount": "89.99",
          "currency_code": "EUR"
        },
        "presentment_money": {
          "amount": "89.99",
          "currency_code": "EUR"
        }
      },
      "total_discount_set": {
        "shop_money": {
          "amount": "0.00",
          "currency_code": "EUR"
        },
        "presentment_money": {
          "amount": "0.00",
          "currency_code": "EUR"
        }
      },
      "discount_allocations": [],
      "duties": [],
      "admin_graphql_api_id": "gid://shopify/LineItem/487817672276298554",
      "tax_lines": []
    },
    {
      "id": 976318377106520300,
      "variant_id": null,
      "title": "Mid-century lounger",
      "quantity": 1,
      "sku": "SKU2006-020",
      "variant_title": null,
      "vendor": null,
      "fulfillment_service": "manual",
      "product_id": 788032119674292900,
      "requires_shipping": true,
      "taxable": true,
      "gift_card": false,
      "name": "Mid-century lounger",
      "variant_inventory_management": null,
      "properties": [],
      "product_exists": true,
      "fulfillable_quantity": 1,
      "grams": 1000,
      "price": "159.99",
      "total_discount": "5.00",
      "fulfillment_status": null,
      "price_set": {
        "shop_money": {
          "amount": "159.99",
          "currency_code": "EUR"
        },
        "presentment_money": {
          "amount": "159.99",
          "currency_code": "EUR"
        }
      },
      "total_discount_set": {
        "shop_money": {
          "amount": "5.00",
          "currency_code": "EUR"
        },
        "presentment_money": {
          "amount": "5.00",
          "currency_code": "EUR"
        }
      },
      "discount_allocations": [
        {
          "amount": "5.00",
          "discount_application_index": 0,
          "amount_set": {
            "shop_money": {
              "amount": "5.00",
              "currency_code": "EUR"
            },
            "presentment_money": {
              "amount": "5.00",
              "currency_code": "EUR"
            }
          }
        }
      ],
      "duties": [],
      "admin_graphql_api_id": "gid://shopify/LineItem/976318377106520349",
      "tax_lines": []
    }
  ]
}
```

---

- [<i class="mdi mdi-chevron-left"></i>**Websocket Events *Go Back***](/Servers-Clients/WebSocket-Server/Events)
{.btn-grid .my-5}