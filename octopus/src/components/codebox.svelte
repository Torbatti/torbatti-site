<script>
    let currentLang =  "JavaScript";
    let languages = {
        "JavaScript" : ["JavaScript",""]
        ,"Php" : ["Php",""]
        ,"Rust" : ["Rust",""]
        ,"Go" : ["Go",""]
        ,"Haskell" : ["Haskell",""]
        ,"Python" : ["Python",""]
        ,"Ruby" : ["Ruby",""]
}
function langHandler(langValue){
    currentLang = langValue;
}
</script>

<codeBox>
    <div class="window">
        <div class="topBar w-[23rem] h-6 bg-slate-500 rounded-t-md flex items-center md:w-[40rem]">
            <div class="dots ml-3 w-2 h-2 rounded-full bg-red-400"></div>
            <div class="dots ml-2 w-2 h-2 rounded-full bg-amber-300"></div>
            <div class="dots ml-2 w-2 h-2 rounded-full bg-lime-300"></div>
        </div>
        <div class="Box w-[23rem] h-56 bg-slate-400 flex md:h-96 md:w-[40rem]">
        
            <div class="langs w-[7rem] h-56 md:h-96 md:w-32">
                <div class="langBox border-slate-700">
                    {#each Object.entries(languages)  as [lang,langValue]}
                        <div class="lang mt-1 md:mt-3 w-24 md:w-32 md:h-10 flex items-center pl-2" 
                            class:border-l-4="{currentLang == langValue[0]}" on:click={()=>{langHandler(langValue[0])}}
                            class:border-slate-800="{currentLang == langValue[0]}"
                        >
                            {langValue[0]}
                        </div>
                    {/each}
                </div>
            </div>

            <div class="codeBox w-[16rem] h-56 bg-zinc-800 md:h-96 md:w-[32rem]">
                {#each Object.entries(languages)  as [lang,langValue]}
                    <div class="showTag" class:hidden="{currentLang !== langValue[0]}" class:flex="{currentLang == langValue[0]}">
                        {langValue[1]}
                    </div>
                {/each}
            </div>
            
        </div>
    </div>
</codeBox>


<style>

</style>