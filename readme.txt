if ansible-user is missig on server:
 astra: sudo useradd -G astra-admin,astra-console -m ansible-user
        sudo pdpl-user -i 63 ansible-user
debian: sudo useradd -G sudo -m ansible-user
redhat: sudo useradd -G wheel -m ansible-user
	sudo mkdir /home/ansible-user/.ssh
	<copy open ssh-key (authorized_keys) in dir /home/ansible-user/.ssh>
	sudo cp authorized_keys /home/ansible-user/.ssh/
	sudo chmod 644 /home/ansible-user/.ssh/authorized_keys
	sudo chown ansible-user:ansible-user /home/ansible-user/.ssh/authorized_keys
	sudo chmod 700 /home/ansible-user/.ssh
        sudo chown ansible-user:ansible-user /home/ansible-user/.ssh
	<add line in sudoers>:
				ansible-user ALL=(ALL) NOPASSWD:ALL
