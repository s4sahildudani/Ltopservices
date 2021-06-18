<script>
//   function validation(){
//   alert("Confirm you mail");
//  }
 let formobj = {
  "user":"",
"pass":""
 }
 let apidata= {
"auth":"signup",
"c_id":"3v9h9sli9f0c4bhepe81vsho1j",
"user":"",
"pass":"",
 }
 async function handlesubmit() {
apidata.user=formobj.user
apidata.pass=formobj.pass
  const res = await fetch("https://38fteogd70.execute-api.ap-south-1.amazonaws.com/default/botocognitoauth",{
   method:'POST',
   mode:"cors",
   
headers:{
"X-API-KEY":"xnFSKlZEm01aSvcgdd7Bx5ttpzyF494F1WOF0JvZ",
   "Content-Type":"application/json"
},
body:JSON.stringify(apidata)

});
console.log(res.status)
res.json().then((e) =>{
  console.log(e)
})
 };
 
</script>
<main>
  <div id="login-box">
    <div class="left">
      <h1>Sign up</h1>
      
      <input type="text" name="username" placeholder="Username"  bind:value={formobj.user} />
      <!-- <input type="text" name="email" placeholder="E-mail"  bind:value={formobj.Email} /> -->
      <input type="password" name="password" placeholder="Password"  bind:value={formobj.pass} />
      <!-- <input type="password" name="password2" placeholder="Retype password" bind:value={formobj.pass} /> -->
      
      <button type="submit" class="button"   id="sad" name="signup_submit" value="Sign me up" on:click={handlesubmit}  >
       <a href="/ltop/confirmvalidation">Submit</a>
      </button>
     
    </div>
    
    
    
    <div class="right">
      <span class="loginwith">Sign in with<br />social network</span>
      
      <button class="social-signin facebook">Log in with facebook</button>
      <button class="social-signin twitter">Log in with Twitter</button>
      <button class="social-signin google">Log in with Google+</button>
      <a class="button" href="/ltop/confirmvalidation" id="bas">Confirm your mail</a>
    </div>
    
    <div class="or">OR</div>

  </div>
  <div>
    
  </div>
  {JSON.stringify(formobj)}
{JSON.stringify(apidata)}
</main>


<style>
@import url(https://fonts.googleapis.com/css?family=Roboto:400,300,500);
*:focus {
  outline: none;
}
#bas{
  background-color: black;
}
main{
  margin: 0;
  padding: 0;
  background: #DDD;
  font-size: 16px;
  color: #222;
  font-family: 'Roboto', sans-serif;
  font-weight: 300;
  height: 100vh;
}

#login-box {
  position: relative;
  margin: 5% auto;
  width: 600px;
  height: 400px;
  background: #FFF;
  border-radius: 2px;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.4);
}
#sad{
  color: white;
  background-color: #16a085;
}
.left {
  position: absolute;
  top: 0;
  left: 0;
  box-sizing: border-box;
  padding: 40px;
  width: 300px;
  height: 400px;
}

h1 {
  margin: 0 0 20px 0;
  font-weight: 300;
  font-size: 28px;
}

input[type="text"],
input[type="password"] {
  display: block;
  box-sizing: border-box;
  margin-bottom: 20px;
  padding: 4px;
  width: 220px;
  height: 32px;
  border: none;
  border-bottom: 1px solid #AAA;
  font-family: 'Roboto', sans-serif;
  font-weight: 400;
  font-size: 15px;
  transition: 0.2s ease;
}

input[type="text"]:focus,
input[type="password"]:focus {
  border-bottom: 2px solid #16a085;
  color: #16a085;
  transition: 0.2s ease;
}

/* input[type="submit"] {
  margin-top: 28px;
  width: 120px;
  height: 32px;
  background: #16a085;
  border: none;
  border-radius: 2px;
  color: #FFF;
  font-family: 'Roboto', sans-serif;
  font-weight: 500;
  text-transform: uppercase;
  transition: 0.1s ease;
  cursor: pointer;
} */

/* input[type="submit"]:hover,
input[type="submit"]:focus {
  opacity: 0.8;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.4);
  transition: 0.1s ease;
}

input[type="submit"]:active {
  opacity: 1;
  box-shadow: 0 1px 2px rgba(0, 0, 0, 0.4);
  transition: 0.1s ease;
} */

.or {
  position: absolute;
  top: 180px;
  left: 280px;
  width: 40px;
  height: 40px;
  background: #DDD;
  border-radius: 50%;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.4);
  line-height: 40px;
  text-align: center;
}

.right {
  position: absolute;
  top: 0;
  right: 0;
  box-sizing: border-box;
  padding: 40px;
  width: 300px;
  height: 400px;
  background: url('https://goo.gl/YbktSj');
  background-size: cover;
  background-position: center;
  border-radius: 0 2px 2px 0;
}

.right .loginwith {
  display: block;
  margin-bottom: 40px;
  font-size: 28px;
  color: #FFF;
  text-align: center;
}

button.social-signin {
  margin-bottom: 20px;
  width: 220px;
  height: 36px;
  border: none;
  border-radius: 2px;
  color: #FFF;
  font-family: 'Roboto', sans-serif;
  font-weight: 500;
  transition: 0.2s ease;
  cursor: pointer;
}

button.social-signin:hover,
button.social-signin:focus {
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.4);
  transition: 0.2s ease;
}

button.social-signin:active {
  box-shadow: 0 1px 2px rgba(0, 0, 0, 0.4);
  transition: 0.2s ease;
}

button.social-signin.facebook {
  background: #32508E;
}

button.social-signin.twitter {
  background: #55ACEE;
}

button.social-signin.google {
  background: #DD4B39;
}
</style>
