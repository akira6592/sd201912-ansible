# sd201912-ansible


# 実行例

```
$ ansible-playbook -i inventory.ini gather_info.yml 

PLAY [ios] ********************************************************************************************************

TASK [create directory] *******************************************************************************************
changed: [ios01]

TASK [gather facts] ***********************************************************************************************
ok: [ios01]
ok: [ios02]

TASK [execute show commands] **************************************************************************************
ok: [ios01]
ok: [ios02]

TASK [output to files] ********************************************************************************************
changed: [ios01] => (item=show version)
changed: [ios02] => (item=show version)
changed: [ios01] => (item=show ip route)
changed: [ios02] => (item=show ip route)

TASK [create report] **********************************************************************************************
changed: [ios01]

PLAY RECAP ********************************************************************************************************
ios01                      : ok=5    changed=3    unreachable=0    failed=0    skipped=0    rescued=0    ignored=0   
ios02                      : ok=3    changed=1    unreachable=0    failed=0    skipped=0    rescued=0    ignored=0   

$ 
```
