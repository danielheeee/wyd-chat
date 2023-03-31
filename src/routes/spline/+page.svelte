<script>
    import ScrollFadeOut from "../components/scroll-fade-out.svelte";
    import * as THREE from "three";
    import * as SC from "svelte-cubed";
    import SplineLoader from "@splinetool/loader";
    import { onMount } from "svelte";

    let model;

    // import spline scene
    const loader = new SplineLoader();

    onMount(() => {
        loader.load(
            "https://prod.spline.design/mdUgwHJT1OGxImYZ/scene.splinecode",
            (splineScene) => {
                model = splineScene;
            }
        );
    });

    let spin = 0;

    SC.onFrame(() => {
        spin += 0.001;
    });
</script>

<div>
    <div class="canvas">
        <SC.Canvas
            antialias
            background={new THREE.Color("#ebebeb")}
            shadows={THREE.PCFShadowMap}
        >
            <SC.Primitive
                object={model}
                scale={[1, 1, 1]}
                position={[0, 0, 0]}
                rotation={[0, spin, 0]}
            />
    
            <SC.PerspectiveCamera position={[1000, 300, 300]} />
            <SC.HemisphereLight intensity={0.75} color="#eaeaea" />
        </SC.Canvas>
    </div>
    <div class="flex flex-row justify-center mt-[20vh] max-h-screen">
        <div class="max-w-lg">
            <ScrollFadeOut>
                <p>
                    POLAにも、たくさんのお母さんが働いています。
                    もちろん、お母さんになることを選ばない人も、
                    選びたくても選べなかった人もいます。
                    その多様な生き方や価値観こそ、かけがえのない財産。
                    私たちは、そう強く信じています。
                    POLAで働くお母さんにできることは何か。
                    POLAが、世の中のお母さんにできることは何か。
                    シングルマザーなど、
                    さまざまなお母さんが働きやすい環境づくり。
                    法律が認める養子縁組にとどまらず、
                </p>
            </ScrollFadeOut>
        </div>
    </div>
</div>

<style>
    .canvas {
        width: 100vw;
        height: 100vh;
        position: fixed;
        top: 0;
        left: 0;
        z-index: -1;
    }
</style>
