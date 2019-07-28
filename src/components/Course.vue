<template>
<section>
	
 	Liste de course. 
 	<input type="hidden" :value="courses">
 	<li v-for="course in tab">
			{{course}}
  		</li>
  		<input type="text" :value="newItem" @input="ajoutval">
  		<p id="cacher">{{new1}}</p>
  		<button @click="ajouter(new1,tab)">ajouter achat</button>

 </section>
</template>

<script lang="ts">
import { Component, Vue,Prop } from 'vue-property-decorator';


@Component	
export default class Course extends Vue {
	tab: string[]=["liquide vaisselle","pain","pattes","beurre","lait"]
	@Prop(Array) courses: string[];
	new1: string;
	@Prop(String) newItem: string;
	ajoutval(event): void{
			this.new1=event.target.value
			this.$emit('listeChanged',this.new1);
		
	}
	ajouter(new1,tab){
		tab.push(new1);
	}

	
}
</script>

<style>
#cacher{
	display:none;
}
</style>