# Taxonomy

**Add Custom Fields to a Taxonomy**

To add the fields on the “Add new” screen we are going to use an action hook {TAXONOMY}_add_form_fields and all we have to do is to echo the fields. You have to replace {TAXONOMY} with the actual taxonomy name, for example it could be post_tag for Tags or category for Categories.

I decided that we will add fields to WordPress Tags taxonomy, so the filter hook is going to look like post_tag_add_form_fields.

Read more: https://rudrastyh.com/wordpress/add-custom-fields-to-taxonomy-terms.html

```php
add_action( 'post_tag_add_form_fields', 'rudr_add_term_fields' );

function rudr_add_term_fields( $taxonomy ) {
	?>
		<div class="form-field">
			<label for="rudr_text">Text Field</label>
			<input type="text" name="rudr_text" id="rudr_text" />
			<p>Field description may go here.</p>
		</div>
		<div class="form-field">
			<label>Image Field</label>
			<a href="#" class="button rudr-upload">Upload image</a>
			<a href="#" class="rudr-remove" style="display:none">Remove image</a>
			<input type="hidden" name="rudr_img" value="">
		</div>
	<?php
}
```

References:
* https://rudrastyh.com/woocommerce/payment-complete-hooks.html
* https://rudrastyh.com/woocommerce/payment-gateway-plugin.html