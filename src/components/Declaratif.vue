<template>
	<section>
		<input type="text" :value="name" @input="changeNom">
  		Bonjour {{nom}}
  	</section>
</section>

</template>

<script lang="ts">
import { Component, Vue, Prop } from 'vue-property-decorator';

@Component
export default  class Declaratif extends Vue{
	nom:string="TOTO"
	@Prop(String) name:string
	
		changeNom(event): void{
			this.nom=event.target.value
			this.$emit('nomChanged',this.nom);
		
	}
}

	

</script>

<style>

</style>