<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Circle Properties Calculator</title>
</head>
<body>

  <h1>Circle Properties Calculator</h1>

  <label for="radius">Enter the radius of the circle:</label>
  <input type="number" id="radius" placeholder="Radius" step="any">

  <button onclick="calculateCircleProperties()">Calculate</button>

  <h2>Results:</h2>
  <p id="circumferenceResult">The circumference is: </p>
  <p id="areaResult">The area is: </p>

  <script>
    function calculateCircleProperties() {
      // Get the radius value from the input
      const radius = parseFloat(document.getElementById('radius').value);
      
      // Check if the radius is a valid positive number
      if (isNaN(radius) || radius <= 0) {
        alert('Please enter a valid positive number for the radius.');
        return;
      }
      
      // Calculate the circumference and area
      const circumference = 2 * Math.PI * radius;
      const area = Math.PI * radius * radius;

      // Display the results with 2 decimal places
      document.getElementById('circumferenceResult').textContent = 'The circumference is: ' + circumference.toFixed(2);
      document.getElementById('areaResult').textContent = 'The area is: ' + area.toFixed(2);
    }
  </script>

</body>
</html>
