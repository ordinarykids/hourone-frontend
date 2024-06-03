<script>
	import { onMount } from 'svelte';
	import ProjectDetail from '$lib/projectDetail.svelte';

	let projects = [];

	onMount(async () => {
		fetch('http://localhost:1337/api/avatars', {
			method: 'GET',
			headers: {
				'Content-Type': 'application/json'
			}
		})
			.then((response) => response.json())
			.then((data) => {
				//   console.log(data)
				projects = data.data;
			})
			.then((data) => {
				//    console.log('eeasdasdra' + data)

				for (let i = 0; i < projects.length; i++) {
					//  console.log(projects[i])
				}
			});
	});
</script>

<h1>Hi.</h1>

<ul>
	{#each projects as project, i}
		<ProjectDetail {project} />asd
	{/each}
</ul>
