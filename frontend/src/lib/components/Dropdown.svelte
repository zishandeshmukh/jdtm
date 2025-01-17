<script>
    export let data = ['Empty']
    export let title='Title'
    export let value=null   
    let selected=false
</script>

<div class="flex w-64 flex-col gap-2 items-left p-3 rounded-lg bg-blue-100">
    <div class="pl-2">{title}</div>
     <div class="relative group">
        <div class="w-full h-full px-3 py-1 rounded-lg focus:outline-none cursor-default select-none bg-white {selected?"text-gray-800":"text-gray-400"}" >{value}</div>
        <div class="absolute top-full  left-0 w-full pt-2   items-left opacity-0 group-hover:opacity-100   transition-all duration-200 z-50">
            <div class="flex flex-col flex-col gap-1 p-2 rounded-xl bg-white overflow-y-auto h-0 group-hover:h-32  transition-all duration-200">
                {#each data as item}
                    <button on:click={()=>{selected=true;value=item}} class="hover:bg-gray-100 hover:shadow-lg hover:border-gray-300 rounded-lg pl-3 py-1 text-left">{item}</button>
                {/each}
            </div>
        </div>
     </div>
</div>
