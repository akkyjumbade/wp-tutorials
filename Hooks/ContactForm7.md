# ContactForm7

* https://docs.hookmax.com/plugin/contact-form-7/5.5.3/action/wpcf7_after_save/#

```php
do_action( 'wpcf7_after_save', $this );

```

```php
// define the wpcf7_after_save callback 
function custom_wpcf7_after_save( $instance ){ 
   //custom code here
} 

//add the action 
add_action('wpcf7_after_save', 'custom_wpcf7_after_save', 10, 1);
```


