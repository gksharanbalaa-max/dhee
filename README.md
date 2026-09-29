# dhee
My project is about Employee salary prediction 

My HTML code :

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Employee Salary Prediction</title>

    <style>
        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
            font-family: Arial, sans-serif;
        }

        body {
            min-height: 100vh;
            background: linear-gradient(135deg, #667eea, #764ba2);
            display: flex;
            justify-content: center;
            align-items: center;
            padding: 30px;
        }

        .container {
            width: 100%;
            max-width: 650px;
            background: white;
            padding: 35px;
            border-radius: 18px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.2);
        }

        h1 {
            text-align: center;
            color: #333;
            margin-bottom: 10px;
        }

        .description {
            text-align: center;
            color: #666;
            margin-bottom: 25px;
        }

        .form-group {
            margin-bottom: 18px;
        }

        label {
            display: block;
            margin-bottom: 7px;
            font-weight: bold;
            color: #444;
        }

        input,
        select {
            width: 100%;
            padding: 12px;
            border: 1px solid #ccc;
            border-radius: 8px;
            font-size: 15px;
        }

        input:focus,
        select:focus {
            outline: none;
            border-color: #667eea;
        }

        button {
            width: 100%;
            padding: 14px;
            border: none;
            border-radius: 8px;
            background: #667eea;
            color: white;
            font-size: 17px;
            font-weight: bold;
            cursor: pointer;
            margin-top: 10px;
        }

        button:hover {
            background: #5568d9;
        }

        .result {
            margin-top: 25px;
            padding: 20px;
            background: #f1f5ff;
            border-radius: 10px;
            text-align: center;
            display: none;
        }

        .result h2 {
            color: #333;
            margin-bottom: 8px;
        }

        #salary {
            color: #667eea;
            font-size: 25px;
            font-weight: bold;
        }

        .footer {
            text-align: center;
            margin-top: 20px;
            color: #888;
            font-size: 13px;
        }
    </style>
</head>

<body>

<div class="container">

    <h1>Employee Salary Prediction</h1>

    <p class="description">
        Enter employee details to predict the estimated salary.
    </p>

    <form id="salaryForm">

        <div class="form-group">
            <label for="age">Age</label>
            <input type="number" id="age" name="age"
                   min="18" max="70" required>
        </div>

        <div class="form-group">
            <label for="experience">Years of Experience</label>
            <input type="number" id="experience" name="experience"
                   min="0" max="50" step="0.1" required>
        </div>

        <div class="form-group">
            <label for="education">Education Level</label>
            <select id="education" name="education" required>
                <option value="">Select Education</option>
                <option value="High School">High School</option>
                <option value="Bachelor">Bachelor's Degree</option>
                <option value="Master">Master's Degree</option>
                <option value="PhD">PhD</option>
            </select>
        </div>

        <div class="form-group">
            <label for="job">Job Role</label>
            <select id="job" name="job" required>
                <option value="">Select Job Role</option>
                <option value="Software Engineer">Software Engineer</option>
                <option value="Data Analyst">Data Analyst</option>
                <option value="Data Scientist">Data Scientist</option>
                <option value="Manager">Manager</option>
                <option value="HR">HR</option>
                <option value="Accountant">Accountant</option>
            </select>
        </div>

        <div class="form-group">
            <label for="location">Location</label>
            <select id="location" name="location" required>
                <option value="">Select Location</option>
                <option value="Chennai">Chennai</option>
                <option value="Bangalore">Bangalore</option>
                <option value="Hyderabad">Hyderabad</option>
                <option value="Mumbai">Mumbai</option>
                <option value="Delhi">Delhi</option>
            </select>
        </div>

        <button type="submit">Predict Salary</button>

    </form>

    <div class="result" id="result">
        <h2>Estimated Salary</h2>
        <p id="salary">₹0</p>
    </div>

    <div class="footer">
        Employee Salary Prediction System
    </div>

</div>

<script>
    document.getElementById("salaryForm").addEventListener("submit", function(event) {

        event.preventDefault();

        /*
         * This is only a demo calculation.
         * Replace this section with a request to your
         * machine-learning backend.
         */

        const age = Number(document.getElementById("age").value);
        const experience = Number(
            document.getElementById("experience").value
        );

        // Demo formula — NOT an ML prediction
        let predictedSalary = 25000 + (experience * 7000) + (age * 500);

        document.getElementById("salary").textContent =
            "₹" + Math.round(predictedSalary).toLocaleString("en-IN");

        document.getElementById("result").style.display = "block";
    });
</script>

</body>
</html>

it is totally about Employee salary prediction
