<script lang="ts">
  import { onMount } from "svelte";

    export function navigateToInputSymptoms() {
        window.location.href = "/input-symptoms";
    }
    export function navigateToCoughTest() {
        window.location.href = "/cough-test";
    }

    onMount(() => {
        (document.getElementsByClassName("plot-wrapper")[0] as HTMLDivElement).style.width = "100%";
    });
</script>

<link rel="stylesheet" href="/css/home.css"/>

<div class="bg">
    <div class="gradient"></div>
    <div class="plot-wrapper">
        <img class="plot" src="/img/plot.svg"/>
    </div>
    <span class="caption">Soundwave of a cough</span>
</div>
<div class="left-container">
    <h1>
        Detect Covid<img src="/img/logo.svg"/>
    </h1>
    <h2>With just a cough</h2>
    <p>
        Rapidly improving AI technology now allows the diagnosis<br>of COVID-19 from a cough with an accuracy of 85%,<br>and it is only getting better. Try it out yourself now.
    </p>
    <p>
        Additionally, you can input your symptoms directly<br>which can diagnose you as symptomatic for COVID-19<br> with a 95% accuracy. Learn more <a on:click={() => {window.location.href = "/guide"}}>here.</a>
    </p>
    <p>
        If you need help taking the tests, view the <a on:click={() => {window.location.href = "/guide"}}>guide.</a>
    </p>
    <div>
        <button on:click={navigateToCoughTest}>
            Cough Test
        </button>
        <button on:click={navigateToInputSymptoms}>
            Input Symptoms
        </button>
    </div>
</div>
