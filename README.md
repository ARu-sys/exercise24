<!DOCTYPE html>
<html>
<head>
    <title>Circle Properties</title>
    <script>
        function calcCircumference(radius) {
            const circumference = 2 * Math.PI * radius;
            console.log(The circumference is ${circumference.toFixed(2)});
        }

        function calcArea(radius) {
            const area = Math.PI * radius * radius;
            console.log(The area is ${area.toFixed(2)});
        }

        // Call the functions with a sample radius
        const sampleRadius = 5; // You can change this value
        calcCircumference(sampleRadius);
        calcArea(sampleRadius);
    </script>
</head>
<body>
    <h1>Circle Properties</h1>
    <p>Open the console to see the calculations for circumference and area of a circle.</p>
    <p>The calculations are based on a sample radius of 5 (or any value you set in the script).</p>
</body>
</html>
