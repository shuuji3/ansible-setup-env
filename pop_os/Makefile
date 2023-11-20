.PHONY: ansible setup

setup: ansible ansible-galaxy
	ansible-playbook main.yaml -K -vv

debug: ansible ansible-galaxy
	ansible-playbook debug.yaml -K -vv

ansible:
ifeq ($(shell which ansible),)
	sudo apt update && sudo apt install ansible-core
endif

ansible-galaxy: requirements.yaml
	ansible-galaxy install -r requirements.yaml
