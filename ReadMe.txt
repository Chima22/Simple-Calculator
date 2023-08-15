This is a simple calculator made by Ugokwe Chima to paritce my JS skills.

  This project consist of three stack language:
  1: HTML
  2: CSS
  3: Javascript 

  1: The HTML code is the structure of the calculator:
  <form >
            <input type="text" class="screen">
        </form>

        <div class="buttons">
            <button type="buttons" class="btn btn-yellow" data-num="*">*</button>
            <button type="buttons" class="btn btn-yellow" data-num="/">/</button>
            <button type="buttons" class="btn btn-yellow" data-num="-">-</button>
            <button type="buttons" class="btn btn-yellow" data-num="+">+</button>

            <button type="buttons" class="btn btn-grey" data-num="9">9</button>
            <button type="buttons" class="btn btn-grey" data-num="8">8</button>
            <button type="buttons" class="btn btn-grey" data-num="7">7</button>
            <button type="buttons" class="btn btn-grey" data-num="6">6</button>
            <button type="buttons" class="btn btn-grey" data-num="5">5</button>
            <button type="buttons" class="btn btn-grey" data-num="4">4</button>
            <button type="buttons" class="btn btn-grey" data-num="3">3</button>
            <button type="buttons" class="btn btn-grey" data-num="2">2</button>
            <button type="buttons" class="btn btn-grey" data-num="1">1</button>
            <button type="buttons" class="btn btn-grey" data-num="0">0</button>
            <button type="buttons" class="btn btn-grey" data-num=".">.</button>

            <button type="buttons" class="btn-equal" id="but">=</button>
            <button type="buttons" class="btn-clear">c</button>

2: The CSS consist of the looks or design of the calculator:
*{
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}
body{
    min-height: 100vh;
    background: #efeff2;
    display: flex;
    align-items: center;
    justify-content: center;
   
}

 .calculator{
    width: 300px;
    height: 520px;
    box-shadow: 4px 4px 30px rgb(0, 0, 0, 0.3);
    background:#22252D;
    border-radius: 12px;
    overflow: hidden;
 }

 form input{
    width: 100%;
    height: 100px;
    border: none;
    border-radius: 12px;
    padding: 1rem;
    font-size: 2rem;
    color: white;
    background: #000;
    text-align: right;
    pointer-events: none;
 }
    .buttons{
        display: flex;
        flex-wrap: wrap;
        justify-content:space-between;
        padding: 20px;
        /* margin: 0 20px; */
    }
 button{
    flex: 5% 0 10%;
    width: 60px;
    height: 50px;
    border-radius: 12px;
    margin: 15px 0;
    font-size: 22px;
    font-weight: 600;
    cursor: pointer;

 }

.btn-yellow{
    background: rgb(245, 146, 62);
    color: #ffff;
}

.btn-grey{
    background: rgb(224, 224, 224);
}
.btn-equal{
    background:green;
}
 .btn-clear{
    background: red;
 }
 while 
 3: The JS consist of the arithemetic calculations(calculator functions):
 let screen = document.querySelector('.screen');
let buttons = document.querySelectorAll('.btn');
let clear = document.querySelector('.btn-clear');
let equal = document.querySelector('.btn-equal');

 buttons.forEach(function(button){
    button.addEventListener('click', function(e){
        let value= e.target.dataset.num;
        screen.value += value;
         
    })
 });

  equal.addEventListener('click', function(e){
    if(screen.value === ''){
        screen.value = 0;
    }else{
        let answer = eval(screen.value);
        screen.value = answer;
    }
  })

  clear.addEventListener('click', function(e){
      screen.value = " ";

  })

  Please do well to reveiwe and give feed back and also network with me on Git for more improvement.

  Thanks