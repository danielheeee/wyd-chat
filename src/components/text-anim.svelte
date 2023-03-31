<div class='drop-in'>
    <slot/>
</div>

<style>
    .drop-in {
        animation: drop-in 1s ease 200ms backwards;
    }

    @keyframes drop-in {
        from {
            opacity: 0;
            color: transparent;
            transform: translateY(-100px);
        }
        to {
            opacity: 1;
            color: black;
            transform: translate(0px);
        }
    }
</style>
