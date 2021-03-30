# Bash Cheatsheet

## Shortcuts
```
Ctrl + A              # 移動到行首，同 <Home>
Ctrl + E              # 移動到行末，同 <End>
Alt  + B              # Backward a word
Alt  + F              # Forward a word
Ctrl + U              # Delete all characters before cursor
Ctrl + K              # Delete all characters after cursor
Ctrl + W              # Delete word before cursor
Alt  + D              # Delete word after cursor
Alt  + T              # Swap words before cursor
Ctrl + Y              # Paste deleted content
Ctrl + P              # Scroll up through history
Ctrl + N              # Scroll down through history
Crtl + R              # Reverse search
Ctrl + P              # Forward search
Ctrl + G              # Exit search
```


## parameter

`$#` number of parameter
`$*` "$1 $2 $3 $4"
`$@` "$1" "$2" "$3" "$4"


## Variable

```
var=something
echo $var
unset var
```

## Parameter expansion ${}

```
echo ${var}
echo ${var/old/new}
echo ${#var}
echo ${var:0:4}
```

## Command

```
`command`

$(command)
```

## Environment Variable

```
env
set
declare
```

## Process

```
Ctrl + Z              # background
fg                    # foreground
```

## Execute

```
#!/usr/bin/env bash
```

## Download and Execute Script

```
curl -fsSL https://get.yihsiu.io -o get-nodejs.sh
sudo sh get-nodejs.sh
```

```
 wget -qO- https://raw.githubusercontent.com/yihsiu806/utility/master/get-nodejs.sh | sh
```

## Read line from STDIN

```bash
while IFS= read -r line; do
    echo $line
done < /dev/stdin
```

## Read line from file

```bash
while IFS= read -r line; do
    echo $line
done < filename
```

## Test Connectivity

```bash
if ping -q -c 1 -W 1 ${IP} > /dev/null; then
    logger -t ${TAG} ping ${IP} success!
else
    logger -t ${TAG} ping ${IP} fail!
fi
```

## Check Root Privilege

```bash
if [ $EUID -eq 0 ]; then
    echo "User has root privilege."
else
    echo "User has no root privilege. Use sudo."
fi
```

## Check Command Exist

```bash
cmd=curl
if type "$cmd" &> /dev/null; then
    echo "Command \"$cmd\" exist"
else
    echo "Command \"$cmd\" not found"
fi
```

## Check Line Number

```bash
files=$(ls)

for file in $files
do
    lines=$(cat $file | wc -l)
    #echo $file : $lines
    if [ $lines -gt 32 ]
    then
        echo $v too big!!
    fi
done
```


## Reference
1. https://devhints.io/bash
2. https://learnxinyminutes.com/docs/bash/
3. https://github.com/skywind3000/awesome-cheatsheets/blob/master/languages/bash.sh