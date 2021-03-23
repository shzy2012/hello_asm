# 汇编入门

开发环境(macOS)
```bash
brew install gcc nasm gdb
```

macOS 编译运行
```bash
nasm -f macho64 64.asm && ld -macosx_version_min 10.7.0 -lSystem -o 64 64.o && ./64
nasm -f macho64 average.asm && gcc average.o && ./a.out
nasm -f bin boot.asm -o boot.bin

nasm -f macho64 average.asm
```

nasm
```bash
-f format     select output file format
   bin                  Flat raw binary (MS-DOS, embedded, ...) [default]
   ith                  Intel Hex encoded flat binary
   srec                 Motorola S-records encoded flat binary
   aout                 Linux a.out
   aoutb                NetBSD/FreeBSD a.out
   coff                 COFF (i386) (DJGPP, some Unix variants)
   elf32                ELF32 (i386) (Linux, most Unix variants)
   elf64                ELF64 (x86-64) (Linux, most Unix variants)
   elfx32               ELFx32 (ELF32 for x86-64) (Linux)
   as86                 as86 (bin86/dev86 toolchain)
   obj                  Intel/Microsoft OMF (MS-DOS, OS/2, Win16)
   win32                Microsoft extended COFF for Win32 (i386)
   win64                Microsoft extended COFF for Win64 (x86-64)
   ieee                 IEEE-695 (LADsoft variant) object file format
   macho32              Mach-O i386 (Mach, including MacOS X and variants)
   macho64              Mach-O x86-64 (Mach, including MacOS X and variants)
   dbg                  Trace of all info passed to output stage
   elf                  Legacy alias for "elf32"
   macho                Legacy alias for "macho32"
   win                  Legacy alias for "win32"
```

