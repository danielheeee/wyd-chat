<script>
        export let show_navbar;
</script>

<img
    src="https://picsum.photos/100"
    alt=""
    class="
    fixed right-4 top-4
    w-12 h-12 p-2 rounded-full
    border-[0.5px] border-slate-700 
    hover:w-11 hover:h-11 duration-300 fly"
    on:mouseenter={() => (show_navbar = true)}
/>

<style>
    @keyframes fly {
        0% {
            transform: translateX(20vh);
        }
        100% {
            transform: translateX(0);
        }
    }

    .fly {
        animation: fly 1s ease 200ms backwards;
    }
</style>