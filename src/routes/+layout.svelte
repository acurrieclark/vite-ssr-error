<script lang="ts">
	import { browser } from '$app/environment';
</script>

{#if browser}
	<slot />
{/if}
