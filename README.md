<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title> Document </title>

    <style>
        .container {
            height: 600px;
            width: 100%;
            background-color: white;
            display: flex;
            justify-content: center;
            align-items: center;
        }

        .box1 {
            height: 500px;
            width: 50%;
            background-color: white;
            justify-content: center;
            margin-top: 3rem;
            margin-left: 3rem;

        }

        .box2 {

            height: 500px;
            width: 50%;
            display: flex;
            background-color:pink;
            justify-content: center;
            align-items: center;
            margin-top: 3rem;
            
        }

        .heading {
            justify-content: center;
            align-items: center;
            font-weight: lighter;
            color: red;
            font-size: x-small;
            font-family: Helvetica, Arial, sans-serif;
            margin-top: 5rem;

        }

        .main-heading {
            margin-top: 2rem;
            font-family: Helvetica, Arial, sans-serif;
            font-style: calc();
        
        }

        .btn-open-popup {
            height: 30px;
            background-color: red;
            width: 95px;
            color: aliceblue;
            border: 3px solid #f04a49;
            border-color: tomato;
            border-bottom: 0cap;
            border-right: tomato;
            margin-top: 1rem;
            font-size: 25px;
            cursor: pointer;
            padding: 12px 24px;
            font-size: 18px;
            border: none;
            transition: background-color 0.3s ease;
        }


        .btn:hover {
            background-color: brown;
            color: #fff;
            transition: all 0.5s ease 0s;
        }

        .btn-open-popup {
            padding: 12px 24px;
            font-size: 18px;
            background-color: green;
            color: #fff;
            border: none;
            border-radius: 8px;
            cursor: pointer;
            transition: background-color 0.3s ease;
        }

        .btn-open-popup:hover {
            background-color: rgb(213, 8, 8);
        }

        .overlay-container {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0, 0, 0, 0.6);
            justify-content: center;
            align-items: center;
            opacity: 0;
            transition: opacity 0.3s ease;
        }

        .popup-box {
            /* background: #fff; */
            background-color: pink;
            padding: 24px;
            border-radius: 12px;
            box-shadow: 0 0 20px rgba(0, 0, 0, 0.4);
            width: 320px;
            text-align: center;
            opacity: 0;
            transform: scale(0.8);
            animation: fadeInUp 0.5s ease-out forwards;
        }

        .form-container {
            display: flex;
            flex-direction:column;
        }

        /* .form-label {
            margin-bottom: 10px;
            font-size: 16px;
            color: #444;
            text-align: left;
        } */        

        .form-input {
            padding: 10px;
            margin-bottom: 20px;
            border: 1px solid #ccc;
            border-radius: 8px;
            font-size: 16px;
            width: 100%;
            box-sizing: border-box;
        }

        .btn-submit,
        .btn-close-popup {
            padding: 12px 24px;
            border: none;
            border-radius: 8px;
            cursor: pointer;
            transition: background-color 0.3s ease, color 0.3s ease;
        }

        .btn-submit {
            background-color: green;
            color: #fff;
        }

        .btn-close-popup {
            margin-top: 12px;
            background-color: #e74c3c;
            color: #fff;
        }

        .btn-submit:hover,
        .btn-close-popup:h over {
            background-color: #4caf50;
        }


        @keyframes fadeInUp {
            from {
                opacity: 0;
                transform: translateY(20px);
            }

            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        .overlay-container.show {
            display: flex;
            opacity: 1;
        }
    </style>
</head>
<body>
    <div class="container">
        <div class="box1">
            <div class="heading">
                <h1>AWARD WINNING </h1>
            </div>
            <div class="main-heading">
                <h1> DIGITAL MARKETING<br>
                    AGENCY</h1>
            </div>
            <p>Fyle has the singular aim of reducing the time and efforts spent on business expemse
                management giving accountants their precious timeback
                our real time ,user freiendly, platform makes expense reporting and accountants with
                never-before-seen visibility.
            </p>
            <button class="btn-open-popup" onclick="togglePopup()">
                contact
            </button>
            <div id="popupOverlay" class="overlay-container">
                <div class="popup-box">
                    <h2 style="color:black;">Talk to us</h2>
                    <form class="form-container">
                        <input class="form-input" type="text" placeholder="firstname" id="name" name="name" required>
                        <input class="form-input" type="text" placeholder="lastname" id="name" name="name" required>


                        <input class="form-input" type="email" placeholder="work email" id="email" name="email"
                            required>


                        <p> <input type="checkbox"> i agree to these terms and conditions, and provide consent to send
                            me communication</p>


                        <button class="btn-submit" type="submit">
                            <a href="C:\Users\shalini singh\OneDrive\Desktop\git demo\js\internshala\index2.html">submit</a>
                        </button>
                    </form>

                    <button class="btn-close-popup" onclick="togglePopup()">
                        Close
                    </button>
                </div>
            </div>
        </div>
        <div class="box2"></div>
    </div>
    <script>
        function togglePopup() {
            const overlay = document.getElementById('popupOverlay');
            overlay.classList.toggle('show');
        } 
    </script>






</body>

</html>
