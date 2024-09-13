<script>
    import SectionWrapper from "./SectionWrapper.svelte";

    let faqs = [
        {
            question: "How do I book a room?",
            answer: "To book a room, please visit our website, select the desired dates, room type, and desired number of guests. You will then be able to complete the booking process."
        },
        {
            question: "What is the cancellation policy?",
            answer: "We offer a 14-day cancellation policy. If you wish to cancel your booking, please contact our customer service team within 14 days of your booking date. Upon cancellation, we will refund your deposit."
        },
        {
            question: "How do I secure my booking?",
            answer: "To secure your booking, please provide your full name, contact information, and a valid payment method. We will then verify your information and process your booking."
        },
        {
            question: "What is the check-in and check-out time?",
            answer: "Check-in time is 10 AM, and we will check out your booking in the future" 
        }
    ]
</script>
<SectionWrapper id="faqs">
    <div
        class="flex flex-col gap-10 sm:gap-14 md:gap-24 py-20 flex-1 items-center justify-center"
    >
        <div class="flex flex-col gap-2">
            <p class="opacity-60 text-base sm:text-lg md:text-xl text-center">
                For all your questions, qualms and queries
            </p>
            <h3
                class="text-4xl sm:text-5xl md:text-6xl max-w-[1000px] mx-auto w-full font-semibold text-center"
            >
                Frequently Asked Questions
            </h3>
        </div>
        <div class="flex flex-col gap-8 sm:gap-10 md:gap-14 w-full">
            {#each faqs as faq}
                <div class="flex flex-col gap-2 text-left max-w-[800px] w-full mx-auto relative p-4 px-6">
                    <div class="absolute top-0 left-0 w-1/3 h-[1px] bg-slate-950 -translate-x-4"></div>
                    <div class="absolute top-0 left-0 h-2/3 w-[1px] bg-slate-950 -translate-y-4"></div>
                    <h4 class="text-lg sm:text-xl md:text;2xl pt-2">
                        {faq.question}
                    </h4>
                    <p class="pl-2">{faq.answer}</p>
                </div>
            {/each}
        </div>
    </div>
</SectionWrapper>