<template>
<div>
    <h1>Country Navigator</h1>

	<ul class="list-group">
		<li  v-for="country in data.countries" v-bind:key="country" class="list-group-item">
			{{country.name}}
		</li>
	</ul>

</div>
</template>


<script>
import data from '../data/data';
export default {
	name: "CountryNavigator",
	data(){
		return {
			data
		}

	}	
}
</script>


<style scoped>

</style>