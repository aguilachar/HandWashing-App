<script>
    import Timer from "./Timer.svelte";
    import HowTo from "./HowTo.svelte";
</script>

<h1>Handwashing App</h1>

<Timer />

<HowTo />

<h6>
    <a href="https://www.who.int/gpsc/clean_hands_protection/en/">Image Source</a>
</h6>

<style>
    h1 {
        text-align: center;
        background-color: aliceblue;
        font-family: 'Lato', -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue';
    }

    h6 {
        text-align: center;
        font-weight: 350;
        border-radius: 4rem;
        margin-top: 0.5rem;
        font-size: 0.5rem;

    }
</style>