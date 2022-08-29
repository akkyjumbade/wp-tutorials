# WC_Cart

```php
$cart = WC()->cart;

```

```php
// $cart conditionals (if)
$cart->is_empty()
$cart->needs_payment()
$cart->show_shipping()
$cart->needs_shipping()
$cart->needs_shipping_address()
$cart->display_prices_including_tax()
```

```php
// Get $cart totals
$cart->get_cart_contents_count();
$cart->get_cart_subtotal();
$cart->subtotal_ex_tax;
$cart->subtotal;
$cart->get_displayed_subtotal();
$cart->get_taxes_total();
$cart->get_shipping_total();
$cart->get_coupons();
$cart->get_coupon_discount_amount( 'coupon_code' );
$cart->get_fees();
$cart->get_discount_total();
$cart->get_total();
$cart->total;
$cart->get_tax_totals();
$cart->get_cart_contents_tax();
$cart->get_fee_tax();
$cart->get_discount_tax();
$cart->get_shipping_total();
$cart->get_shipping_taxes();
```

```php
// Loop over $cart items
foreach ( $cart->get_cart() as $cart_item_key => $cart_item ) {
   $product = $cart_item['data'];
   $product_id = $cart_item['product_id'];
   $quantity = $cart_item['quantity'];
   $price = $cart->get_product_price( $product );
   $subtotal = $cart->get_product_subtotal( $product, $cart_item['quantity'] );
   $link = $product->get_permalink( $cart_item );
   // Anything related to $product, check $product tutorial
   $attributes = $product->get_attributes();
   $whatever_attribute = $product->get_attribute( 'whatever' );
   $whatever_attribute_tax = $product->get_attribute( 'pa_whatever' );
   $any_attribute = $cart_item['variation']['attribute_whatever'];
   $meta = wc_get_formatted_cart_item_data( $cart_item );
}
```

```php
// Get $cart customer billing / shipping
$cart->get_customer()->get_billing_first_name();
$cart->get_customer()->get_billing_last_name();
$cart->get_customer()->get_billing_company();
$cart->get_customer()->get_billing_email();
$cart->get_customer()->get_billing_phone();
$cart->get_customer()->get_billing_country();
$cart->get_customer()->get_billing_state();
$cart->get_customer()->get_billing_postcode();
$cart->get_customer()->get_billing_city();
$cart->get_customer()->get_billing_address();
$cart->get_customer()->get_billing_address_2();
$cart->get_customer()->get_shipping_first_name();
$cart->get_customer()->get_shipping_last_name();
$cart->get_customer()->get_shipping_company();
$cart->get_customer()->get_shipping_country();
$cart->get_customer()->get_shipping_state();
$cart->get_customer()->get_shipping_postcode();
$cart->get_customer()->get_shipping_city();
$cart->get_customer()->get_shipping_address();
$cart->get_customer()->get_shipping_address_2();
```
```php 
// Other stuff
$cart->get_cross_sells();
$cart->get_cart_item_tax_classes_for_shipping();
$cart->get_cart_hash();
$cart->get_customer();

```