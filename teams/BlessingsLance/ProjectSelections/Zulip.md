# Zulip Developer Environment Setup

> The Zulip development environment can be installed on macOS, Windows, and Linux. 
> For first time contributors, they recommend giving the Zulip development environment its own virtual machine.

## Prerequisites

- **WSL** - For direct evironment installation on your windows machine.
- **Vagrant** - Recommended for first time contributors, makes uninstallation of the environment easy
- **RAM** -- You will need atleast 2 GB of available RAM 
- **Git** — With submodule support

---

## 1. Install Prerequisites

>  There is a step by step guide on how to install Git, setup a GitHub account and create a SSH key to access your codeon GitHub efficiently.
> https://zulip.readthedocs.io/en/latest/git/setup.html 
> Zulip’s development environment is most easily set up on Windows using the Windows Subsystem for Linux.
> Enable virtualization through your BIOS settings.

> Launch the Ubuntu shell as an administrator and run the following command:

```bash
sudo apt update && sudo apt upgrade
```

> Install the dependencies:

```bash
sudo apt install rabbitmq-server memcached redis-server postgresql
```
> Open  /etc/rabbitmq/rabbitmq-env.conf using: 

```bash
sudo nano /etc/rabbitmq/rabbitmq-env.conf
```
> Confirm the following lines at the end of your file, if not add them:

```
NODE_IP_ADDRESS=127.0.0.1
NODE_PORT=5672
```
> Download Docker for Desktop at: https://www.docker.com/

## 2. Get Zulip Code

> In your browser, visit https://github.com/zulip/zulip and click the Fork button. You will need to be logged in to GitHub to do this.
> Open Terminal or Git BASH and clone your fork and connect Zulip upstream repo:

```bash
git clone --config pull.rebase git@github.com:YOURUSERNAME/zulip.git
cd zulip
git remote add -f upstream https://github.com/zulip/zulip.git
```
> Replace "YOURUSERNAME" with your actual Git username

> Should look something like this:
```
git clone --config pull.rebase git@github.com:YOURUSERNAME/zulip.git
Cloning into 'zulip'...
remote: Counting objects: 73571, done.
remote: Compressing objects: 100% (2/2), done.
remote: Total 73571 (delta 1), reused 0 (delta 0), pack-reused 73569
Receiving objects: 100% (73571/73571), 105.30 MiB | 6.46 MiB/s, done.
Resolving deltas: 100% (51448/51448), done.
Checking connectivity... done.
Checking out files: 100% (1912/1912), done.
```

## 3. Start  the  Development Environment

> Run the following to install the Zulip development environment and start it.

```bash
# Install/update the Zulip development environment
./tools/provision
# Enter the Zulip Python environment
source .venv/bin/activate
# Start the development server
./tools/run-dev
```
> 

If you are facing problems or you see error messages after running **./tools/run-dev**, you can try running **./tools/provision** again.


## 4. Developing

> You’ll work by editing files on your host machine, in the directory where you cloned Zulip. Use your favorite editor (Sublime, Atom, Vim, Emacs, Notepad++, etc.).
> When you save changes they will be synced automatically to the Zulip development environment on the virtual machine/container.

### VSCode setup (Optional)

The Visual Studio Code Remote - WSL extension  **(https://code.visualstudio.com/docs/remote/wsl-tutorial)** is recommended for editing files when developing with WSL. When you have it installed, you can run:


```bash
code .
```
> It’s good to have the terminal running **./tools/run-dev** up as you work since error messages including tracebacks along with every backend request will be printed there. 

### Rebuilding the development environment ###

> If you ever want to recreate your development environment again from scratch, You can follow these steps:

> a. To find the distribution name to unregister (delete), open Command Prompt or PowerShell and use the following command:

```bash
wsl --list --verbose
```
> b. If you are unsure about which distribution to unregister, you can log into the WSL distributions to ensure you are deleting the one containing your development environment using the command:

```bash
wsl -d <Distribution Name> ##e.g. Ubuntu 
```
> c.To uninstall your WSL distribution, enter the command:

```bash
wsl --unregister <Distribution Name>
```

> **Next, follow the setup instructions,** starting from [Step 1: Install prerequisites]
>If you just want to rebuild the development database, the following is much faster:

```bash
./tools/rebuild-dev-database
```
## 5. Shutting down the development environment for use later

> On Windows with WSL 2, you do not need to shut down the environment. Simply close your terminal window(s).
> Alternatively, you can use a command to terminate/shutdown your WSL2 environment with PowerShell using:

```bash
wsl --terminate <environment_name>
```
### Resuming the development environment ###

> On Windows with WSL 2, to resume developing you just need to open a new Git BASH window. Then change into your zulip folder and verify the Python environment was properly activated (you should see (zulip-server)). If the (zulip-server) part is missing, run:

```bash
source .venv/bin/activate
```
---
