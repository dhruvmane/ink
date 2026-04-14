<style>
    @import url('https://fonts.googleapis.com/css2?family=Courier+Prime:ital,wght@0,400;0,700;1,400;1,700&display=swap');

    :root {
        --font-size: 12px;
    }

    * {
        display: grid;
    }

    .document {
        font-family: 'Courier Prime';
        font-size: var(--font-size);

        justify-self: center;
        margin: 70px;
        padding: 100px;
        height: 1123px;
        width: 694px;
    }

</style>
<script>
    // import Navbar from '../../components/Navbar.svelte'
    
    // Import Icons
    // import backIcon from '../../lib/icons/back.svg'

    // Navbar Buttons
    // const leftButtonsList = [{label:"Home Page", href:"/"}]
</script>
<main>
    <div contenteditable="true" class="document"></div>
</main>
