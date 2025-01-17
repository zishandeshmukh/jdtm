<script>
	import { districts } from '$lib/districts.js';
    import Dropdown from '$lib/components/Dropdown.svelte';
    import { flip } from 'svelte/animate';
	import { dndzone } from 'svelte-dnd-action';
    import {types} from '$lib/type.js'
    
	function handleDndConsider(e) {
		items = e.detail.items;
	}
	function handleDndFinalize(e) {
		items = e.detail.items;
	}

    let inputClass="mt-1 p-2 pl-3 rounded-lg w-full"
    let from='City/ Location',to='City/ Location'
    let items=[]
    let itemName='',itemWeight=0,itemType='Item Type',date=0,time=0
    function addItem(){
        items=[...items,{
            id:items.length+1,
            name:itemName,
            weight:itemWeight,
            type:itemType,
            from:from,
            to:to,
            date:date,
            time:time
        }]
    }
</script>

<div  class="px-0 md:px-10 font-semibold py-3 bg-gray-200 flex flex-col overflow-y-hidden " style="max-width:100vw;">
    <div class="flex flex-col justify-around gap-4 mx-auto w-full md:w-5/6 overflow-y-hidden">
        
        <!-- ye header hai -->
        <div class="px-3 py-5 flex text-white text-xl flex-row bg-teal-600 rounded-lg items-center justify-between"  style="max-height:12svh;">
            <div class="flex  flex-row gap-4 justify-around items-center">
                <img src="" alt="logo">
                <div class=" text-2xl px-2 font-semibold">Jivandeep Travels</div>
            </div>
            <div class="flex flex-row gap-6 justify-around items-center">
                <button>Person</button>
                <button>Parcel</button>
                <button>Help</button>
            </div>
            <div class="flex flex-row gap-2 justify-around items-center p-2 rounded-xl bg-white">
                <img src="" alt="">
            </div>
        </div>

        <!-- ye hai ticket system -->

        <div class="px-3 py-5 flex  flex-col text-black text-lg  bg-white overflow-x-auto rounded-lg items-center justify-between" >
            
            <div class="w-full flex flex-row  gap-2 pb-4 ">

                <div class="flex flex-col gap-2 items-left p-3 w-3/5 rounded-lg bg-blue-100">
                    <div class="pl-2">Item name</div>
                    <div class="flex flex-col relative">
                        <input bind:value={itemName} class="w-full h-full p-2 rounded-lg focus:outline-none" placeholder="Item">                        
                    </div>
                </div>

                <div class="flex flex-col gap-2 items-left p-3 rounded-lg bg-blue-100 w-1/5">
                    <div class="pl-2">Weight (Kg)</div>
                    <div class="flex flex-col relative">
                        <input bind:value={itemWeight} class="w-full h-full p-2 rounded-lg focus:outline-none" type="number" min=0 placeholder="Weight">                        
                    </div>
                </div>

                <Dropdown title="Item type" bind:value={itemType} data={types}></Dropdown>
                
            </div>
            
            <div class="w-full flex flex-row justify-around gap-2">

                <Dropdown title="From" bind:value={from} data={districts}></Dropdown>

                <Dropdown title="To" bind:value={to} data={districts}></Dropdown>


                <div class="flex flex-col gap-2 items-left p-3 rounded-lg bg-blue-100">
                    <div class="pl-2">Date</div>
                    <div class="flex flex-col relative">
                        <input bind:value={date} class="w-full h-full p-2 rounded-lg focus:outline-none" type="date" placeholder="Date">
                    </div>
                </div>

                <div class="flex flex-col gap-2 items-left p-3 rounded-lg bg-blue-100">
                    <div class="pl-2">Time</div>
                    <div class="flex flex-col relative">
                        <input bind:value={time} class="w-full h-full p-2 rounded-lg focus:outline-none" type="time" placeholder="Time">
                    </div>
                </div>

                <button on:click={addItem} class="text-3xl flex flex-grow px-6 rounded-xl items-center text-center justify-center bg-blue-400 text-white">
                    +
                </button>
            </div>

            <div class="w-full flex flex-row pt-1 rounded-xl my-5 bg-gray-300/50"></div>

            <div class="w-full flex flex-row justify-between gap-3 overflow-y-hidden" style="max-height:400px;">
                <div class="w-1/2 flex flex-row  bg-gray-200 rounded-lg ">
                    <div class="flex flex-col p-5 items-left w-full">
                        <div class="block text-gray-700 pl-2">Name</div>
                        <input type="text" class={inputClass} placeholder="Name"/>
                        
                        <div class="block text-gray-700 mt-2 pl-2">Mobile</div>
                        <input type="text" class={inputClass} placeholder="Mobile"/>
                
                        <div class="block text-gray-700 mt-2 pl-2">Email</div>
                        <input type="email" class={inputClass} placeholder="Email"/>
                
                        <div class="block text-gray-700 mt-2 pl-2">Address</div>
                        <input type="text" class={inputClass} placeholder="Address"/>
                    </div>
                    
                </div>
    
                <div 

                use:dndzone={{items, flipDurationMs:200,dropTargetStyle:{}}} 
                on:consider={handleDndConsider} 
                on:finalize={handleDndFinalize}                

                class="w-1/2 flex flex-col bg-gray-200 rounded-2xl p-2 gap-3 overflow-y-auto">
                    {#each items as item, index (item.id)}
                        <div animate:flip="{{duration: 200}}"  class="relative outline-none group cursor-move flex flex-row gap-2 p-2 rounded-lg bg-white">
                            <div class="text-left">{index+1}.</div>
                            <div class="text-left">Name : {item.name}, Type : {item.type} <br> Weight : {item.weight} Kg, From : {item.from}, To : {item.to} <br> Date : {item.date}, Time : {item.time}</div>
                            <div class="hover:cursor-pointer opacity-0 group-hover:opacity-100 transition-all duration-300 absolute top-0 right-0 p-2">
                                <button on:click={()=>{items.splice(index,1);items=items;}} class="text-red-500 hover:bg-red-500 px-2 py-1 rounded-2xl hover:text-white transition-all duration-200 hover:scale-105 transform">✕</button>
                            </div>
                        </div>
                    {/each}
                </div>
            </div>

        </div>
        
    </div>
</div>