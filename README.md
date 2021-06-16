سید مجید ساعدی ، تمرین 10

-------------------------------

سوال 1

    #!/bin/bash

    echo "Age:"

    read age

    if [ $age -ge 18 ]

    then

        echo "You may go to the party."
   
    elif [ $age -lt 18 ] 

    then

        echo "do you have permission from your parents?"
    
        read letter
    
        if [ $letter = "yes" ]
    
    then
    
          echo "You may go to the party but be back before midnight."
       
    else
    
          echo "You may not go to the party."    
       
        fi
    
    fi

-------------------------------

سوال 2

    #!/bin/bash

    export i=1

    while [ $i -le 100 ]

    do 

	      mkdir user$i;
  
	      i=$((i+1)); 
  
    done

-------------------------------

سوال 3

    #!/bin/bash
    echo directory:
    read dir
    cnt=0
    for file in $(find $dir -type f -name "*.jpg");
    do
	mv $file $dir/img$((cnt = cnt + 1)).jpg
    done
    for file in $(find $dir -type f -name "*.png");
    do
        mv $file $dir/img$((cnt = cnt + 1)).png
    done

-------------------------------

سوال 4

    #!/bin/bash
    echo "Choose Operator (1,2,3,4) : 1)sum(+)  2)sub(-)  3)mul(*)  4)div(/)"
    read op
    echo "Enter first number:"
    read number1
    echo "Enter second number:"
    read number2
    if [ $op = 1 ]
    then
        echo "Result = "$(($number1+$number2))
    elif [ $op = 2 ]
    then
        echo "Result = "$(($number1-$number2))
    elif [ $op = 3 ]
    then
        echo "Result = "$(($number1*$number2))
    elif [ $op = 4 ]
    then
        echo "Result = "$(($number1/$number2))
    else
        echo "Please Try Again!!!"
    fi

