.PHONY: ansible setup

setup: ansible ansible-galaxy
	ansible-playbook main.yaml -K -vv

debug: ansible ansible-galaxy
	ansible-playbook debug.yaml -K -vv

ansible:
ifeq ($(shell which ansible),)
	pip install ansible-core resolvelib github3
endif

ansible-galaxy: requirements.yaml
	ansible-galaxy install -r requirements.yaml
