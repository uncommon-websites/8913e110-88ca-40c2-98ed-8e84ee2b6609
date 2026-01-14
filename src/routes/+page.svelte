<script lang="ts">
	// Icons
	const icons = {
		thermometer: `<svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="w-5 h-5"><path d="M14 14.76V3.5a2.5 2.5 0 0 0-5 0v11.26a4.5 4.5 0 1 0 5 0z"/></svg>`,
		heart: `<svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="w-5 h-5"><path d="M20.84 4.61a5.5 5.5 0 0 0-7.78 0L12 5.67l-1.06-1.06a5.5 5.5 0 0 0-7.78 7.78l1.06 1.06L12 21.23l7.78-7.78 1.06-1.06a5.5 5.5 0 0 0 0-7.78z"/></svg>`,
		trendingUp: `<svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="w-5 h-5"><polyline points="23 6 13.5 15.5 8.5 10.5 1 18"/><polyline points="17 6 23 6 23 12"/></svg>`,
		shield: `<svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="w-5 h-5"><path d="M12 22s8-4 8-10V5l-8-3-8 3v7c0 6 8 10 8 10z"/></svg>`,
		database: `<svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="w-5 h-5"><ellipse cx="12" cy="5" rx="9" ry="3"/><path d="M21 12c0 1.66-4 3-9 3s-9-1.34-9-3"/><path d="M3 5v14c0 1.66 4 3 9 3s9-1.34 9-3V5"/></svg>`,
		download: `<svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="w-5 h-5"><path d="M21 15v4a2 2 0 0 1-2 2H5a2 2 0 0 1-2-2v-4"/><polyline points="7 10 12 15 17 10"/><line x1="12" y1="15" x2="12" y2="3"/></svg>`,
		upload: `<svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="w-5 h-5"><path d="M21 15v4a2 2 0 0 1-2 2H5a2 2 0 0 1-2-2v-4"/><polyline points="17 8 12 3 7 8"/><line x1="12" y1="3" x2="12" y2="15"/></svg>`,
		barChart: `<svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="w-5 h-5"><line x1="12" y1="20" x2="12" y2="10"/><line x1="18" y1="20" x2="18" y2="4"/><line x1="6" y1="20" x2="6" y2="16"/></svg>`,
		clock: `<svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="w-5 h-5"><circle cx="12" cy="12" r="10"/><polyline points="12 6 12 12 16 14"/></svg>`,
		check: `<svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="w-4 h-4"><polyline points="20 6 9 17 4 12"/></svg>`,
		arrowRight: `<svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="w-4 h-4"><line x1="5" y1="12" x2="19" y2="12"/><polyline points="12 5 19 12 12 19"/></svg>`,
		activity: `<svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="w-5 h-5"><polyline points="22 12 18 12 15 21 9 3 6 12 2 12"/></svg>`,
		sun: `<svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="w-5 h-5"><circle cx="12" cy="12" r="5"/><line x1="12" y1="1" x2="12" y2="3"/><line x1="12" y1="21" x2="12" y2="23"/><line x1="4.22" y1="4.22" x2="5.64" y2="5.64"/><line x1="18.36" y1="18.36" x2="19.78" y2="19.78"/><line x1="1" y1="12" x2="3" y2="12"/><line x1="21" y1="12" x2="23" y2="12"/><line x1="4.22" y1="19.78" x2="5.64" y2="18.36"/><line x1="18.36" y1="5.64" x2="19.78" y2="4.22"/></svg>`,
	};
</script>

<div class="min-h-screen bg-white">
	<!-- Header -->
	<header class="flex items-center justify-between px-6 py-4 max-w-7xl mx-auto">
		<div class="flex items-center gap-2">
			<!-- Logo Icon -->
			<div class="text-gray-900">
				<svg width="32" height="32" viewBox="0 0 89 88" fill="none" xmlns="http://www.w3.org/2000/svg">
					<circle cx="44.7578" cy="44" r="42.5" stroke="currentColor" stroke-width="3"/>
					<path d="M72.2578 44C72.2578 55.8989 69.0763 66.6027 64.0115 74.2872C58.9387 81.9839 52.1003 86.5 44.7578 86.5C37.4153 86.5 30.5769 81.9839 25.5042 74.2872C20.4394 66.6027 17.2578 55.8989 17.2578 44C17.2578 32.1011 20.4394 21.3973 25.5042 13.7128C30.5769 6.01614 37.4153 1.5 44.7578 1.5C52.1003 1.5 58.9387 6.01614 64.0115 13.7128C69.0763 21.3973 72.2578 32.1011 72.2578 44Z" stroke="currentColor" stroke-width="3"/>
					<path d="M54.2578 44C54.2578 56.0646 53.0338 66.9366 51.0808 74.7489C50.1014 78.6666 48.959 81.7306 47.7482 83.779C46.4781 85.9279 45.4189 86.5 44.7578 86.5C44.0968 86.5 43.0375 85.9279 41.7674 83.779C40.5566 81.7306 39.4143 78.6666 38.4349 74.7489C36.4818 66.9366 35.2578 56.0646 35.2578 44C35.2578 31.9354 36.4818 21.0634 38.4349 13.2511C39.4143 9.33343 40.5566 6.26943 41.7674 4.22098C43.0375 2.07212 44.0968 1.5 44.7578 1.5C45.4189 1.5 46.4781 2.07212 47.7482 4.22098C48.959 6.26943 50.1014 9.33343 51.0808 13.2511C53.0338 21.0634 54.2578 31.9354 54.2578 44Z" stroke="currentColor" stroke-width="3"/>
				</svg>
			</div>
			<span class="font-bold text-xl tracking-tight">Bioenergetic</span>
		</div>
		<nav class="flex items-center gap-6 text-sm font-medium">
			<a href="#features" class="text-gray-600 hover:text-gray-900">Features</a>
			<a href="#" class="bg-gray-100 px-4 py-2 rounded-lg text-gray-900 hover:bg-gray-200 transition-colors">Sign In</a>
		</nav>
	</header>

	<main>
		<!-- Hero Section -->
		<section class="max-w-4xl mx-auto px-6 pt-12 pb-20 text-center">
			<div class="inline-flex items-center gap-2 text-gray-500 text-sm mb-6">
				{@html icons.activity}
				<span>Web-based metabolic tracking</span>
			</div>
			
			<h1 class="text-5xl md:text-6xl font-bold tracking-tight text-gray-900 mb-6 leading-[1.1]">
				Clear metabolic insights through simple tracking
			</h1>
			
			<p class="text-xl text-gray-600 mb-10 max-w-2xl mx-auto">
				Track body temperature and heart rate to understand your metabolic health. Privacy-first, data-sovereign, and beautifully simple.
			</p>

			<div class="flex flex-col sm:flex-row items-center justify-center gap-4 mb-16">
				<a href="#" class="bg-gray-900 text-white px-8 py-3 rounded-xl font-medium hover:bg-gray-800 transition-colors">
					Start Tracking
				</a>
				<a href="#features" class="text-gray-600 px-8 py-3 rounded-xl font-medium hover:text-gray-900 transition-colors">
					Learn More
				</a>
			</div>

			<!-- App Interface Preview -->
			<div class="relative rounded-2xl border border-gray-200 shadow-2xl bg-white overflow-hidden mb-12">
				<div class="absolute inset-0 bg-gradient-to-br from-gray-50 to-white"></div>
				
				<!-- Mock Interface -->
				<div class="relative p-8 md:p-12">
					<!-- Quote at top -->
					<div class="text-center mb-8 text-sm text-gray-500 italic max-w-2xl mx-auto">
						"Energy and structure are interdependent at every level."
					</div>
					
					<!-- Navigation Tabs -->
					<div class="flex justify-center gap-2 mb-8 text-sm font-medium">
						<button class="px-4 py-2 bg-gray-900 text-white rounded-lg">Today</button>
						<button class="px-4 py-2 text-gray-600 hover:bg-gray-100 rounded-lg">Yesterday</button>
						<button class="px-4 py-2 text-gray-600 hover:bg-gray-100 rounded-lg">Day</button>
						<button class="px-4 py-2 text-gray-600 hover:bg-gray-100 rounded-lg">Week</button>
						<button class="px-4 py-2 text-gray-600 hover:bg-gray-100 rounded-lg">Month</button>
						<button class="px-4 py-2 text-gray-600 hover:bg-gray-100 rounded-lg">Year</button>
					</div>
					
					<!-- Metrics Display -->
					<div class="grid grid-cols-1 md:grid-cols-2 gap-6 max-w-3xl mx-auto mb-8">
						<!-- Temperature Card -->
						<div class="bg-gray-50 rounded-xl p-6 border border-gray-200">
							<div class="flex items-center gap-2 text-gray-600 mb-4">
								{@html icons.thermometer}
								<span class="text-sm font-medium">Body Temperature</span>
							</div>
							<div class="text-4xl font-bold text-gray-900 mb-2">98.6°F</div>
							<div class="text-sm text-primary-600">+0.3° from yesterday</div>
						</div>
						
						<!-- Heart Rate Card -->
						<div class="bg-gray-50 rounded-xl p-6 border border-gray-200">
							<div class="flex items-center gap-2 text-gray-600 mb-4">
								{@html icons.heart}
								<span class="text-sm font-medium">Heart Rate</span>
							</div>
							<div class="text-4xl font-bold text-gray-900 mb-2">72 bpm</div>
							<div class="text-sm text-primary-600">-2 bpm from yesterday</div>
						</div>
					</div>
					
					<!-- Additional Nav -->
					<div class="flex justify-center gap-6 text-sm font-medium text-gray-600">
						<button class="hover:text-gray-900">Statistics</button>
						<button class="hover:text-gray-900">Data Log</button>
						<button class="hover:text-gray-900">Export</button>
					</div>
				</div>
			</div>

			<!-- Bottom Icons -->
			<div class="flex flex-wrap justify-center gap-8 md:gap-12 text-sm font-medium text-gray-700">
				<div class="flex items-center gap-2">
					{@html icons.thermometer}
					<span>Temperature tracking</span>
				</div>
				<div class="flex items-center gap-2">
					{@html icons.heart}
					<span>Heart rate monitoring</span>
				</div>
				<div class="flex items-center gap-2">
					{@html icons.trendingUp}
					<span>Trend visualization</span>
				</div>
				<div class="flex items-center gap-2">
					{@html icons.shield}
					<span>Privacy-first</span>
				</div>
			</div>
		</section>

		<!-- Features Grid -->
		<section id="features" class="max-w-6xl mx-auto px-6 py-20">
			<h2 class="text-3xl md:text-4xl font-bold text-gray-900 mb-4 max-w-2xl leading-tight">
				Simple tracking. Powerful insights. Complete control.
			</h2>
			<p class="text-lg text-gray-600 mb-12 max-w-2xl">
				Bioenergetic gives you the tools to monitor metabolic signals without complexity or compromise.
			</p>

			<div class="grid grid-cols-1 md:grid-cols-3 gap-6">
				<!-- Card 1 -->
				<div class="bg-gray-50 p-8 rounded-2xl flex flex-col items-start h-64">
					<div class="mb-auto text-gray-900">
						{@html icons.shield}
					</div>
					<div>
						<h3 class="font-bold text-lg mb-2 text-gray-900">Your data, your choice</h3>
						<p class="text-sm text-gray-600 leading-relaxed">Keep data local on your device or sync to the cloud. You decide.</p>
					</div>
				</div>

				<!-- Card 2 -->
				<div class="bg-gray-50 p-8 rounded-2xl flex flex-col items-start h-64">
					<div class="mb-auto text-gray-900">
						{@html icons.barChart}
					</div>
					<div>
						<h3 class="font-bold text-lg mb-2 text-gray-900">Visualize trends</h3>
						<p class="text-sm text-gray-600 leading-relaxed">See patterns across Today, Yesterday, Day, Week, Month, and Year views</p>
					</div>
				</div>

				<!-- Card 3 -->
				<div class="bg-gray-50 p-8 rounded-2xl flex flex-col items-start h-64">
					<div class="mb-auto text-gray-900">
						{@html icons.download}
					</div>
					<div>
						<h3 class="font-bold text-lg mb-2 text-gray-900">Export & import</h3>
						<p class="text-sm text-gray-600 leading-relaxed">Full control with data export and import for backup or analysis</p>
					</div>
				</div>

				<!-- Card 4 -->
				<div class="bg-gray-50 p-8 rounded-2xl flex flex-col items-start h-64">
					<div class="mb-auto text-gray-900">
						{@html icons.thermometer}
					</div>
					<div>
						<h3 class="font-bold text-lg mb-2 text-gray-900">Temperature tracking</h3>
						<p class="text-sm text-gray-600 leading-relaxed">Monitor body temperature as a key metabolic signal</p>
					</div>
				</div>

				<!-- Card 5 -->
				<div class="bg-gray-50 p-8 rounded-2xl flex flex-col items-start h-64">
					<div class="mb-auto text-gray-900">
						{@html icons.heart}
					</div>
					<div>
						<h3 class="font-bold text-lg mb-2 text-gray-900">Heart rate monitoring</h3>
						<p class="text-sm text-gray-600 leading-relaxed">Track pulse as a window into metabolic function</p>
					</div>
				</div>

				<!-- Card 6 -->
				<div class="bg-gray-50 p-8 rounded-2xl flex flex-col items-start h-64">
					<div class="mb-auto text-gray-900">
						{@html icons.clock}
					</div>
					<div>
						<h3 class="font-bold text-lg mb-2 text-gray-900">Track over time</h3>
						<p class="text-sm text-gray-600 leading-relaxed">Build a comprehensive history to spot long-term patterns</p>
					</div>
				</div>
			</div>
		</section>

		<!-- How It Works Section -->
		<section class="max-w-6xl mx-auto px-6 py-20 bg-gray-50">
			<div class="mb-16">
				<span class="inline-block bg-primary-100 text-primary-700 px-3 py-1 rounded-full text-xs font-semibold uppercase tracking-wide mb-6">
					How it works
				</span>
				<h2 class="text-4xl md:text-5xl font-bold text-gray-900 mb-6 tracking-tight">
					Track. Visualize. Understand.
				</h2>
				<p class="text-xl text-gray-600 max-w-2xl leading-relaxed">
					A streamlined interface designed for daily metabolic monitoring inspired by bioenergetic principles.
				</p>
			</div>

			<div class="bg-white rounded-3xl p-8 md:p-12 mb-16 border border-gray-200">
				<!-- Time Period Navigation -->
				<div class="mb-12">
					<h3 class="text-lg font-bold text-gray-900 mb-4">Multiple time perspectives</h3>
					<div class="flex flex-wrap gap-3">
						<div class="bg-gray-900 text-white px-6 py-3 rounded-xl font-medium">Today</div>
						<div class="bg-gray-100 text-gray-700 px-6 py-3 rounded-xl font-medium">Yesterday</div>
						<div class="bg-gray-100 text-gray-700 px-6 py-3 rounded-xl font-medium">Day</div>
						<div class="bg-gray-100 text-gray-700 px-6 py-3 rounded-xl font-medium">Week</div>
						<div class="bg-gray-100 text-gray-700 px-6 py-3 rounded-xl font-medium">Month</div>
						<div class="bg-gray-100 text-gray-700 px-6 py-3 rounded-xl font-medium">Year</div>
					</div>
					<p class="text-sm text-gray-600 mt-4">Switch between time periods to spot patterns and track progress over different scales.</p>
				</div>

				<!-- Data Views -->
				<div class="grid grid-cols-1 md:grid-cols-3 gap-6 mb-12">
					<div class="bg-gray-50 rounded-xl p-6 border border-gray-200">
						<div class="flex items-center gap-2 text-gray-900 mb-3">
							{@html icons.barChart}
							<span class="font-bold">Statistics</span>
						</div>
						<p class="text-sm text-gray-600">View averages, trends, and statistical summaries of your metabolic data.</p>
					</div>

					<div class="bg-gray-50 rounded-xl p-6 border border-gray-200">
						<div class="flex items-center gap-2 text-gray-900 mb-3">
							{@html icons.database}
							<span class="font-bold">Data Log</span>
						</div>
						<p class="text-sm text-gray-600">Access your complete history of temperature and heart rate readings.</p>
					</div>

					<div class="bg-gray-50 rounded-xl p-6 border border-gray-200">
						<div class="flex items-center gap-2 text-gray-900 mb-3">
							{@html icons.trendingUp}
							<span class="font-bold">Visualizations</span>
						</div>
						<p class="text-sm text-gray-600">See your data as charts and graphs to identify patterns easily.</p>
					</div>
				</div>

				<!-- Data Control -->
				<div class="bg-primary-50 rounded-xl p-6 border border-primary-200">
					<h3 class="text-lg font-bold text-gray-900 mb-4">Complete data sovereignty</h3>
					<div class="grid grid-cols-1 md:grid-cols-2 gap-6">
						<div>
							<div class="flex items-center gap-2 text-primary-700 font-medium mb-2">
								{@html icons.shield}
								<span>Local or cloud storage</span>
							</div>
							<p class="text-sm text-gray-600">Choose to keep your data on your device only, or sync to the cloud with your Google account.</p>
						</div>
						<div>
							<div class="flex items-center gap-2 text-primary-700 font-medium mb-2">
								{@html icons.download}
								<span>Import & export</span>
							</div>
							<p class="text-sm text-gray-600">Back up your data, switch devices, or analyze in spreadsheets—your data, your way.</p>
						</div>
					</div>
				</div>
			</div>

			<div class="max-w-3xl">
				<h3 class="text-2xl font-bold text-gray-900 mb-6">Inspired by bioenergetic thinking</h3>
				<p class="text-lg text-gray-600 mb-4 leading-relaxed">
					Body temperature and heart rate serve as proxies for metabolic health, reflecting the efficiency of cellular energy production. This approach draws from Ray Peat–style bioenergetic principles.
				</p>
				<p class="text-gray-600 leading-relaxed">
					Track the effects of dietary changes, thyroid support, lifestyle modifications, and more—all with a tool that respects your privacy and gives you complete control over your health data.
				</p>
			</div>
		</section>

		<!-- Privacy & Control Section -->
		<section class="max-w-6xl mx-auto px-6 py-20">
			<div class="mb-16">
				<span class="inline-block bg-gray-100 text-gray-700 px-3 py-1 rounded-full text-xs font-semibold uppercase tracking-wide mb-6">
					Privacy & Control
				</span>
				<h2 class="text-4xl md:text-5xl font-bold text-gray-900 mb-6 tracking-tight">
					Your health data stays yours
				</h2>
				<p class="text-xl text-gray-600 max-w-2xl leading-relaxed">
					Bioenergetic is built with data sovereignty at its core. No lock-in, no forced cloud storage, no hidden data collection.
				</p>
			</div>

			<div class="grid grid-cols-1 md:grid-cols-2 gap-8 mb-12">
				<!-- Local Storage -->
				<div class="bg-gray-50 rounded-2xl p-8 border border-gray-200">
					<div class="w-12 h-12 bg-gray-900 rounded-xl flex items-center justify-center mb-6 text-white">
						{@html icons.shield}
					</div>
					<h3 class="text-2xl font-bold text-gray-900 mb-4">Local-first option</h3>
					<p class="text-gray-600 mb-6 leading-relaxed">
						Keep all your metabolic data stored locally on your device. No account required, no data ever leaves your control. Perfect for maximum privacy.
					</p>
					<ul class="space-y-3">
						<li class="flex items-start gap-3">
							<div class="text-primary-600 mt-0.5">{@html icons.check}</div>
							<span class="text-sm text-gray-600">No account creation needed</span>
						</li>
						<li class="flex items-start gap-3">
							<div class="text-primary-600 mt-0.5">{@html icons.check}</div>
							<span class="text-sm text-gray-600">Data never leaves your device</span>
						</li>
						<li class="flex items-start gap-3">
							<div class="text-primary-600 mt-0.5">{@html icons.check}</div>
							<span class="text-sm text-gray-600">Anonymous and private by default</span>
						</li>
					</ul>
				</div>

				<!-- Cloud Sync -->
				<div class="bg-gray-50 rounded-2xl p-8 border border-gray-200">
					<div class="w-12 h-12 bg-primary-600 rounded-xl flex items-center justify-center mb-6 text-white">
						{@html icons.database}
					</div>
					<h3 class="text-2xl font-bold text-gray-900 mb-4">Optional cloud sync</h3>
					<p class="text-gray-600 mb-6 leading-relaxed">
						Sign in with Google to sync your data across devices. Access your metabolic history from anywhere while maintaining control with export options.
					</p>
					<ul class="space-y-3">
						<li class="flex items-start gap-3">
							<div class="text-primary-600 mt-0.5">{@html icons.check}</div>
							<span class="text-sm text-gray-600">Sync across multiple devices</span>
						</li>
						<li class="flex items-start gap-3">
							<div class="text-primary-600 mt-0.5">{@html icons.check}</div>
							<span class="text-sm text-gray-600">Easy sign-in with Google</span>
						</li>
						<li class="flex items-start gap-3">
							<div class="text-primary-600 mt-0.5">{@html icons.check}</div>
							<span class="text-sm text-gray-600">Export data anytime</span>
						</li>
					</ul>
				</div>
			</div>

			<!-- Data Portability -->
			<div class="bg-gradient-to-br from-primary-50 to-white rounded-2xl p-8 md:p-12 border border-primary-100">
				<div class="max-w-3xl">
					<h3 class="text-2xl font-bold text-gray-900 mb-4">Full data portability</h3>
					<p class="text-lg text-gray-600 mb-8 leading-relaxed">
						Import and export your data freely. Back up to your own storage, analyze in spreadsheets, or migrate to other tools. No vendor lock-in, ever.
					</p>
					<div class="flex flex-wrap gap-4">
						<div class="flex items-center gap-2 text-gray-700 font-medium">
							{@html icons.download}
							<span>Export to CSV</span>
						</div>
						<div class="flex items-center gap-2 text-gray-700 font-medium">
							{@html icons.upload}
							<span>Import from files</span>
						</div>
						<div class="flex items-center gap-2 text-gray-700 font-medium">
							{@html icons.database}
							<span>Backup & restore</span>
						</div>
					</div>
				</div>
			</div>
		</section>

		<!-- Who uses it Section -->
		<section class="max-w-7xl mx-auto px-6 py-20 bg-gray-50">
			<div class="mb-16">
				<span class="inline-block bg-gray-100 text-gray-700 px-3 py-1 rounded-full text-xs font-semibold uppercase tracking-wide mb-6">
					Use cases
				</span>
				<h2 class="text-4xl md:text-5xl font-bold text-gray-900 mb-6 tracking-tight">
					Who uses Bioenergetic?
				</h2>
				<p class="text-xl text-gray-600 max-w-2xl leading-relaxed">
					From biohackers to those managing thyroid health, Bioenergetic serves anyone monitoring metabolic signals.
				</p>
			</div>

			<div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-6">
				<!-- Card 1 -->
				<div class="bg-white p-8 rounded-xl border border-gray-200 min-h-[220px] flex flex-col">
					<div class="text-primary-600 mb-4">
						{@html icons.sun}
					</div>
					<h3 class="font-bold text-lg text-gray-900 mb-3">Bioenergetic enthusiasts</h3>
					<p class="text-sm text-gray-600 mt-auto leading-relaxed">Track metabolic markers following Ray Peat–inspired principles to optimize cellular energy production.</p>
				</div>

				<!-- Card 2 -->
				<div class="bg-white p-8 rounded-xl border border-gray-200 min-h-[220px] flex flex-col">
					<div class="text-primary-600 mb-4">
						{@html icons.activity}
					</div>
					<h3 class="font-bold text-lg text-gray-900 mb-3">Thyroid health monitoring</h3>
					<p class="text-sm text-gray-600 mt-auto leading-relaxed">Monitor temperature and pulse as indicators of thyroid function and metabolic rate.</p>
				</div>

				<!-- Card 3 -->
				<div class="bg-white p-8 rounded-xl border border-gray-200 min-h-[220px] flex flex-col">
					<div class="text-primary-600 mb-4">
						{@html icons.trendingUp}
					</div>
					<h3 class="font-bold text-lg text-gray-900 mb-3">Diet experimentation</h3>
					<p class="text-sm text-gray-600 mt-auto leading-relaxed">Track how different foods, meal timing, and macronutrient ratios affect your metabolic markers.</p>
				</div>

				<!-- Card 4 -->
				<div class="bg-white p-8 rounded-xl border border-gray-200 min-h-[220px] flex flex-col">
					<div class="text-primary-600 mb-4">
						{@html icons.heart}
					</div>
					<h3 class="font-bold text-lg text-gray-900 mb-3">Stress monitoring</h3>
					<p class="text-sm text-gray-600 mt-auto leading-relaxed">Observe how stress, sleep, and lifestyle changes impact your resting heart rate and temperature.</p>
				</div>

				<!-- Card 5 -->
				<div class="bg-white p-8 rounded-xl border border-gray-200 min-h-[220px] flex flex-col">
					<div class="text-primary-600 mb-4">
						{@html icons.clock}
					</div>
					<h3 class="font-bold text-lg text-gray-900 mb-3">Circadian rhythm tracking</h3>
					<p class="text-sm text-gray-600 mt-auto leading-relaxed">Monitor daily temperature and pulse patterns to understand your circadian metabolic rhythms.</p>
				</div>

				<!-- Card 6 -->
				<div class="bg-white p-8 rounded-xl border border-gray-200 min-h-[220px] flex flex-col">
					<div class="text-primary-600 mb-4">
						{@html icons.barChart}
					</div>
					<h3 class="font-bold text-lg text-gray-900 mb-3">Health optimization</h3>
					<p class="text-sm text-gray-600 mt-auto leading-relaxed">Use objective data to guide lifestyle choices and track the effectiveness of health interventions.</p>
				</div>
			</div>
		</section>

		<!-- CTA Section -->
		<section class="max-w-4xl mx-auto px-6 py-20 text-center">
			<h2 class="text-4xl md:text-5xl font-bold text-gray-900 mb-6 tracking-tight">
				Start tracking your metabolic health
			</h2>
			<p class="text-xl text-gray-600 mb-10 max-w-2xl mx-auto">
				Simple, privacy-focused metabolic tracking. No hardware required, no subscriptions, no lock-in.
			</p>
			<div class="flex flex-col sm:flex-row items-center justify-center gap-4">
				<a href="#" class="bg-gray-900 text-white px-8 py-4 rounded-xl font-medium text-lg hover:bg-gray-800 transition-colors">
					Sign In with Google
				</a>
				<a href="#" class="text-gray-600 px-8 py-4 rounded-xl font-medium text-lg hover:text-gray-900 transition-colors">
					Try Locally
				</a>
			</div>
			<p class="text-sm text-gray-500 mt-6">
				Start with local storage or sync across devices—your choice.
			</p>
		</section>

		<!-- Footer -->
		<footer class="max-w-7xl mx-auto px-6 py-12 border-t border-gray-100">
			<div class="grid grid-cols-1 md:grid-cols-3 gap-8 mb-12">
				<div>
					<div class="flex items-center gap-2 mb-4">
						<div class="text-gray-900">
							<svg width="24" height="24" viewBox="0 0 89 88" fill="none" xmlns="http://www.w3.org/2000/svg">
								<circle cx="44.7578" cy="44" r="42.5" stroke="currentColor" stroke-width="3"/>
								<path d="M72.2578 44C72.2578 55.8989 69.0763 66.6027 64.0115 74.2872C58.9387 81.9839 52.1003 86.5 44.7578 86.5C37.4153 86.5 30.5769 81.9839 25.5042 74.2872C20.4394 66.6027 17.2578 55.8989 17.2578 44C17.2578 32.1011 20.4394 21.3973 25.5042 13.7128C30.5769 6.01614 37.4153 1.5 44.7578 1.5C52.1003 1.5 58.9387 6.01614 64.0115 13.7128C69.0763 21.3973 72.2578 32.1011 72.2578 44Z" stroke="currentColor" stroke-width="3"/>
								<path d="M54.2578 44C54.2578 56.0646 53.0338 66.9366 51.0808 74.7489C50.1014 78.6666 48.959 81.7306 47.7482 83.779C46.4781 85.9279 45.4189 86.5 44.7578 86.5C44.0968 86.5 43.0375 85.9279 41.7674 83.779C40.5566 81.7306 39.4143 78.6666 38.4349 74.7489C36.4818 66.9366 35.2578 56.0646 35.2578 44C35.2578 31.9354 36.4818 21.0634 38.4349 13.2511C39.4143 9.33343 40.5566 6.26943 41.7674 4.22098C43.0375 2.07212 44.0968 1.5 44.7578 1.5C45.4189 1.5 46.4781 2.07212 47.7482 4.22098C48.959 6.26943 50.1014 9.33343 51.0808 13.2511C53.0338 21.0634 54.2578 31.9354 54.2578 44Z" stroke="currentColor" stroke-width="3"/>
							</svg>
						</div>
						<span class="font-bold text-lg">Bioenergetic</span>
					</div>
					<p class="text-sm text-gray-600 leading-relaxed">
						Clear metabolic insights through streamlined tracking of body temperature and heart rate.
					</p>
				</div>

				<div>
					<h4 class="font-bold text-sm text-gray-900 mb-4">Product</h4>
					<div class="space-y-2 text-sm text-gray-600">
						<a href="#features" class="block hover:text-gray-900">Features</a>
						<a href="#" class="block hover:text-gray-900">Privacy</a>
						<a href="#" class="block hover:text-gray-900">Data Export</a>
						<a href="#" class="block hover:text-gray-900">Documentation</a>
					</div>
				</div>

				<div>
					<h4 class="font-bold text-sm text-gray-900 mb-4">Resources</h4>
					<div class="space-y-2 text-sm text-gray-600">
						<a href="#" class="block hover:text-gray-900">Getting Started</a>
						<a href="#" class="block hover:text-gray-900">Bioenergetic Principles</a>
						<a href="#" class="block hover:text-gray-900">Support</a>
						<a href="#" class="block hover:text-gray-900">Contact</a>
					</div>
				</div>
			</div>

			<div class="flex flex-col md:flex-row justify-between items-center pt-8 border-t border-gray-100 text-sm text-gray-500">
				<p>© 2025 Bioenergetic. All rights reserved.</p>
				<div class="flex gap-6 mt-4 md:mt-0">
					<a href="#" class="hover:text-gray-900">Terms</a>
					<a href="#" class="hover:text-gray-900">Privacy</a>
				</div>
			</div>
		</footer>

	</main>
</div>

