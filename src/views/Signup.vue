<template>
    <div class="row">
        <div class="col-md-6 offset-md-3">
            <div class="card my-5">
                <div class="card-header">
                    <h3 class="text-center">Sign Up</h3>
                </div>
                <div class="card-body">
                    <div class="form-group">
                        <input v-model="name" type="text" placeholder="Name" class="form-control" required>
                    </div>
                    <div class="form-group">
                        <input v-model="email" type="text" placeholder="Email" class="form-control" required>
                    </div>
                    <div class="form-group">
                        <input v-model="password" type="password" placeholder="Password" class="form-control" required>
                    </div>
                    <button @click="registerUser" class="btn btn-secondary form-control">Sign Up</button>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
import Axios from 'axios'

export default {
    data() {
        return {
            name: '',
            email: '',
            password: ''
        }
    },
    methods: {
        registerUser() {
            console.log(this.name, this.email, this.password)
            Axios.post("users.json", {
                name: this.name,
                email: this.email,
                password: this.password
            })
            .then(response => {
                console.log(response)
                console.log(this.data.name)
            }).catch(error => {
                console.log(error)
            })
        }
    }
}
</script>