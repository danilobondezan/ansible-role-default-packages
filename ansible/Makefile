#Default Variables
hosts ?= None

# Setup ansible in a python virtual environment
.PHONY: venv
venv:
		pip3 install virtualenv
		virtualenv .default-packages
		. .default-packages/bin/activate && \
		pip install --upgrade -r requirements.txt

.PHONY: setup
setup:
	git submodule update --init --recursive

# Default Packages
.PHONY: default-packages
default-packages: setup
	ansible-playbook default-packages.yml \
	-e "hosts=$(hosts)" \
	$(custom-args)
