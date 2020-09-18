<template>
	
	<div class="mx-20 my-10">
		
		<h1 class="text-2xl font-bold  text-gray-800">Your Cards</h1>

		<div id="cards" class=" mt-12">
			
			<div id="card-one" class="
			w-6/12 h-56 border border-gray-700 rounded bg-white flex flex-col justify-center p-10
			">
				<div id="name" class="font-bold mb-5 text-gray-800"> Hamza Ahmed</div>
				<div id="card-number" class="font-bold text-xl text-gray-700">1234-4321-5678-8765</div>
				<div id="expiry" class="text-sm text-gray-700">Exp: 10/26</div>
				<div id="master-logo>" class="mt-8 text-sm text-gray-600 font-bold">MasterCard</div>
				<div id="bank-logo" class="text-sm text-gray-600 font-bold">Bank Of America</div>
			</div>

		</div>
	</div>

</template>


<script>

// import Store from '@/Store'

export default {
  name: 'Cards',


}
</script>