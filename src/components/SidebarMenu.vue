<template>

	<div id="sidebar-main">

		<div id="sidebar-logo" class="text-white text-3xl font-bold mb-6">
			EasyPeazy
		</div>

		<div id="sidebar-menu" class="">
		<ul>
		<li class="text-teal-100 py-2 flex items-center" v-for="item in menu" :key="item">


			<span id="icon" class="w-1/12" v-html="item.icon"></span>
			<router-link :to="{ name: item.route }" class="ml-4">{{item.name}}</router-link>
			
		</li>
        </ul>
		</div>
	</div>
	
</template>

<script>

	import Store from '@/Store';

	export default {
		name: 'sidebar',
			
		computed: {
			menu(){
			return Store.menu;
			},
		}
	}


</script>