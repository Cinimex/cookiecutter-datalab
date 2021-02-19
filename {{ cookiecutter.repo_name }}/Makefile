init:
	git init && \
	conda env create -f ./environment.yml && \
	pre-commit install && \
	conda activate {{ cookiecutter.project_name }}

# activate environment
a:
	conda activate {{ cookiecutter.project_name }}

# commit
c:
	cz c && cz bump --changelog

# commit and push to master
push-master: c 
	git push --tags origin master

# commit and push to dev
p: c
	git push --tags origin develop