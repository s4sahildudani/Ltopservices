<script>
let formobj = {
  "user":"",
 }
 let apidata= {
 "auth": "forgotpassword",
  "c_id": "3v9h9sli9f0c4bhepe81vsho1j",
"user": ""
 }
async function handlesubmit() {
apidata.user=formobj.user
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
 }

</script>
<main>
 <h1>Forget password</h1>
 <div id="ddf">
     <h2>Enter url</h2>
     <input type="text"  placeholder="Url"  bind:value={formobj.user} >
     <a class="button" href="/" on:click={handlesubmit}>Submit</a>
 </div>
</main>
<style>
h1{
    text-align: center;
    background-color: rgb(255, 255, 255);
    color: rgb(202, 9, 9);
}
#ddf{
    text-align: center;
}
</style>