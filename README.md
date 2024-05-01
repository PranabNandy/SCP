# SCP
- It is standard for System Co-Processor which helps the actual processor for better Execution Performance
- Like CPU Co-Processor


## Histroy of SCP
![Screenshot from 2024-05-01 12-45-48](https://github.com/PranabNandy/SCP/assets/34576104/a9289b6a-a57e-4935-9441-3aceac992891)


## SCP IP
![Screenshot from 2024-05-01 12-19-26](https://github.com/PranabNandy/SCP/assets/34576104/7cc023af-aa51-467d-8c39-af2b83f98d9c)

## Communication Protocol
![Screenshot from 2024-05-01 12-44-14](https://github.com/PranabNandy/SCP/assets/34576104/df80bce3-9380-4947-afb2-dff86e6931d0)
![Screenshot from 2024-05-01 13-13-57](https://github.com/PranabNandy/SCP/assets/34576104/2bf8d502-622e-4445-9635-e7588ba321b7)

## Responsibilites of SCP
- Performing DCVS operation
   + Take help from PMU counter
   + Take help from AMU counter
  
- debug Purpose
  + CacheDump
  + **RegDump**
- **MPMM Feature** `(cpuctl module)`
- CPU Profiling
- **Qultivate Feature** `(cpuinfo module)`
- Implemented Timer based Scheduler in Baremetal Code 
  + used he concept of ready queue
  + Systicktimer
  + Task Priority
- Implemented SCMI communication Protocol
- Implemented various algo for performance enhancement
   + memlat 
   + pmfs ( Performance metric based freq scaling(pulse swallow))
   + cpuFreq_Stats (dcvs residency date)
   + PLH ( perf lock hardening)
   + pf_Tune ( APSS cpu prefetch tuning based on CPU load)
