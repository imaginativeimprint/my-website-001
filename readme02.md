<!DOCTYPE html>
<html lang="en">
<head>
   <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
   <title>My Website</title>
   <style>
    /* Body styling */
    body {
      font-family: Arial, sans-serif;
      margin: 20px;
      transition: background-color 0.3s, color 0.3s, filter 0.3s; /* Smooth transition for blur effect */
    }

    /* Background modes */
    body.light-mode {
      background-color: #ffffff;
      color: #000000;
    }
    body.dark-mode {
      background-color: #000000;
      color: #ffffff;
    }
    body.blur {
      filter: blur(5px); /* Apply blur effect to body when menu is open */
    }

    /* Kebab menu styling */
    .kebab-menu {
      position: absolute;
      top: 10px;
      right: 10px;
      display: inline-block;
    }

    .kebab-icon {
      cursor: pointer;
      font-size: 24px;
    }

    /* Dropdown menu styling */
    .menu-dropdown {
      display: none; /* Initially hidden */
      position: fixed; /* Centered relative to the viewport */
      top: 50%; /* Center vertically */
      left: 50%; /* Center horizontally */
      transform: translate(-50%, -50%); /* Corrects alignment */
      background-color: #f1f1f1;
      box-shadow: 0px 8px 16px rgba(0, 0, 0, 0.2);
      padding: 20px; /* Add padding inside the menu */
      width: 300px; /* Medium size */
      text-align: center; /* Center content inside */
      z-index: 1000; /* Bring to the front */
      border-radius: 10px; /* Optional rounded edges */
    }

    /* Dropdown menu links and buttons styling */
    .menu-dropdown a, .menu-dropdown button {
      display: block;
      margin: 10px 0;
      text-decoration: none;
      color: #333;
    }

    .menu-dropdown a:hover, .menu-dropdown button:hover {
      text-decoration: underline;
    }

    /* Overlay styling for blurring background */
    .overlay {
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      background: rgba(0, 0, 0, 0.5); /* Semi-transparent overlay */
      display: none; /* Initially hidden */
      z-index: 999; /* Below the menu but above everything else */
    }
  </style>
</head>
<body>

  <!-- Kebab Menu Icon -->
  <div class="kebab-menu">
    <span class="kebab-icon" onclick="toggleMenu()">☰</span>
  </div>

  <!-- Dropdown Menu -->
  <div class="overlay" onclick="toggleMenu()"></div>
  <div class="menu-dropdown">
    <h3>Menu</h3>
    <a href="#">Link 1</a>
    <a href="#">Link 2</a>
    <button onclick="toggleMenu()">Close</button>
  </div>

  <script>
    // JavaScript to handle menu toggle
    function toggleMenu() {
      const body = document.body;
      const menu = document.querySelector('.menu-dropdown');
      const overlay = document.querySelector('.overlay');

      // Toggle menu and background blur
      if (menu.style.display === 'block') {
        menu.style.display = 'none'; // Hide menu
        overlay.style.display = 'none'; // Hide overlay
        body.classList.remove('blur'); // Remove blur
      } else {
        menu.style.display = 'block'; // Show menu
        overlay.style.display = 'block'; // Show overlay
        body.classList.add('blur'); // Apply blur
      }
    }
  </script>
</head>
<body class="light-mode">
  <div class="kebab-menu">
    <div class="kebab-icon" onclick="toggleMenu()">☰</div>
    <div class="menu-dropdown" id="dropdown">
      <div>
        <strong>Owner Profile</strong>
        <p><img src="C:\Users\user\OneDrive\Pictures\Screenshots\Screenshot 2025-02-10 220135.png" alt="Profile Photo" style="width:50px;height:50px;border-radius:50%;"></p>
        <p>Name: Shashank</p>
        <p>Email: shashank18at2024@gmail.com</p>
      </div>
      <details>
            <summary>
                <h6 id="section1">Educational qualification</h6>
            </summary>
            <p>
                <ul>
                    <li>
                        <h7>Bachelor of Engineering in Computer Science and Engineering (2025 - Present)</h7>
                        Currently pursuing my 1st semester at East West Institute of Technology through CET quota.<br>
                        Gaining foundational knowledge in computer science principles and practical applications.
                    </li>
                </ul>
                <br>
                <ul>
                    <li>
                        <h7>Pre-University Course (PUC) - Science Stream (2022 - 2024)</h7>
                        Secured distinction in the Karnataka Pre-University Examination.<br>
                        Specialized in subjects like Physics, Chemistry, Mathematics.
                    </li>
                </ul>
                <br>
                <ul>
                    <li>
                        <h7>Secondary Education (2012 - 2022)</h7>
                        Achieved distinction in the Karnataka Secondary Education Examination (10th Standard).
                    </li>
                </ul>
                <ul>
                    <li>
                        <h7>Skills and Certifications</h7>
                        Proficient in Python, HTML, and Web Development.<br>
                        Successfully completed relevant courses and hands-on projects in web technologies.
                    </li>
                </ul>
            </p>
        </details>
      <button onclick="toggleTheme()">Toggle Theme</button>
      <div class="menu-dropdown" id="dropdown">
  <div>
    <strong>Your Profile</strong>
    <p>
      <img src="C:\Users\user\OneDrive\Pictures\Screenshots\Screenshot 2025-02-10 220135.png" alt="Profile Photo" style="width:50px;height:50px;border-radius:50%;">
    </p>
    <p>Name: Shashank</p>
    <p>Email: shashank18at2024@gmail.com</p>
  </div>
  <button onclick="toggleTheme()">Toggle Theme</button>

  <!-- Educational Qualification Section -->
  <div>
    
  </div>
</div>

    </div>
  </div>
  <script>
    function toggleMenu() {
      const dropdown = document.getElementById('dropdown');
      dropdown.style.display = dropdown.style.display === 'block' ? 'none' : 'block';
    }
    function toggleTheme() {
      document.body.classList.toggle('dark-mode');
      document.body.classList.toggle('light-mode');
    }
  </script>
</body>
</html>
    <style>
        /* Inline CSS */
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            background-color: #f4f4f9;
            color: #333;
        }
        header {
            background-image: url(https://assets.onecompiler.app/42zp5pya9/43bjn4kvr/1812589.jpg);
            color: white;
            text-align: center;
            padding: 1em;
        }
        nav {
            text-align: center;
            margin: 10px 0;
        }
        nav a {
            text-decoration: none;
            margin: 0 10px;
            color: #4CAF50;
        }
        nav a:hover {
            color: #007BFF;
        }
        main {
            padding: 20px;
        }
        footer {
            background: #333;
            color: white;
            text-align: center;
            padding: 1em 0;
            position: fixed;
            bottom: 0;
            width: 100%;
        }
        a {
            text-decoration: none;
            color: #007BFF;
            margin: 0 10px;
        }
        a:hover {
            color: #4CAF50;
        }
    </style>
</head>
<body>
    <header>
        <h1>Welcome to My Website</h1>
    </header>
    <nav>
        <a href="http://www.linkedin.com/in/shashank-p-6966b0315">About Me</a>
        <a href="#section1">Educational Qualification</a>
        <a href="#section2">Section 2</a>
        <a href="#section3">Section 3</a>
    </nav>
    <main>
        <h2 id="about">About Me</h2>
        <p>Hello! I'm Shashank P, passionate about the technology field.</p> 
        <details>
            <summary>
                <h2 id="section1">section 1</h2>
            </summary>
            <p>
                
            </p>
        </details>
        <details>
            <summary>
                <h2 id="section2">Python Basic PDF</h2>
            </summary>
            <p>
                <a href="https://docs.google.com/document/d/1eTNzsIDHbGF_3FBRk7L6-RM3HeFyWyeL3Rbp8IcaJzM/edit?usp=drivesdk" target="_blank" download>Click here to download the PDF</a><br>
                <iframe src="https://docs.google.com/document/d/1eTNzsIDHbGF_3FBRk7L6-RM3HeFyWyeL3Rbp8IcaJzM/edit?usp=drivesdk" width="400px" height="600px">
                    Your browser does not support iframes. Please
                    <a href="https://docs.google.com/document/d/1eTNzsIDHbGF_3FBRk7L6-RM3HeFyWyeL3Rbp8IcaJzM/edit?usp=drivesdk">download the PDF here</a>
                </iframe>
            </p>
        </details>
        <details>
            <summary>
                <h2 id="section3">Python Simple Project</h2>
            </summary>
            <p>
                <a href="https://docs.google.com/document/d/1KTYYMn3Lgany40ugcwd_jSzFmMoxCvTeXFx10FdCxW0/edit?usp=drivesdk" target="_blank" download>Click here to download the PDF</a><br>
                <iframe src="https://docs.google.com/document/d/1KTYYMn3Lgany40ugcwd_jSzFmMoxCvTeXFx10FdCxW0/edit?usp=drivesdk" width="400px" height="600px">
                    Your browser does not support iframes. Please
                    <a href="https://docs.google.com/document/d/1KTYYMn3Lgany40ugcwd_jSzFmMoxCvTeXFx10FdCxW0/edit?usp=drivesdk">download the PDF here</a>
                </iframe>
            </p>
        </details>
        <br>
        <p>Explore my profiles below:</p>
        <div>
            <a href="https://www.linkedin.com/in/shashank-p-6966b0315?miniProfileUrn=urn%3Ali%3Afs_miniProfile%3AACoAAFAD1tIBWeJ5El079otY4ykuY0YsitNCQ3c&lipi=urn%3Ali%3Apage%3Ad_flagship3_search_srp_all%3BypVV2GC8T7Sg2nboNafnLQ%3D%3D" target="_blank" onclick="return showAlert();">LinkedIn</a> |
            <a href="https://www.instagram.com/imaginative_imprint" target="_blank" onclick="return showAlert1();">Instagram</a> |
            <a href="https://github.com/imaginativeimprint" target="_blank" onclick="return showAlert2();">GitHub</a>
        </div>
    </main>
    <footer>
        <p>&copy; 2025 My Website. All rights reserved.</p>
    </footer>
    <script>
        function showAlert() {
            alert("Opening LinkedIn Profile");
            return true; // Allow navigation to proceed
        }

        function showAlert1() {
            alert("Opening Instagram Profile");
            return true; // Allow navigation to proceed
        }

        function showAlert2() {
            alert("Opening GitHub Profile");
            return true; // Allow navigation to proceed
        }
    </script>
</body>
</html>
