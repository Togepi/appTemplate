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
</script>


<div>
	<!-- Scroll below to see the snippet code  -->

	<main class="overflow-hidden">
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
		<section>
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

						<h1 class="mt-8 font-amarante uppercase font-bold text-3xl text-balance lg:text-9xl  lg:mt-16 xl:text-[18.25rem]">
							1804						</h1>
						<p class="mx-auto font-amarante mt-8 max-w-6xl text-3xl text-balance">
						En année 1804 est un jeu de rôle grandeur nature où vous prenez le rôle d'une divinité. 
							Incarner vos valeurs morales et inspirer votre peuple.
						</p>

						<div class="mt-12 flex flex-col items-center justify-center gap-2 md:flex-row">
							<div
								class="border bg-foreground/10 p-0.5"
								style="border-radius: calc(0.5rem + 0.125rem + 4px);"
							>
								<Button href="#link" size="lg" class="rounded-xl px-5 text-base">
									<span class="text-nowrap">Découvrir le jeu</span>
								</Button>
							</div>
							<Button size="lg" variant="ghost" class="rounded-xl px-5">Je débute le jeu de rôle</Button>
						</div>
					</div>
				</div>

				<div class="relative mt-8 -mr-56 overflow-hidden px-2 sm:mt-12 sm:mr-0 md:mt-20">
					<div
						class="absolute inset-0 z-10 bg-linear-to-b from-transparent from-35% to-background"
					></div>
					<div
						class="relative mx-auto max-w-6xl overflow-hidden rounded-2xl border bg-background p-4 shadow-lg inset-shadow-2xs shadow-zinc-950/15 ring-background dark:inset-shadow-white/20"
					>
						<img
							class="relative hidden aspect-15/8 rounded-2xl bg-background dark:block"
							src="https://cdna.artstation.com/p/assets/images/images/091/235/896/large/egor-kapustin-dionysis-fin.jpg?1756226715"
							alt="app screen"
							width="2700"
							height="1440"
						/>
						<img
							class="relative z-2 aspect-15/8 rounded-2xl border border-border/25 dark:hidden"
							src="https://cdna.artstation.com/p/assets/images/images/091/235/896/large/egor-kapustin-dionysis-fin.jpg?1756226715"
							alt="app screen"
							width="2700"
							height="1440"
						/>
					</div>
				</div>
			</div>
		</section>
		
	</main>
</div>

