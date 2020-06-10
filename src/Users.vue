<template>
    <div class="container users">
        <h2>Users</h2>
        <table class="table table-hover">
            <thead class="thead-dark">
                <tr>
                    <th scope="col">Name</th>
                    <th scope="col">Username</th>
                    <th scope="col">Email</th>
                </tr>
            </thead>
            <tbody v-for="user in users" :key="user.id">
                <tr>
                    <th scope="row">{{ user.name }}</th>
                    <td>{{ user.username }}</td>
                    <td>{{ user.email }}</td>
                </tr>
            </tbody>
        </table>
    </div>
</template>

<script>
import axios from 'axios'

export default {
    name: 'Users',
    data() {
        return {
            users: [],
        }
    },
    methods: {
        
    },
    created(){
        axios.get('https://jsonplaceholder.typicode.com/users/')
        .then(response => {
            console.log(response)
            this.users = response.data
        }).catch(err => {
            console.log(err)
        })
    }
}
</script>

<style>
    .users {
        margin: 60px;
    }
    .users h2 {
        text-align: center;
        margin: 15px 0;
    }
    tbody tr th {
        font-weight: normal;
    }
</style>