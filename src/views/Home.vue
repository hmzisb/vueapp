<template>

<div id="home" class="text-gray-800 ">
	
	<!-- Top Area -->
	<div id="top-section" class="bg-white w-full py-5 px-10 mb-10 px-20">
		<div id="top-bar" class="flex">
			<div id="Search-bar" class="flex flex-row w-4/5 items-center">
				<div class="w-5 text-gray-600 mr-3" v-html="icon.search"></div>
				<input type="text" name="search" placeholder="Search transactions" class="w-4/5">
			</div>
			<div id="action-bar" class="flex flex-row items-center w-1/5">
				<div class="w-5 text-gray-600 mr-3" v-html="icon.bell"></div>
				<img src="../assets/images/hamza.jpg" class="w-6 rounded-full mr-3">
				<label class=" text-xs">Hamza Ahmed</label>
			</div>
		</div>


		<div class="flex self-center items-center text-center justify-center justify-center ">
		<div id="divider" class="border border-gray-200 mt-2 mb-5 w-full "></div>
		</div>

		<!-- Intro Section -->
		<div id="intro-section" class="flex w-full">

			<!-- left side -->
			<div id="info-section" class="flex w-8/12 items-center">
				<img id="main-avatar" src="../assets/images/hamza.jpg" class="w-12 h-12 rounded-full mr-3">
				<div id="info">
					<div id="top-line">
						<h3 class="font-bold text-sm">Good Morning, Hamza Ahmed</h3>
					</div>
					<div id="bottom-line" class="text-xs flex flex-row text-grey-400 py-1">
						<p class=""><div class="w-4 mr-1"><span v-html="icon.building"></span></div>
							Duke Street
						</p>
						<p class="ml-4"><div class="w-4 mr-1 text-green-700"><span class="t" v-html="icon.verified"></span></div> 	Verified Account
						</p>
			
					</div>
				</div>
			</div>


			<!-- Right side -->
			<div id="action-section"  class="flex w-4/12 justify-evenly items-center">
				<button class="bg-teal-800 text-white text-sm rounded-md w-5/12 h-8 border border-white">
				Add Money
				</button>
				<button class="bg-white text-teal-800 text-sm  rounded-md w-5/12 h-8 border border-teal-800">
				Send Money
				</button>
			</div>
		</div>
	</div>



	<!-- Overview section -->
	<div id="body-section" class=" mx-20">


	<!-- 	<h3 class="font-bold mb-4 text-gray-600">Overview</h3> -->
		<div id="overview-section" class="flex flex-row justify-between mb-10">

			<div id="balance-bar" class="
			bg-white w-4/12 p-5 mr-6 rounded-md flex flex-row items-center content-center 
			">
				<div id="icon-left" class="w-2/6 flex justify-center">
					<div class="w-8 text-gray-600"><span v-html="icon.dollar"></span></div>
				</div>
				<div id="data-right" class="w-4/6 flex justify-center flex-col">
					<p class="text-gray-600">Account Balance</p>
					<p class="text-black">$30,000</p>
				</div>
				
			</div>

			<div id="balance-bar" class="
			bg-white w-4/12 mr-6 p-5 rounded-md flex flex-row items-center content-center 
			">
				<div id="icon-left" class="w-2/6 flex justify-center">
					<div class="w-8 text-gray-600"><span v-html="icon.refresh"></span></div>
				</div>
				<div id="data-right" class="w-4/6 flex justify-center flex-col">
					<p class="text-gray-600">Pending</p>
					<p class="text-black">-$20,000</p>
				</div>
				
			</div>

			<div id="balance-bar" class="
			bg-white w-4/12 p-5 rounded-md flex flex-row items-center content-center 
			">
				<div id="icon-left" class="w-2/6 flex justify-center">
					<div class="w-8 text-gray-600"><span v-html="icon.transfer"></span></div>
				</div>
				<div id="data-right" class="w-4/6 flex justify-center flex-col">
					<p class="text-gray-600">Processed <span class="text-xs">(30 days)</span></p>
					<p class="text-black">$55,395</p>
				</div>
				
			</div>




		</div>
	


		<!-- Recent Activity Section -->
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
				  <!--   <tr>
				      <td class="border rounded px-4 py-2">A Long and Winding Tour</td>
				      <td class="border rounded px-4 py-2">Adam</td>
				      <td class="border rounded px-4 py-2">112</td>
				      <td class="border rounded px-4 py-2">858</td>
				    </tr>
				    <tr>
				      <td class="border rounded px-4 py-2">Intro to JavaScript</td>
				      <td class="border rounded px-4 py-2">Chris</td>
				      <td class="border rounded px-4 py-2">1,280</td>
				      <td class="border rounded px-4 py-2">858</td>
				    </tr> -->
				</tbody>
			</table>
		</div>

	</div>

</div>

</template>

<script>

import Store from '@/Store'

export default {
  name: 'Home',

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

