# links
https://camposha.info/flutter-php-mysql-fill-listview-with-images-and-text/

https://medium.com/@santosenoque.ss/how-to-connect-flutter-app-to-mysql-web-server-and-phpmyadmin-e100f47bfb82

https://www.coderzheaven.com/2019/09/28/flutter-datatable-mysql/

https://flutter-examples.com/flutter-online-user-registration-using-php-mysql-server/

https://flutterawesome.com/a-flutter-application-that-demonstrate-simple-crud-operations/

https://github.com/idrcorner/Flutter-CRUD-phpMyAdmin

https://github.com/codigoalphacol/tiendaFlutterMysql

https://www.freecodecamp.org/news/learn-bootstrap-4-in-30-minute-by-building-a-landing-page-website-guide-for-beginners-f64e03833f33/

https://azmind.com/bootstrap-4-tutorial-one-page-website/

==============================================WP=========================================================
https://secondlinethemes.com/display-custom-post-types-wordpress/
https://github.com/technext/listrace
https://www.tychesoftwares.com/creating-custom-api-endpoints-in-the-wordpress-rest-api/
https://afterimagedesigns.com/wp-bootstrap-starter/components/
https://www.udemy.com/user/abul-hossain/
https://github.com/ranjanpandey2006/html5blank




















========vue=============

<!DOCTYPE html>
<html>
<head>
    <script src="https://cdn.jsdelivr.net/npm/vue"></script>
    <script src="https://unpkg.com/axios/dist/axios.min.js"></script>
    <style>
        .header {
            background-color: deepskyblue;
            color: #fff;
            text-align: center;
        }

        /* Alt + Shift + F - indent*/
        .button-fancy {
            background-color: dodgerblue;
            padding: 4px;
            color: white;
            font-size: 14px;
            font-weight: bold;
            border: none;
            border-radius: 10px;
            font-family: monospace, sans-serif;
            cursor: pointer;
            min-width: 100px;
            transition-property: background-color, width;
            transition-duration: 1s, 4s;
        }

        .button-fancy:hover {
            background-color: forestgreen;
            width: 200px;
        }

        .button-fancy-yellow {
            background-color: goldenrod;
        }

        #app {
            width: auto;
            margin-left: auto;
            margin-right: auto;
        }

        .spacer-bottom {
            margin-bottom: 5px;
        }

        input {
            padding: 8px;
            min-width: 160px;
            border: blue;
            border-bottom: blue;
            font-family: monospace;
        }
    </style>
   <meta name="viewport" content="width=device-width, initial-scale=1.0">
</head>

<body>
    <!--comment in html-->
    <div id="app">
        <h1 class="header">Playground Vue</h1>
        <h3>{{ name }}</h3>
        <p>{{age}}</p>
        <p>{{salary}}</p>
        <p v-if="tax">Your tax is: {{tax}}</p>
        <ul>
            <li v-for="(hobby,index) in hobbies" :key="hobby">
                <div>
                    {{hobby}} <button @click="deleteHobby(index)">X</button>
                </div>
            </li>
        </ul>
        <div class="spacer-bottom">
            <input v-model="newHobby" type="text" placeholder="Enter your hobby" />
            <button @click="addHobby()" class="button-fancy" v-bind:class="isDoctor ? 'button-fancy-yellow' : ''"> Add hobby </button>
        </div>
        <div>
            <input v-model="profession" type="text" placeholder="Enter your profession" />
            <button @click="calculateTax()" class="button-fancy button-fancy-yellow"> Click </button>
        </div>
        <div>
            <button @click="loadNotes()" class="button-fancy"> Refresh notes </button>
            <p v-if="isLoading">Please wait while loading...</p>
            <ul>
                <li v-for="note in notes" :key="note.id">
                    <p>Note Id: {{note.id}}
                     Note content: {{note.content}}
                     Note title: {{note.title}}
                    Note creation date: {{note.createdAt}}</p>
                </li>
            </ul>
        </div>
    </div>

    <script>
        var myObject = new Vue({
            el: '#app',
            data: {
                name: 'Rahul!',
                age: 24,
                salary: 40000.00,
                profession: '',
                tax: '',
                hobbies: ['Cricket', 'Music', 'Cooking', 'Dance'],
                newHobby: '',
                isDoctor: false,
                isLoading: true,
                notes: [],
                employee: {}
            },
            mounted() {
                //alert("I will be called on load");
                // https://pandeymadhuri.github.io/index
                this.loadNotes();
            },
            methods: {
                calculateTax() {
                    // this is a sinle line comment
                    /* multi line comment*/
                    // debbuger only works in js code
                    if (this.profession == 'doctor') {
                        this.tax = 0.01 * this.salary;
                        this.isDoctor = true;
                    } else if (this.profession == 'developer') {
                        this.tax = 0.02 * this.salary;
                        this.isDoctor = !this.isDoctor;
                    } 
                },
                addHobby() {
                    this.hobbies.push(this.newHobby);
                },
                deleteHobby(index) {
                    this.hobbies.splice(index, 1);
                },
                loadNotes(){
                    axios.get("https://notesv2.herokuapp.com/api/notes?field=creationDate&type=desc")
                    .then(response => {
                        this.notes = response.data;
                        this.isLoading = false;
                    });
                }
            }
        })
    </script>

</body>

</html>

========================
