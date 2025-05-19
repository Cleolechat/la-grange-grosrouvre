# la-grange-grosrouvre
<!DOCTYPE html>
<html lang="fr">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>La Grange de Grosrouvre</title>
  <link href="https://cdn.jsdelivr.net/npm/tailwindcss@2.2.19/dist/tailwind.min.css" rel="stylesheet">
  <link rel="stylesheet" href="https://unpkg.com/leaflet@1.9.3/dist/leaflet.css" />
  <script src="https://unpkg.com/leaflet@1.9.3/dist/leaflet.js"></script>
  <style>
    #map { height: 300px; }
  </style>
</head>
<body class="bg-gray-50 text-gray-800 font-sans">
  <header class="bg-green-800 text-white p-6 text-center">
    <h1 class="text-3xl font-bold">La Grange de Grosrouvre</h1>
    <p class="text-lg mt-2">Maison à louer les week-ends et vacances à Grosrouvre (78490)</p>
  </header>

  <section class="max-w-5xl mx-auto p-6">
    <h2 class="text-2xl font-semibold mb-4">Bienvenue !</h2>
    <p class="mb-4">
      Charmante maison au cœur de la nature, à seulement 50 mètres de la forêt de Rambouillet et 5 minutes de Montfort l'Amaury. Idéale pour les séjours en famille ou entre amis.
    </p>
    <ul class="list-disc list-inside mb-6">
      <li>Capacité : 10 personnes</li>
      <li>5 chambres, 2 salles de bain</li>
      <li>Wifi, cheminée, grand jardin de 5000 m²</li>
      <li>Portique avec balançoire pour les enfants</li>
      <li>Prix : 400€ par nuit</li>
    </ul>

    <h3 class="text-xl font-semibold mb-2">Galerie</h3>
    <div class="grid grid-cols-1 md:grid-cols-2 gap-4 mb-6">
      <img src="IMG1.jpg" alt="Chambre 1" class="w-full rounded-lg shadow" />
      <img src="IMG2.jpg" alt="Chambre 2" class="w-full rounded-lg shadow" />
      <img src="IMG3.jpg" alt="Salon" class="w-full rounded-lg shadow" />
      <img src="IMG4.jpg" alt="Salle à manger" class="w-full rounded-lg shadow" />
      <img src="IMG5.jpg" alt="Salle de bain" class="w-full rounded-lg shadow" />
      <img src="IMG6.jpg" alt="Extérieur" class="w-full rounded-lg shadow" />
    </div>

    <h3 class="text-xl font-semibold mb-2">Localisation</h3>
    <div id="map" class="mb-6 rounded-lg shadow"></div>

    <h3 class="text-xl font-semibold mb-2">Disponibilités & Réservations</h3>
    <p class="mb-2">Veuillez nous envoyer un email pour réserver :</p>
    <a href="mailto:location@grange-grosrouvre.fr" class="text-blue-600 underline">location@grange-grosrouvre.fr</a>
  </section>

  <footer class="bg-green-800 text-white text-center p-4">
    © 2025 La Grange de Grosrouvre
  </footer>

  <script>
    const map = L.map('map').setView([48.7815, 1.7875], 14);
    L.tileLayer('https://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png', {
      attribution: '&copy; OpenStreetMap contributors'
    }).addTo(map);
    L.marker([48.7815, 1.7875]).addTo(map)
      .bindPopup("La Grange de Grosrouvre<br>53 route des Haizettes")
      .openPopup();
  </script>
</body>
</html>
