<script>
let view = 'plan'
import Plan from './Plan.svelte';

</script>

<header class="navbar p-2">
	
</header>
<div class="container-fluid">
	<div class="row">
		<main>		
			{#if view == 'plan'}
			<Plan/>
			{:else}
			{/if}
			</main>
		</div>
	</div>




