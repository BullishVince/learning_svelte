<script>
    import HowTo from './HowTo.svelte';
    import Timer from './Timer.svelte';

    let audio;

    function timerEnds(e) {
        console.log(e);
        audio.play();
    }
</script>

<style>
    h1, h3 {
        text-align: center;
    }
</style>

<h1>Handwashing App</h1>

<Timer on:end={timerEnds}/>

<HowTo />
<h3>
    <a href="https://www.unwater.org/app/uploads/2020/03/handwashing.png">Picture Source</a>
    <a href="https://freesound.org/people/jobro/sounds/60443">Sound Source</a>
</h3>>

<audio bind:this={audio}>
    <source src="tada.wav" />
</audio>