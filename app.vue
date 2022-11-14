<script setup lang="ts">

async function testFetchContentType() {
		
	
	let add_to_cart_data = {
			product_id: "123",
			item_quantity: "10",
			
	};
	
	await useFetch(() => `/addToCart`, {
        method: 'POST',
        mode: 'no-cors',
    	headers: {
    		"content-type": "application/json"
    	},
        body: add_to_cart_data,
        initialCache: false,
        
        onResponse({ request, response, options }) {
    	    // Process the response data
    	    
    	   window.console.error("Add to cart... ");	    	 


    	},
 
    	
    } );

	
}

</script>

<template>

	<p> Check network tab in web developer tools...</p>
	
  	 <button  @click="testFetchContentType()" >TEST FETCH</button>
	

</template>
