# Stress Test Commands and Outputs

## Input
---------------------------
```bash
free --mega
```

## Output
---------------------------
```bash
               total        used        free      shared  buff/cache   available
Mem:            4105        1162        2179          41        1041        2942
Swap:           4105           0        4105
```

## Input
---------------------------
```bash
free --mega | awk 'NR==2 {print $4}' > free_mega_before_stress
```

## Output
---------------------------
*No output returned to terminal.*

## Input
---------------------------
```bash
stress --vm 1 --vm-bytes 512M --vm-keep -t 300s &
```

## Output
---------------------------
```bash
[4] 3885
stress: info: [3885] dispatching hogs: 0 cpu, 0 io, 1 vm, 0 hdd
```

## Input
---------------------------
```bash
free --mega
```

## Output
---------------------------
```bash
               total        used        free      shared  buff/cache   available
Mem:            4105        1694        1647          41        1042        2411
Swap:           4105           0        4105
```

## Input
---------------------------
```bash
stress --vm 1 --vm-bytes 512M --vm-keep -t 300s &
```

## Output
---------------------------
```bash
[5] 3891
stress: info: [3891] dispatching hogs: 0 cpu, 0 io, 1 vm, 0 hdd
```

## Input
---------------------------
```bash
free --mega
```

## Output
---------------------------
```bash
               total        used        free      shared  buff/cache   available
Mem:            4105        2239        1102          41        1042        1866
Swap:           4105           0        4105
```

## Input
---------------------------
```bash
free --mega | awk 'NR==2 {print $4}' > free_mega_during_stress
```

## Output
---------------------------
*No output returned to terminal.*

## Input
---------------------------
```bash
ps -eo pid,%mem,%cpu,cmd --sort=-%mem | head -n 6
```

## Output
---------------------------
```bash
    PID %MEM %CPU CMD
   3886 13.0  100 stress --vm 1 --vm-bytes 512M --vm-keep -t 300s
   3892 13.0 99.9 stress --vm 1 --vm-bytes 512M --vm-keep -t 300s
   2276  9.1  2.6 /usr/bin/gnome-shell
   2906  2.2  0.0 /usr/libexec/mutter-x11-frames
   2767  1.8  0.0 /usr/libexec/gsd-xsettings
```

## Input
---------------------------
```bash
bc <<< "$(cat free_mega_before_stress) - $(cat free_mega_during_stress)"
```

## Output
---------------------------
```bash
1074
```

## Input
---------------------------
```bash
stress: info: [3885] successful run completed in 300s
```

## Output
---------------------------
*No output returned to terminal.*
```

