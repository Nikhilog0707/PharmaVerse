<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>B Pharmacy Notes</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      margin: 0;
      background-color: #f9f9f9;
      animation: fadeIn 1s ease-in;
    }
    header {
      background-color: #0077b6;
      color: white;
      padding: 20px;
      text-align: center;
      animation: slideDown 1s ease-in;
    }
    nav {
      background-color: #023e8a;
      display: flex;
      justify-content: center;
      padding: 10px;
    }
    nav a {
      color: white;
      margin: 0 15px;
      text-decoration: none;
      font-weight: bold;
      transition: transform 0.3s ease;
    }
    nav a:hover {
      text-decoration: underline;
      transform: scale(1.1);
    }
    .container {
      padding: 20px;
    }
    .notes-section {
      margin-bottom: 30px;
    }
    h2 {
      color: #03045e;
    }
    ul {
      list-style-type: none;
      padding: 0;
    }
    li {
      margin: 8px 0;
    }
    a.note-link {
      color: #0077b6;
      text-decoration: none;
    }
    a.note-link:hover {
      text-decoration: underline;
    }
    input[type="text"], input[type="file"], input[type="submit"] {
      width: 100%;
      padding: 10px;
      margin-bottom: 20px;
      border: 1px solid #ccc;
      border-radius: 5px;
    }
    .upload-form, .payment-section {
      margin: 40px 0;
      padding: 20px;
      background: #e0f7fa;
      border-radius: 10px;
      box-shadow: 0 0 10px rgba(0,0,0,0.1);
    }
    @keyframes fadeIn {
      from { opacity: 0; }
      to { opacity: 1; }
    }
    @keyframes slideDown {
      from { transform: translateY(-50px); opacity: 0; }
      to { transform: translateY(0); opacity: 1; }
    }
  </style>
</head>
<body>

<header>
  <h1>B Pharmacy Notes</h1>
  <p>All Semester Notes at One Place</p>
</header>

<nav>
  <a href="#sem1">Sem 1</a>
  <a href="#sem2">Sem 2</a>
  <a href="#sem3">Sem 3</a>
  <a href="#sem4">Sem 4</a>
  <a href="#sem5">Sem 5</a>
  <a href="#sem6">Sem 6</a>
  <a href="#sem7">Sem 7</a>
  <a href="#sem8">Sem 8</a>
</nav>

<div class="container">
  <input type="text" id="search" placeholder="Search notes...">

  <div class="notes-section" id="sem1">
    <h2>Semester 1</h2>
    <ul>
      <li><a class="note-link" href="#">Human Anatomy & Physiology - PDF - ₹49 <button>Buy</button></a></li>
      <li><a class="note-link" href="#">Pharmaceutical Inorganic Chemistry - PDF - ₹49 <button>Buy</button></a></li>
    </ul>
  </div>

  <div class="notes-section" id="sem2">
    <h2>Semester 2</h2>
    <ul>
      <li><a class="note-link" href="#">Pharmaceutical Organic Chemistry I - PDF - ₹49 <button>Buy</button></a></li>
      <li><a class="note-link" href="#">Pathophysiology - PDF - ₹49 <button>Buy</button></a></li>
    </ul>
  </div>

  <!-- Upload Form -->
  <div class="upload-form">
    <h2>Upload Your Notes</h2>
    <form action="#" method="POST" enctype="multipart/form-data">
      <input type="text" name="title" placeholder="Title of the Note">
      <input type="file" name="noteFile">
      <input type="submit" value="Upload Note">
    </form>
  </div>

  <!-- Payment Section -->
  <div class="payment-section">
    <h2>Payment Information</h2>
    <p>We accept UPI, Google Pay, and Paytm. Please make payment to the UPI ID: <strong>pharma.notes@upi</strong></p>
    <p>After payment, your download link will be activated or emailed.</p>
  </div>
</div>

<script>
  document.getElementById("search").addEventListener("keyup", function () {
    let filter = this.value.toLowerCase();
    let links = document.querySelectorAll(".note-link");
    links.forEach(link => {
      if (link.textContent.toLowerCase().includes(filter)) {
        link.parentElement.style.display = "block";
      } else {
        link.parentElement.style.display = "none";
      }
    });
  });
</script>

</body>
</html>
