# jokeapp-javascript
html content
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <link rel="stylesheet" href="joke.css">
</head>
<body>
    <div id="container">
        <h3>best jokes</h3>
        <div id="joke" class="joke">awsome joke loading</div>
        <button id="jokebtn" class="btn" style="margin:0 auto; display:block; width: 100px;">next joke</button>
    </div>
    <script src="newproject.js"></script>
</body>
</html>
javascript content
const jokes=document.querySelector('#joke');
const jokesbtn=document.querySelector('#jokebtn')
const generatejokes=()=>{
    const setHeader={
        headers:{
            Accept:"application/json"
        }
    }

fetch('https://icanhazdadjoke.com',setHeader).
then((res)=>res.json()).
then((data)=>{joke.innerHTML=data.joke})

}
jokesbtn.addEventListener('click',generatejokes)
css content
body{
 display: flex;
 justify-content: center;
 align-items: center;
 height: 100%;
 width: 100%;
 overflow: hidden;

}
#container{
 
    overflow: hidden;
    width: 30%;
    text-align: center;
    justify-content: center;
    position: relative;
}
