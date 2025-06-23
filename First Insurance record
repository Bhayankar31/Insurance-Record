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
  </style>
</head>
<body class="bg-gray-50 min-h-screen flex items-center justify-center p-4">
  <main class="w-full max-w-3xl bg-white rounded-lg shadow-lg p-6 md:p-10">
    <h1 class="text-3xl font-semibold text-gray-800 mb-6 text-center">
      Insurance Form
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

      <div class="grid grid-cols-1 md:grid-cols-3 gap-6">
        <div>
          <label for="price" class="block text-gray-700 font-medium mb-1"
            >Price</label
          >
          <input
            type="number"
            id="price"
            name="price"
            min="0"
            step="0.01"
            required
            class="w-full rounded-md border border-gray-300 px-3 py-2 focus:outline-none focus:ring-2 focus:ring-blue-500"
            placeholder="Price in ₹"
          />
        </div>
        <div>
          <label for="policy" class="block text-gray-700 font-medium mb-1"
            >Policy Number</label
          >
          <input
            type="text"
            id="policy"
            name="policy"
            required
            class="w-full rounded-md border border-gray-300 px-3 py-2 focus:outline-none focus:ring-2 focus:ring-blue-500"
            placeholder="Policy Number"
          />
        </div>
        <div>
          <label for="fileAttach" class="block text-gray-700 font-medium mb-1"
            >Attach File</label
          >
          <input
            type="file"
            id="fileAttach"
            name="fileAttach"
            accept=".pdf,.jpg,.jpeg,.png"
            class="w-full text-gray-700"
          />
        </div>
      </div>

      <div class="grid grid-cols-1 md:grid-cols-3 gap-6">
        <div>
          <label for="startDate" class="block text-gray-700 font-medium mb-1"
            >Starting Date (dd/mm/yyyy)</label
          >
          <input
            type="text"
            id="startDate"
            name="startDate"
            required
            placeholder="dd/mm/yyyy"
            pattern="^(0[1-9]|[12][0-9]|3[01])/(0[1-9]|1[012])/[0-9]{4}$"
            class="w-full rounded-md border border-gray-300 px-3 py-2 focus:outline-none focus:ring-2 focus:ring-blue-500"
          />
        </div>
        <div>
          <label for="period" class="block text-gray-700 font-medium mb-1"
            >Period (Years)</label
          >
          <input
            type="number"
            id="period"
            name="period"
            min="0"
            max="100"
            required
            class="w-full rounded-md border border-gray-300 px-3 py-2 focus:outline-none focus:ring-2 focus:ring-blue-500"
            placeholder="Number of years"
          />
        </div>
        <div>
          <label for="endDate" class="block text-gray-700 font-medium mb-1"
            >Ending Date</label
          >
          <input
            type="text"
            id="endDate"
            name="endDate"
            readonly
            class="w-full rounded-md border border-gray-300 bg-gray-100 px-3 py-2 cursor-not-allowed"
            placeholder="Auto-calculated"
          />
        </div>
      </div>

      <div>
        <label for="expiryDays" class="block text-gray-700 font-medium mb-1"
          >Expiry Status</label
        >
        <input
          type="text"
          id="expiryDays"
          name="expiryDays"
          readonly
          class="w-full rounded-md border border-gray-300 bg-gray-100 px-3 py-2 cursor-not-allowed"
          placeholder="Auto-calculated"
        />
      </div>

      <button
        type="button"
        id="savePdfBtn"
        class="w-full bg-blue-600 hover:bg-blue-700 text-white font-semibold py-3 rounded-md transition-colors duration-200"
      >
        Save Form Data as PDF
      </button>
    </form>
  </main>

  <script src="https://cdnjs.cloudflare.com/ajax/libs/jspdf/2.5.1/jspdf.umd.min.js"></script>
  <script>
    const { jsPDF } = window.jspdf;

    const form = document.getElementById('insuranceForm');
    const startDateInput = form.startDate;
    const periodInput = form.period;
    const endDateInput = form.endDate;
    const expiryDaysInput = form.expiryDays;
    const savePdfBtn = document.getElementById('savePdfBtn');

    // Parse dd/mm/yyyy → Date object
    function parseDateDMY(dateStr) {
      const [dd, mm, yyyy] = dateStr.split('/').map(Number);
      const date = new Date(yyyy, mm - 1, dd);
      return (date.getDate() === dd && date.getMonth() === mm - 1 && date.getFullYear() === yyyy) ? date : null;
    }

    // Format Date object → dd/mm/yyyy
    function formatDateDMY(date) {
      const dd = String(date.getDate()).padStart(2, '0');
      const mm = String(date.getMonth() + 1).padStart(2, '0');
      const yyyy = date.getFullYear();
      return `${dd}/${mm}/${yyyy}`;
    }

    function updateEndDateAndExpiry() {
      const startDateStr = startDateInput.value.trim();
      const periodYears = parseInt(periodInput.value, 10);

      if (!startDateStr || isNaN(periodYears) || periodYears < 0) {
        endDateInput.value = '';
        expiryDaysInput.value = '';
        return;
      }

      const startDate = parseDateDMY(startDateStr);
      if (!startDate) {
        endDateInput.value = '';
        expiryDaysInput.value = '';
        return;
      }

      const endDate = new Date(startDate);
      endDate.setFullYear(endDate.getFullYear() + periodYears);
      endDate.setDate(endDate.getDate() - 1);

      const today = new Date();
      today.setHours(0, 0, 0, 0);
      endDate.setHours(0, 0, 0, 0);

      const diffDays = Math.floor((endDate - today) / (1000 * 60 * 60 * 24));

      endDateInput.value = formatDateDMY(endDate);
      expiryDaysInput.value = diffDays > 0
        ? `${diffDays} day(s) left`
        : diffDays === 0
          ? 'Expires today'
          : `${Math.abs(diffDays)} day(s) expired`;
    }

    startDateInput.addEventListener('input', updateEndDateAndExpiry);
    periodInput.addEventListener('input', updateEndDateAndExpiry);

    savePdfBtn.addEventListener('click', () => {
      if (!parseDateDMY(startDateInput.value.trim())) {
        alert('Please enter a valid Starting Date in dd/mm/yyyy format.');
        startDateInput.focus();
        return;
      }

      if (!parseDateDMY(endDateInput.value.trim())) {
        alert('Calculated Ending Date is invalid.');
        return;
      }

      const formData = {
        Name: form.name.value.trim(),
        "Mobile Number": form.mobile.value.trim(),
        Address: form.address.value.trim(),
        "Aadhar Number": form.adhar.value.trim(),
        "Chechis Number": form.chechis.value.trim(),
        "Motor Number": form.motor.value.trim(),
        Price: form.price.value.trim(),
        "Policy Number": form.policy.value.trim(),
        "Starting Date": startDateInput.value.trim(),
        Period: periodInput.value.trim(),
        "Ending Date": endDateInput.value.trim(),
        "Expiry Status": expiryDaysInput.value.trim(),
        "File Attached": form.fileAttach.files.length > 0 ? form.fileAttach.files[0].name : "No file attached"
      };

      const doc = new jsPDF();

      doc.setFontSize(18);
      doc.text("Insurance Form Data", 105, 20, null, null, "center");

      doc.setFontSize(12);
      let y = 35;
      const lineHeight = 10;
      const pageHeight = doc.internal.pageSize.height;

      for (const [key, value] of Object.entries(formData)) {
        const text = `${key}: ${value}`;
        const splitText = doc.splitTextToSize(text, 180);
        if (y + splitText.length * lineHeight > pageHeight - 20) {
          doc.addPage();
          y = 20;
        }
        doc.text(splitText, 15, y);
        y += splitText.length * lineHeight;
      }

      doc.save("insurance-record.pdf");
    });
  </script>
</body>
</html>
