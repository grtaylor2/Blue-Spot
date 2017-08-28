Version 1.4 has new filter functions that would help update the label and image in the cart in the header area.

- zp_shop_alternate_text
    => filter to change the text when you hover the cart amount

- zp_cart_singular_label
    => cart label when there's only 1 item on the cart

- zp_cart_plural_label
    => cart label when there's more items on the cart

- zp_header_cart_image
    => filter to change the default cart image.


Example functions:

add_filter( 'zp_shop_alternate_text', 'zp_change_alternate_text' );

function zp_change_alternate_text(){
  return __('this is an alternat text', 'eshop');

}



add_filter( 'zp_cart_singular_label', 'zp_change_singular_label' );

function zp_change_singular_label(){
return __('this is a test %d singular text', 'eshop');

}

add_filter( 'zp_cart_plural_label', 'zp_change_plural_label' );

function zp_change_plural_label(){

return __('this is a test %d plural text', 'eshop');

}


add_filter( 'zp_header_cart_image', 'zp_change_cart_image' );

function zp_change_cart_image(){
$image_url = '<img src="FULL_IMAGE_URL" height="" width="" />';
return 	$image_url;

}