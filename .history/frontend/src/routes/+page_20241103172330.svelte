<script>
  // Add any Svelte logic here if needed
</script>

<div class="flex flex-col items-center bg-gray-100 min-h-screen">
  <div class="w-full max-w-4xl bg-teal-600 p-4 flex items-center justify-between text-white rounded-t-lg">
    <div class="flex items-center space-x-2">
      <img src="/path/to/logo.png" alt="Logo" class="w-10 h-10" />
      <h1 class="text-xl font-bold">Jivandeep Travels</h1>
    </div>
    <div class="flex space-x-8">
      <button class="flex items-center space-x-1">
        <img src="/path/to/bus-icon.png" alt="Bus" class="w-6 h-6" />
        <span>Person</span>
      </button>
      <button class="flex items-center space-x-1">
        <img src="/path/to/parcel-icon.png" alt="Parcel" class="w-6 h-6" />
        <span>Parcel</span>
      </button>
      <button class="flex items-center space-x-1">
        <img src="/path/to/help-icon.png" alt="Help" class="w-6 h-6" />
        <span>Help</span>
      </button>
    </div>
    <button class="bg-white p-2 rounded-full">
      <img src="/path/to/profile-icon.png" alt="Profile" class="w-6 h-6" />
    </button>
  </div>

  <div class="bg-white w-full max-w-4xl p-4 rounded-b-lg shadow-lg">
    <div class="flex space-x-2">
      <div class="flex-1 flex flex-col items-center bg-blue-100 rounded-l-lg py-4">
        <label class="text-gray-700">From</label>
        <input type="text" class="mt-2 p-2 rounded-lg w-10/12" placeholder="City/Location" />
      </div>
      <div class="flex-1 flex flex-col items-center bg-blue-100 py-4">
        <label class="text-gray-700">To</label>
        <input type="text" class="mt-2 p-2 rounded-lg w-10/12" placeholder="City/Location" />
      </div>
      <div class="flex-1 flex flex-col items-center bg-blue-100 rounded-r-lg py-4">
        <label class="text-gray-700">Date</label>
        <input type="date" class="mt-2 p-2 rounded-lg w-10/12" />
      </div>
      <button class="bg-blue-500 text-white p-3 rounded-full ml-2">
        <span class="text-xl font-bold">+</span>
      </button>
    </div>

    <div class="flex space-x-2 mt-4">
      <div class="flex-1 bg-blue-200 p-4 rounded-lg">
        <label class="block text-gray-700">Name</label>
        <input type="text" class="mt-1 p-2 rounded w-full" />
        
        <label class="block text-gray-700 mt-2">Mobile</label>
        <input type="text" class="mt-1 p-2 rounded w-full" />

        <label class="block text-gray-700 mt-2">Email</label>
        <input type="email" class="mt-1 p-2 rounded w-full" />

        <label class="block text-gray-700 mt-2">Address</label>
        <input type="text" class="mt-1 p-2 rounded w-full" />
      </div>

      <div class="flex-1 bg-blue-200 p-4 rounded-lg">
        <label class="block text-gray-700">Journey</label>
        <input type="text" class="mt-1 p-2 rounded w-full" />

        <label class="block text-gray-700 mt-2">Unik Ticket No.</label>
        <input type="text" class="mt-1 p-2 rounded w-full" />
        
        <!-- Add any additional fields as necessary here -->
      </div>
    </div>
  </div>
</div>

<style>
  /* Add any additional custom styles here */
</style>
