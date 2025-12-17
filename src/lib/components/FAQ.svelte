<script>
	let openIndex = 0;
	const faqs = [
		{
			question: "How does CukaiMax work?",
			answer: "CukaiMax uses AI to automatically scan and categorize your receipts into LHDN relief categories. Simply upload a photo of your receipt throughout the year, and we'll track everything for you. When tax season arrives, export your LHDN-ready summary in minutes."
		},
		{
			question: "Is my financial data secure?",
			answer: "Absolutely. We use bank-grade AES-256 encryption, are PDPA compliant, and store all data exclusively on Malaysian servers. Your data is protected with the same security standards used by financial institutions, and we never share or sell your information."
		},
		{
			question: "What LHDN relief categories does CukaiMax support?",
			answer: "CukaiMax supports all 40+ LHDN relief categories including Lifestyle, Medical, Books & Journals, Parents, Insurance, EPF, PRS, Education, and many more. Our AI automatically categorizes receipts into the correct bucket and tracks your relief caps."
		},
		{
			question: "Can I try CukaiMax for free?",
			answer: "Yes! Our free tier includes 20 receipt uploads, real-time deduction tracking, refund estimator, and 7-year secure storage. No credit card required. Upgrade to Premium (RM99/year) for unlimited uploads and LHDN-ready exports."
		},
		{
			question: "How long does CukaiMax store my receipts?",
			answer: "We automatically store your receipts securely for 7 years, which aligns with Malaysian tax document retention requirements. You can export or delete your data anytime."
		},
		{
			question: "Does CukaiMax integrate with LHDN e-Filing?",
			answer: "CukaiMax generates LHDN-ready CSV and PDF summary files that you can use directly with LHDN e-Filing. We organize all your deductions by category, making tax filing quick and easy."
		}
	];
</script>

<section class="py-24">
	<div class="mx-auto max-w-[1400px] px-6">
		<div class="grid grid-cols-1 gap-16 lg:grid-cols-12">
			<!-- Left Side -->
			<div class="lg:col-span-4">
				<div class="mb-4 text-[10px] font-bold tracking-widest text-gray-500 uppercase">[06] FAQ</div>
				<h2 class="mb-6 text-4xl font-medium tracking-tight text-gray-900">Your questions, answered</h2>
				<p class="mb-8 text-lg leading-relaxed text-gray-600">
					Have more questions? We're here to help. Contact us at hello@cukaimax.com for personalized support.
				</p>
				<a href="mailto:hello@cukaimax.com" class="inline-block bg-gray-900 px-6 py-3 text-[11px] font-bold tracking-widest text-white transition-colors hover:bg-gray-800 uppercase">
					Contact Support
				</a>
			</div>

			<!-- Right Side (Accordion) -->
			<div class="lg:col-span-8">
				<div class="divide-y divide-gray-200 border-t border-b border-gray-200">
					{#each faqs as faq, i}
						<div class="group">
							<button 
								class="flex w-full items-center justify-between py-6 text-left focus:outline-none"
								onclick={() => openIndex = openIndex === i ? -1 : i}
							>
								<span class="text-lg font-medium text-gray-900">{faq.question}</span>
								<span class="ml-4 flex h-6 w-6 items-center justify-center text-gray-400">
									{#if openIndex === i}
										<svg width="12" height="12" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M18 6L6 18M6 6l12 12"/></svg>
									{:else}
										<svg width="12" height="12" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M12 5v14M5 12h14"/></svg>
									{/if}
								</span>
							</button>
							{#if openIndex === i}
								<div class="pb-6 text-gray-600 leading-relaxed">
									{faq.answer}
								</div>
							{/if}
						</div>
					{/each}
				</div>
			</div>
		</div>
	</div>
</section>