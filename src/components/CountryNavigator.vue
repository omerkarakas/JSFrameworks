<template>
<div>
    <h1>Country Navigator</h1>
	<h2>{{title}}</h2>

	<ul class="list-group">
		<li v-for="country in data.countries" 
		@click="showcountry(country)" 
		v-bind:key="country.id" class="list-group-item">
			
			<!-- <span title="Bu ülkeyi kacirma">  -->

			<span v-bind:title="country.details" :id="country.id">
				
				{{country.name}} - {{country.id}}
			</span>
		</li>
	</ul>

	<h3>Sayac : {{counter}} </h3>
	<button v-on:click="counter++" class="btn btn-success"> + </button> &nbsp;
	<button @click="counter--" class="btn btn-danger"> - </button> &nbsp;
	<button v-on:click="increment()" class="btn btn-success"> + </button> &nbsp;
	<button @click="decrement" class="btn btn-danger"> - </button> &nbsp;




</div>
</template>


<script>
import data from '../data/data';
export default {
	name: "CountryNavigator",
	data(){
		return {
			data,
			title : 'Select a country',
			counter : 0
		}

	},
	methods: {

		increment(){
			this.counter++;
		},

		decrement : function(){
			this.counter--;
		},

		showcountry : function(country){
			alert('Clicked on '+ country.name);
		}


	}	
}
</script>


<style scoped>

</style>