<style>
    * {
        text-align: left;
        font-family: 'Chivo Mono';
    }

    .navBar {
        margin: 0;
        position: fixed;
        display: inline-block;
        top: 0;
        left: 0;
        height: 75px;
        min-width: 100vw;

        background: rgba(202, 202, 202, 0.1);
        backdrop-filter: blur(10px);
    }

    .button-left {
        margin: 0;
        margin-top: 13px;
        margin-right: 10px;
        padding: 12px;
        min-width: 50px;
        float: left;
    }
    
    .button-right {
        margin: 0;
        margin-top: 13px;
        margin-left: 10px;
        padding: 15px;
        min-width: 50px;
        float: right;
    }

    .right-button-field {
        margin-right: 30px;
        justify-content: flex-end;
    }
    
    .left-button-field {
        margin-left: 30px;
        justify-content: flex-start;
    }

    .button-label {
        transform: translate(0px, -15px);
        font-size: 15px;
    }

    button {
        height: 50px;
        border-radius: 100px;
        border: 0;

        text-align: center;
        font-size: 20px;
        transition: 0.1s ease-in-out;
    }

    button:hover {
        transition: 0.1s ease-in-out;
        background: rgb(112, 112, 112);
        color: white;
    }

</style>

<script lang=ts>
    let { leftButtons, rightButtons }: any = $props()
</script>

<main>
    <div class="navBar">
        <div class="right-button-field">
            {#if rightButtons}
                {#each rightButtons as button}
                    <button class="button-right" title={button.label}><p class="button-label">{button.label}</p></button>
                {/each}
            {/if}
        </div>
        <div class="left-button-field">
            {#if leftButtons}
                {#each leftButtons as button}
                    <button class="button-left" title={button.label}><p class="button-label">{button.label}</p></button>
                {/each}
            {/if}
        </div>
    </div>
</main>