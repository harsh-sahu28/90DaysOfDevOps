# Day 16 – Shell Scripting Basics

## TASK 1

```bash
-   cat hello.sh
    #!/bin/bash

    echo "Hello, DevOps!"
```

```bash
-   sudo chmod +x hello.sh  # making it executable
-   ./hello.sh    >> running the shell script
Hello, DevOps!
```

## TASK 2
```bash
-   cat variables.sh
    #!/bin/bash

    NAME='Harsh'
    ROLE="Learner"

    echo "Hello, I am $NAME and I am a $ROLE"
```

```bash
-   ./variables.sh
Hello, I am Harsh and I am a Learner
```
## TASK 3
```bash
-   cat greet.sh
    #!/bin/bash
    #
    read -p "Enter name: " NAME
    read -p "Enter favourite tool: " TOOL

    echo "Hello $NAME, you favourite tool is $TOOL "
```
```bash
./greet.sh
Enter name: Harsh
Enter favourite tool: shell
Hello Harsh, you favourite tool is shell
```

## TASK 4

### check_number.sh

```bash
cat check_number.sh
#!/bin/bash

read -p "Enter the number: " Number

if ((Number > 0)); then
    echo "positive"
elif ((Number < 0)); then
    echo "negative"
else
    echo "zero"
fi
```

### Run
```bash
./check_number.sh
```

### Output
```
Enter the number: 2
positive
```

## TASK 6