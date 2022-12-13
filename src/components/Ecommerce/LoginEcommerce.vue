<template>
  <main class="login-form mx-auto">
      <div class="container">
          <div class="row justify-content-center">
              <div class="col-md-8">
                  <div class="card">
                      <div class="card-header"> Login </div>
                      <div class="card-body">
                          <form action="" method="">
                              <div class="form-group row">
                                  <label for="email_address" class="col-md-4 col-form-label text-md-right">E-Mail Address</label>
                                  <div class="col-md-6">
                                      <input v-model="email_address" type="text" id="email_address" class="form-control" name="email-address" required autofocus>
                                  </div>
                              </div>
  
                              <div class="form-group row">
                                  <label for="password" class="col-md-4 col-form-label text-md-right">Password</label>
                                  <div class="col-md-6">
                                      <input v-model="password" type="password" id="password" class="form-control" name="password" required>
                                  </div>
                              </div>
  
                              <div class="form-group row">
                                  <div class="col-md-6 offset-md-4">
                                      <div class="checkbox">
                                          <label>
                                              <input type="checkbox" name="remember"> Remember Me
                                          </label>
                                      </div>
                                  </div>
                              </div>
  
                              <div class="col-md-6 offset-md-4">
                                  <button type="submit" class="btn btn-primary" @click="login()">
                                      Register
                                  </button>
                                  <a href="#" class="btn btn-link">
                                      Forgot Your Password?
                                  </a>
                              </div>
                            </form>
                      </div>
                  </div>
              </div>
          </div>
      </div>
  
  </main>
  </template>
    
  <script>
  export default {
    name: 'LoginEcommerce',
    props: [],
    data() {
          return {
            password: '',
            email_address: ''
          };
    },
    methods: {
          login() {     
            if (this.password === '123' && this.email_address === 'marcelo@gmail.com'){
              alert('Usuario logeado correctamente');
            }
            else if (this.password === '' && this.email_address === '') {
              alert('Complete el formulario');
            } else {
              alert('Usuario no logeado');
      }}
      }
      
  }
  </script>
    
    <!-- Add "scoped" attribute to limit CSS to this component only -->
  <style scoped>
  
  
  .my-form
  {
      padding-top: 1.5rem;
      padding-bottom: 1.5rem;
  }
  
  .my-form .row
  {
      margin-left: 0;
      margin-right: 0;
  }
  
  .login-form
  {
      padding-top: 1.5rem;
      padding-bottom: 1.5rem;
      width: 50%;
  }
  
  .login-form .row
  {
      margin-left: 0;
      margin-right: 0;
  }
  </style>