<script>
    import SVG from './SVG.svelte';
    import Form from './Form.svelte';
    import List from './List.svelte';
    import Visualization from './Visualization.svelte';
</script>

<style>
		@import url("https://fonts.googleapis.com/css?family=IBM+Plex+Mono:400,700&display=swap");
		:global(*) {
			box-sizing: border-box;
			padding: 0;
			margin: 0;
		}
		:global(body) {
			color: hsl(240, 25%, 95%);
			background: hsl(240, 25%, 20%);
			font-family: "IBM Plex Mono", monospace;
		}
			/* absolute position the span in the top left corner of each heading */
		:global(h2) {
				position: relative;
				font-size: 1.85rem;
				padding: 0.25rem;
				font-weight: 400;
		}
		:global(h2 span) {
				position: absolute;
				top: 0%;
				right: 100%;
				transform: translateY(-50%);
				display: block;
				width: 1.25em;
				height: 1.25em;
				border-radius: 0.75rem;
				background: hsla(240, 25%, 50%, 0.3);
		}
		:global(h2 span svg) {
				display: block;
				width: 100%;
				height: 100%;
				filter: drop-shadow(0 0 3px hsla(240, 25%, 0%, 0.5));
		}
		:global(.app > * + * + *) {
			margin-top: 5rem;
		}
		:global(section > * + *) {
				margin-top: 1rem;
		}

    .app {
        max-width: 900px;
        width: 80vw;
        margin: 2rem auto;
    }
</style>

<div class="app">
    <SVG />
    <Form />
    <List />
    <Visualization />
</div>