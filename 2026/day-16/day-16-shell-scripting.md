# Day 16 – Shell Scripting Basics

## TASK 1
-   cat hello.sh
    #!/bin/bash

    echo "Hello, DevOps!"
-   sudo chmod +x hello.sh  # making it executable
-   ./hello.sh    >> running the shell script
Hello, DevOps!

## TASK 2

-   cat variables.sh
    #!/bin/bash

    NAME='Harsh'
    ROLE="Learner"

    echo "Hello, I am $NAME and I am a $ROLE"

-   ./variables.sh
Hello, I am Harsh and I am a Learner

## TASK 3

-   cat greet.sh
    #!/bin/bash
    #
    read -p "Enter name: " NAME
    read -p "Enter favourite tool: " TOOL

    echo "Hello $NAME, you favourite tool is $TOOL "

-   ./greet.sh
    Enter name: Harsh
    Enter favourite tool: shell
    Hello Harsh, you favourite tool is shell

##  TASK 4

-   cat check_number.sh
---
#!/bin/bash
#
read -p "Enter the number: " Number

    if ((Number > 0)); then
        echo "positive"
    elif ((Number < 0)); then
        echo "negative"
    else
        echo "zero"
    fi

-   ./check_number.sh
    Enter the number: 2
    positive

## TASK 6