# Linux for DevOps: 5-Day Learning Guide

## What is Linux?
- Linux is an operating system kernel created by Linus Torvalds in 1991.
- A complete Linux system usually includes the Linux kernel plus GNU tools, libraries, and applications.
- When people say “Linux,” they often mean a distribution such as Ubuntu, CentOS, Debian, Fedora, or Alpine.

## What is an operating system?
- An operating system (OS) is software that manages hardware, runs applications, and provides services to users and programs.
- It handles process scheduling, memory management, device I/O, file systems, and security.
- Examples: Linux, Windows, macOS, FreeBSD.

## What is the Linux kernel?
- The Linux kernel is the core part of the operating system.
- It controls hardware, manages processes, handles memory, and provides system calls to applications.
- The kernel runs in privileged mode and isolates hardware from user programs.

## What is a shell?
- The shell is a command interpreter in user space, not part of the kernel.
- It accepts user commands, launches programs, and connects commands with pipes.
- Common shells: `bash`, `zsh`, `sh`, `dash`, `fish`.

## How does Linux interact with hardware?
- The kernel uses device drivers to control hardware devices.
- User programs request services through system calls like `read()`, `write()`, `open()`, `ioctl()`.
- Linux exposes hardware through device files in `/dev` and runtime information in `/proc` and `/sys`.
- The kernel schedules CPU time, manages RAM, and handles interrupts from devices.

## Why is Linux so popular?
- Open source: source code is freely available and modifiable.
- Stable and secure: used widely on servers, cloud, containers, and embedded systems.
- Performance: efficient on many hardware types.
- Flexibility: many distributions and custom variants.
- Community: strong ecosystem, documentation, and support.
- Cost: most distributions are free.

## Where is Linux used?
- Servers and data centers
- Cloud computing and virtual machines
- Containers and orchestration (`Docker`, `Kubernetes`)
- Network devices and routers
- Embedded systems, IoT devices, appliances
- Desktops and laptops
- Supercomputers

## Why is Linux important for DevOps?
- Most CI/CD, automation, and cloud infrastructure run on Linux.
- Containers and orchestration platforms are Linux-based.
- DevOps tools like Ansible, Chef, Puppet, Terraform, Jenkins, GitLab Runner often run best on Linux.
- Linux provides powerful automation, scripting, and monitoring capabilities.
- Understanding Linux gives you direct control over infrastructure and pipelines.

## Basic Linux architecture
- Kernel
  - Manages hardware, memory, processes, and drivers.
  - Provides system calls to user space.
- System libraries
  - Shared libraries such as `glibc`, `libc` used by applications.
- User space
  - Shells, applications, services, and tools.
- Init/systemd
  - Starts system services and manages boot.
- File system hierarchy
  - `/` root
  - `/bin`, `/usr/bin`, `/sbin`
  - `/etc` configuration
  - `/var` variable data
  - `/home` user files
  - `/proc`, `/sys` kernel interfaces

## How to install Linux
1. Choose a distribution:
   - Ubuntu, Debian, CentOS/RHEL, Fedora, Alpine, Rocky Linux.
2. Install options:
   - Virtual machine: VirtualBox, VMware, Hyper-V.
   - WSL on Windows: `wsl --install` and choose Ubuntu.
   - Live USB: write ISO to USB with Rufus.
   - Dual boot: install alongside Windows.
3. Basic install steps:
   - Download ISO from the distribution website.
   - Create a bootable USB.
   - Boot the machine from USB.
   - Follow installer prompts: language, time zone, disk partition, user.
4. Post-install:
   - Update packages: `sudo apt update && sudo apt upgrade` or `sudo dnf update`.
   - Install essential tools: `sudo apt install git curl vim`.

## 5-Day Linux Learning Plan for DevOps Engineers

### Day 1: Linux fundamentals
- Learn what Linux is and how it is structured.
- Work with the shell: `pwd`, `ls`, `cd`, `mkdir`, `touch`, `cp`, `mv`, `rm`.
- Explore the file system: `/`, `/home`, `/etc`, `/var`, `/usr`, `/tmp`.
- Read files: `cat`, `less`, `head`, `tail`.
- Practice basic commands:
  - `echo Hello`
  - `history`
  - `man ls`
- Understand distributions and package managers.

### Day 2: Users, permissions, shell, and text editing
- Users and groups: `id`, `whoami`, `useradd`, `usermod`, `passwd`.
- File permissions:
  - `ls -l`
  - `chmod 755 file`
  - `chown user:group file`
- Learn a shell: `bash`, `history`, environment variables.
- Edit config files with `nano` or `vim`.
- Practice with scripts:
  - `#!/bin/bash`
  - `chmod +x script.sh`
  - `./script.sh`

### Day 3: Processes, services, networking, and storage
- Process management:
  - `ps aux`
  - `top` / `htop`
  - `kill`, `killall`, `pkill`
  - `nice`, `renice`
- Services and init:
  - `systemctl status nginx`
  - `systemctl start|stop|restart|enable`
- Networking basics:
  - `ip addr`
  - `ping 8.8.8.8`
  - `ss -tuln`
  - `curl https://example.com`
- Storage and disks:
  - `df -h`
  - `du -sh /home`
  - `lsblk`
- Mounting and devices: `/dev`, `/proc`, `/sys`.

### Day 4: Automation, packages, and containers
- Package management:
  - Debian/Ubuntu: `apt update`, `apt install`, `apt remove`, `apt search`
  - RHEL/CentOS: `yum`, `dnf`
- Shell scripting for automation:
  - loops, conditionals, functions.
  - `if`, `for`, `while`.
- Cron and scheduled tasks:
  - `crontab -e`
  - `0 2 * * * /usr/bin/backup.sh`
- Learn container basics:
  - `docker run hello-world`
  - `docker ps`, `docker images`
  - `kubectl get pods` (if Kubernetes installed)
- Basic infrastructure-as-code concepts with Terraform or Ansible.

### Day 5: DevOps tools and practice
- Git and source control:
  - `git clone`, `git add`, `git commit`, `git push`.
- CI/CD concepts and tools: Jenkins, GitHub Actions, GitLab CI.
- Monitoring and logging:
  - `journalctl -u ssh`
  - `dmesg | tail`
  - `tail -f /var/log/syslog`
- Security basics:
  - `ufw status`
  - `sshd` config in `/etc/ssh/sshd_config`
  - `sudo` and privilege separation.
- Practice project:
  - Deploy a Docker container.
  - Write a Bash script to install and configure a service.
  - Create a Git repo and push your automation.

## Quick Linux command list for DevOps
- Navigation: `pwd`, `cd`, `ls`, `find`
- Files: `cp`, `mv`, `rm`, `mkdir`, `chmod`, `chown`
- Text: `cat`, `grep`, `awk`, `sed`, `less`
- Processes: `ps`, `top`, `htop`, `kill`, `systemctl`
- Networking: `ip`, `ping`, `curl`, `ss`, `netstat`
- Disk: `df`, `du`, `mount`, `lsblk`
- Packages: `apt`, `dnf`, `yum`
- Containers: `docker`, `kubectl`

## Recommended next steps
- Use a Linux VM or WSL for daily practice.
- Build a small project: deploy an Nginx web app in Docker.
- Learn one configuration tool: Ansible, Terraform, or Helm.
- Read Linux man pages: `man bash`, `man systemctl`, `man sshd`.
- Keep a personal cheat sheet of commands.

## Notes for GitHub
- Copy this file into your GitHub repository as `linux-devops-5-day-guide.md`.
- Use the plan as a study tracker and update it with your own notes.
- Add links to your completed tasks and commands.

---

Happy learning! This guide covers the essential Linux knowledge you need to start as a DevOps engineer.
