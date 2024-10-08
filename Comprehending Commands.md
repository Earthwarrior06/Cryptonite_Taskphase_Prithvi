

hacker@commands~cat-not-the-pet-but-the-command:~$ cat flag
pwn.college{M3f0T9AxsmP23RuPwPtaz3mS6-T.dFzN1QDL5cDO0czW}

hacker@commands~catting-absolute-paths:~$ cat /flag
pwn.college{s9wuB6YgNppY_LjRHzJN92tl_Hm.dlTM5QDL5cDO0czW}

You cannot use the 'cd' command in this level, and must retrieve the flag by
absolute path. Plus, I hid the flag in a different directory! You can find it
in the file /usr/include/uuid/flag. Go cat it out **without** cding into that
directory!
hacker@commands~more-catting-practice:~$ cat /usr/include/uuid/flag
pwn.college{MjFm_P77fiNedz5-b3fRfWQ_nUG.dBjM5QDL5cDO0czW}

hacker@commands~grepping-for-a-needle-in-a-haystack:~$ grep pwn.college /challenge/data.txt
pwn.college{YakTBd-HbBSkcQtdYAECBE30ERM.ddTM4QDL5cDO0czW}

hacker@commands~listing-files:~$ ls /challenge
7289-renamed-run-20559  DESCRIPTION.md
hacker@commands~listing-files:~$ /challenge/7289-renamed-run-20559
Yahaha, you found me! Here is your flag:
pwn.college{olIdYPm9UHRPZG8X-o7N_3lA_3w.dhjM4QDL5cDO0czW}

hacker@commands~touching-files:~$ cd /tmp
hacker@commands~touching-files:/tmp$ touch pwn
hacker@commands~touching-files:/tmp$ touch college
hacker@commands~touching-files:/tmp$ /challenge/run
Success! Here is your flag:
pwn.college{kAJ2xB0AB2V_Mk3-z8TBryHnWY7.dBzM4QDL5cDO0czW}

hacker@commands~removing-files:~$ touch delete_me
hacker@commands~removing-files:~$ rm delete_me
hacker@commands~removing-files:~$ /challenge/check
Excellent removal. Here is your reward:
pwn.college{sHsJpV2YUzylTySYNFhXiOr0M2O.dZTOwUDL5cDO0czW}

hacker@commands~hidden-files:~$ cd /
hacker@commands~hidden-files:/$ ls -a
.   .dockerenv            bin   challenge  etc   lib    lib64   media  nix  proc  run   srv  tmp  var
..  .flag-22190235328083  boot  dev        home  lib32  libx32  mnt    opt  root  sbin  sys  usr
hacker@commands~hidden-files:/$ cat /.flag-22190235328083
pwn.college{U7hBVIO9G_RrwrkHy3T_q_PkjPK.dBTN4QDL5cDO0czW}

hacker@commands~an-epic-filesystem-quest:~$ cd /
hacker@commands~an-epic-filesystem-quest:/$ ls -a
.   .dockerenv  bin   challenge  etc   home  lib32  libx32  mnt  opt   root  sbin  sys  usr
..  README      boot  dev        flag  lib   lib64  media   nix  proc  run   srv   tmp  var
hacker@commands~an-epic-filesystem-quest:/$ cat /README
Yahaha, you found me!
The next clue is in: /usr/share/help/eu
hacker@commands~an-epic-filesystem-quest:/$ cd /usr/share/help/eu
hacker@commands~an-epic-filesystem-quest:/usr/share/help/eu$ ls -a
.  ..  REVELATION  gedit
hacker@commands~an-epic-filesystem-quest:/usr/share/help/eu$ cat REVELATION
Tubular find!
The next clue is in: /opt/linux/linux-5.4/Documentation/devicetree/bindings/pwm

Watch out! The next clue is **trapped**. You'll need to read it out without 'cd'ing into the directory; otherwise, the clue will self destruct!
hacker@commands~an-epic-filesystem-quest:/usr/share/help/eu$ ls /opt/linux/linux-5.4/Documentation/devicetree/bindings/pwm
CUE-TRAPPED                   img-pwm.txt             pwm-fsl-ftm.txt       pwm-sprd.txt      renesas,pwm-rcar.txt
allwinner,sun4i-a10-pwm.yaml  imx-pwm.txt             pwm-hibvt.txt         pwm-st.txt        renesas,tpu-pwm.txt
atmel-hlcdc-pwm.txt           imx-tpm-pwm.txt         pwm-lp3943.txt        pwm-stm32-lp.txt  spear-pwm.txt
atmel-pwm.txt                 lpc1850-sct-pwm.txt     pwm-mediatek.txt      pwm-stm32.txt     st,stmpe-pwm.txt
atmel-tcb-pwm.txt             lpc32xx-pwm.txt         pwm-meson.txt         pwm-tiecap.txt    ti,twl-pwm.txt
brcm,bcm7038-pwm.txt          mxs-pwm.txt             pwm-mtk-disp.txt      pwm-tiehrpwm.txt  ti,twl-pwmled.txt
brcm,iproc-pwm.txt            nvidia,tegra20-pwm.txt  pwm-omap-dmtimer.txt  pwm-tipwmss.txt   vt8500-pwm.txt
brcm,kona-pwm.txt             nxp,pca9685-pwm.txt     pwm-rockchip.txt      pwm-zx.txt
cirrus,clps711x-pwm.txt       pwm-bcm2835.txt         pwm-samsung.txt       pwm.txt
google,cros-ec-pwm.txt        pwm-berlin.txt          pwm-sifive.txt        pxa-pwm.txt
hacker@commands~an-epic-filesystem-quest:/usr/share/help/eu$ cat CUE-TRAPPED
cat: CUE-TRAPPED: No such file or directory
hacker@commands~an-epic-filesystem-quest:/usr/share/help/eu$ cat /opt/linux/linux-5.4/Documentation/devicetree/bindings/pwm/CUE-TRAPPED
Yahaha, you found me!
The next clue is in: /usr/share/racket/collects/syntax/private

The next clue is **hidden** --- its filename starts with a '.' character. You'll need to look for it using special options to 'ls'.
hacker@commands~an-epic-filesystem-quest:/usr/share/help/eu$ cd /usr/share/racket/collects/syntax/private
hacker@commands~an-epic-filesystem-quest:/usr/share/racket/collects/syntax/private$ ls -a
.   .MEMO         compiled      id-set.rkt    keyword.rkt        modcollapse-noctc.rkt  modresolve-noctc.rkt  util
..  boundmap.rkt  doctable.rkt  id-table.rkt  modcode-noctc.rkt  modhelp.rkt            template-runtime.rkt
hacker@commands~an-epic-filesystem-quest:/usr/share/racket/collects/syntax/private$ cat .MEMO
Congratulations, you found the clue!
The next clue is in: /opt/aflplusplus/frida_mode/src/lib

Watch out! The next clue is **trapped**. You'll need to read it out without 'cd'ing into the directory; otherwise, the clue will self destruct!
hacker@commands~an-epic-filesystem-quest:/usr/share/racket/collects/syntax/private$ ls /opt/aflplusplus/frida_mode/src/lib
EVIDENCE-TRAPPED  lib.c  lib_apple.c
hacker@commands~an-epic-filesystem-quest:/usr/share/racket/collects/syntax/private$ cat /opt/aflplusplus/frida_mode/src/lib/EVIDENCE-TRAPPED
Tubular find!
The next clue is in: /usr/share/doc/ruby-xmlrpc

The next clue is **delayed** --- it will not become readable until you enter the directory with 'cd'.
hacker@commands~an-epic-filesystem-quest:/usr/share/racket/collects/syntax/private$ cd /usr/share/doc/ruby-xmlrpc
hacker@commands~an-epic-filesystem-quest:/usr/share/doc/ruby-xmlrpc$ ls -a
.  ..  README.md  TEASER  changelog.Debian.gz  copyright
hacker@commands~an-epic-filesystem-quest:/usr/share/doc/ruby-xmlrpc$ cat TEASER
Congratulations, you found the clue!
The next clue is in: /usr/share/javascript/mathjax/unpacked/jax/output/SVG/fonts/STIX-Web/Latin/Regular

The next clue is **delayed** --- it will not become readable until you enter the directory with 'cd'.
hacker@commands~an-epic-filesystem-quest:/usr/share/doc/ruby-xmlrpc$ cd /usr/share/javascript/mathjax/unpacked/jax/output/SVG/fonts/STIX-Web/Latin/Regular
hacker@commands~an-epic-filesystem-quest:/usr/share/javascript/mathjax/unpacked/jax/output/SVG/fonts/STIX-Web/Latin/Regular$ ls -a
.  ..  INSIGHT  Main.js
hacker@commands~an-epic-filesystem-quest:/usr/share/javascript/mathjax/unpacked/jax/output/SVG/fonts/STIX-Web/Latin/Regular$ cat INSIGHT
Tubular find!
The next clue is in: /opt/linux/linux-5.4/include/dt-bindings/clk

The next clue is **delayed** --- it will not become readable until you enter the directory with 'cd'.
hacker@commands~an-epic-filesystem-quest:/usr/share/javascript/mathjax/unpacked/jax/output/SVG/fonts/STIX-Web/Latin/Regular$ cd /opt/linux/linux-5.4/include/dt-bindings/clk
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/include/dt-bindings/clk$ ls
NOTE  lochnagar.h  ti-dra7-atl.h
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/include/dt-bindings/clk$ cat NOTE
Lucky listing!
The next clue is in: /opt/linux/linux-5.4/arch/microblaze/include/asm

The next clue is **delayed** --- it will not become readable until you enter the directory with 'cd'.
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/include/dt-bindings/clk$ cd /opt/linux/linux-5.4/arch/microblaze/include/asm
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/arch/microblaze/include/asm$ ls
Kbuild         checksum.h  elf.h         hash.h      mmu.h             pgalloc.h    sections.h     tlb.h
TRACE          cmpxchg.h   entry.h       highmem.h   mmu_context.h     pgtable.h    setup.h        tlbflush.h
asm-compat.h   cpuinfo.h   exceptions.h  hw_irq.h    mmu_context_mm.h  processor.h  string.h       uaccess.h
asm-offsets.h  cputable.h  fixmap.h      io.h        module.h          ptrace.h     switch_to.h    unaligned.h
atomic.h       current.h   flat.h        irq.h       page.h            pvr.h        syscall.h      unistd.h
cache.h        delay.h     ftrace.h      irqflags.h  pci-bridge.h      registers.h  thread_info.h  unwind.h
cacheflush.h   dma.h       futex.h       kgdb.h      pci.h             seccomp.h    timex.h        user.h
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/arch/microblaze/include/asm$ cat TRACE
CONGRATULATIONS! Your perserverence has paid off, and you have found the flag!
It is: pwn.college{8dklioX5O2dWPqNkcu_mBTlR4VE.dljM4QDL5cDO0czW}

hacker@commands~making-directories:~$ cd /tmp
hacker@commands~making-directories:/tmp$ mkdir pwn
hacker@commands~making-directories:/tmp$ ls
bin  hsperfdata_root  pwn  tmp.XvrUsDZh8M
hacker@commands~making-directories:/tmp$ cd pwn
hacker@commands~making-directories:/tmp/pwn$ touch my_file
hacker@commands~making-directories:/tmp/pwn$ /challenge/run
Uh oh! /tmp/pwn/college does not exist. Please use the 'touch' command to
create it!
hacker@commands~making-directories:/tmp/pwn$ cd ~
hacker@commands~making-directories:~$ /challenge/run
Uh oh! /tmp/pwn/college does not exist. Please use the 'touch' command to
create it!
hacker@commands~making-directories:~$ cd /tmp
hacker@commands~making-directories:/tmp$ cd pwn
hacker@commands~making-directories:/tmp/pwn$ touch college
hacker@commands~making-directories:/tmp/pwn$ /challenge/run
Success! Here is your flag:
pwn.college{4yCsrpfCUa_H0RjOE_FxksfJNoH.dFzM4QDL5cDO0czW}

