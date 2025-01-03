<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>1113572 - exercise 24</title>
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
    // Function to calculate and display the circumference
    function calcCircumference(radius) {
      const circumference = 2 * Math.PI * radius;
      return circumference.toFixed(2);
    }

    // Function to calculate and display the area
    function calcArea(radius) {
      const area = Math.PI * Math.pow(radius, 2);
      return area.toFixed(2);
    }

    // Function to handle user input and update results
    function calculateCircleProperties() {
      const radius = parseFloat(document.getElementById('radius').value);
      if (isNaN(radius) || radius <= 0) {
        alert('Please enter a valid positive number for the radius.');
        return;
      }

      const circumference = calcCircumference(radius);
      const area = calcArea(radius);

      document.getElementById('circumferenceResult').textContent = The circumference is: ${circumference};
      document.getElementById('areaResult').textContent = The area is: ${area};
    }
  </script>
</body>
</html>
