
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
- Implemented SCMI Communication Protocol
- Implemented various algo for performance enhancement
   + memlat 
   + pmfs ( Performance metric based freq scaling(pulse swallow))
   + cpuFreq_Stats (dcvs residency date)
   + PLH ( perf lock hardening)
   + pf_Tune ( APSS cpu prefetch tuning based on CPU load)

![Screenshot from 2024-05-01 15-11-07](https://github.com/PranabNandy/SCP/assets/34576104/18ef9b44-cdbd-4104-9297-2b16b9436e11)

### what is Freq supplied to SCP?
- It is 300 MHz
- Same PLL is shared between **SCP** and **NoC(network on chip) IP**
- Now suppose we need only 130 MHz but as we don't use any divider we directly supply this to SCP
- with extra freq (170MHz extra), power loss is not so high
### what is SCP utilization in the system?
- answer 35% ( even though it is 5% only)

### SysTick Timer
- It is a special timer in most arm cortex-A/ Cortex-M processors that's usually reserved for calculating time slices in an RTOS.
- By default, it generates INT in every 1 mSec.

### what is the starting point of `your responsibility` in the Project that comes under your team?
- Product Manager<------- `requirement gathering`--------> Customer
- HW design team -------> design the RTL
- We don't work in entire Automotive SoC
- **RTL** : It is nothing but SW code written in VHDL
- Then we flushed the RTL into **FPGA**
- The we called it **RUMI**
- HW team takes input from us while designing the **EPSS IP** in the designing phase
- Then we start writing the Code (`SCP.elf Image`) for the HW IP called **EPSS IP**
- This IP is for the power and performance of `ARM Core Running Linux` on it

### why do we have a pre-silicon phase?
- Because here we can not achieve something like a performance limit or power consumption limit then we can change the entire design in RTL which is nothing but SW code
- In Post-silicon, if we want to change something then we need to manufacture the entire board again which is a very costly process

### what our team is used to do before 2019?
- Architecture Investigating
  + What will be the size of Virtual Memory?
  + Feature of ARM CPU
  + Arm Core Enhancement

### what we do in ARM architecture?
- We deliver 2 images that runs in ARM cores
   + Sysini ( SYStem Initialization library)
   + CacheDump
- We also have protocol stack which is having ATF but not  deliverable
- SCP `-----}` deliverable `-------}` RISC-V





