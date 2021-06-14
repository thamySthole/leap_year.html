# leap_year.html
it calculates how many leap days you've seen since you were born
<html>

<head>
    <style>
        * {
            margin: 0px;
            padding: 0px;
        }
        input,
        button {
            position: absolue;
            height: 30px;
            margin-top: 100px;
            margin-left: 40px;
            font-size: 1rem;
            color: #adefef;
            outline: none;
            padding: 3px;
        }
        input {
            border: 2px solid #adefef;
            border-radius: 3px;
        }
        button {
            margin-left: 0px;
            border-radius: 3px;
            background: #2eedde;
            border: 0px solid;
            color: grey;
        }
        button:Active{
            opacity: 3px;
            background: #adefef;
            color: white;
        }
   
            </style>
</head>

<body>
   <h1>leapyear counter</h1>
    <input class='text' type="text" placeholder="year of birth" />
        <button type="button">send</button>
        <div>
  
</div>
    
    <script>
alert('this counts leaps years you have since you were born please enter you date of birth                                           much love✈️✈️🤘')
    let print = console.log
   
    let span = document.querySelector('span');
    let btnSend = document.querySelector('button');
    let inputText = document.querySelector('input');
        let div = document.querySelector('div');
  
        btnSend.addEventListener('click', boom)
        
       
        //generating all the years 
        function year_generator(){
          let all_years = []
          
          for(i=1800;i < 2021;i+=1){
            //control yaer or year with leapyear
            let yearStr = ''+i+''
            let y = parseInt(yearStr)
            
           if(y %2 == 0){
               let obj = {
                 year:i,
                 leap: true
               }
              
               all_years.push(obj)
               
            }else{
              let obj = {
                 year:''+i+'',
                 leap: false
               }
           
               all_years.push(obj)
          
            }
          }
        
         return all_years
        }
      let h4 = document.createElement('h4')
        
        
        function boom(){
         let year = parseInt(inputText.value)
         inputText.innerHTML = ''
          let leap_year = []
          let control_years = year_generator()
          
         for(i=0;i<control_years.length;i+=4){
           leap_year.push(control_years[i])
         }
         
         let leap_days = 0
         
         for(i=0;i<leap_year.length;i+=1){
            if(leap_year[i].year > year ){
              leap_days += 1
            }}
    
          h4.innerHTML= `you have seen ${leap_days} leap years in your life  `
          div.append(h4)
        
        setInterval(()=> h4.innerHTML = '',4000)
        
        }
    </script>
</body>
</html/>
