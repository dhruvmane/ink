<script lang=ts>

    let scripts: {label: string}[] = []
</script>
<main>
    <div class="file-explorer">
            <div class="search-bar">
                <span>🔍</span>
                <input type="text" placeholder="Search for your script..">
            </div>
            <button class="create-new-button">+</button>
            <button class="create-new-button">🗑</button>

            <div class="files">
                {#each scripts as script}
                    <div class="file">
                        <div class="file-info">
                            <p>{script.label}</p>
                        </div>
                    </div>
                {/each}
            </div>
    
    </div>
</main>
<style>
    button {
        padding: 10px 10px;
        cursor: pointer;
    }
    
    .file-explorer {

        display: flex;
        flex-wrap: wrap;
        gap: 10px;
        
        box-sizing: border-box;
        
        margin: 0;
        padding: 10px;
        
        justify-self: center;
        
        width: 550px;

        border-radius: 24px;
        background: rgb(192, 192, 192);
        

        .files {
            display: flex;
            flex-wrap: wrap;

            background: rgb(243, 243, 243);
            min-height: 200px;
            width: 550px;

            border-radius: 24px;

            margin: 10px;

            padding-top: 12px;
            padding-bottom: 12px;

        }
        
        
        .create-new-button {

            align-self: left;
            
            box-sizing: border-box;
            
            height: 40px;
            width: 40px;
            
            margin: 0;
            padding: 0;
            
            margin-top: 10px;
            
            font-size: 30px;

            border: none;
            border-radius: 22px;
        }

        .search-bar {

            text-align: left;
            padding-left: 12px;
            padding-top: 1px;
            
            margin: 10px 5px;

            height: 40px;
            width: 400px;

            background: white;
            border: none;
            border-radius: 22px;

            input {
                text-align: left;
                border: none;
                height: 40px;
                width: 80%;
                box-sizing: border-box;
                
                font-size: 15px;
            }            

            input:focus {
                outline: none
            }

            span {
                margin: 0px 3px;
                filter: saturate(0%);
                font-size: 14px;
            }
        }

    }
</style>