<template>
    <div>
        <pre>
        {{ JSON.stringify(formValues, null, 2) }}
        </pre>
    </div>
    <form @submit.prevent="submitForm">
        <!-- input -->
        <div>
        <label for="name">Name</label>
        <input type="text" id="name" v-model.trim.lazy="formValues.name">
        </div>

        <!-- text area input -->
        <div>
        <label for="profile">Profile Summary</label>
        <textarea id="profile" v-model="formValues.profileSummary"></textarea>
        </div>

        <!-- single select -->
        <div>
        <label for="country">Country</label>
        <select id="country" v-model="formValues.country">
            <option value="">Select a country</option>
            <option value="india">India</option>
            <option value="vietnam">Vietnam</option>
            <option value="singapore">Singapore</option>
        </select>
        </div>

        <!-- multiple select -->
        <div>
        <label for="job-location">Job Location</label>
        <select id="job-location" multiple v-model="formValues.jobLocation">
            <option value="india">India</option>
            <option value="vietnam">Vietnam</option>
            <option value="singapore">Singapore</option>
        </select>
        </div>

        <!-- single checkbox -->
        <div>
        <input type="checkbox" id="remoteWork" v-model="formValues.remoteWork" true-value="yes" false-value="no">
        <label for="remoteWork">Open to remote work?</label>
        </div>

        <!-- multiple checkbox -->
        <div>
        <label>Skill Set</label>
        <input type="checkbox" id="html" value="html" v-model="formValues.skillSet">
        <label for="html">HTML</label>
        <input type="checkbox" id="css" value="css" v-model="formValues.skillSet">
        <label for="css">CSS</label>
        <input type="checkbox" id="javascript" value="javascript" v-model="formValues.skillSet">
        <label for="javascript">JavaScript</label>
        </div>

        <!-- radio group -->
        <div>
        <label>Years of Experience</label>
        <input type="radio" id="0-2" value="0-2" v-model="formValues.yearsOfExperience">
        <label for="0-2">0-2</label>
        <input type="radio" id="3-5" value="3-5" v-model="formValues.yearsOfExperience">
        <label for="3-5">3-5</label>
        <input type="radio" id="6-10" value="6-10" v-model="formValues.yearsOfExperience">
        <label for="6-10">6-10</label>
        <input type="radio" id="10+" value="10+" v-model="formValues.yearsOfExperience">
        <label for="10+">10+</label>
        </div>

        <!-- number modifier -->
        <div>
        <label for="age">Age</label>
        <input type="number" id="age" v-model.number="formValues.age">
        <!-- <input @keyup.enter="submitForm" type="number" id="age" v-model.number="formValues.age"> -->
        </div>

        <!-- submit -->
        <div>
        <button>Submit</button>
        </div>
    </form>
</template>

<script>
export default {
    name: 'App',
    data() {
        return {
        formValues: {
            name: '',
            profileSummary: '',
            country: '',
            jobLocation: [],
            remoteWork: 'no',
            skillSet: [],
            yearsOfExperience: '',
            age: null,
        }
        }
    },
    methods: {
        submitForm(event) {
        // event.preventDefault();
        console.log('Form values', this.formValues)
        }
    }
}
</script>

<style>

</style>