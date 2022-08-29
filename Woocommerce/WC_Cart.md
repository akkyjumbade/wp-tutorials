# WC_Cart

```php
$cart = WC()->cart;

```

```php
// $cart conditionals (if)
WC()->cart->is_empty()
WC()->cart->needs_payment()
WC()->cart->show_shipping()
WC()->cart->needs_shipping()
WC()->cart->needs_shipping_address()
WC()->cart->display_prices_including_tax()
 
// Get $cart totals
WC()->cart->get_cart_contents_count();
WC()->cart->get_cart_subtotal();
WC()->cart->subtotal_ex_tax;
WC()->cart->subtotal;
WC()->cart->get_displayed_subtotal();
WC()->cart->get_taxes_total();
WC()->cart->get_shipping_total();
WC()->cart->get_coupons();
WC()->cart->get_coupon_discount_amount( 'coupon_code' );
WC()->cart->get_fees();
WC()->cart->get_discount_total();
WC()->cart->get_total();
WC()->cart->total;
WC()->cart->get_tax_totals();
WC()->cart->get_cart_contents_tax();
WC()->cart->get_fee_tax();
WC()->cart->get_discount_tax();
WC()->cart->get_shipping_total();
WC()->cart->get_shipping_taxes();
  
// Loop over $cart items
foreach ( WC()->cart->get_cart() as $cart_item_key => $cart_item ) {
   $product = $cart_item['data'];
   $product_id = $cart_item['product_id'];
   $quantity = $cart_item['quantity'];
   $price = WC()->cart->get_product_price( $product );
   $subtotal = WC()->cart->get_product_subtotal( $product, $cart_item['quantity'] );
   $link = $product->get_permalink( $cart_item );
   // Anything related to $product, check $product tutorial
   $attributes = $product->get_attributes();
   $whatever_attribute = $product->get_attribute( 'whatever' );
   $whatever_attribute_tax = $product->get_attribute( 'pa_whatever' );
   $any_attribute = $cart_item['variation']['attribute_whatever'];
   $meta = wc_get_formatted_cart_item_data( $cart_item );
}
 
// Get $cart customer billing / shipping
WC()->cart->get_customer()->get_billing_first_name();
WC()->cart->get_customer()->get_billing_last_name();
WC()->cart->get_customer()->get_billing_company();
WC()->cart->get_customer()->get_billing_email();
WC()->cart->get_customer()->get_billing_phone();
WC()->cart->get_customer()->get_billing_country();
WC()->cart->get_customer()->get_billing_state();
WC()->cart->get_customer()->get_billing_postcode();
WC()->cart->get_customer()->get_billing_city();
WC()->cart->get_customer()->get_billing_address();
WC()->cart->get_customer()->get_billing_address_2();
WC()->cart->get_customer()->get_shipping_first_name();
WC()->cart->get_customer()->get_shipping_last_name();
WC()->cart->get_customer()->get_shipping_company();
WC()->cart->get_customer()->get_shipping_country();
WC()->cart->get_customer()->get_shipping_state();
WC()->cart->get_customer()->get_shipping_postcode();
WC()->cart->get_customer()->get_shipping_city();
WC()->cart->get_customer()->get_shipping_address();
WC()->cart->get_customer()->get_shipping_address_2();
 
// Other stuff
WC()->cart->get_cross_sells();
WC()->cart->get_cart_item_tax_classes_for_shipping();
WC()->cart->get_cart_hash();
WC()->cart->get_customer();

```