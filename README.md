<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Glorixia Studio - Partner With Us</title>
  <link rel="apple-touch-icon" sizes="180x180" href="apple-touch-icon.png">
  <link rel="icon" type="image/png" sizes="32x32" href="favicon-32x32.png">
  <link rel="icon" type="image/png" sizes="16x16" href="favicon-16x16.png">
  <style>
    /* Global Reset */
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }
    body, html {
      font-family: Arial, sans-serif;
      background-color: #f3f4f6;
      color: #333;
      max-width: 100%;
      overflow-x: hidden;
    }
    .container {
      display: flex;
      justify-content: center;
      align-items: center;
      min-height: 100vh;
      padding: 2rem;
    }
    .content {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 2rem;
      max-width: 1200px;
      width: 100%;
    }
    .card {
      background: white;
      border-radius: 1rem;
      padding: 2rem;
      box-shadow: 0 4px 12px rgba(0,0,0,0.1);
    }
    h1, h2 {
      margin-bottom: 1rem;
    }
    p {
      margin-bottom: 1rem;
    }
    ul {
      padding-left: 1.2rem;
    }
    .cta {
      display: block;
      text-align: center;
      background: #4f46e5;
      color: white;
      text-decoration: none;
      padding: 1rem;
      border-radius: 0.75rem;
      margin-top: 2rem;
      transition: background 0.3s ease;
    }
    .cta:hover {
      background: #4338ca;
    }
    .right-card {
      background: #4f46e5;
      color: white;
      display: flex;
      flex-direction: column;
      justify-content: space-between;
    }
    .right-card ul {
      list-style: none;
      padding-left: 0;
    }
    .right-card li {
      margin-bottom: 1rem;
    }
    .contact-info {
      margin-top: 2rem;
      padding-top: 1rem;
      border-top: 1px solid rgba(255,255,255,0.3);
      font-size: 0.9rem;
      text-align: center;
    }
    /* Hidden form by default */
    #consultation-form {
      display: none;
      margin-top: 2rem;
    }
    form input, form select, form button {
      display: block;
      width: 100%;
      margin-bottom: 1rem;
      padding: 0.75rem;
      border: 1px solid #ccc;
      border-radius: 0.5rem;
      font-size: 1rem;
    }
    form button {
      background: #4f46e5;
      color: white;
      border: none;
      cursor: pointer;
      transition: background 0.3s ease;
    }
    form button:hover {
      background: #4338ca;
    }

    /* Mobile view fixes */
    @media (max-width: 768px) {
      .container {
        padding: 1rem;
      }
      .content {
        grid-template-columns: 1fr;
        width: 100%;
        gap: 1.5rem;
        text-align: center;
      }
      .card {
        padding: 1.5rem;
      }
      form input, form select, form button {
        width: 90%;
        max-width: 350px;
        margin-left: auto;
        margin-right: auto;
      }
    }
  </style>
</head>
<body>
  <div class="container">
    <div class="content">
      
      <!-- Left Card -->
      <div class="card">
        <h1>Grow Your Business with Glorixia Studio</h1>
        <p>No upfront costs. Full digital transformation. Just a fair revenue share.</p>
        <ul>
          <li><strong>Website & Online Systems:</strong> Custom site, booking & payment integration, merch setup.</li>
          <li><strong>Social Media Management:</strong> Overhaul, ongoing content, photography & video editing.</li>
          <li><strong>Analytics & Growth:</strong> Monthly reports on traffic, engagement, and sales performance.</li>
          <li><strong>Independent Contractor:</strong> No employee costs. Your data stays confidential.</li>
        </ul>
        <a href="#consultation-form" class="cta" onclick="toggleForm()">Schedule a Consultation</a>

        <!-- Hidden Form -->
        <form id="consultation-form" action="mailto:glorixiastudio@gmail.com" method="POST" enctype="text/plain">
          <input type="text" name="name" placeholder="Your Name" required>
          <input type="email" name="email" placeholder="Your Email" required>
          <input type="tel" name="phone" placeholder="Your Phone Number">
          <label for="date">Select a Date for Appointment:</label>
          <input type="date" name="date" required>
          <button type="submit">Send Request</button>
        </form>
      </div>
      
      <!-- Right Card -->
      <div class="card right-card">
        <div>
          <h2>Our Simple Deal</h2>
          <ul>
            <li>💰 10% of Gross Monthly Revenue</li>
            <li>📅 2-Year Term + 1-Year Renewals</li>
            <li>⏳ 7-Day Grace Period on Payments</li>
            <li>💻 Buyout Option for Website Ownership</li>
            <li>⚖️ Liability Limited to Last 6 Months of Fees</li>
          </ul>
        </div>
        <div class="contact-info">
          <p><strong>Email:</strong> glorixiastudio@gmail.com</p>
          <p><strong>Phone:</strong> 217-254-3478</p>
          <p>Governing Law: Illinois. Disputes: mediation, then arbitration/court. See the Master Services Agreement & Revenue Share Addendum for full terms.</p>
        </div>
      </div>

    </div>
  </div>

  <script>
    function toggleForm() {
      const form = document.getElementById('consultation-form');
      form.style.display = form.style.display === 'block' ? 'none' : 'block';
    }
  </script>
</body>
</html>
