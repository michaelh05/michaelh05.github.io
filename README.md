<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Glorixia Studio Offer</title>
<style>
  body { margin: 0; font-family: Arial, sans-serif; background: #f3f4f6; color: #333; scroll-behavior: smooth; }
  .container { display: flex; flex-wrap: wrap; max-width: 1000px; margin: auto; padding: 20px; }
  .card { flex: 1; min-width: 300px; margin: 10px; border-radius: 16px; box-shadow: 0 4px 12px rgba(0,0,0,0.1); padding: 20px; transition: transform 0.2s, box-shadow 0.2s; }
  .card:hover { transform: translateY(-4px); box-shadow: 0 8px 16px rgba(0,0,0,0.15); }
  .left { background: #fff; }
  .right { background: #4f46e5; color: #fff; display: flex; flex-direction: column; justify-content: space-between; padding: 25px; line-height: 1.6; }
  h1, h2 { margin-top: 0; }
  ul { padding: 0; list-style: none; }
  ul li { margin: 12px 0; font-size: 16px; }
  .btn, button { display: inline-block; background: linear-gradient(135deg, #6366f1, #4338ca); color: #fff; padding: 12px 20px; border-radius: 12px; text-decoration: none; font-weight: bold; text-align: center; cursor: pointer; transition: background 0.3s, transform 0.2s, box-shadow 0.3s; border: none; }
  .btn:hover, button:hover { background: linear-gradient(135deg, #4338ca, #6366f1); transform: translateY(-2px); box-shadow: 0 4px 12px rgba(0,0,0,0.25); }
  footer { text-align: center; margin-top: 30px; font-size: 16px; font-weight: bold; color: #222; background: #e5e7eb; padding: 15px 0; border-radius: 12px; }
  form { display: flex; flex-direction: column; gap: 14px; margin-top: 20px; }
  input, textarea, select { padding: 12px; border-radius: 10px; border: 1px solid #ccc; font-size: 16px; width: 100%; box-sizing: border-box; transition: border-color 0.3s, box-shadow 0.3s, transform 0.2s, background 0.3s; background: #fff; }
  input:hover, textarea:hover, select:hover { border-color: #4f46e5; transform: translateY(-1px); background: #f0f0ff; }
  input:focus, textarea:focus, select:focus { border-color: #4f46e5; outline: none; box-shadow: 0 0 10px rgba(79,70,229,0.4); background: #fff; }
  select { color: #333; appearance: none; -webkit-appearance: none; -moz-appearance: none; }
  a { color: inherit; text-decoration: none; font-weight: bold; }
  .form-card { background: #4f46e5; color: #fff; padding: 30px; border-radius: 16px; display: none; }
  label { font-weight: bold; margin-top: 6px; }
  @media (max-width: 768px) {
    .container { flex-direction: column; }
    .btn, button { width: 100%; }
  }
</style>
</head>
<body>

<div class="container">
  <!-- Left Section -->
  <div class="card left">
    <h1>Grow Your Business with Glorixia Studio</h1>
    <p>No upfront costs. Full digital transformation. Just a fair revenue share.</p>
    <ul>
      <li><b>Website & Online Systems:</b> Custom website, booking & payment integration, merch setup.</li>
      <li><b>Social Media Management:</b> Overhaul, content, photography & video editing.</li>
      <li><b>Analytics & Growth:</b> Monthly reports on traffic, engagement, and sales performance.</li>
      <li><b>Independent Contractor:</b> No employee costs. Your data stays confidential.</li>
    </ul>
    <button class="btn" id="showFormBtn">Schedule Your Free Consultation</button>
  </div>

  <!-- Right Section -->
  <div class="card right">
    <div>
      <h2>Our Simple Deal</h2>
      <ul>
        <li><strong>10% of Gross Monthly Revenue</strong></li>
        <li><strong>2-Year Term</strong> + 1-Year Renewals</li>
        <li><strong>7-Day Grace Period</strong> on Payments</li>
        <li><strong>Buyout Option</strong> for Website Ownership</li>
        <li><strong>Liability Limited</strong> to Last 6 Months of Fees</li>
      </ul>
    </div>
    <p style="font-size: 15px; line-height: 1.5; margin-top: 15px; opacity: 0.9; border-top: 1px solid rgba(255,255,255,0.4); padding-top: 10px;">
      Governing Law: Illinois. Disputes: mediation, then arbitration/court.<br>
      See the Master Services Agreement & Revenue Share Addendum for full terms.
    </p>
  </div>
</div>

<!-- Contact Form Section -->
<div id="contact" class="container">
  <div class="card form-card" style="flex: 1 1 100%;">
    <h2>Book a Consultation</h2>
    <form action="mailto:glorixiastudio@gmail.com?subject=New Consultation Request – Glorixia Studio" method="POST" enctype="text/plain">
      <label for="Name">Full Name</label>
      <input type="text" name="Name" placeholder="Your Full Name" required>

      <label for="Email">Email Address</label>
      <input type="email" name="Email" placeholder="Your Email Address" required>

      <label for="Phone">Phone Number</label>
      <input type="tel" name="Phone" placeholder="Your Phone Number">

      <label for="Date">Select a Date</label>
      <select name="Date" required id="dateSelect"></select>

      <label for="Time">Select a Time Slot</label>
      <select name="Time" required id="timeSelect"></select>

      <label for="Message">Message</label>
      <textarea name="Message" rows="4" placeholder="Tell us about your business..."></textarea>

      <button type="submit">Submit Booking Request</button>
    </form>
  </div>
</div>

<!-- Footer -->
<footer>
  Email: <a href="mailto:glorixiastudio@gmail.com">glorixiastudio@gmail.com</a> | Phone: <a href="tel:+12172543478">217-254-3478</a><br>
  © 2025 Glorixia Studio
</footer>

<!-- Scripts -->
<script>
  const showFormBtn = document.getElementById('showFormBtn');
  const formCard = document.querySelector('.form-card');
  showFormBtn.addEventListener('click', function() {
    formCard.style.display = 'block';
    formCard.scrollIntoView({ behavior: 'smooth' });
  });

  // Generate next 14 days for date dropdown dynamically
  const dateSelect = document.getElementById('dateSelect');
  const today = new Date();
  for (let i = 0; i < 14; i++) {
    const optionDate = new Date();
    optionDate.setDate(today.getDate() + i);
    const formatted = optionDate.toISOString().split('T')[0];
    const display = optionDate.toDateString();
    const opt = document.createElement('option');
    opt.value = formatted;
    opt.textContent = display;
    dateSelect.appendChild(opt);
  }

  // Generate time slots (9:00 AM to 5:00 PM, 30-min intervals)
  const timeSelect = document.getElementById('timeSelect');
  for (let h = 9; h <= 16; h++) {
    [0,30].forEach(min => {
      const option = document.createElement('option');
      const displayHour = h % 12 === 0 ? 12 : h % 12;
      const displayMinutes = min.toString().padStart(2,'0');
      const ampm = h < 12 ? 'AM' : 'PM';
      option.value = `${h.toString().padStart(2,'0')}:${displayMinutes}`;
      option.textContent = `${displayHour}:${displayMinutes} ${ampm}`;
      timeSelect.appendChild(option);
    });
  }
</script>

</body>
</html>
