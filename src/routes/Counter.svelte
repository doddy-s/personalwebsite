<script lang="ts">
	import { c } from '../lib/state';
	import { setC } from '../lib/state';

	let count = c;
	$: setC(count);
</script>

<div class="flex flex-row">
	<button
		class="bg-red-600 aspect-square w-12"
		on:click={() => (count -= 1)}
		aria-label="Decrease the counter by one"
	/>

	<div class="text-4xl px-24">
		{count}
	</div>

	<button
		class="bg-green-600 aspect-square w-12"
		on:click={() => (count += 1)}
		aria-label="Increase the counter by one"
	/>
</div>
