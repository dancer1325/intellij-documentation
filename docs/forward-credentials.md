[//]: # (Source: https://www.jetbrains.com/help/idea/forward-credentials.html)
[//]: # (Downloaded: 2025-12-17 19:27:17)

# Sharing credentials

When building a Dev Container on a remote server, accessing a remote server and cloning a project require authentication. The supported method of authentication is through SSH keys or a password.

If you have password authentication, refer to the following procedure on how to generate a file with the SSH keys, forward it a remote server, and share your Git credentials.

### Create and forward the SSH keys

  1. Open the local terminal and generate the SSH keys with the following command:

ssh-keygen

For more information on SSH keys, refer to the [SSH](https://www.ssh.com/academy/ssh/agent) documentation.

System generates the key-pair. By default, it will be stored in your `~/.ssh/` folder where `~` is your home directory. The public key will be stored in the same location as the private key. It starts with the same name as the private key and have a `.pub` suffix. For example, `id_rsa` and `id_rsa.pub`. If you need, you can change the key-pair location.

As a result, you have the SSH key-pair file on your local machine.

  2. After the key-pair is generated, install the keys on a remote server with the following command:

ssh-copy-id your_remote_server_name

The keys are added to the remote server, and you can build a Dev Container. For more information, refer to [SSH documentation](https://www.ssh.com/academy/ssh/copy-id#copy-the-key-to-a-server).

  3. Connect to a remote server and clone a project into a Dev Container. 

![Adding New Dev Container](https://resources.jetbrains.com/help/img/idea/2025.3/remote_server_dev_container.png)

For more detailed information, refer to [Dev Container overview](connect-to-devcontainer.html).

  4. Make sure you are authenticated on GitHub. You can either use the [SSH agent forwarding](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/using-ssh-agent-forwarding#setting-up-ssh-agent-forwarding) or log in to your GitHub account. 

![Git login](https://resources.jetbrains.com/help/img/idea/2025.3/github_login_dev_container.png)
  5. After the Dev Container environment is prepared, click Continue to open a project. 

![Environment prepared](https://resources.jetbrains.com/help/img/idea/2025.3/cloning_to_dev_container.png)



01 May 2025

[Limitations](dev-container-limitations.html)[Using SSH keys](using-ssh-keys.html)
