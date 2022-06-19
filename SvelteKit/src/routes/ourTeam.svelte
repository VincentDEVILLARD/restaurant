<body>
        <h1>Our team</h1>

        <p style="margin:25px 100px">We are a team of three French students, all members of the Media and Digital Chair. We created this website about a brunch and healthy restaurant, because it seemed interesting to code such a website.</p>

        <div class="blank"></div>

        <div class="grid-container">
            <div class="first column">
                <div class="photo"><img src="https://media-exp1.licdn.com/dms/image/C4E03AQGfemGvNWru8A/profile-displayphoto-shrink_400_400/0/1611926167825?e=1661385600&v=beta&t=5kHCVRwIzK3oBrioFtQ_rhVmv16aWFUpJowTd0yjPxk" alt='This is Margot'></div>
                <h4><a href="https://www.linkedin.com/in/margot-clavel/">Margot Clavel</a></h4>
                <p>Advanced Master Student in Marketing and Digital.<br>She is from Lyon.<br>Her favorite food is avocado toast !</p>
            </div>

            <div class ="second column">
                <div class="photo"><img src="https://media-exp1.licdn.com/dms/image/C4E03AQEOKvJcbA4MJw/profile-displayphoto-shrink_400_400/0/1642762022194?e=1661385600&v=beta&t=pRA0UGQC7ZR3WbQTLZ5jZHO7rm7V7vIe66EIK5kV46Y" alt='This is Marie-Clementine'></div>
                <h4><a href="https://www.linkedin.com/in/marie-clementine-crestia">Marie-Clémentine Crestia</a></h4>
                <p>Third year student of the Master in Management, PGE Program.<br>She is from Bordeaux.<br>Her favorite food is risotto !</p>
            </div>

            <div class ="third column">
                <div class="photo"><img src="https://media-exp1.licdn.com/dms/image/C4D03AQHMQM_lKky9iA/profile-displayphoto-shrink_400_400/0/1614090638272?e=1661385600&v=beta&t=K5T-DhITZ_sbyqFx8JRY994FirmNMy-33-5quLtTPFQ" alt='This is Vincent'></div>
                <h4><a href="https://www.linkedin.com/in/vincent-devillard/">Vincent Devillard</a></h4>
                <p>Fourth year student of the Master in Management, PGE Program.<br>He is from Lyon.<br>His favorite food is pizza !</p>
            </div>

        </div>




    </body>

<style>
    h1{
        text-align: center;
        font-size: 50px;
    }

    h4{
        text-align: center;
    }

    p{
        text-align: justify;
        margin: 10px;
    }

    .grid-container{
        display: grid;
        justify-content: center;
        grid-template-columns: repeat(3, 300px);
        column-gap: 100px;
        margin-left:25px;
        margin-right: 25px;
    }

    .column{
        border: 2px hsl(85,34%,60%) solid;
        justify-content: center;
    }

    .first{
        grid-column: 1 / 2;
    }

    .second{
        grid-column: 2 / 3;
    }

    .third{
        grid-column: 3 / 4;
    }

    img{
        width: 280px;
        justify-content:center;
    }

    .photo{
        margin: 5px;
        justify-content: center;
    }

    .blank{
        height: 3vh;
    }

</style>