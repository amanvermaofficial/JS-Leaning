# Projects

## project1

```javascript

const buttons = document.querySelectorAll('.button');
const body = document.querySelector('body');

buttons.forEach(function (button) {
  console.log(button);
  button.addEventListener('click', (e) => {
    console.log(e.target);
    if (e.target.id === 'grey') {
      body.style.backgroundColor = e.target.id;
    }
    if (e.target.id === 'yellow') {
      body.style.backgroundColor = e.target.id;
    }
    if (e.target.id === 'blue') {
      body.style.backgroundColor = e.target.id;
    }
    if (e.target.id === 'white') {
      body.style.backgroundColor = e.target.id;
    }
    
  });
});

```
## project2

```javascript



let button = document.getElementById('btn')

//This UseCase  will give you empty
//let weight = parseInt(document.getElementById('weight').value)

button.addEventListener('click',function calculateBmi(){
  let weight = parseInt(document.getElementById('weight').value)
  let height = parseInt(document.getElementById('height').value)
  let result = document.getElementById("results")
  if(height==="" || isNaN(height)){
       result.innerHTML = `Please Provide valid height`
  }
  else if(weight==="" || isNaN(weight)){
       result.innerHTML = `Please Provide valid weigth`
  }
  else{

     let bmi = (weight / ((height * height) 
    / 10000)).toFixed(2);
    if(bmi<18.6){
      result.innerHTML = `UnderWeight Your Bmi : ${bmi}`
    }
    if(bmi>18.6 || bmi<24.9){
      result.innerHTML = `Normal Range Your Bmi : ${bmi}`
    }
    if(bmi>24.9){
      result.innerHTML = `Overweight Your Bmi : ${bmi}`
    }
  
  }
})
