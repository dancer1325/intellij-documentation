[//]: # (Source: https://www.jetbrains.com/help/idea/using-ssh-keys.html)
[//]: # (Downloaded: 2025-12-17 20:05:44)

## Troubleshooting

You may receive an error on Linux and Windows since the SSH agent is not running by default on these systems. On macOS, the SSH agent is running by default.

To resolve such issues, use the following steps:

  1. Ensure that you are running your local PowerShell as an administrator.

  2. Enter the following command:

Set-Service ssh-agent -StartupType Automatic Start-Service ssh-agent Get-Service ssh-agent 




  1. Start the SSH agent with the following command:

eval "$(ssh-agent -s)" 

  2. Add the following lines to `~/.bash_profile` or `~/.zprofile` if you prefer to use the `Zsh` shell instead of `bash`.

if [ -z "$SSH_AUTH_SOCK" ]; then # Check for a currently running instance of the agent RUNNING_AGENT="`ps -ax | grep 'ssh-agent -s' | grep -v grep | wc -l | tr -d '[:space:]'`" if [ "$RUNNING_AGENT" = "0" ]; then # Launch a new instance of the agent ssh-agent -s > $HOME/.ssh/ssh-agent fi eval `cat $HOME/.ssh/ssh-agent` > /dev/null ssh-add $HOME/.ssh/<your ssh key> 2> /dev/null fi 

On the last line of the suggested code, replace <your ssh key> with your specific ssh key. For example, `ssh-add $HOME/.ssh/id_ed344 2> /dev/null`



