<template>
<section>
	
 	<p v-if="bool">{{visible}}</p>
 	<p v-if="!bool">{{cacher}}</p>
 	<button @click="toggle(bool)">Toggle</button>
 </section>
</template>

<script lang="ts">
import { Component, Vue,Prop } from 'vue-property-decorator';


@Component	
export default class Condition extends Vue {
	bool: boolean=false;
	cacher: string=""
	visible: string="je suis cacher"
	@Prop(Boolean) bool:boolean;
	toggle(bool): void{
		if(this.bool)
			this.bool=false
		else
			this.bool=true
	}
	
}
</script>

<style>

</style>