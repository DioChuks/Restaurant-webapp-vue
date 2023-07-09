<script></script>
<template>
  <div class="reservation" id="reservation">
    <div class="image"></div>
    <div class="form">
      <h1 class="heading">book a table</h1>
      <center>
        <h3 class="sub-heading">~ check out our place ~</h3>
      </center>
      <form action="">
        <div class="form-holder">
          <div>
            <select name="peopleReserved" id="peopleReserved">
              <option value="1">1 people</option>
              <option value="2">2 people</option>
              <option value="3">3 people</option>
              <option value="4">4 people</option>
            </select>
            <input type="text" name="" placeholder="Time" />
            <input type="text" name="" placeholder="Phone" />
          </div>
          <div>
            <input type="date" name="" placeholder="Date" />
            <input type="text" name="" placeholder="Name" />
            <input type="email" name="" placeholder="Email" />
          </div>
        </div>
        <button type="submit" class="btn">
          <span><i class="fa fa-check"></i> order now</span>
        </button>
      </form>
    </div>
  </div>
</template>
