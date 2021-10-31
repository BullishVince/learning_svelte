<script>
    import ProgressBar from './ProgressBar.svelte';
    
    const totalSeconds = 20;
    let secondsLeft = totalSeconds;

    let isRunning = false;
    function startTimer() {
        isRunning = true;
        let timer = setInterval(() => {
        secondsLeft -= 1;
        if (secondsLeft <= 0) {
            clearInterval(timer);
            isRunning = false;
            secondsLeft = totalSeconds;
        }
    },1000);

    }
</script>

<style>
    h2 {
        margin: 0;
    }
    .start {
        background-color: rgb(154, 73, 73);
        width: 100%;
        margin: 10px 0;
    }
    button:disabled {
        background-color: rgb(194,194,194);
        cursor: not-allowed;
    }
</style>

<div bp="grid">
    <h2 bp="offset-5@md 4@md 12@sm">Seconds Left: {secondsLeft}</h2>
</div>
<ProgressBar />

<div bp="grid">
    <button bp="offset-5@md 4@md 12@sm" 
        class="start"
        disabled={isRunning}
        on:click={startTimer}>Start</button>
</div>