<body>
    <h1>Contact Us</h1>

    <div class="grid-container">
        <div class="phoneAddress">
            <br>
            <h3>Phone Numbers</h3>
            <p>
                <img src="https://cdn.icon-icons.com/icons2/37/PNG/512/restaurant_4373.png" style="width:20px ; margin-right:5px">
                01.02.03.04.05<br>
                <img src="https://cdn.icon-icons.com/icons2/614/PNG/512/phone-call-auricular-symbol-in-black_icon-icons.com_56483.png" style="width:15px ; margin-right:10px">
                06.07.08.09.10
            </p> 
            <br>
            <h3>Address</h3>
            <p>1 avenue Bernard Hirsh<br>95000 CERGY<br></p>
        </div>

        <div class="openingHours">
            <h3>Opening Hours</h3>
            <div class="grid-hours-container">
                <p class="days" style="line-height:25px">Monday<br>
                    Tuesday<br>
                    Wednesday<br>
                    Thursday<br>
                    Friday<br>
                    Saturday<br>
                    Sunday
                </p>
                <p class="hours brunch" style="text-align:center">Brunch<br>10:00-15:00</p>
                <p class="hours tapas" style="text-align:center">Tapas<br>18:00-00:00</p>
                <img class="monday tapas" src="https://cdn.icon-icons.com/icons2/317/PNG/512/sign-check-icon_34365.png" style="width:20px">
                <img class="tuesday brunch" src="https://cdn.icon-icons.com/icons2/317/PNG/512/sign-check-icon_34365.png" style="width:20px">
                <img class="tuesday tapas" src="https://cdn.icon-icons.com/icons2/317/PNG/512/sign-check-icon_34365.png" style="width:20px">
                <img class="wednesday brunch" src="https://cdn.icon-icons.com/icons2/317/PNG/512/sign-check-icon_34365.png" style="width:20px">
                <img class="wednesday tapas" src="https://cdn.icon-icons.com/icons2/317/PNG/512/sign-check-icon_34365.png" style="width:20px">
                <img class="thursday brunch" src="https://cdn.icon-icons.com/icons2/317/PNG/512/sign-check-icon_34365.png" style="width:20px">
                <img class="thursday tapas" src="https://cdn.icon-icons.com/icons2/317/PNG/512/sign-check-icon_34365.png" style="width:20px">
                <img class="friday brunch" src="https://cdn.icon-icons.com/icons2/317/PNG/512/sign-check-icon_34365.png" style="width:20px">
                <img class="friday tapas" src="https://cdn.icon-icons.com/icons2/317/PNG/512/sign-check-icon_34365.png" style="width:20px">
                <img class="saturday brunch" src="https://cdn.icon-icons.com/icons2/317/PNG/512/sign-check-icon_34365.png" style="width:20px">
                <img class="saturday tapas" src="https://cdn.icon-icons.com/icons2/317/PNG/512/sign-check-icon_34365.png" style="width:20px">
                <img class="sunday brunch" src="https://cdn.icon-icons.com/icons2/317/PNG/512/sign-check-icon_34365.png" style="width:20px">
            </div>
        </div>

    </div>
   <!--plan ggmaps-->
    <iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d2615.7894982019775!2d2.0762479511534155!3d49.03361049620581!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x47e6f53ac7cdeffd%3A0xed5be7deea3e4bc1!2s1%20Av.%20Bernard%20Hirsch%2C%2095000%20Cergy!5e0!3m2!1sfr!2sfr!4v1655657461710!5m2!1sfr!2sfr" width="600" height="450" style="border:0;" allowfullscreen="" loading="lazy" referrerpolicy="no-referrer-when-downgrade"></iframe>

</body>

<style>
    body{
        margin:25px;
    }

    iframe{
        width:400px;
        height:400px;
    }

    h1{
        text-align: center;
    }

    .grid-container{
        display: grid;
        grid-template-columns: repeat(2, 50%);
        gap:75px;
    }

    .phoneAddress{
        grid-column: 2/3;
        grid-row: 1/2;
        justify-items: center;
    }

    .openingHours{
        grid-column: 1/2;
        grid-row: 1/2;
    }   

    .grid-hours-container{
        display: grid;
        grid-template-columns: repeat(3, 100px);
        grid-template-rows: 50px repeat(7,25px);
        justify-items: center;
        align-items: center;
        margin-bottom: 25px;
    }

    .days{
        grid-column: 1/2;
        grid-row:2/9
    }

    .monday{
        grid-row:2/3;
    }

    .tuesday{
        grid-row:3/4;
    }

    .wednesday{
        grid-row:4/5;
    }

    .thursday{
        grid-row:5/6;
    }

    .friday{
        grid-row:6/7;
    }

    .saturday{
        grid-row:7/8;
    }

    .sunday{
        grid-row: 8/9;
    }

    .brunch{
        grid-column: 2/3;
    }

    .tapas{
        grid-column: 3/4;
    }

</style>