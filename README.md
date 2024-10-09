<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Travel Reservation Form</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 20px;
        }
        .container {
            width: 350px;
            margin: 0 auto;
            padding: 20px;
            border: 1px solid #ccc;
            border-radius: 5px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
        }
        h1 {
            font-size: 24px;
            text-align: center;
        }
        b {
            display: block;
            margin-bottom: 15px;
            text-align: left;
        }
        label {
            display: block;
            margin-bottom: 5px;
            font-weight: bold;
        }
        input[type="text"],
        input[type="email"],
        input[type="date"],
        select {
            width: 49%;
            padding: 8px;
            margin-bottom: 10px;
            border: 1px solid #ccc;
            border-radius: 3px;
        }
        input[type="checkbox"],
        input[type="radio"] {
            margin-right: 5px;
        }
        .checkbox-group,
        .radio-group {
            margin-bottom: 10px;
        }
        .checkbox-group label,
        .radio-group label {
            display: inline-block;
            margin-right: 10px;
            font-weight: bold;
        }
        .submit-btn {
            width: 80%;
            padding: 10px;
            background-color: #e4dfdf;
            color: rgb(5, 5, 5);
            border: 0.5px solid #ccc;
            border-radius: 3px;
            cursor: pointer;
        }
        .checkbox-group, .radio-group {
            display: flex;
            flex-direction: column;
        }
        .terms-label {
            font-weight: bold;
        }
        .radio-group-inline {
            display: flex;
            align-items: center;
        }
        .radio-group-inline label {
            margin-right: 20px;
        }

        /* Chỉnh kích thước ô chọn tour nhỏ hơn một nửa */
        select#tourpackage {
            width: 24%; /* Giảm còn 1 nửa so với các ô khác */
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>Travel reservation form</h1>
        <b>* denotes mandatory</b>
        <form>
            <label for="fullname">Full name*:</label>
            <input type="text" id="fullname" name="fullname" placeholder="FirstName LastName" required>
            
            <label for="email">Email address*:</label>
            <input type="email" id="email" name="email" placeholder="EMAIL_ADDRESS" required>
            
            <label for="tourpackage">Select Tour Package*:</label>
            <select id="tourpackage" name="tourpackage" required>
                <option value="goa">Goa</option>
            </select>
            
            <label for="arrivaldate">Arrival date*:</label>
            <input type="date" id="arrivaldate" name="arrivaldate" required>
            
            <label for="numofpersons">Number of persons*:</label>
            <input type="text" id="numofpersons" name="numofpersons" placeholder="UNKNOWN_TYPE" required>
            
            <b>What would you want to avail?*</b>
            <div class="checkbox-group">
                <label>Boarding<input type="checkbox" id="boarding" name="boarding"></label>
                <label>Fooding<input type="checkbox" id="fooding" name="fooding"></label>
                <label>Sight seeing<input type="checkbox" id="sightseeing" name="sightseeing"></label>
            </div>
            
            <label for="couponcode">Discount Coupon code:</label>
            <input type="text" id="couponcode" name="couponcode" placeholder="UNKNOWN_TYPE"> 
            
            <p class="terms-label">Terms and conditions*</p>
            <div class="radio-group-inline">
                <label><input type="radio" id="agree" name="terms" value="agree" required> I agree</label>
                <label><input type="radio" id="disagree" name="terms" value="disagree" required> I disagree</label>
            </div>
            
            <button type="submit" class="submit-btn">Complete reservation</button>
        </form>
    </div>
</body>
</html>
