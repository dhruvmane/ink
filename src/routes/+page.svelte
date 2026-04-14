<style>
    @import url('https://fonts.googleapis.com/css2?family=Chivo+Mono:ital,wght@0,100..900;1,100..900&display=swap');

    * {
        scrollbar-width: thin;
    }

    .title-card {
        margin-top: 14vh;
    }

    img {
        margin: 0;
        padding: 0;
        margin-bottom: 40px;
    }

    .subtitle {

        margin-top: 22px;

        h2 {
            margin: 0;
            margin-top: -37px;
            margin-bottom: 40px;
            padding: 0;
            font-family: 'Chivo Mono';
            font-weight: 200;
        }
    
    }

    

    

</style>
<script>
    import '../App.css'
    import Navbar from '../components/Navbar.svelte'
    import FileExplorer from '../components/FileExplorer.svelte';

    import wordMark from '$lib/icons/wordmark.svg'
    import searchIcon from '$lib/icons/search.svg'

</script>
<main>
    <div>
        <Navbar rightButtons={[{label:"Sign In."}]}/>
        <div class="title-card">
            <img src={wordMark} alt="Ink.">
            <div class="subtitle">
                <h2>Free Screenwriting Software.</h2>
                <h2> by Writers, for Writers. </h2>
            </div>
        </div>
        <FileExplorer />
    </div>
</main>