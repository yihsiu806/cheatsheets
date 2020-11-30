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