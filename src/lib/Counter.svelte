<script>
    let message = "";
    let count = 0;
    const updateClicks = () => {
        if (count < 5) {
            count++
        } else {
             message = "You have reached maximum count"
        }
    }
</script>

{#if message}
    <p class="message">{message}</p>
{/if}
<div></div>
<div>
    <button on:click="{updateClicks}"><strong>{count}</strong> {count === 1 ? "Click" : "Clicks"}
    </button>
</div>

<style>
    button {
        padding: 12px 22px;
        background-color: #3a5b5b;
        outline: none;
        border-radius: 5px;
        border: none;
        color: white;
        font-size: 1.0125rem;
        text-align: center;
        width: 125px;
    }

    .message {
        background-color: #c5f8bd;
        padding: 8px;
    }
</style>