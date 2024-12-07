<script lang="ts">
	import '../app.css';
	let { children } = $props();
</script>

{@render children()}

<style>
	:global(html) {

    	scroll-behavior: smooth;
}
	:global(section){

		scroll-margin-top: 150px;

	}
</style>


