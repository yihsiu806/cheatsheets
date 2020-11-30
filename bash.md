### Test Connectivity

```bash
test_connectivity() {
    if ping -q -c 1 -W 1 ${IP} > /dev/null
    then
        logger -t ${TAG} ping ${IP} success!    
    else 
        logger -t ${TAG} ping ${IP} fail!
    fi
}
```