<!DOCTYPE html>
<html lang="it">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1" />
<title>Bottone con richiesta GET</title>
<style>
  .lgbt-button {
    padding: 12px 24px;
    font-size: 18px;
    color: white;
    border: none;
    border-radius: 8px;
    cursor: pointer;
    background: linear-gradient(90deg, 
      #E40303, /* rosso */
      #FF8C00, /* arancio */
      #FFED00, /* giallo */
      #008026, /* verde */
      #004DFF, /* blu */
      #750787  /* viola */
    );
    transition: transform 0.2s ease;
  }
  .lgbt-button:hover {
    transform: scale(1.05);
  }
</style>
</head>
<body>

<button class="lgbt-button" onclick="sendGetRequest()">Clicca per GET</button>

<script>
  function sendGetRequest() {
    fetch('https://jsonplaceholder.typicode.com/todos/1') // esempio URL GET
      .then(response => response.json())
      .then(data => {
        alert('Risposta ricevuta: ' + JSON.stringify(data));
      })
      .catch(error => {
        alert('Errore nella richiesta: ' + error);
      });
  }
</script>

</body>
</html>
