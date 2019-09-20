<html>
<body>
 </head> 
 <div id="login">
  <label>Usuario:</label> <input type="text" name="Usuario" v-model="input.Usuario" placeholder="Usuario" />
<br>
<label>Contraseña:</label> 
  <input type="password" name="password" v-model="input.password" placeholder="Password" />
  <br>
  <button @click="" type="button" v-on:click="login()">Login</button>
 </div>
 <div>
  <b-button>Button</b-button>
  <b-button variant="danger">Button</b-button>
  <b-button variant="success">Button</b-button>
  <b-button variant="outline-primary">Button</b-button>
</div>
  </body>
</html>