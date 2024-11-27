# DevOps Notes
### Notes for self on managing software development environments
====

Task: Install Docker Desktop to a custom directory on Windows system (Powershell command)
Source: https://docs.docker.com/desktop/install/windows-install/#install-from-the-command-line

	Start-Process 'Docker Desktop Installer.exe' -Wait -ArgumentList "install -y --accept-license --installation-dir=G:\CodingEnv\Docker '
 	--backend=wsl-2 --hyper-v-default-data-root=G:\{path\to\Docker\folder} --windows-containers-default-data-root={path\to\Docker\folder}"
*Still, need to set the custom folder again in Docker Desctop Settings-> Resources-> Advanced - Disk image location*

_Flag `-y` helps to fix the stale install prompt step (a confirmation window with WSL-2 and desctop shortcut confirmation checkboxes will appear)_
_Parameters have to be passed with `-ArgumentList ""` inside double quotes_
_`--backend=wsl-2` is the default option and can be skipped

---
Task: Update all the installed applications in Powershell in a batch, keeping interactions to a minimum

	winget update --all --include-unknown --accept-package-agreements
---
Task: Stop all running Docker containers

	docker stop $(docker ps -a -q)

