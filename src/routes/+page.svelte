<style>
    @import url('https://fonts.googleapis.com/css2?family=Chivo+Mono:ital,wght@0,100..900;1,100..900&display=swap');

    .title-card {
        margin-top: 25vh;
    }

    h1 {
        margin: 0;
        padding: 0;
        font-size: 100px;
        letter-spacing: -10px;
    }

    h2 {
        margin: 0;
        margin-top: -13px;
        margin-bottom: 40px;
        padding: 0;
        font-family: 'Chivo Mono';
        font-weight: 200;
    }


</style>
<script>
    import '../App.css'
    import Navbar from '../components/Navbar.svelte'
    import PrimaryButton from '../components/button/Primary.svelte'


</script>
<main>
    <div>
        <Navbar rightButtons={[{label:"Sign In"}]}/>
        <div class="title-card">
            <h1>Ink</h1>
            <h2>Open Source Screenwriting Application.</h2>
        </div>
        <div class="file-explorer">
            <PrimaryButton label="Create New Script" href="/create"/>
            <PrimaryButton label="Open Existing Script"/>
        </div>
    </div>
</main>