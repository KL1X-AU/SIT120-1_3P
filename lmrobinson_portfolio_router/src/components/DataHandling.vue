<template>
    <div class="form-container">
        <h2>Movie Rental Form</h2>
        <div class="form-row">
            <label>First Name</label><br>
            <input v-model="firstname" type="text" class="pill" >
        </div>
        <div class="form-row">
            <label>Last Name</label><br>
            <input v-model="lastname" type="text" class="pill">
        </div>
        <div class="form-row">
            <label>Movie</label><br>
            <select v-model="selection" name="" id="" class="pill">
                <option disabled>Please Select A Movie</option>
                <option v-for="movie in movies">{{movie}}</option>
            </select>
        </div>
        <div class="form-row">
            <label>Hire Date</label><br>
            <input v-model="hirestart" type="date" class="pill">
        </div>
        <div class="form-row">
            <label>Return Date</label><br>
            <input v-model="hireend" type="date" class="pill">
            <p v-show="hireend < hirestart">Please Select A Return Date Later Than ({{hirestart}})</p>
        </div>
        <div class="form-row">
            <label>Email</label><br>
            <input v-model="email" type="email" class="pill">
        </div>
        <div class="form-row">
            <label>Phone Number</label><br>
            <input v-model="phonenumber" type="number" class="pill">
        </div>
        <div class="form-row">
            <button @click="LogToConsole">Generate Receipt</button>
        </div>
    </div>
    <div v-if="receipt" class="receipt-container">
        <div class="receiptheader">
            <h2>Your Receipt</h2>
            <p>Please present this receipt upon movie collection.</p>
            <h2>Details</h2>
        </div>
        <div class="receiptlabels">
            <p v-for="item in receiptlabels">{{item}}</p>
        </div>
        <div class="receiptitems">
            <p v-for="item in receiptarray">{{item}}</p>
        </div>
    </div>
</template>

<script>
    export default {
        data() {
            return {
                movies: ["Movie 1", "Movie 2", "Movie 3", "Movie 4", "Movie 5", "Movie 6"],
                firstname: "Lachlan",
                lastname: "Robinson",
                hirestart: "2023-09-11",
                hireend: "2023-09-14",
                hiredays: 0,
                email: "lmrobinson@deakin.edu.au",
                phonenumber: "0449005985",
                receiptarray: [],
                receiptlabels: ['First Name','Last Name','Hire Start Date',"Hire End Date",/*"Days Hired",*/"Movie Title","Email Address","Phone Number"],
                receipt:false,
                selection: "",
            };
         },
    methods: {
        /*
        daysHired(start,end) {
            const startDate = new Date(start)
            const endDate = new Date(end)
            const timeDiff = endDate.getTime() - startDate.getTime()
            const daysDiff = Math.floor(timeDiff / (1000 * 60 * 60 * 24))
            return daysDiff.toString()
        },
        */
        LogToConsole() {
            if(!this.firstname) {
                alert("Please Enter Your First Name")
                return
            };
            if(!this.lastname) {
                alert("Please Enter Your Last Name")
                return
            }
            if(!this.hirestart) {
                alert("Please Enter Your Hire Start Date")
                return
            }
            if(!this.hireend) {
                alert("Please Enter Your Hire End Date")
                return
            }
            if(!this.email) {
                alert("Please Enter Your Email")
                return
            }
            if(!this.phonenumber) {
                alert("Please Enter Your Phone Number")
                return
            }
            if(this.hireend < this.hirestart) {
                alert("Please enter a valid return date.")
                return
            }

            this.receiptarray = [],
            console.log(this.firstname),this.receiptarray.push(this.firstname), this.firstname = "",
            console.log(this.lastname),this.receiptarray.push(this.lastname), this.lastname = "",
            console.log(this.hirestart),this.receiptarray.push(this.hirestart), this.hirestart = "",
            console.log(this.hireend),this.receiptarray.push(this.hireend), this.hireend = "",
            //this.receiptarray.push(this.daysHired(this.hirestart,this.hireend)),this.hiredays = 0,
            console.log(this.selection),this.receiptarray.push(this.selection), this.selection = "",
            console.log(this.email),this.receiptarray.push(this.email), this.email = "",
            console.log(this.phonenumber),this.receiptarray.push(this.phonenumber), this.phonenumber = ""
            
            this.receipt = true
        },
    },
    computed: {
    }
};
</script>

<style scoped>
    .form-container {
        padding: 2vw;
        text-align: center;
        background-color: rgb(228, 228, 228);
        margin: 3vw;
        border-radius: 3vw;
    }

    .form-row {
        display: block;
        margin: auto;
        margin-top: 1vw;
        text-align: center;
        position: relative;
    }

    .form-row label {
        font-size: 2vw;
        font-family: Arial;
        width:100%;
    }

    input, select {
        box-sizing: border-box;
        padding: 0.5vw;
    }

    input[type="date"]::-webkit-calendar-picker-indicator {
        background: transparent;
        bottom:0;
        top:0;
        left:0;
        right:0;
        position: absolute;
        color: transparent;
        cursor:pointer;
        height: 100%;
        width:100%;
    }

    .pill {
        width: 50%;
        min-height: 3vw;
        border-radius: 1.5vw;
        border: 0.1vw solid rgb(92, 92, 92);
    }

    h2 {
        font-family: Arial;
        font-size: 3vw;
    }

    p {
        font-family: Arial;
        font-size: clamp(12px,2vw,5vw);
        color:red;
    }

    .receipt-container {
        display: grid;
        grid-template-columns: 50% 50%;
        text-align: center;
        margin:auto;
        padding: 2vw;
        text-align: center;
        background-color: rgb(228, 228, 228);
        margin: 3vw;
        border-radius: 3vw;
    }

    .receiptheader {
        grid-row: 1;
        grid-column-start: 1;
        grid-column-end: 3;
        text-align: center;
    }

    .receiptitems {
        grid-column: 2;
        grid-row:2
    }

    .receiptlabels {
        grid-column: 1;
        grid-row:2
    }

    .receipt-container p {
        color: black;
        font-family: 'Courier New', Courier, monospace;
    }

</style>