# VSCode Add Wayland Flags
This is a simple Ansible project to automate adding Wayland flags to Visual Studio Code's configuration. It copies the `code.desktop` file to the custom user location for desktop files and adds the flags to the `Exec` line. Usable for **official Microsoft Visual Studio Code installed via system package manager**.

## Usage

Run the playbook:

```bash
ansible-playbook main.yml
```

## Additional Setup

To ensure Visual Studio Code always runs with the Wayland flags, add the following to your `.bashrc`:



```bash
alias code='/usr/bin/code --enable-features=UseOzonePlatform --ozone-platform=wayland'
```

After editing your `.bashrc`, reload it:

```bash
source ~/.bashrc
``` 
