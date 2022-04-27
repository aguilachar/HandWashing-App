<div bp="grid">
<h2 bp="offset-5@md 4@md 12@sm">
Seconds Left:

</h2>

</div>

<ProgressBar />

<div bp="grid">
    <button bp="offset-5@md 4@md 12@sm"
    class="start">Start</button>
</div>

<style>
    h2 {
        margin: 0;
    }

    .start {
        background-color: steelblue;
        width: 100%;
        margin: 10px 0;
    }
    
    </style>

<script>
    import ProgressBar from "./ProgressBar.svelte";
</script>