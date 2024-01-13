<script lang="ts">
	const boxesWidth = 6;
	const boxesHeight = 5;
	const boxWidth = 10;
	const boxHeight = 7;
	const boxGap = 1;
	const svgWidth = boxesWidth * (boxWidth + boxGap) - boxGap;
	const svgHeight = boxesHeight * (boxHeight + boxGap) - boxGap;
	const numColors = (1 << 24) - 1;
</script>

<p>🏗️ Under construction 🚧</p>

<svg viewBox="0 0 {svgWidth} {svgHeight}">
	{#each Array(boxesWidth) as _, boxX}
		{#each Array(boxesHeight) as _, boxY}
			<rect
				x={boxX * (boxWidth + boxGap)}
				y={boxY * (boxHeight + boxGap)}
				width={boxWidth}
				height={boxHeight}
				fill="#{Math.floor(Math.random() * numColors).toString(16)}"
			/>
		{/each}
	{/each}
</svg>
