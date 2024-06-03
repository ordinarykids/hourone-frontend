<script>
	import { onMount } from 'svelte';
	export let project = { title: '' };

	// console.log('asd' + project)

	onMount(async () => {
		console.log('asd' + project);
	});
</script>

<div class="my-4">
	<li>{project.attributes.name}</li>
</div>
