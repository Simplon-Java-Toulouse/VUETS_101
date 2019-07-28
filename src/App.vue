<template>
<section>
  <div id="app">
	
  	<Declaratif :name="nom" @nomChanged="nom=$event" />
  	<Condition :bool="bool"/>
  	<ul>
  		<Course :courses="tab" :newItem="new1" @listeChanged="new1=$event"/>
  		
  	</ul>
  </div>
 </section>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';
import Declaratif from './components/Declaratif';
import Condition from './components/Conditon';
import Course    from  './components/Course';
@Component({
	components:{
		Declaratif,	
		Condition,
		Course
	}
})	
export default class App extends Vue {
	new1: string;
	nom: string = "TOTO";
	bool: boolean=false;
	tab: string[]=["liquide vaisselle","pain","pattes","beurre","lait"]
	
}
</script>

<style>

</style>
