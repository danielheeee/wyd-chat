<div
    class="scroll-fade-out text-2xl font-semibold leading-9 min-h-[200vh] overflow-hidden"
    on:scroll={() => console.log("scrolling")}
>
    <slot />
</div>

<style>
    .scroll-fade-out {
        background-image: linear-gradient(
            transparent 0,
            black 15%,
            black 85%,
            transparent 100%
        );
        background-clip: text;
        -webkit-background-clip: text;
        background-attachment: fixed;
    }

    .scroll-fade-out :global(*) {
        color: transparent;
        line-height: 2.6;
    }
</style>
