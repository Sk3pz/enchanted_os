# EnchantedOS
EnchantedOS is an operating system using the Rust programming language with speed and security in mind. This project's design goal is to bring a new, lightweight OS that doesn't get in the way of your daily tasks.

Building and Running:

Current Versions:

1.) Ensure QEMU is installed:
    - download from https://www.qemu.org/ and install
    - ensure qemu is added to path

2.) Installing BootImage: (must be run outside of the project directory due to our forced target)
    - run the command `rustup component add llvm-tools-preview`
    - install bootimage with `cargo install bootimage` 

3.) Set the rust toolchain version to nightly to gain access to important features
    - run the command `rustup override add nightly` or `rustup override set nightly` 
      if already installed.
        (can be set back to stable with `rustup override set stable`)

4.) install the rust source so the kernel can recompile parts it uses with 
    `rustup component add rust-src` 
    (must be run inside the project directory)

5.) run with `cargo run` and build with `cargo build` as normal.

----------------
 
In Process:

 - Simple File System
 - Custom Bootloader
 - VGA Graphics mode interface

TODO:
 - command processing
 - built-in assembler
 - built-in c compiler (possibly LLVM?)
 - application running (make / run applications on the os, currently all processes are just the kernel)
 - ext4 and NTFS file systems
 - better memory management
 - Support for .exe file execution
 - ABI
 - Operating System:
   * Drivers
   * Scheduler
   * etc
