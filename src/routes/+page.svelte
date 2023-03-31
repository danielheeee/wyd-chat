<script>
    import Navbar from "../components/navbar.svelte";
    import PageOnload from "../components/page-onload.svelte";
    import ScrollFadeOut from "../components/scroll-fade-out.svelte";
    import TextAnim from "../components/text-anim.svelte";
    import VoiceInput from "../components/voice-input.svelte";
</script>

<PageOnload />
<Navbar />
<div class="flex content-center px-6 mt-[10vh] lg:px-[30vw]">
    <ScrollFadeOut>
        <TextAnim>
            Whose woods these are I think I know. His house is in the village
            though; He will not see me stopping here To watch his woods fill up
            with snow.
        </TextAnim>
        <TextAnim>
            My little horse must think it queer To stop without a farmhouse near
            Between the woods and frozen lake The darkest evening of the year.
            He gives his harness bells a shake To ask if there is some mistake.
            The only other sound’s the sweep Of easy wind and downy flake. The
            woods are lovely, dark and deep, But I have promises to keep, And
            miles to go before I sleep, And miles to go before I sleep
        </TextAnim>
    </ScrollFadeOut>
    <VoiceInput />
</div>
