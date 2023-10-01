.PHONY: ansible setup

setup: ansible ansible-galaxy
	ansible-playbook main.yaml -K -vvv

ansible:
ifeq ($(shell which ansible),)
	sudo apt update && sudo apt install ansible
endif

ansible-galaxy: requirements.yaml
	ansible-galaxy install -r requirements.yaml
