<!DOCTYPE html>
<html>
<head>
<title>BIENVENIDO A MI WI-FI - Conexión Gratuita</title>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<style>
  body {
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    text-align: center;
    margin: 0;
    height: 100vh;
    display: flex;
    justify-content: center;
    align-items: center;
    background-image: url('https://i.ibb.co/zHRxpJdF/924c5899ef57dc11f50a81cd8eaba285-0.webp');
    background-size: cover;
    background-position: center center;
    background-repeat: no-repeat;
    background-attachment: fixed;
    background-color: #f0f2f5;
    overflow: hidden;
  }

  .portal-overlay {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background-color: rgba(0, 0, 0, 0.6); 
    z-index: -1;
  }

  .portal-container {
    width: 90%;
    max-width: 450px;
    background: transparent; 
    border-radius: 12px;
    box-shadow: 0 10px 25px rgba(0, 0, 0, 0.2); 
    padding: 30px;
    display: flex;
    flex-direction: column;
    align-items: center;
    position: relative;
    z-index: 1;
    border: 1px solid rgba(255, 255, 255, 0.3);
  }

  .content {
    color: white; 
    text-align: center;
    text-shadow: 1px 1px 3px rgba(0, 0, 0, 0.8); 
    width: 100%; 
  }

  h1 {
    color: #ffffff; 
    margin-bottom: 15px;
    font-size: 1.8em;
    text-transform: uppercase; /* ¡Todo a mayúsculas con CSS! */
  }

  p {
    font-size: 1.0em;
    line-height: 1.6;
    margin-bottom: 20px;
    color: #e0e0e0; 
  }

  .terms-acceptance {
    margin-bottom: 25px; 
    display: flex;
    align-items: center;
    justify-content: center; 
    font-size: 0.95em;
    color: #cccccc;
    text-shadow: none; 
  }

  .terms-acceptance input[type="checkbox"] {
    margin-right: 8px;
    width: 18px; 
    height: 18px;
    accent-color: #28a745; 
  }

  .terms-acceptance a {
    color: #87CEEB !important; 
    text-decoration: none;
    font-weight: bold; 
  }

  .connect-button {
    background-color: #28a745; 
    color: white;
    padding: 14px 30px;
    text-align: center;
    text-decoration: none;
    display: inline-block;
    font-size: 1.1em;
    border-radius: 8px;
    cursor: pointer;
    transition: background-color 0.3s ease;
    border: none;
    opacity: 0.6;
    pointer-events: none;
  }

  .connect-button.active { 
    opacity: 1;
    pointer-events: auto;
  }

  .connect-button:hover {
    background-color: #218838; 
    box-shadow: 0 4px 10px rgba(0, 0, 0, 0.2);
  }

  .info-text {
    font-size: 0.9em;
    color: #cccccc; 
    margin-top: 25px;
  }

  .info-text a {
    color: #87CEEB !important; 
    text-decoration: none;
  }

  @media (max-width: 600px) {
    .portal-container {
      width: 95%;
      padding: 20px;
    }
    h1 {
      font-size: 1.5em;
    }
    .connect-button {
      padding: 12px 25px;
      font-size: 1em;
    }
  }
</style>
</head>
<body>

  <div class="portal-overlay"></div> 

  <div class="portal-container">
    <div class="content">
      <!-- Texto del h1 ahora en mayúsculas -->
      <h1>BIENVENIDO A MI WI-FI!</h1>
      <p>Disfruta de mi conexión a Internet de alta velocidad.</p>

      <div class="terms-acceptance">
        <input type="checkbox" id="acceptTerms">
        <label for="acceptTerms">Acepto los <a href="#" target="_blank">Términos y Condiciones</a></label>
      </div>

      <a href="http://www.google.com" id="connectButton" class="connect-button">Conectar a Internet</a>

      <p class="info-text">Al conectar, se aplica mi política de privacidad.</p>
    </div>
  </div>

  <script>
    const acceptTermsCheckbox = document.getElementById('acceptTerms');
    const connectButton = document.getElementById('connectButton');

    acceptTermsCheckbox.addEventListener('change', function() {
      if (this.checked) {
        connectButton.classList.add('active');
        connectButton.style.cursor = 'pointer';
        connectButton.href = "http://www.google.com";
      } else {
        connectButton.classList.remove('active');
        connectButton.style.cursor = 'not-allowed';
        connectButton.href = "#";
      }
    });

    window.onload = function() {
      connectButton.classList.remove('active');
      connectButton.style.cursor = 'not-allowed';
      connectButton.href = "#";
    };
  </script>

</body>
</html>
