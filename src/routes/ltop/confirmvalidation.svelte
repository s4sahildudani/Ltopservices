<script>
 let formobj = {
  "user":"",
   "confirmcode":""
 }
 let apidata= {
 "auth": "confirmsignup",
"c_id": "3v9h9sli9f0c4bhepe81vsho1j",
"user": "",
"c_code": ""
 }
 async function handlesubmit() {
apidata.user=formobj.user
apidata.c_code=formobj.confirmcode
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
    <h2>Confirm your Verification</h2>
    <input type="text" placeholder="Enter user" bind:value={formobj.user}>
<input type="text" placeholder="Enter Code"  bind:value={formobj.confirmcode}>
<a class="button" href="/ltop/login"  on:click={handlesubmit}>
    Submit
</a>
{JSON.stringify(formobj)}
{JSON.stringify(apidata)}
</main>
<style>
    main{
        height: 50vh;
        background-color: aqua;
    }
</style>