# DevOps_notes
Notes for self on managing software development environments


# Task: Install Docker Desctop to a custom directory on Windows system
# https://docs.docker.com/desktop/install/windows-install/#install-from-the-command-line

#Powershell command
Start-Process 'Docker Desktop Installer.exe' -Wait -ArgumentList "install -y --accept-license --installation-dir=G:\CodingEnv\Docker --backend=wsl-2 --hyper-v-default-data-root=G:\CodingEnv\Docker\wsl\disk --windows-containers-default-data-root=G:\CodingEnv\Docker\win_containers"
		
	-y flag helps to fix the stale install prompt step (a confirmation window with WSL-2 and desctop shortcut confirmation checkboxes will appear)

Still need to set the custom folder again in Docker Desctop Settings-> Resources-> Advanced - Disk image location

# Task: Update all the installed applications in Powershell in a batch, keeping interactions to a minimum
winget update --all --include-unknown --accept-package-agreements
