/**
 *  https://blog.logrocket.com/getting-started-with-bootstrapvue-2d8bf907ef11/
 **/
<script>
import DateInput from "./date_input";

export default {
  name: "SideBar",

  components: {
    DateInput
  },
  props: [ "FieldID"],

  methods: {
    getMeal() {
      return "Something Else";
    }
  },

  data() {
    return {
      meal:"Something"
    };
  }
}
</script>



<template>
    <div class="sidebar col-2 mb-3 mt-3">
        <div class="card rounded-lg h-100">
            <div class="card-header">
                <h2>Logo</h2>
            </div>

            <div class="card-body">
<b-nav vertical class="w-25">
  <b-nav-item active>
      <label class="text-white font-weight-bold" for="start-date">Start Date</label>
      <b-nav-form>
        <b-form-input
          id="start-date"
          type="date"
          v-model="aDate">
        </b-form-input>
      </b-nav-form>
  </b-nav-item>


  <b-nav-item>
      <label class="text-white font-weight-bold" for="end-date">End Date</label>
      <b-nav-form>
        <b-form-input
          id="end-date"
          type="date"
          v-model="aDate">
        </b-form-input>
      </b-nav-form>
  </b-nav-item>

  <b-nav-item>
      <label class="text-white font-weight-bold" for="pID">Patient ID</label>
      <b-nav-form>
        <b-form-input
          id="pID"
          type="text"
          v-model="pID">
        </b-form-input>
      </b-nav-form>
  </b-nav-item>

  <b-nav-item>
      <label class="text-white font-weight-bold" for="uID">User ID</label>
      <b-nav-form>
        <b-form-input
          id="uID"
          type="text"
          v-model="uID">
        </b-form-input>
      </b-nav-form>
  </b-nav-item>

</b-nav>
  <!--
        <b-container>
            <b-navbar-brand href="#">Mealzers</b-navbar-brand>
            <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>
            <b-collapse id="nav-collapse" is-nav>
              <!  -- Right aligned nav items --  >
              <b-navbar-nav class="ml-auto">
                <b-nav-form>
                  <b-form-input
                    type="date"
                    v-model="aDate">
                  </b-form-input>

                  <b-form-input
                    size="sm"
                    class="mr-sm-2"
                    placeholder="Search for a meal"
                    v-model="meal"
                    ></b-form-input>
                  <b-button
                    size="sm"
                    class="my-2 my-sm-0"
                    type="submit"
                    @click.prevent="getMeal"
                    >Search</b-button>

                </b-nav-form>

                <b-nav-item-dropdown right>
                  <!  -- Using 'button-content' slot --  >
                  <template slot="button-content"><em>User</em></template>
                  <b-dropdown-item href="#">Profile</b-dropdown-item>
                  <b-dropdown-item href="#">Sign Out</b-dropdown-item>
                </b-nav-item-dropdown>

              </b-navbar-nav>
            </b-collapse>

          </b-container>
      </b-navbar>
                <nav class="navbar navbar-inverse visible-xs p-2">
                    <ul class="nav flex-sm-column">
                        <li class="nav-item">
                          <DateInput :date="FieldID" :config="options" @rcvDateInput="theDate"/>
                        </li>




                        <li class="nav-item">
                            <div class="date form-group col-xs-4">
                                <label for="enddate">End Date</label>:
                                <div class="input-group">
                                    <input type="text" id="enddate" class="form-control" placeholder="dd/mm/yyyy" title="format: dd/mm/yyyy" aria-autocomplete="none" style="min-width: 7em;">
                                    <span class="input-group-addon rounded-right bg-dark">
                                        <span class="fa fa-calendar" aria-hidden="true"></span>
                                    </span>
                                </div>
                            </div>
                        </li>


                    </ul>
                </nav>
                -->
            </div>
        </div>
    </div>
</template>

<style>
.sidebar {
    text-align: left;
}

.sidebar .card-body {
    padding:0;
}

.sidebar .nav-link label {
    margin-bottom: 0;
}
</style>



