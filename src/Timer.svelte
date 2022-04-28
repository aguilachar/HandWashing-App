<div bp="grid">
    <h2 bp="offset-5@md 4@md 12@sm">
        Seconds Left: {secondsLeft}</h2>

</div>

<ProgressBar {progress} />

<div bp="grid">
    <button 
    on:click={startTimer} 
    disabled={isRunning} 
    bp="offset-5@md 4@md 12@sm"
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

    .start[disabled] {
        background-color: rgb(157, 157, 157);
        cursor: not-allowed;
    }
    
    </style>

<script>
    import ProgressBar from "./ProgressBar.svelte";

    const totalSeconds = 20;
    let secondsLeft = totalSeconds;
    
    function startTimer() {
        isRunning = true;
        const timer = setInterval(() => {
        secondsLeft -=1;
        if (secondsLeft == 0) {
            clearInterval(timer);
            isRunning = false;
            secondsLeft = totalSeconds;
        }
    }, 1000);
 }

    let isRunning = false;
    $: progress = ((totalSeconds - secondsLeft) / totalSeconds) * 100;

</script>