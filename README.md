index.html.
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Progressive Credit | Loan Application</title>
  <meta name="description" content="Apply for a loan with Progressive Credit. Review loan terms before applying.">
  <style>
    * { box-sizing: border-box; }
    body {
      margin: 0;
      font-family: Arial, sans-serif;
      background: #f3f6fb;
      color: #17233c;
    }
    header {
      background: #123b70;
      color: white;
      padding: 24px 18px;
      text-align: center;
    }
    header h1 { margin: 0 0 8px; }
    header p { margin: 0; }
    main {
      max-width: 620px;
      margin: 25px auto;
      padding: 0 14px;
    }
    .card {
      background: white;
      padding: 22px;
      border-radius: 14px;
      box-shadow: 0 4px 18px #142b4810;
      margin-bottom: 18px;
    }
    h2 { margin-top: 0; }
    label {
      display: block;
      font-weight: bold;
      margin: 15px 0 6px;
    }
    input, select {
      width: 100%;
      padding: 12px;
      border: 1px solid #cbd5e1;
      border-radius: 7px;
      font-size: 16px;
    }
    button {
      width: 100%;
      border: 0;
      background: #1467c5;
      color: white;
      padding: 14px;
      margin-top: 20px;
      border-radius: 8px;
      font-size: 16px;
      font-weight: bold;
    }
    .notice {
      background: #fff7df;
      padding: 12px;
      border-radius: 8px;
      line-height: 1.5;
      font-size: 14px;
    }
    footer {
      text-align: center;
      padding: 20px;
      color: #526078;
      font-size: 13px;
    }
  </style>
</head>
<body>
  <header>
    <h1>Progressive Credit</h1>
    <p>Your financial goals start here.</p>
  </header>

  <main>
    <section class="card">
      <h2>Loan Application</h2>
      <p>Complete the form to express your interest in a loan.</p>

      <div class="notice">
        This is a demonstration website. Applications are not
        transmitted or stored, and submitting this form does not
        mean that a loan is approved.
      </div>

      <form id="loanForm">
        <label for="name">Full name</label>
        <input id="name" name="name" autocomplete="name"
          required maxlength="100">

        <label for="phone">Phone number</label>
        <input id="phone" name="phone" type="tel"
          autocomplete="tel" required maxlength="20">

        <label for="location">Town or city</label>
        <input id="location" name="location"
          autocomplete="address-level2" required maxlength="100">

        <label for="amount">Requested amount (ZMW)</label>
        <input id="amount" name="amount" type="number"
          min="1" max="1000000" step="1" required>

        <label for="period">Preferred repayment period</label>
        <select id="period" name="period" required>
          <option value="">Choose a period</option>
          <option value="1 month">1 month</option>
          <option value="3 months">3 months</option>
          <option value="6 months">6 months</option>
          <option value="12 months">12 months</option>
        </select>

        <label for="employment">Employment status</label>
        <select id="employment" name="employment" required>
          <option value="">Choose an option</option>
          <option>Employed</option>
          <option>Self-employed</option>
          <option>Business owner</option>
          <option>Other</option>
        </select>

        <button type="submit">Submit test application</button>
      </form>

      <p id="message" role="status"></p>
    </section>

    <section class="card">
      <h2>Contact Us</h2>
      <p>Contact details will be added here before launch.</p>
    </section>
  </main>

  <footer>
    &copy; 2026 Progressive Credit. All rights reserved.
  </footer>

  <script>
    document.getElementById("loanForm").addEventListener(
      "submit", function(event) {
        event.preventDefault();
        document.getElementById("message").textContent =
          "Demo only: no application was sent or saved. " +
          "Connect a secure application service before launch.";
      }
    );
  </script>
</body>
</html>
create loan application website 