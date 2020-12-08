


# Shortcuts
```
Ctrl + A # 移動到行首，同 <Home>
Ctrl + E # 移動到行末，同 <End>
Alt  + B # Backward a word
Alt  + F # Forward a word
Ctrl + U # Delete all characters before cursor
Ctrl + K # Delete all characters after cursor
Ctrl + W # Delete word before cursor
Alt  + D # Delete word after cursor
Alt  + T # Swap words before cursor
Ctrl + Y # Paste deleted content
Ctrl + P # Scroll up through history
Ctrl + N # Scroll down through history
Crtl + R # Reverse search
Ctrl + P # Forward search
Ctrl + G # Exit search
```

# Process
```
Ctrl + Z # background
fg       # foreground
```

### Read line from STDIN
```bash
while IFS= read -r line; do
    echo $line
done < /dev/stdin
```

### Read line from file
```bash
while IFS= read -r line; do
    echo $line
done < filename
```

### Test Connectivity
```bash
if ping -q -c 1 -W 1 ${IP} > /dev/null; then
    logger -t ${TAG} ping ${IP} success!
else
    logger -t ${TAG} ping ${IP} fail!
fi
```

### Check Root Privilege
```bash
if [ $EUID -eq 0 ]; then
    echo "User has root privilege."
else
    echo "User has no root privilege. Use sudo."
fi
```

### Check Command Exist
```bash
cmd=curl
if type "$cmd" &> /dev/null; then
    echo "Command \"$cmd\" exist"
else
    echo "Command \"$cmd\" not found"
fi
```

# Reference
1. https://devhints.io/bash
2. https://learnxinyminutes.com/docs/bash/
3. https://github.com/skywind3000/awesome-cheatsheets/blob/master/languages/bash.sh