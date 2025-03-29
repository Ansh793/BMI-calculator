Weight (kg):
Height (m):
Calculate
<script>
    function calculateBMI() {
        let weight = document.getElementById('weight').value;
        let height = document.getElementById('height').value;
        if (weight > 0 && height > 0) {
            let bmi = weight / (height * height);
            let category = '';
            if (bmi < 18.5) {
                category = 'Underweight';
            } else if (bmi < 24.9) {
                category = 'Normal weight';
            } else if (bmi < 29.9) {
                category = 'Overweight';
            } else {
                category = 'Obese';
            }
            document.getElementById('result').innerText = `BMI: ${bmi.toFixed(2)} (${category})`;
        } else {
            document.getElementById('result').innerText = 'Please enter valid values';
        }
    }
</script>
