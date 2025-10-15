- React condtional statement
-------------------------------
        (&&) ->  if statement

        Example : 
        ----------
                function Home(){
                    const [age,setAge] = useState(21)
                    
                    return <div>
                        <h1> Age - {age} </h1>

                        { (age >=18) && (
                            <h6> Eligible....</h6>
                        ) }
                        
                    </div>
                }

        (? :) -> Ternary operator -> (?) - Trueblock (:) -> False block    (IF-ELSE statement)

            Example
            -------

                function Home(){

                    const [age,setAge] = useState(5)

                    return <div>
                        <h1> Age - {age} </h1>

                        { (age >= 18) ? 
                        (
                            <h6> Eligible....</h6>
                        ) 
                        :
                        (
                            <h2> Not Eligible</h2>
                        )
                        
                        }
                        
                    </div>
                }





- React looping - (map)
--------------------------
Example 1 - (Simple IF)
-----------
function Home(){

  const [fruit,setFruit] = useState(["apple","orange","banana"])
  
  return <div>
      { fruit.length != 0  && 
          fruit.map((value,index) => {
            return <p> {value} </p>
          })
      } 
  </div>
}

Example 2 - (Ternary Operator)
-----------

function Home(){

  const [fruit,setFruit] = useState([])
  
  return <div>
      { fruit.length != 0  ?
          fruit.map((value,index) => {
            return <p> {value} </p>
          })
        :
        <h6> Fruits not found</h6>
      } 
  </div>
}
