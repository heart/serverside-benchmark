
# Computer Spec
- AMD Ryzen 5 1400 Quad-Core Processor 3.60 GHz.
- 16 GB of RAM
- Windows 10 Pro 64 bit

# Software Versions
- php-7.4
- Node v14.15.0
- Swoole 4.5.6


Disable hyper-v (which will required a couple of restarts)
dism.exe /Online /Disable-Feature:Microsoft-Hyper-V

When you finish all the required restarts, reserve the port you want so hyper-v doesn't reserve it back
netsh int ipv4 add excludedportrange protocol=tcp startport=50051 numberofports=1

Re-Enable hyper-V (which will require a couple of restart)
dism.exe /Online /Enable-Feature:Microsoft-Hyper-V /All