<script>
    let formobj = {
  "user":"",
  "pass":""
    }
    let apidata= {
"auth":"login",
"pool_id":"ap-south-1_9WoXGfjYO",
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
    // credentials:'include',
headers:{
    "X-API-KEY":"xnFSKlZEm01aSvcgdd7Bx5ttpzyF494F1WOF0JvZ",
   "Content-type":"application/json"
},
body:JSON.stringify(apidata)

})
console.log(res.status)
res.json().then((e) =>{
  console.log(e)
})
 }
//     let Email;
//     let Password;
//  const handleSubmit =() =>{
//      console.log(Email,Password);
//  }

</script>
<main>
    <section class="hero is-success is-fullheight">
        <div class="hero-body">
            <div class="container has-text-centered">
                <div class="column is-4 is-offset-4">
                    <h3 class="title has-text-black">Login</h3>
                    <hr class="login-hr">
                    <p class="subtitle has-text-black">Please login to proceed.</p>
                    <div class="box">
                        <figure class="avatar">
                            <img src="https://placehold.it/128x128" alt="">
                        </figure>
                        <form >
                            <div class="field">
                                <div class="control">
                                    <input class="input is-large" type="text" placeholder="username" bind:value={formobj.user} >
                                </div>
                            </div>

                            <div class="field">
                                <div class="control">
                                    <input class="input is-large" type="password" placeholder="Your Password" bind:value={formobj.pass}>
                                </div>
                            </div>
                            <div class="field">
                                <label class="checkbox">
                  <input type="checkbox">
                  Remember me
                </label>
                            </div>
                            <a class="button is-block is-info is-large is-fullwidth" href="/customer/loghomecust" on:click={handlesubmit}>Login <i class="fa fa-sign-in" aria-hidden="true"></i></a>
                        </form>
                    </div>
                    <p class="has-text-grey">
                        <a href="/">Sign Up</a> &nbsp;·&nbsp;
                        <a href="/ltop/forget">Forgot Password</a> &nbsp;·&nbsp;
                        <a href="/">Need Help?</a>
                    </p>
                </div>
            </div>
        </div>
    </section>
</main>
{JSON.stringify(formobj)}
{JSON.stringify(apidata)}