// Create.vue

<template>
  
<div class="container">
    <h1 class="top">Top Sellers</h1><hr>
<div class="card1">
  <img src="@/assets/tshirt/1.jpg" height="300px" width="250px" />
  <h2>Norms Shirt</h2>
  <p class="price">158.00 PHP</p>
</div>
<div class="card1">
    <img src="@/assets/tshirt/2.jpg" height="300px" width="250px" />
      <h2>Versace Jeans</h2>
  <p class="price">300.00 PHP</p>
</div>
<div class="card1">
    <img src="@/assets/tshirt/3.jpg" height="300px" width="250px" />
      <h2>Demon Slayer</h2>
  <p class="price">500.00 PHP</p>
</div>
<div class="card1">
    <img src="@/assets/tshirt/4.jpg" height="300px" width="250px" />
      <h2>Bangalore Shirt</h2>
  <p class="price">450.00PHP</p>
</div>
<div class="card1">
    <img src="@/assets/tshirt/5.png" height="300px" width="250px" />
      <h2>Displace Shirt</h2>
  <p class="price">300.00PHP</p>
</div>
<div class="card1">
    <img src="@/assets/1.jpg" height="300px" width="250px" />
      <h2>Black Shirt</h2>
  <p class="price">200.00PHP</p>
</div>
<div class="card1">
    <img src="@/assets/tshirt/7.jpg" height="300px" width="250px" />
      <h2>Math Wizard</h2>
  <p class="price">400.00PHP</p>
</div>
<div class="card1">
    <img src="@/assets/tshirt/versace.jpg" height="300px" width="250px" />
      <h2>Versace Shirt</h2>
  <p class="price">700.00PHP</p>
  
</div>
      <br><br><br>
        <div class="card">
            <div class="card-header">
                <h3>Add Item</h3>
            </div>
            <div class="card-body">
                <form v-on:submit.prevent="addItem">
                    <div class="form-group">
                        <label>Item Name:</label>
                        <input type="text" class="form-control" v-model="item.name"/>
                    </div>
                    <div class="form-group">
                        <label>Item Price:</label>
                        <input type="text" class="form-control" v-model="item.price"/>
                        <br>
                    </div>
                    <div class="form-group">
                        <input type="submit" class="btn btn-primary" value="Add Item"/>
                    </div>
                    <div class="footer">
                    <h6>For more information, Visit Contacts page, Est 2021.</h6>
                    </div>
                </form>
            </div>
        </div>
    </div>
    
</template>

<script>
export default {
  component: {
      name: 'AddItem'
  },
  data() {
      return {
          item: {}
      }
  },
  methods: {
      addItem() {
           let uri = 'http://localhost:4000/items/add';
            this.axios.post(uri, this.item).then((response) => {
                console.log(response.data)
            });
        }
    }
}
</script>