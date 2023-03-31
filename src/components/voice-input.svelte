
<div
    class="fixed content-center w-full max-w-fit
            left-1/2 -ml-[28px] bottom-10 p-3
            border-[0.5px] border-slate-700 rounded-full 
            hover:p-2 hover:ml-[-24px] duration-300 
            fly-in
            "
>
    <svg
        width="30"
        height="30"
        stroke-width="0"
        class="hover:fill-current hover:text-slate-500 duration-300"
        xmlns="http://www.w3.org/2000/svg"
        viewBox="0 0 24 24"
        ><g
            ><path fill="none" d="M0 0h24v24H0z" />
            <path
                d="M12 3a3 3 0 0 0-3 3v6a3 3 0 0 0 6 0V6a3 3 0 0 0-3-3zm0-2a5 5 0 0 1 5 5v6a5 5 0 0 1-10 0V6a5 5 0 0 1 5-5zM2.192 13.962l1.962-.393a8.003 8.003 0 0 0 15.692 0l1.962.393C20.896 18.545 16.85 22 12 22s-8.896-3.455-9.808-8.038z"
            /></g
        ></svg
    >
</div>

<style>
    @keyframes flyInBottom {
        0% {
            transform: translateY(20vh);
        }
        100% {
            transform: translateY(0);
        }
    }

    .fly-in {
        animation: flyInBottom 1s ease 200ms backwards;
    }
</style>
