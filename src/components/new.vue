<template>
  <div class="container">
    <h3>Users:</h3>
    <table class="table" border="1" cellpadding="8" >
      <thead>
        <tr>
          <th>Id</th>
          <th>Name</th>
          <th>Username</th>
          <th>Email</th>
          <th>City</th>
          <th>Website</th>
          <th>Company</th>
        </tr>
      </thead>
      <tbody>
        <tr v-for="user in users" v-bind:key="user.id">
          <th scope="row">{{user.id}}</th>
          <td>{{user.name}}</td>
          <td>{{user.username}}</td>
          <td>{{user.email}}</td>
          <td>{{user.address.city}}</td>
          <td>{{user.website}}</td>
          <td>{{user.company.name}}</td>
        </tr>

      </tbody>
    </table>
  </div>
</template>



<script>
import axios from 'axios'
export default {
  data() {
    return {
      users: null,
    };
  },
  created: function() {
    axios
      .get('https://jsonplaceholder.typicode.com/users')
      .then(res => {
        this.users = res.data;
      })
  }
}
</script>

<style >
  table{
    text-align: left;
    width: 80%;
    margin: auto;
  }
</style>
