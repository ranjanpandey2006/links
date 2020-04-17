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
Advocats
---------------



 <div class="text-center">
    <h2><strong>Committee Members</strong></h2>
    <h4>Name of office bearer of CAC - central action committee of all odisha bar association </h4><br>
  </div>
  <div class="row slideanim">
    <div class="col-sm-4 col-xs-12">
      <div class="panel panel-default text-center">
        <div class="panel-heading">
          <h2>Ashok Kumar Dash</h2>
        </div>
        <div class="panel-body">
          <p><strong>Advocate Sundargargh, Convener</strong></p>
		  <h3>+919437187834</h3>
        </div>
      </div>      
    </div>     
    <div class="col-sm-4 col-xs-12">
      <div class="panel panel-default text-center">
        <div class="panel-heading">
          <h2>Promod Kumas Dash</h2>
        </div>
        <div class="panel-body">
          <p><strong>Advocate Sambalpur</strong></p>
		  <h3>Co-Convener</h3>
        </div>
      </div>      
    </div>       
    <div class="col-sm-4 col-xs-12">
      <div class="panel panel-default text-center">
        <div class="panel-heading">
          <h2>Niranjan Tripathy</h2>
        </div>
        <div class="panel-body">
          <p><strong>Advocate Sambalpur, General Secretary</strong></p>
		  <h3>+919439892172</h3>
        </div>
      </div>      
    </div>

	<div class="col-sm-4 col-xs-12">
      <div class="panel panel-default text-center">
        <div class="panel-heading">
          <h2>Prasanna Padhi</h2>
        </div>
        <div class="panel-body">
          <p><strong>Advocate of Nuapada district</strong></p>
		  <h3>Joint Convener</h3>
        </div>
      </div>      
    </div>     
    <div class="col-sm-4 col-xs-12">
      <div class="panel panel-default text-center">
        <div class="panel-heading">
          <h2>Sureshwar Mishra</h2>
        </div>
        <div class="panel-body">
          <p><strong>Advocate Sambalpur, Member of CAC</strong></p>
		  <h3>+919437348049</h3>
        </div>
      </div>      
    </div>       
    <div class="col-sm-4 col-xs-12">
      <div class="panel panel-default text-center">
        <div class="panel-heading">
          <h2>Satyanaran Panda</h2>
        </div>
        <div class="panel-body">
          <p><strong>Advocate Sambalpur, Member of CAC</strong></p>
		  <h3>+919437050349</h3>
        </div>
      </div>      
    </div> 
	
	<div class="col-sm-4 col-xs-12">
      <div class="panel panel-default text-center">
        <div class="panel-heading">
          <h2>Promod Churia</h2>
        </div>
        <div class="panel-body">
          <p><strong>Advocate Kuchinda</strong></p>
		  <h3>Member of CAC</h3>
        </div>
      </div>      
    </div>
    <div class="col-sm-4 col-xs-12">
      <div class="panel panel-default text-center">
        <div class="panel-heading">
          <h2>Bijitendriya Pradhan</h2>
        </div>
        <div class="panel-body">
          <p><strong>President District Bar Association Sambalpur</strong></p>
		  <h3>+919437083871</h3>
        </div>
      </div>      
    </div>	
    <div class="col-sm-4 col-xs-12">
      <div class="panel panel-default text-center">
        <div class="panel-heading">
          <h2>All Bar Presidents</h2>
        </div>
        <div class="panel-body">
          <p><strong>District Bar</strong></p>
		  <h3>Joint Convener</h3>
        </div>
      </div>      
    </div>
    
  </div>
  
   <h2><strong>Supporters</strong></h2><br>
  
    
  <div class="row slideanim">
		 <div class="col-sm-3 col-xs-12">
			<div class="panel panel-success">
			  <div class="panel-body">Pravin Singhdeo +919437137234</div>
			</div>
		 </div>
		 <div class="col-sm-3 col-xs-12">
			<div class="panel panel-success">
			  <div class="panel-body">Reena Trivedi  +919937007617</div>
			</div>
		 </div>
		 <div class="col-sm-3 col-xs-12">
			<div class="panel panel-success">
			  <div class="panel-body">Satyanarayan Panda  +919437050349</div>
			</div>
		 </div>
		 <div class="col-sm-3 col-xs-12">
			<div class="panel panel-success">
			  <div class="panel-body">Chandrakanta Mohanty  +919437137041</div>
			</div>
		 </div>
		 
		 <div class="col-sm-3 col-xs-12">
			<div class="panel panel-success">
			  <div class="panel-body">Rangeya Sarangi +919437220157</div>
			</div>
		 </div>
		 <div class="col-sm-3 col-xs-12">
			<div class="panel panel-success">
			  <div class="panel-body">Saroj Kumar Buxi +919937136362</div>
			</div>
		 </div>
		 <div class="col-sm-3 col-xs-12">
			<div class="panel panel-success">
			  <div class="panel-body">Bansidhara Sahu +919437737008</div>
			</div>
		 </div>
		 <div class="col-sm-3 col-xs-12">
			<div class="panel panel-success">
			  <div class="panel-body">Sujeet Mishra +919437136851</div>
			</div>
		 </div>
		 
		 <div class="col-sm-3 col-xs-12">
			<div class="panel panel-success">
			  <div class="panel-body">Manoranjan Panda +919090409933</div>
			</div>
		 </div>
		 <div class="col-sm-3 col-xs-12">
			<div class="panel panel-success">
			  <div class="panel-body">Antaryami Panigrahi +919437668752</div>
			</div>
		 </div>
		 <div class="col-sm-3 col-xs-12">
			<div class="panel panel-success">
			  <div class="panel-body">Prashanta Kar +919437219188</div>
			</div>
		 </div>
		 <div class="col-sm-3 col-xs-12">
			<div class="panel panel-success">
			  <div class="panel-body">Debendra Satpathy  +919437418223</div>
			</div>
		 </div>
  </div>
  
  <h3><strong>History Of Sambalpur Bar Association</strong></h3><br>
      <p>In 1886 we find an advocate of Sambalpur K.Mitra appeared on behalf of Mitrabhanu Sai to end his exile.It seems that he is the first Indian advocate of SBP.
In 1900 we find there were 6 Indian Advocates at SBP- <strong>Jogendra Nath Sen, Bamapada Chatterjee, Debendra Nath Mitra, Vijaya Chandra Mazumdar,K.P.Mitra and Chunnilal Dubey. </strong>Chandra Sekhar Behera is the first native or son of soil to join SBP Bar as an Advocate on 23rd September 1901. <strong>Sambalpur Bar Association was formed on 23rd December 1908.</strong>In 1918 the total no. of Advocates at SBP was 21, among them 7 were Sambalpuri speaking namely <strong>Chandra Sekhar Behera,Ram Narayan Mishra, Parsuram Mishra, Biswaksen Mishra, Balunkeswar Mishra, Natbar Gadtia,Gokul Chandra Babu.</strong> Later on Biswaksen Mishra and Balunkeswar Mishra moved to Bargarh to start the family of Advocates there, as more joined at SBP. The first ever Advocate of Bolangir Kapileswar Pr. Nanda after getting B.L in 1927 joined Sambalpur Bar. After 3 years of learning he moved to Bargarh and finally went to Bolangir. He along with other 5 Advocates and 2 Muktiars formed Bolangir Bar Association. In 1934 the no. of Advocates at Sambalpur was more than 50 in that year.
	  </p>
	  </div>
  </div>
</div>

<div class="container-fluid bg-grey">
  <div class="row">
    
    <div class="col-sm-12">
      <h2><strong>Overview</strong></h2>
      <h4><strong>Mission:</strong> Our mission is to establish permanent high court bench in western Odisha for the welfare of the people.</h4><br>
      <p><strong>Background:</strong> Central government constituted Justice Jaswant Singh commission to inquire and fix the criteria for creation of permanent bench of original high court in any other place and the commission has given some criteria.
		<br>Western Odisha satisfies the criteria's of the commision hence Central Action Committee has made the request to the state and
		central government for the establishment of Permanent High Court Bench in western Odisha.
	  </p>
---------------
