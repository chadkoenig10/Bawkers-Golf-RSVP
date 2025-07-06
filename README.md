<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1" />
<title>Golf Event RSVP</title>
<style>
  body {
    font-family: Arial, sans-serif;
    margin: 0; padding: 20px;
    background: #f8f9fa;
    color: #333;
  }
  .container {
    max-width: 400px;
    margin: 0 auto;
    background: white;
    padding: 20px;
    border-radius: 8px;
    box-shadow: 0 2px 6px rgb(0 0 0 / 0.1);
  }
  h1 {
    text-align: center;
    color: #2c3e50;
  }
  img {
    display: block;
    max-width: 100%;
    margin: 15px auto;
    border-radius: 8px;
  }
  label {
    display: block;
    margin-top: 15px;
    font-weight: bold;
  }
  input[type="text"], select {
    width: 100%;
    padding: 8px;
    margin-top: 5px;
    box-sizing: border-box;
    border-radius: 4px;
    border: 1px solid #ccc;
  }
  button {
    margin-top: 20px;
    width: 100%;
    background-color: #27ae60;
    border: none;
    padding: 12px;
    color: white;
    font-weight: bold;
    border-radius: 6px;
    cursor: pointer;
    font-size: 16px;
  }
  button:hover {
    background-color: #219150;
  }
  .thank-you {
    text-align: center;
    font-size: 18px;
    color: #27ae60;
    margin-top: 20px;
  }
</style>
</head>
<body>

<div class="container">
  <h1>Golf Event RSVP</h1>
  <p><strong>Date:</strong> Saturday, July 20, 2025<br />
     <strong>Time:</strong> 9:00 AM<br />
     <strong>Location:</strong> Riverside Golf Course</p>
  
  <!-- Event flyer image -->
  <img src="https://example.com/your-golf-flyer.jpg" alt="Golf Event Flyer" />

  <form id="rsvpForm">
    <label for="name">Your Name</label>
    <input type="text" id="name" name="name" required placeholder="Enter your name" />
    
    <label for="response">Will you be golfing?</label>
    <select id="response" name="response" required>
      <option value="" disabled selected>Select an option</option>
      <option value="Yes">Yes, I'll be there</option>
      <option value="No">No, can't make it</option>
      <option value="Maybe">Maybe</option>
    </select>
    
    <button type="submit">Submit RSVP</button>
  </form>

  <div class="thank-you" id="thankYouMessage" style="display:none;">
    Thanks for your response! See you on the course ⛳
  </div>
</div>

<script>
  const form = document.getElementById('rsvpForm');
  const thankYou = document.getElementById('thankYouMessage');

  form.addEventListener('submit', function(e) {
    e.preventDefault();

    // In real use, you would send the data to a backend or Google Sheet here.
    // For this demo, just show thank you message.

    form.style.display = 'none';
    thankYou.style.display = 'block';

    // Optional: clear form fields if you want to allow new submission later
    form.reset();
  });
</script>

</body>
</html>
