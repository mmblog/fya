jQuery(document).on('change', '.prodname select', function() {
    var itemKey = jQuery(this).attr('name');
    var quantity = jQuery(this).val();

    jQuery.ajax({
        url: wc_cart_params.ajax_url,
        type: 'POST',
        data: {
            action: 'update_cart',
            item_key: itemKey,
            quantity: quantity
        },
        success: function(response) {
            // Actualiza la vista del carrito con los nuevos datos
            console.log("Listo")
            jQuery('.woocommerce-cart-form').html(response);
        },
		error: function(jqXHR, textStatus, errorThrown) {
            console.log('Error:', errorThrown);
        }
    });
});