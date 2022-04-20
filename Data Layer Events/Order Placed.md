# Order Placed

### 

## Javascript Code
```js
window.appEventData = window.appEventData || [];
appEventData.push({
  "event": "Order Placed",
    "cart": {
        "cartID": "<cartID>"
    },
    "payment": {
        "paymentAmount": <paymentAmount>,
        "paymentMethod": "<paymentMethod>"
    },
    "shipping": {
        "shippingMethod": "<shippingMethod>"
    },
    "transaction": {
        "cartRevenue": <cartRevenue>,
        "finalRevenue": <finalRevenue>,
        "item": [
            {
                "price": {
                    "sellingPrice": "<sellingPrice>"
                },
                "productInfo": {
                    "productID": "<productID>"
                },
                "quantity": <quantity>,
                "shippingCost": "<shippingCost>",
                "tax": "<tax>"
            }
        ],
        "payment": [
            {
                "paymentGateway": "<paymentGateway>",
                "paymentID": "<paymentID>"
            }
        ],
        "purchaseID": "<purchaseID>",
        "total": {
            "currency": "<currency>"
        }
    },
    "voucherDiscount": {
        "autoDiscountAmount": "<autoDiscountAmount>",
        "autoDiscountCode": "<autoDiscountCode>",
        "autoDiscountCodesApplied": <autoDiscountCodesApplied>,
        "manualDiscountAmount": "<manualDiscountAmount>",
        "manualDiscountCode": "<manualDiscountCode>",
        "manualDiscountCodesEntered": <manualDiscountCodesEntered>,
        "rewardsDiscountAmount": <rewardsDiscountAmount>,
        "totalDiscountAmount": <totalDiscountAmount>
    }
});
```

## Variable Definitions

|Path|Type|Description|Example|Pattern|Min Length|Max Length|Minimum|Maximum|Multiple Of|
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|cart.cartID|string|Back-end identifier for a shopping cart|12345, 435678, 34567, XCV456, XCV876|||||||
|payment.paymentAmount|number|Order level payment amount \(not for use with merchandising\)||||||||
|payment.paymentMethod|string|Allow payment method to be captured prior to Order Placed event||||||||
|shipping.shippingMethod|string|The shipping method associated with an order.||||||||
|transaction.cartRevenue|number|Total cart revenue \(not for use with merchandising\)||||||||
|transaction.finalRevenue|number|Final revenue \(not for use with merchandising\)||||||||
|transaction.item[n].price.sellingPrice|string|String representation of the price paid after coupons or discounts. Positive. Up to two decimal places for cents. No currency symbol.|200, 29.99, 50, 0|^[0-9]*(\.[0-9]{1,2})?$||||||
|transaction.item[n].productInfo.productID|string|Unique Identifier of a product or offering.  Must match the format of back-end systems if used as a key for import of product meta data. Most often, one level above SKU for products with SKU variants. |155, 65588, 987764448|||||||
|transaction.item[n].quantity|integer|Integer number of products being acted upon \(added to a cart, removed from wishlist, purchased, reserved\)|1, 2, 3, 4, 5||||1|||
|transaction.item[n].shippingCost|string|The shipping costs for all items within the shippingGroup of the transaction.|15.05, 2, 0.22, 2.2|^[0-9]*(\.[0-9]{1,2})?$||||||
|transaction.item[n].tax|string|String representation of the tax collected at a shipment level for a transaction. Positive. Up to two decimal places for cents. No currency symbol.|5.05, 20, 10.22, 9.2|^[0-9]*(\.[0-9]{1,2})?$||||||
|transaction.payment[n].paymentGateway|string|Captures the digital payment gateway was used to complete transactions for orders?|PayPal, Stripe|||||||
|transaction.payment[n].paymentID|string|Unique identifier of a payment.  Typically an integration key from a back-end system.|ZPH-87698-098|||||||
|transaction.purchaseID|string|Unique identifier of the purchase. Max Length 20. Used as Unique ID of the purchase or deduplication.|ABC-132456789, DEF-132456789, 0987654567|^[a-zA-Z0-9]{6,20}$|6|20||||
|transaction.total.currency|string|Currency of the transaction. ISO 4217 \(3 character alpha\), uppercase |USD, CAD, GBP, CHF|^[A-Z]{3}$|3|3||||
|voucherDiscount.autoDiscountAmount|string|The total discount from any auto-applied discount codes||||||||
|voucherDiscount.autoDiscountCode|string|Track automatically-applied discount codes in a separate eVar than manually-entered discount codes||||||||
|voucherDiscount.autoDiscountCodesApplied|number|Counts the number of automatically-applied discount codes.||||||||
|voucherDiscount.manualDiscountAmount|string|The total discount from any manually-entered discount codes||||||||
|voucherDiscount.manualDiscountCode|string|Track manually-entered discount codes in a separate eVar than automatically-applied discount codes||||||||
|voucherDiscount.manualDiscountCodesEntered|number|Counts the number of discount codes entered manually.||||||||
|voucherDiscount.rewardsDiscountAmount|number|Total discount amount from rewards points||||||||
|voucherDiscount.totalDiscountAmount|number|Total discount amount from all sources||||||||




