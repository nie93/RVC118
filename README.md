# RVC118
This is the Analytic project of Regional Voltage Controller using IEEE 118-bus system, generated using 
openECA Client v1.0.5.0.


## Capacitor Bank Capacity
| No. | BusNum | Capacity(MVar) |
| --: | -----: | -------------: | 
| 1 |  34 |  0 ~  50 | 
| 2 |  44 | 10 ~  50 |
| 3 |  45 | 10 ~  50 | 
| 4 |  48 |  0 ~ 100 |
| 5 |  74 | 12 ~ 100 |
| 6 | 105 |  0 ~  20 |


```python
if combination[0] == 1:
    psspy.shunt_data(34, r"""1""", 1, [_f, 50])
if combination[0] == 0:
    psspy.shunt_data(34, r"""1""", 1, [_f, 0])
if combination[1] == 1:
    psspy.shunt_data(44, r"""1""", 1, [_f, 50])
if combination[1] == 0:
    psspy.shunt_data(44, r"""1""", 1, [_f, 10])
if combination[2] == 1:
    psspy.shunt_data(45, r"""1""", 1, [_f, 50])
if combination[2] == 0:
    psspy.shunt_data(45, r"""1""", 1, [_f, 10])
if combination[3] == 1:
    psspy.shunt_data(48, r"""1""", 1, [_f, 100])
if combination[3] == 0:
    psspy.shunt_data(48, r"""1""", 1, [_f, 0])
if combination[4] == 1:
    psspy.shunt_data(74, r"""1""", 1, [_f, 100])
if combination[4] == 0:
    psspy.shunt_data(74, r"""1""", 1, [_f, 12])
if combination[5] == 1:
    psspy.shunt_data(105, r"""1""", 1, [_f, 20])
if combination[5] == 0:
    psspy.shunt_data(105, r"""1""", 1, [_f, 0])
```


## I/Os

| I/O | Name | DataType | PointTag | SignalType | SignalReference | ID (Assigned) |
| :-: | :--- | :------- | :------- | :--------: | :-------------- | :------------ |
| O | ActSnB34Close  | short | SS_118:ACTSNB34CLOSE  | DIGI | SS118-ACTSNB34CLOSE  | PPA:63 |
| O | ActSnB44Close  | short | SS_118:ACTSNB44CLOSE  | DIGI | SS118-ACTSNB44CLOSE  | PPA:64 |
| O | ActSnB45Close  | short | SS_118:ACTSNB45CLOSE  | DIGI | SS118-ACTSNB45CLOSE  | PPA:65 |
| O | ActSnB48Close  | short | SS_118:ACTSNB48CLOSE  | DIGI | SS118-ACTSNB48CLOSE  | PPA:66 |
| O | ActSnB74Close  | short | SS_118:ACTSNB74CLOSE  | DIGI | SS118-ACTSNB74CLOSE  | PPA:67 |
| O | ActSnB105Close | short | SS_118:ACTSNB105CLOSE | DIGI | SS118-ACTSNB105CLOSE | PPA:68 |
| O | ActSnB34Trip   | short | SS_118:ACTSNB34TRIP   | DIGI | SS118-ACTSNB34TRIP   | PPA:69 |
| O | ActSnB44Trip   | short | SS_118:ACTSNB44TRIP   | DIGI | SS118-ACTSNB44TRIP   | PPA:70 |
| O | ActSnB45Trip   | short | SS_118:ACTSNB45TRIP   | DIGI | SS118-ACTSNB45TRIP   | PPA:71 |
| O | ActSnB48Trip   | short | SS_118:ACTSNB48TRIP   | DIGI | SS118-ACTSNB48TRIP   | PPA:72 |
| O | ActSnB74Trip   | short | SS_118:ACTSNB74TRIP   | DIGI | SS118-ACTSNB74TRIP   | PPA:73 |
| O | ActSnB105Trip  | short | SS_118:ACTSNB105TRIP  | DIGI | SS118-ACTSNB105TRIP  | PPA:74 |
| I | StateSnB34CapBkrV  | short | SS_118:STATESNB34CAPBKRV  | DIGI | SS118-STATESNB34CAPBKRV  | PPA:75 |
| I | StateSnB44CapBkrV  | short | SS_118:STATESNB44CAPBKRV  | DIGI | SS118-STATESNB44CAPBKRV  | PPA:76 |
| I | StateSnB45CapBkrV  | short | SS_118:STATESNB45CAPBKRV  | DIGI | SS118-STATESNB45CAPBKRV  | PPA:77 |
| I | StateSnB48CapBkrV  | short | SS_118:STATESNB48CAPBKRV  | DIGI | SS118-STATESNB48CAPBKRV  | PPA:78 |
| I | StateSnB74CapBkrV  | short | SS_118:STATESNB74CAPBKRV  | DIGI | SS118-STATESNB74CAPBKRV  | PPA:79 |
| I | StateSnB105CapBkrV | short | SS_118:STATESNB105CAPBKRV | DIGI | SS118-STATESNB105CAPBKRV | PPA:80 |
| I | MeasB1VoltV   | double | SS_118:MEASB1VOLTV   | VPHM | SS118-MEASB1VOLTV   | PPA:81  |
| . | ...           | ...    | ...                  | ...  | ...                 | ...     |
| I | MeasB118VoltV | double | SS_118:MEASB118VOLTV | VPHM | SS118-MEASB118VOLTV | PPA:198 |
| N/A | ResetSignal     | short | SS_118:RESET | DIGI | SS118-RESET | PPA:62 |
| N/A | LoadIncrementPercentage | double | SS_118:LOADINCRE | DIGI | SS118-LOADINCRE | PPA:41 |
| N/A | VoltSecurityStatus | short | | | | |  

* i = 1, 2, ..., 118
* k = 1, 2, ..., 6

## SQL Script Supplement
```sql

```






<!--| O | ActTxRaise      | short  | SS_118:ACTTXRAISE      | DIGI | SS118-ACTXRAISE   | PPA:42 |
| O | ActTxLower      | short  | SS_118:ACTTXLOWER      | DIGI | SS118-ACTTXLOWER  | PPA:43 |
| O | ActSn1Close     | short  | SS_118:ACTSN1CLOSE     | DIGI | SS118-ACTSN1CLOSE | PPA:44 |
| O | ActSn1Trip      | short  | SS_118:ACTSN1TRIP      | DIGI | SS118-ACTSN1TRIP  | PPA:45 |
| O | ActSn2Close     | short  | SS_118:ACTSN2CLOSE     | DIGI | SS118-ACTSN2CLOSE | PPA:46 |
| O | ActSn2Trip      | short  | SS_118:ACTSN2TRIP      | DIGI | SS118-ACTSN2TRIP  | PPA:47 |
| I | StateTxTapV     | short  | SS_118:STATETXTAPV     | DIGI | SS118-STATETXTAPV | PPA:48 |
| I | StateSn1CapBkrV | short  | SS_118:STATESN1CAPBKRV | DIGI | SS118-STATESN1CAPBKRV | PPA:49 |
| I | StateSn2CapBkrV | short  | SS_118:STATESN2CAPBKRV | DIGI | SS118-STATESN2CAPBKRV | PPA:50 |
| I | StateSn1BusBkrV | short  | SS_118:STATESN1BUSBKRV | DIGI | SS118-STATESN1BUSBKRV | PPA:51 |
| I | StateSn2BusBkrV | short  | SS_118:STATESN2BUSBKRV | DIGI | SS118-STATESN2BUSBKRV | PPA:52 |
| I | MeasTxVoltV     | double | SS_118:MEASTXVOLTV     | VPHM | SS118-MEASTXVOLTV  | PPA:53 |
| I | MeasSn1VoltV    | double | SS_118:MEASSN1VOLTV    | VPHM | SS118-MEASSN1VOLTV | PPA:54 |
| I | MeasSn2VoltV    | double | SS_118:MEASSN2VOLTV    | VPHM | SS118-MEASSN2VOLTV | PPA:55 |
| I | MeasTxMwV       | double | SS_118:MEASTXMWV       | CALC | SS118-MEASTXMWV    | PPA:56 |
| I | MeasTxMvrV      | double | SS_118:MEASTXMVRV      | CALC | SS118-MEASTXMVRV   | PPA:57 |
| I | MeasGn1MwV      | double | SS_118:MEASGN1MWV      | CALC | SS118-MEASGN1MWV   | PPA:58 |
| I | MeasGn1MvrV     | double | SS_118:MEASGN1MVRV     | CALC | SS118-MEASGN1MVRV  | PPA:59 |
| I | MeasGn2MwV      | double | SS_118:MEASGN2MWV      | CALC | SS118-MEASGN2MWV   | PPA:60 |
| I | MeasGn2MvrV     | double | SS_118:MEASGN2MVRV     | CALC | SS118-MEASGN2MVRV  | PPA:61 |
| N/A | LoadIncrementPercentage | double | SS_118:LOADINCRE | DIGI | SS118-LOADINCRE | PPA:41 |-->


