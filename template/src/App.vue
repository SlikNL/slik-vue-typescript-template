<template>
	<div id="app">
		<img src="./assets/logo.svg">
		{{#router}}
		<router-view></router-view>
		{{else}}
		<HelloWorld></HelloWorld>
		{{/router}}
	</div>
</template>

<script lang="ts">
	import { Component, Emit, Inject, Model, Prop, Provide, Vue, Watch } from 'vue-property-decorator'

	{{#unless router}}
	import HelloWorld from './components/HelloWorld.vue'
	{{/unless}}

	@Component({
	name: 'app'{{#router}}{{else}},
	components: {
		HelloWorld
	}{{/router}}
	})
	export default class App extends Vue {
		// Data()
		msg: string = 'App was created!'
		
		// Computed
		get mtdMessage(): string {
			return this.greet()
		}

		// Methods
		greet(): string {
			return `Mounted: ${this.msg}`
		}

		// Watch
		@Watch('msg')
		OnMessageChange(val: string, oldVal: string): void {
			console.log(`Message was changed from ${oldVal} to ${val}`)
		}

		// Created, Mounted etc
		mounted() {
			console.log(this.mtdMessage)
			this.msg = 'Nice'
		}
	}
</script>

<style lang="less">
	// Main for general styling that apply to everything
	@import 'less/main';

	// Files in /components/ folder for component styling
	@import 'less/components/App';
</style>
