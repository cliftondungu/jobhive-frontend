<template>
  <footer class="footer">
    <div class="container">
      <p>&copy; {{ currentYear }} JobHive. All rights reserved.</p>
    </div>
  </footer>
</template>

  <script>
  export default {
    data() {
      return {
        currentYear: new Date().getFullYear()
      }
    }
  }
  </script>
  
  <style>
  .footer {
    display: grid;
    grid-template-columns: 1fr;
    background-color: #f5f5f5;
    padding: 20px;
    font-size: 14px;
    text-align: center;
    box-shadow: 0 -2px 4px rgba(0, 0, 0, 0.1);
  }
  
  .container {
    display: grid;
    grid-template-columns: auto 1fr;
    align-items: center;
    max-width: 960px;
    margin: 0 auto;
  }
  
  nav ul {
    list-style: none;
    margin: 0;
    padding: 0;
    display: flex;
    justify-content: center;
  }
  
  nav li {
    margin: 0 10px;
  }
  
  nav a {
    text-decoration: none;
    color: #333;
    transition: color 0.2s ease-in-out;
  }
  
  nav a:hover {
    color: #0066cc;
  }
  </style>
  