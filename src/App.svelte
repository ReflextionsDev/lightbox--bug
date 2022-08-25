<script>
	import { Lightbox } from "svelte-lightbox";
</script>

<main>
	<div style="display: flex;">

		<!-- Lightbox in wrapper doesn't fill entire space -->
		<div class="wrapper">
			<Lightbox>
				<img src="pic.jpg" alt="" />
			</Lightbox>
		</div>
		
		<!-- Img directly in wrapper fills all space -->
		<div class="wrapper">
			<img src="pic.jpg" alt="" />
		</div>
	</div>

	<div style="display: flex;">

		<!-- Wrapper in lightbox does fill all space, but image preview retain object-fit aspect -->
		<Lightbox>
			<div class="wrapper">
				<img src="pic.jpg" alt="" />
			</div>
		</Lightbox>

		<!-- Img directly in wrapper fills all space -->
		<div class="wrapper">
			<img src="pic.jpg" alt="" />
		</div>
	</div>
</main>

<style>
	img {
		object-fit: cover;
		width: 100%;
		height: 100%;
	}

	.wrapper {
		width: 500px;
		height: 500px;
	}
</style>
