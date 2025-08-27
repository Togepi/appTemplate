<script lang="ts">
	// Shadcn Svelte UI Button Component
	import Button from '$lib/components/ui/button/button.svelte';

	// You can store Hero Header Component in seperate file
	// I have used snippet for better readability


	import ArrowRight from '@lucide/svelte/icons/arrow-right';
	import ChevronRight from '@lucide/svelte/icons/chevron-right';
	import { scrollY } from 'svelte/reactivity/window';

	type MenuItem = {
		name: string;
		href: string;
	};

	let menuItems: MenuItem[] = [
		{ name: 'Features', href: '#a' },
		{ name: 'Solution', href: '#a' },
		{ name: 'Pricing', href: '#a' },
		{ name: 'About', href: '#a' }
	];

	let menuState = $state(false);
	let isScrolled = $derived.by(() => {
		if (scrollY.current !== undefined && scrollY.current > 50) {
			return true;
		}
		return false;
	});
	let link_bg = 'https://cdnb.artstation.com/p/assets/images/images/034/079/331/large/koke-nunez-iceland1.jpg?1611332096'
	let total_bg = "bg-[url('https://cdna.artstation.com/p/assets/images/images/046/457/238/large/pengzhen-zhang-demo.jpg?1645296652')]";
	const parts = [
  "bg-[url('",
  link_bg,
  "')]",
];
	let text = parts.filter(Boolean).join("");

	console.log(text)
</script>


<div>
	<!-- Scroll below to see the snippet code  -->

	<main class="overflow-hidden {total_bg} bg-cover bg-bottom py-32" >
		<div class="absolute inset-0 isolate hidden opacity-65 contain-strict lg:block">
			<div
				class="absolute top-0 left-0 h-320 w-140 -translate-y-87.5 -rotate-45 rounded-full bg-[radial-gradient(68.54%_68.72%_at_55.02%_31.46%,hsla(0,0%,85%,.08)_0,hsla(0,0%,55%,.02)_50%,hsla(0,0%,45%,0)_80%)]"
			></div>
			<div
				class="absolute top-0 left-0 h-320 w-60 [translate:5%_-50%] -rotate-45 rounded-full bg-[radial-gradient(50%_50%_at_50%_50%,hsla(0,0%,85%,.06)_0,hsla(0,0%,45%,.02)_80%,transparent_100%)]"
			></div>
			<div
				class="absolute top-0 left-0 h-320 w-60 -translate-y-87.5 -rotate-45 bg-[radial-gradient(50%_50%_at_50%_50%,hsla(0,0%,85%,.04)_0,hsla(0,0%,45%,.02)_80%,transparent_100%)]"
			></div>
		</div>
		<section >
			<div class="relative pt-24 md:pt-36">
				<div
					class="absolute inset-0 -z-10 size-full [background:radial-gradient(125%_125%_at_50%_100%,transparent_0%,var(--color-background)_75%)]"
				></div>
				<div class="mx-auto max-w-7xl px-6">
					<div class="text-center sm:mx-auto lg:mt-0 lg:mr-auto">
						<div>
							<a
								href="#link"
								class="group mx-auto flex w-fit items-center gap-4 rounded-full border bg-muted p-1 pl-4 shadow-md shadow-zinc-950/5 transition-colors duration-300 hover:bg-background dark:border-t-white/5 dark:shadow-zinc-950 dark:hover:border-t-border"
							>
								<span class="text-sm text-foreground">Les inscriptions sont déjà ouvertes</span>
								<span
									class="block h-4 w-0.5 border-l bg-white dark:border-background dark:bg-zinc-700"
								></span>

								<div
									class="size-6 overflow-hidden rounded-full bg-background duration-500 group-hover:bg-muted"
								>
									<div
										class="flex w-12 -translate-x-1/2 duration-500 ease-in-out group-hover:translate-x-0"
									>
										<span class="flex size-6">
											<ArrowRight class="m-auto size-3" />
										</span>
										<span class="flex size-6">
											<ArrowRight class="m-auto size-3" />
										</span>
									</div>
								</div>
							</a>
						</div>

						<h1 class="mt-8 font-amarante  font-bold text-3xl text-balance lg:text-9xl text-white   lg:mt-16 xl:text-[3.25rem]">
							Royaume de l’Avalanche : plongez au cœur des vallées gelées					</h1>
						<p class="mx-auto  mt-8 max-w-4xl text-lg text-balance text-white text-shadow-black text-shadow-2xs font-semibold">
Avalanche est un jeu de rôle grandeur nature épisodique et sandbox. 
Chaque joueuse incarne une tribu qui tente de survivre au coeur de montagnes habitées par des hivers mortels.						</p>

						<div class="mt-12 flex flex-col items-center justify-center gap-2 md:flex-row">
							<div
								class=" bg-foreground/10 p-0.5 "
								style="border-radius: calc(0.5rem + 0.125rem + 4px);"
							>
								<Button href="#link" size="lg" class="rounded-xl   px-5 text-base">
									<span class="text-nowrap">Découvrir le jeu</span>
								</Button>
							</div>
							<Button size="lg" variant="outline" class="rounded-xl px-5">Je débute le jeu de rôle</Button>
						</div>
					</div>
				</div>

				
			</div>
		</section>
		
	</main>
</div>

