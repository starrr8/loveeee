<html>
<head>
    <title></title>
</head>
<body>
    <script src="https://ajax.googleapis.com/ajax/libs/jquery/3.2.1/jquery.min.js"></script>
    <script>
        function OnConfirm(msg, myYes) {
            var confirmBox = $("#confirm");
            confirmBox.find(".message").text(msg);
            confirmBox.find(".yes").unbind().click(function () {
                confirmBox.hide();
            });
            confirmBox.find(".yes").click(myYes);
            confirmBox.show();
        }
    </script>
    <style>
        #confirm {
            display: none;
            background-color: #F3F5F6;
            color: #000000;
            border: 1px solid #aaa;
            border-radius: 10px;
            position: fixed;
            width: 350px;
            height: 350px;
            left: 45%;
            top: 10%;
            margin-left: -100px;
            padding: 10px 20px 10px;
            box-sizing: border-box;
            text-align: center;
        }

            #confirm button {
                background-color: #FFFFFF;
                display: inline-block;
                border-radius: 12px;
                border: 1px solid #aaa;
                padding: 5px;
                text-align: center;
                width: 60px;
                cursor: pointer;
            }

            #confirm .message {
                text-align: left;
            }
        
        #boxes {
            position: absolute;
            left: 47%;
            top: 75%;
        }
    </style>
    <center>
    <div id="confirm">
        <div class="message"><img src ="sorry.gif" width = 100%; height= 100%;></div>
        <br />
        <a href = "sorry.html"><button class="yes">back</button></a>
    </div>
    <div id="boxes"><input type="button" value="Click meee!" onclick="OnConfirm();" /></div>
    </center>
</body>
</html>
