<div  class="px-10 py-3 bg-gray-200 flex flex-col overflow-y-hidden" style="width:100vw;height:100vh;">
    <div class="flex flex-col justify-around gap-4 mx-auto w-5/6 overflow-y-hidden">
        
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

        <div class="px-3 py-5 flex overflow-y-auto flex-col text-black text-lg  bg-white rounded-lg items-center justify-between" style="max-height:82svh;">
            
            <div class="w-full flex flex-row  gap-2 pb-4">

                <div class="flex flex-col gap-2 items-left p-3 w-3/5 rounded-lg bg-blue-100">
                    <div class="pl-2">Item name</div>
                    <div class="flex flex-col relative">
                        <input class="w-full h-full p-2 rounded-lg focus:outline-none" placeholder="Item">                        
                    </div>
                </div>

                <div class="flex flex-col gap-2 items-left p-3 rounded-lg bg-blue-100 w-1/5">
                    <div class="pl-2">Weight (Kg)</div>
                    <div class="flex flex-col relative">
                        <input class="w-full h-full p-2 rounded-lg focus:outline-none" type="number" placeholder="Weight">                        
                    </div>
                </div>

                <div class="flex flex-col gap-2 items-left p-3 rounded-lg bg-blue-100">
                    <div class="pl-2">Item type</div>
                    <div class="flex flex-col relative">
                        <input class="w-full h-full p-2 rounded-lg focus:outline-none" placeholder="City/Location">
                        <!-- idhar me city ki array iterate hogi -->
                        <div class="absolute">

                        </div>
                    </div>
                </div>
                
            </div>
            
            <div class="w-full flex flex-row justify-around gap-2">

                <div class="flex flex-col gap-2 items-left p-3 rounded-lg bg-blue-100">
                    <div class="pl-2">From</div>
                    <div class="flex flex-col relative">
                        <input class="w-full h-full p-2 rounded-lg focus:outline-none" placeholder="City/Location">
                        <!-- idhar me city ki array iterate hogi -->
                        <div class="absolute">

                        </div>
                    </div>
                </div>

                <div class="flex flex-col gap-2 items-left p-3 rounded-lg bg-blue-100">
                    <div class="pl-2">To</div>
                    <div class="flex flex-col relative">
                        <input class="w-full h-full p-2 rounded-lg focus:outline-none" placeholder="City/Location">
                        <!-- idhar me city ki array iterate hogi -->
                        <div class="absolute">

                        </div>
                    </div>
                </div>

                <div class="flex flex-col gap-2 items-left p-3 rounded-lg bg-blue-100">
                    <div class="pl-2">Date</div>
                    <div class="flex flex-col relative">
                        <input class="w-full h-full p-2 rounded-lg focus:outline-none" type="date" placeholder="Date">
                    </div>
                </div>

                <div class="flex flex-col gap-2 items-left p-3 rounded-lg bg-blue-100">
                    <div class="pl-2">Time</div>
                    <div class="flex flex-col relative">
                        <input class="w-full h-full p-2 rounded-lg focus:outline-none" type="time" placeholder="Time">
                    </div>
                </div>

                <button class="text-2xl px-6 rounded-xl items-center bg-blue-400 text-white">
                    +
                </button>
            </div>

            <div class="w-full pt-1 rounded-xl my-5 bg-gray-100"></div>

            <div class="w-full flex flex-row bg-gray-200 rounded-2xl">
                <div class="flex flex-col p-5 items-left w-1/2">
                    <div class="block text-gray-700 pl-2">Name</div>
                    <input type="text" class="mt-1 p-2 rounded-lg w-full" placeholder="Name"/>
                    
                    <div class="block text-gray-700 mt-2 pl-2">Mobile</div>
                    <input type="text" class="mt-1 p-2 rounded-lg w-full" placeholder="Mobile"/>
            
                    <div class="block text-gray-700 mt-2 pl-2">Email</div>
                    <input type="email" class="mt-1 p-2 rounded-lg w-full" placeholder="Email"/>
            
                    <div class="block text-gray-700 mt-2 pl-2">Address</div>
                    <input type="text" class="mt-1 p-2 rounded-lg w-full" placeholder="Address"/>
                </div>
            </div>

        </div>
        
    </div>
</div>