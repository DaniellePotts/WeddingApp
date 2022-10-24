
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
                childrenAttending:0,
                totalChildren:0,
                displayChildError:false
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
            childrenAttending:function(value){
                if(value > -1){
                    this.showChildren = false

this.showSubmit=true

                }else{
                    this.displayChildError=true
                }
            },
            partnerAttending: function (value) {
                if (value === true) {
                    this.showPartner = false
                    this.showChildren = this.selectedPerson.hasChildren ? true : false
                }
            }
        },

    }</script>
<style>
@media (min-width: 1024px) {
    .venue {
        /* min-height: 100vh;
      display: flex;
      align-items: center; */
    }
}
</style>
<template>
    <div class="venue">
        <div v-if="this.showSearch">
            <input type="text" id="name" v-model="name" />
            <div v-if="found.length > 0">
                <select v-model="selected">
                    <option>Select...</option>
                    <option id="attendeeName" v-for="item in found" v-bind:value="item">{{ item.name }}</option>
                </select>
            </div>
        </div>
        <div v-if="selectedPerson != null">
            <div v-if="this.showSearch">
                <span>Will you be attending?</span>
                <div>
                    <button class="pure-button" @click="this.attending= true">Yes</button><button class="pure-button"
                        @click="this.attending= false">No</button>
                </div>
            </div>
            <div v-if="this.showPartner">
                <span>Will a friend/partner be attending?</span>
                <div>
                    <button class="pure-button" @click="this.partnerAttending= true">Yes</button><button
                        class="pure-button" @click="this.partnerAttending= false">No</button>
                </div>
            </div>
            <div v-if="selectedPerson.hasChildren && this.showChildren">
                <span>How many children will be attending?</span>
                <div>
                <input type="number" placeholder="0" min=0 v-model="totalChildren" />
                </div>
                <button  class="pure-button" v-if="selectedPerson != null" @click="this.childrenAttending = this.totalChildren">Submit</button>

            </div>
           
        </div>
        <h1 v-if="this.showSubmit">Thank you for your response</h1>
    </div>
</template>