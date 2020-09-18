<template>
	
	<div class="mx-20 my-10">
		<div id="recent-transaction-panel">
			<table class="table-auto w-full bg-gray-100 text-gray-600 text-sm">
				<thead class="border-b border-gray-200">
				    <tr>
				      <th class=" rounded px-4 py-3 text-left">TRANSACTION</th>
				      <th class=" rounded px-4 py-3 text-left">AMOUNT</th>
				      <th class=" rounded px-4 py-3 text-left">STATUS</th>
				      <th class=" rounded px-4 py-3 text-left">DATE</th>
				    </tr>
				  </thead>
				  <tbody>
				    <tr v-for="transaction in transactions"  class="border-b border-gray-200">
				      <td class=" rounded px-4 py-2 flex flex-row items-center">
				      	<div class="w-4 mr-2"><span v-html="icon.transfer"></span></div> {{transaction.info}}
				      </td>
				      <td class=" rounded px-4 py-2">{{transaction.amount}} USD</td>
				      <td class=" rounded px-4 py-2"> 
				      	<span class="bg-green-100 py-1 px-2 text-xs text-green-700 rounded-full"> 
				      		{{transaction.status}}
				      	</span> 
				      </td>
				      <td class=" rounded px-4 py-2">{{transaction.date}}</td>
				    </tr>
				</tbody>
			</table>
		</div>
	</div>

</template>


<script>

import Store from '@/Store'

export default {
  name: 'History',

  computed: {

  	icon(){
				return Store.icons;
			},

  	transactions(){
			return Store.transactions;
		}
	}

}
</script>