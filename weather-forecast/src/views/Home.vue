<template>
  <div class="container mt-5 mx-auto w-90" id="content">
    <div class="row mx-auto">
      <div class="col bg-light rounded p-5" >
        
        <!--
        <form>
          <div class="form-row mt-3">
            <div class="form-group col-md-6">
              <input type="text" class="form-control border-0" id="inputCity" placeholder="Search more places"> 
            </div>
            <div class="form-group col-md-4">
              <select id="inputState" class="form-control border-0 bg-transparent font-weight-bold">
                <option selected disabled hidden>All places</option>
              </select>
            </div>
          </div>
        </form>
          -->
          <h1 class="my-2"><small>Weather <strong>Forecast</strong></small></h1>
          <h3 class="my-2 font-italic"><small>Friday, 25 June 2021</small></h3>
          <div class="row mt-5 mx-auto">
            <table class="table">
              <thead class="contrast-text">
                <tr class="d-flex">
                  <th class="col-4">Place</th>
                  <th class="col-3">Temperature</th>
                  <th class="col-3">Humidity</th>
                  <th class="col-2">Details</th>
                </tr>
              </thead>
              <tbody>
                <tr class="d-flex">
                  <td class="col-4">Berlin</td>
                  <td class="col-3">23°C</td>
                  <td class="col-3">79%</td>
                  <td class="col-2"><a href="#" class="btn btn-primary contrast-text border-0">Check</a></td>
                </tr>
                <tr class="d-flex">
                  <td class="col-4">Paris</td>
                  <td class="col-3">Thornton</td>
                  <td class="col-3">@fat</td>
                  <td class="col-2"><a href="#" class="btn btn-primary contrast-text border-0">Check</a></td>
                </tr>
                <tr class="d-flex">
                  <td class="col-4">Larry</td>
                  <td class="col-3">the Bird</td>
                  <td class="col-3">@twitter</td>
                  <td class="col-2"><a href="#" class="btn btn-primary contrast-text border-0">Check</a></td>
                </tr>
                <tr class="d-flex">
                  <td class="col-12 d-flex justify-content-center"><a href="#" class="btn btn-primary contrast-text border-0 font-weight-bold">Add new place</a></td>
                </tr>
              </tbody>
            </table>
          </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Home",
  components: {

  },
  data(){
    return{
    }
  },

  
};

</script>

<style scoped>
#content{
  color: rgb(61, 50, 88);
}

.contrast-text{
  color: white;
  background-color: rgb(61, 50, 88);
}
</style>