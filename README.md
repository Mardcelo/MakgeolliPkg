# MakgeolliPkg

Type-I Hypervisor 

1. Initialize the host state of current processor, including IDT, GDT, paging structures, to runtime memroy pool. 
2. Initilize TSS with runtime memory pool. Intel VT-x requires host environment to have present TSS. There is no such requirement in AMD-V. 
3. Load host state. For Intel VT-x, copy the state to VMCS. For AMD-V, load them directly. 
4. Load guest state. Copy the state to VMCS/VMCB. 
5. Intercept INIT-signal. Emulate the signal and halt the processor execution to wait for Statup-IPI. 
6. Intercept SIPI. Emulate the interrupt and resume processor execution. 

- [ ] [IA32 define](https://github.com/ia32-doc/ia32-doc/blob/main/out/ia32.h)
- [ ] [NoirVisor (hook implementation)](https://github.com/Zero-Tang/NoirVisor/blob/master/src/booting/efiapp/driver.c)
- [ ] [UEFI programming ](https://github.com/tianocore/tianocore.github.io/wiki/Build-Description-Files)
- [ ] [Bareflank - Small codebase](https://github.com/Bareflank/hypervisor)
- [ ] [STM - Small codebase](https://github.com/jyao1/STM)
- [ ] [hvpp - few techniques](https://github.com/wbenny/hvpp)
- [ ] [zpp_hypervisor -ref](https://github.com/eyalz800/zpp_hypervisor)
- [ ] [UEFI environment techniques](https://github.com/Mattiwatti/EfiGuard)
- [ ] [MiniVisor](https://github.com/tandasat/MiniVisorPkg)
