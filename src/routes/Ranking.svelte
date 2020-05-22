<script>
import {ranking} from './data-ranking.js'
import {onMount} from 'svelte'

onMount( async() => {
    const url = 'https://scorecard-backend.truudeli15.net/back/get-events-ranking.php'
    let res = await fetch(url)
    res = await res.json()
    let data = await res.data
    $ranking = res.data
    console.log(res.data)
})

if (performance.navigation.type == 1) {
	console.info( "This page is reloaded" );
	window.location.replace("https://scorecard-piia.netlify.app/");
} else {
	console.info( "This page is not reloaded");
}
</script>

<div class="flex-container">
    {#each $ranking as event (event.ranking_id)}
        <div class="container">
        <span>{event.contest_name}</span>
        </div>
    {/each}
</div>

<style>
    .flex-container {
        display: flex;
        margin: 0 auto;
        flex-flow: wrap;
        align-items: center;
        max-width: 1000px;
        justify-content: space-around;
    }

    .container {
        font-size: 30px;
        color: #8372e6;
        padding: 1rem;
        box-sizing: border-box;
        align-items: center;
        flex: auto;
        max-width: 250px;
        cursor: pointer;
        text-align: center;
    }

    .container:hover {
        background-color: rgb(206, 204, 204);
    }

    .container span {
        text-align: center;
    }

	@media all and (max-width: 400px) {
        .flex-container {
            flex-direction: column;
        }

        .container span {
            text-align: center;
        }
    }
</style>