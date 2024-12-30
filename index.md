<!-- Custom Styles for Tabs -->
<style>
  /* Container for the tabs */
  .tabs {
    overflow: hidden;
    background-color: #ffefd5;
    margin-bottom: 20px;
    border-radius: 8px;
  }

  /* Style the buttons inside the tab */
  .tabs button {
    background-color: inherit;
    float: left;
    border: none;
    outline: none;
    cursor: pointer;
    padding: 14px 16px;
    transition: background-color 0.3s;
    font-size: 17px;
    border-radius: 8px 8px 0 0;
    margin: 0 2px;
  }

  /* Change background color of buttons on hover */
  .tabs button:hover {
    background-color: #ffdab9;
  }

  /* Create an active/current tablink class */
  .tabs button.active {
    background-color: #ff6347;
    color: white;
  }

  /* Style the tab content */
  .tabcontent {
    display: none;
    padding: 20px;
    border: 2px solid #ffefd5;
    border-top: none;
    background-color: #fffaf0;
    border-radius: 0 8px 8px 8px;
  }

  /* Show the active tab content */
  .tabcontent.active {
    display: block;
  }

  /* Responsive Design */
  @media screen and (max-width: 600px) {
    .tabs button {
      padding: 10px 12px;
      font-size: 15px;
    }
  }
</style>

<!-- Navigation Bar -->
<nav class="navbar">
  <a href="#gallery">Gallery</a>
  <a href="#about">About</a>
  <a href="#contact">Contact</a>
</nav>

<!-- Welcome Section -->
<section id="welcome">
  <h1>Welcome to Ashley's Art Collection 💖</h1>
  <p>
    Dive into a curated selection of traditional Chinese paintings by Ashley. Our mission is to make intricate and beautiful artworks affordable and accessible to everyone.
  </p>
</section>

<!-- Gallery Section with Tabs -->
<section id="gallery">
  <h2>Gallery</h2>

  <!-- Tabs -->
  <div class="tabs">
    <button class="tablink active" onclick="openTab(event, 'Bamboos')">Bamboos</button>
    <button class="tablink" onclick="openTab(event, 'Lotus')">Lotus</button>
    <button class="tablink" onclick="openTab(event, 'Fruits')">Fruits</button>
  </div>

  <!-- Bamboos Tab Content -->
  <div id="Bamboos" class="tabcontent active">
    <h3>Bamboos</h3>
    <div class="gallery-container">
      <div class="gallery-item">
        <a href="Images/bamboo1.jpg" data-lightbox="bamboos" data-title="Bamboo Painting 1">
          <img src="Images/bamboo1_thumb.jpg" alt="Bamboo Painting 1">
        </a>
      </div>
      <div class="gallery-item">
        <a href="Images/bamboo2.jpg" data-lightbox="bamboos" data-title="Bamboo Painting 2">
          <img src="Images/bamboo2_thumb.jpg" alt="Bamboo Painting 2">
        </a>
      </div>
      <!-- Add more bamboo paintings as needed -->
    </div>
  </div>

  <!-- Lotus Tab Content -->
  <div id="Lotus" class="tabcontent">
    <h3>Lotus</h3>
    <div class="gallery-container">
      <div class="gallery-item">
        <a href="Images/lotus1.jpg" data-lightbox="lotus" data-title="Lotus Painting 1">
          <img src="Images/lotus1_thumb.jpg" alt="Lotus Painting 1">
        </a>
      </div>
      <div class="gallery-item">
        <a href="Images/lotus2.jpg" data-lightbox="lotus" data-title="Lotus Painting 2">
          <img src="Images/lotus2_thumb.jpg" alt="Lotus Painting 2">
        </a>
      </div>
      <!-- Add more lotus paintings as needed -->
    </div>
  </div>

  <!-- Fruits Tab Content -->
  <div id="Fruits" class="tabcontent">
    <h3>Fruits</h3>
    <div class="gallery-container">
      <div class="gallery-item">
        <a href="Images/fruits1.jpg" data-lightbox="fruits" data-title="Fruits Painting 1">
          <img src="Images/fruits1_thumb.jpg" alt="Fruits Painting 1">
        </a>
      </div>
      <div class="gallery-item">
        <a href="Images/fruits2.jpg" data-lightbox="fruits" data-title="Fruits Painting 2">
          <img src="Images/fruits2_thumb.jpg" alt="Fruits Painting 2">
        </a>
      </div>
      <!-- Add more fruits paintings as needed -->
    </div>
  </div>
</section>

<!-- About Section -->
<section id="about">
  <h2>About Ashley</h2>
  <p>
    Ashley Wang is a talented artist specializing in traditional Chinese paintings. Her work beautifully captures the essence of nature, focusing on elements like bamboos, lotus flowers, and vibrant fruits. Committed to making art accessible, Ashley strives to offer intricate and high-quality artworks at affordable prices, allowing everyone to bring a piece of culture and beauty into their homes.
  </p>
</section>

<!-- Contact Section -->
<section id="contact">
  <h2>Contact Ashley</h2>
  <p>
    Interested in purchasing a piece or have any questions? Feel free to reach out!
  </p>
  <p>Email: <a href="mailto:ashleymwang@yahoo.com">ashleymwang@yahoo.com</a></p>
  <p>Phone: (603) 277-8450</p>
</section>

<!-- Footer -->
<footer>
  <p>&copy; 2024 Ashley's Art Collection. All rights reserved.</p>
  <p>
    <!-- Social Media Links -->
    <a href="https://www.instagram.com/ashleyart" target="_blank"><i class="fab fa-instagram"></i></a>
    <a href="https://www.facebook.com/ashleyart" target="_blank"><i class="fab fa-facebook-f"></i></a>
    <a href="https://www.twitter.com/ashleyart" target="_blank"><i class="fab fa-twitter"></i></a>
  </p>
</footer>

<!-- Link to Lightbox2 JS for interactive gallery -->
<script src="https://cdnjs.cloudflare.com/ajax/libs/lightbox2/2.11.3/js/lightbox.min.js"></script>

<!-- Simple JavaScript for Tabs -->
<script>
  function openTab(evt, tabName) {
    // Declare all variables
    var i, tabcontent, tablinks;

    // Get all elements with class="tabcontent" and hide them
    tabcontent = document.getElementsByClassName("tabcontent");
    for (i = 0; i < tabcontent.length; i++) {
      tabcontent[i].classList.remove("active");
    }

    // Get all elements with class="tablink" and remove the class "active"
    tablinks = document.getElementsByClassName("tablink");
    for (i = 0; i < tablinks.length; i++) {
      tablinks[i].classList.remove("active");
    }

    // Show the current tab, and add an "active" class to the button that opened the tab
    document.getElementById(tabName).classList.add("active");
    evt.currentTarget.classList.add("active");
  }
</script>
