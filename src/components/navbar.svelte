<script>
    import { fly } from "svelte/transition";
    import Breadcrumbs from "./breadcrumbs.svelte";
    import Pfp from "./pfp.svelte";

    let show_navbar = false;
</script>

<Pfp bind:show_navbar/>
{#if show_navbar}
    <div
        on:mouseleave={() => {show_navbar = false }}
        in:fly={{ x: "100vw", duration: 800}}
        out:fly={{ x: "-100vw", duration: 800}}
        class="
        fixed w-screen h-20 
        z-2
        flex flex-row items-center justify-between
        top-0 -z-10 right-0 pl-6 pr-20
        bg-black"
    >
        <Breadcrumbs />
        <div class="flex flex-row items-center space-x-2">
            <div class="text-white">Chat</div>
            <div class="text-white">Memories</div>
        </div>
    </div>
{/if}
