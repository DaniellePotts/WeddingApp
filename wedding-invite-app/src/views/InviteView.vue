
<script>
import names from '../data/names.json'
export default
    {
        data() {
            return {
                name: '',
                found: [],
                names: names,
                selected: null,
                selectedPerson: null,
                attending: false,
                showPartner: false,
                showSearch: true,
                showChildren: false,
                partnerAttending: false,
                showSubmit: false,
                childrenAttending: 0,
                totalChildren: 0,
                displayChildError: false
            }
        },
        methods:{
            greet: function (){
                alert('TEST!')
            }
        },
        watch: {
            name: function (value) {
                if (value === '') this.found = []
                else {
                    this.found = this.names.filter((n) => n.name.toLowerCase().includes(value.toLowerCase()))
                }
            },
            selected: function (value) {
                this.selectedPerson = value
            },
            attending: function (value) {
                this.showSearch = false
                if (value === true) {
                    if (this.selectedPerson.partner) {
                        this.showPartner = true
                    } else if (this.selectedPerson.hasChildren) {
                        this.showChildren = true
                    } else {
                        this.showSubmit = true
                    }

                }
            },
            childrenAttending: function (value) {
                if (value > -1) {
                    this.showChildren = false

                    this.showSubmit = true

                } else {
                    this.displayChildError = true
                }
            },
            partnerAttending: function (value) {
                if (value === true) {
                    this.showPartner = false
                    this.showChildren = this.selectedPerson.hasChildren ? true : false
                }
            }
        },

    }

    </script>
<style>
input[type=text],
select {
    width: 100%;
    padding: 12px 20px;
    margin: 8px 0;
    display: inline-block;
    border: 1px solid #ccc;
    border-radius: 4px;
    box-sizing: border-box;
}

input[type=submit] {
    width: 100%;
    background-color: #4CAF50;
    color: white;
    padding: 14px 20px;
    margin: 8px 0;
    border: none;
    border-radius: 4px;
    cursor: pointer;
}

input[type=submit]:hover {
    background-color: #45a049;
}

div {
    border-radius: 5px;
    background-color: #f2f2f2;
    padding: 20px;
}

ul {
    list-style-type: none;
    margin: 0;
    padding: 0;
    overflow: hidden;
    background-color: #333;
}

li {
    float: left;
}

li a {
    display: block;
    color: white;
    text-align: center;
    padding: 14px 16px;
    text-decoration: none;
}

li a:hover:not(.active) {
    background-color: #111;
}

.active {
    background-color: #04AA6D;
}
</style>
<template>



    <div>
        
        
        <input v-if="this.showSearch" type="text" id="fname" v-model="name" name="firstname" placeholder="Your name..">
        <select  v-if="found.length > 0" v-model="selected">
                    <option>Select...</option>
                    <option id="attendeeName" v-for="item in found" v-bind:value="item">{{ item.name }}</option>
                </select>
        <label for="lname">Last Name</label>
        <input type="text" id="lname" name="lastname" placeholder="Your last name..">

        <label for="country">Country</label>
        <select id="country" name="country">
            <option value="australia">Australia</option>
            <option value="canada">Canada</option>
            <option value="usa">USA</option>
        </select>

        <input type="submit" value="Submit">
    </div>


</template>