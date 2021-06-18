<script>
//  let formobj = {
//   "user":"",
// "pass":""
//  }
 let apidata= {
    "auth":"logout",
// "c_id":"3v9h9sli9f0c4bhepe81vsho1j",
// "user":"",
// "pass":"" 
 }
 async function handlesubmit() {
// apidata.user=formobj.user
// apidata.pass=formobj.pass
  const res = await fetch("https://38fteogd70.execute-api.ap-south-1.amazonaws.com/default/botocognitoauth",{
   method:'POST',
   mode:"cors",
   credentials:'include',

headers:{
"X-API-KEY":"xnFSKlZEm01aSvcgdd7Bx5ttpzyF494F1WOF0JvZ",
   "Content-Type":"application/json",
    
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
    <button on:click={handlesubmit}><a href="/">Logout</a></button>
    <!-- <button on:click={handlesubmit}>Logout</=> -->
</main>