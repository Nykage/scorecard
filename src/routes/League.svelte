<script>
import {league} from './data-league.js'
import {onMount} from 'svelte'

onMount( async() => {
    const url = 'https://scorecard-backend.truudeli15.net/back/get-events-league.php'
    let res = await fetch(url)
    res = await res.json()
    let data = await res.data
    $league = res.data
    console.log(res.data)
})
</script>

<div class="flex-container">
    {#each $league as event (event.league_id)}
        <div class="container">
        <span>{event.league_name}</span>
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