<template>
    <div>
        <table class="table">
  <thead>
    <tr>
      <th scope="col">ID</th>
      <th scope="col">NAME</th>
      <th scope="col">EMAIL</th>
      <th scope="col">WEBSITE</th>
      <th scope="col">COMPANY</th>
    </tr>
  </thead>
  <tbody>
    <tr v-for="user in users" v-bind:key="user.id">
      <th scope="row">{{user.id}}</th>
      <td>{{user.name}}</td>
      <td>{{user.email}}</td>
      <td>{{user.website}}</td>
      <td>{{user.company.name}}</td>
      <td>@mdo</td>
    </tr>
  </tbody>
</table>
    </div>
</template>

<script>
    import axios from "axios"
export default {
    data() {
        return {
            users:undefined
        };
    },
    created: function() {
        axios.get("https://jsonplaceholder.typicode.com/users").then((res) => {
            this.users = res.data;
            console.log(this.users)
        })
    }
}
</script>

