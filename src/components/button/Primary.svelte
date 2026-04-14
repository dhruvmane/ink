<style>
    * {
        display: inline-block;
        font-size: 12px;
        font-weight: 800;
    }

    .button-field {
        margin: 0;
        padding: 0;
    }

    button {
        margin: 0;
        padding: 20px 15px 20px 20px;
        background: white;
        border: 2px solid rgb(224, 224, 224);
        border-radius: 1px;
        transition: 0.2s ease-in-out;

        width: 250px;
    }

    button:hover {
        border: 2px solid black;
        transition: 0.2s ease-in-out;
    }

    .button-label {
        font-size: 15px;
        text-transform: capitalize;
    }

</style>
<script lang=ts>
    import { goto } from '$app/navigation';
    import btnHover from '../../lib/sounds/btnHover.wav'
    let { label, href }: any = $props()

    function onClick(href: string) {
        switch (href) {
            case undefined:
                return () => goto(`/not-found`);
            case href:
                return () => goto(`${href}`);
        }

    }

</script>
<main>
    <div class="button-field">
        <button title={label.toLowerCase()} onmouseenter={() => {const audio = new Audio(btnHover); audio.play();}} onclick={onClick(href)}><span class="button-label">{label.toUpperCase()}</span></button>
    </div>
</main>