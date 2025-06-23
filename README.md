<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Insurance Form</title>
  <script src="https://cdn.tailwindcss.com"></script>
  <link
    rel="stylesheet"
    href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.15.3/css/all.min.css"
  />
  <link
    href="https://fonts.googleapis.com/css2?family=Inter:wght@400;600&display=swap"
    rel="stylesheet"
  />
  <style>
    body {
      font-family: 'Inter', sans-serif;
    }
    /* Modal scrollbar fix */
    #passwordModal {
      -webkit-overflow-scrolling: touch;
    }
  </style>
</head>
<body class="bg-gray-50 min-h-screen flex items-center justify-center p-4">
  <main class="w-full max-w-3xl bg-white rounded-lg shadow-lg p-6 md:p-10 relative">
    <h1 class="text-3xl font-semibold text-gray-800 mb-6 text-center">
      Customer Information
    </h1>
    <form id="insuranceForm" class="space-y-6" novalidate>
      <div class="grid grid-cols-1 md:grid-cols-2 gap-6">
        <div>
          <label for="name" class="block text-gray-700 font-medium mb-1"
            >Name</label
          >
          <input
            type="text"
            id="name"
            name="name"
            required
            class="w-full rounded-md border border-gray-300 px-3 py-2 focus:outline-none focus:ring-2 focus:ring-blue-500"
            placeholder="Full Name"
          />
        </div>
        <div>
          <label for="mobile" class="block text-gray-700 font-medium mb-1"
            >Mobile Number</label
          >
          <input
            type="tel"
            id="mobile"
            name="mobile"
            required
            pattern="[0-9]{10,15}"
            class="w-full rounded-md border border-gray-300 px-3 py-2 focus:outline-none focus:ring-2 focus:ring-blue-500"
            placeholder="e.g. 9876543210"
          />
        </div>
      </div>

      <div>
        <label for="address" class="block text-gray-700 font-medium mb-1"
          >Address</label
        >
        <textarea
          id="address"
          name="address"
          rows="3"
          required
          class="w-full rounded-md border border-gray-300 px-3 py-2 resize-none focus:outline-none focus:ring-2 focus:ring-blue-500"
          placeholder="Full address"
        ></textarea>
      </div>

      <div class="grid grid-cols-1 md:grid-cols-3 gap-6">
        <div>
          <label for="adhar" class="block text-gray-700 font-medium mb-1"
            >Aadhar Number</label
          >
          <input
            type="text"
            id="adhar"
            name="adhar"
            required
            pattern="[0-9]{12}"
            class="w-full rounded-md border border-gray-300 px-3 py-2 focus:outline-none focus:ring-2 focus:ring-blue-500"
            placeholder="12-digit Aadhar"
          />
        </div>
        <div>
          <label for="chechis" class="block text-gray-700 font-medium mb-1"
            >Chechis Number</label
          >
          <input
            type="text"
            id="chechis"
            name="chechis"
            required
            class="w-full rounded-md border border-gray-300 px-3 py-2 focus:outline-none focus:ring-2 focus:ring-blue-500"
            placeholder="Chechis Number"
          />
        </div>
        <div>
          <label for="motor" class="block text-gray-700 font-medium mb-1"
            >Motor Number</label
          >
          <input
            type="text"
            id="motor"
            name="motor"
            required
            class="w-full rounded-md border border-gray-300 px-3 py-2 focus:outline-none focus:ring-2 focus:ring-blue-500"
            placeholder="Motor Number"
          />
        </div>
      </div>

      <div class="flex space-x-4">
        <button
          type="button"
          id="savePdfBtn"
          class="flex-1 bg-blue-600 hover:bg-blue-700 text-white font-semibold py-3 rounded-md transition-colors duration-200 flex items-center justify-center space-x-2"
        >
          <i class="fas fa-save"></i>
          <span>Save</span>
        </button>
        <button
          type="button"
          id="shareBtn"
          class="flex-1 bg-green-600 hover:bg-green-700 text-white font-semibold py-3 rounded-md transition-colors duration-200 flex items-center justify-center space-x-2"
        >
          <i class="fas fa-share-alt"></i>
          <span>Share</span>
        </button>
      </div>
    </form>

    <!-- Password Modal -->
    <div id="passwordModal" class="fixed inset-0 bg-black bg-opacity-50 flex items-center justify-center hidden z-50">
      <div class="bg-white rounded-lg shadow-lg p-6 w-full max-w-md">
        <h2 class="text-xl font-semibold mb-4 text-gray-800">Enter Password to Save</h2>
        <input
          type="password"
          id="modalPassword"
          class="w-full rounded-md border border-gray-300 px-3 py-2 mb-4 focus:outline-none focus:ring-2 focus:ring-blue-500"
          placeholder="Password"
        />
        <div class="flex justify-end space-x-4">
          <button id="cancelPasswordBtn" class="px-4 py-2 rounded-md bg-gray-300 hover:bg-gray-400 transition">
            Cancel
          </button>
          <button id="submitPasswordBtn" class="px-4 py-2 rounded-md bg-blue-600 text-white hover:bg-blue-700 transition">
            Submit
          </button>
        </div>
      </div>
    </div>

    <!-- Save Confirmation -->
    <div id="saveConfirmation" class="fixed inset-0 bg-black bg-opacity-50 flex items-center justify-center hidden z-50">
      <div class="bg-white rounded-lg shadow-lg p-6 w-full max-w-md text-center">
        <h2 class="text-xl font-semibold mb-4 text-gray-800">Data Saved Successfully!</h2>
        <button id="closeSaveConfirmation" class="mt-4 px-6 py-2 bg-blue-600 text-white rounded-md hover:bg-blue-700 transition">
          Close
        </button>
      </div>
    </div>
  </main>

  <script>
    const form = document.getElementById('insuranceForm');
    const saveBtn = document.getElementById('savePdfBtn');
    const shareBtn = document.getElementById('shareBtn');
    const passwordModal = document.getElementById('passwordModal');
    const modalPasswordInput = document.getElementById('modalPassword');
    const cancelPasswordBtn = document.getElementById('cancelPasswordBtn');
    const submitPasswordBtn = document.getElementById('submitPasswordBtn');
    const saveConfirmation = document.getElementById('saveConfirmation');
    const closeSaveConfirmation = document.getElementById('closeSaveConfirmation');

    // Show password modal on save button click
    saveBtn.addEventListener('click', () => {
      modalPasswordInput.value = '';
      passwordModal.classList.remove('hidden');
      modalPasswordInput.focus();
    });

    // Cancel password modal
    cancelPasswordBtn.addEventListener('click', () => {
      passwordModal.classList.add('hidden');
    });

    // Submit password and save data in localStorage
    submitPasswordBtn.addEventListener('click', () => {
      const password = modalPasswordInput.value.trim();
      if (!password) {
        alert('Please enter a password to save.');
        modalPasswordInput.focus();
        return;
      }

      // You can add password validation here if needed

      // Save form data in localStorage (simulate website save)
      const formData = {
        name: form.name.value.trim(),
        mobile: form.mobile.value.trim(),
        address: form.address.value.trim(),
        adhar: form.adhar.value.trim(),
        chechis: form.chechis.value.trim(),
        motor: form.motor.value.trim(),
        savedAt: new Date().toISOString(),
        password: password // optionally store password hash or omit storing password in real apps
      };

      try {
        localStorage.setItem('insuranceFormData', JSON.stringify(formData));
      } catch (e) {
        alert('Failed to save data locally.');
        passwordModal.classList.add('hidden');
        return;
      }

      passwordModal.classList.add('hidden');
      saveConfirmation.classList.remove('hidden');
    });

    // Close save confirmation modal
    closeSaveConfirmation.addEventListener('click', () => {
      saveConfirmation.classList.add('hidden');
    });

    // Share button functionality (optional)
    shareBtn.addEventListener('click', () => {
      alert('Sharing functionality is not implemented in this version.');
    });
  </script>
</body>
</html>
