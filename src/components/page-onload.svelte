<div class="z-9999">
    <div class="absolute w-screen h-[40%] bg-orange-200 bar-1 top-0" />
    <div class="absolute w-screen h-[40%] bg-orange-300 bar-1 top-[33%]" />
    <div class="absolute w-screen h-[40%] bg-orange-400 bar-1 top-[66%]" />
    <div class="absolute w-screen h-[40%] bg-orange-500 bar-1 top-[100%]" />
</div>

<style>
    @keyframes slideInLeft {
        0% {
            transform: rotateX(0deg);
        }
        100% {
            transform: rotateX(90deg);
        }
    }

    .bar-1 {
        animation: slideInLeft 1s ease 200ms forwards;
    }
</style>
