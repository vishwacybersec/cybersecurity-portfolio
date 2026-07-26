# SPL Queries Used

## 1. Authentication Success vs Failure

```spl
index=soc_projects source="01_soc-lab.csv" (EventCode=4624 OR EventCode=4625)
| eval Login_Status=if(EventCode==4624,"Successful Login","Failed Login")
| stats count by Login_Status
```

---

## 2. Event ID Distribution

```spl
index=soc_projects source="01_soc-lab.csv"
| stats count by EventCode
| sort -count
```

---

## 3. Top Source IP Addresses

```spl
index=soc_projects source="01_soc-lab.csv" EventCode=4625
| stats count by src_ip
| sort -count
```

---

## 4. Targeted User Accounts

```spl
index=soc_projects source="01_soc-lab.csv" EventCode=4625
| stats count by user
| sort -count
```

---

## 5. Attack Timeline

```spl
index=soc_projects source="01_soc-lab.csv" (EventCode=4624 OR EventCode=4625)
| timechart span=5m count by EventCode
```

---

## 6. PowerShell Process Execution

```spl
index=soc_projects source="01_soc-lab.csv" EventCode=4688
| table _time user process_name description
```

---

## 7. Privilege Escalation

```spl
index=soc_projects source="01_soc-lab.csv" EventCode=4672
| table _time user description
```

---

## 8. Account Creation & Domain Admin Changes

```spl
index=soc_projects source="01_soc-lab.csv" (EventCode=4720 OR EventCode=4728)
| table _time EventCode user new_account group_name description
```
