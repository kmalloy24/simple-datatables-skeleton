<script>
	import { Avatar } from '@skeletonlabs/skeleton';
</script>

<h1
	class="text-center h2 p-2 mb-8 bg-gradient-to-br from-primary-500 to-tertiary-500 bg-clip-text text-transparent box-decoration-clone"
>
	Svelte Simple Datatable components styled with Skeleton
</h1>
<div class="w-full grid grid-cols-1 md:grid-cols-2 gap-8">
	<a class="card card-hover" href="/client">
		<header>
			<img
				src="https://vincjo.fr/datatables/logo.svg"
				class="bg-black/50 w-full aspect-[21/9]"
				alt="Post"
			/>
		</header>
		<div class="p-4 space-y-4">
			<h3 class="h3" data-toc-ignore>Client</h3>
			<article>
				<p>
					<!-- cspell:disable -->
					Lorem ipsum dolor sit amet consectetur adipisicing elit. Numquam aspernatur provident eveniet
					eligendi cumque consequatur tempore sint nisi sapiente. Iste beatae laboriosam iure molestias
					cum expedita architecto itaque quae rem.
					<!-- cspell:enable -->
				</p>
			</article>
		</div>
		<hr class="opacity-50" />
		<footer class="p-4 flex justify-start items-center space-x-4">
			<Avatar
				src="https://kylemalloy.com/img/avatar_huc379fd51392f0c4200780900f850561e_275248_288x288_fill_q75_h2_box_center_2.webp"
				width="w-8"
			/>
			<div class="flex-auto flex justify-between items-center">
				<h6 class="font-bold">By Kyle</h6>
				<small>On 1/2/2024</small>
			</div>
		</footer>
	</a>
	<a class="card card-hover overflow-hidden" href="/ssr">
		<header>
			<img
				src="https://vincjo.fr/datatables/logo-remote.svg"
				class="bg-black/50 w-full aspect-[21/9]"
				alt="Post"
			/>
		</header>
		<div class="p-4 space-y-4">
			<h3 class="h3" data-toc-ignore>Server</h3>
			<article>
				<p>
					<!-- cspell:disable -->
					Lorem ipsum dolor sit amet consectetur adipisicing elit. Numquam aspernatur provident eveniet
					eligendi cumque consequatur tempore sint nisi sapiente. Iste beatae laboriosam iure molestias
					cum expedita architecto itaque quae rem.
					<!-- cspell:enable -->
				</p>
			</article>
		</div>
		<hr class="opacity-50" />
		<footer class="p-4 flex justify-start items-center space-x-4">
			<Avatar
				src="https://kylemalloy.com/img/avatar_huc379fd51392f0c4200780900f850561e_275248_288x288_fill_q75_h2_box_center_2.webp"
				width="w-8"
			/>
			<div class="flex-auto flex justify-between items-center">
				<h6 class="font-bold">By Kyle</h6>
				<small>On 1/2/2024</small>
			</div>
		</footer>
	</a>
</div>
