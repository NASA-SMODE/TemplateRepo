# Template for repositories in the S-MODE organization

Here you will find a template with the directory structure that we recommend following when creating repositories in the S-MODE organization. Following this structure is by no means mandatory, but it will help your repository conform with current best practices in scientific computing and it will facilitate collaboration between science team members. The overall idea for this structure draws from [Wilson et al. (2017)](https://doi.org/10.1371/journal.pcbi.1005510) and [@jbusecke](https://github.com/jbusecke)'s [cookiecutter-science-project](https://github.com/jbusecke/cookiecutter-science-project). 

For each project, we recommend creating a repository with the following structure:

```
├── ProjectName
│   ├── README.md
│   ├── .gitignore
│   ├── *environment.yml
│   ├── code/
│   ├── data/
│   │   └── subfolder1/
│   │   └── subfolder2/
│   └── figs/
```
This structure could be applied to any project, regardless of the main program language being used.

*If you are working in Python, we recommend that you use [conda environments](https://docs.conda.io/projects/conda/en/latest/user-guide/concepts/environments.html) and that you add an ```environement.yml``` to your repository. Among other things, working with environments allows you to share your environment so other people can run your code on their machines using the exact same packages as you. More information about how to create and share environments can be found [here](https://docs.conda.io/projects/conda/en/latest/user-guide/tasks/manage-environments.html).

Note that the data folder is part of the directory structure but it is not advised to version-control and push data to GitHub unless it's plain text files (e.g., Markdown, csv, txt). If you keep all data used in your analysis in the data folder/subfolders and use relative paths in your code, for example:

```
data = np.loadtxt('../data/oceanus/ctd_000.csv')
```

It becomes straightforward for a collaborator to clone your repository and run your code without having to adjust any paths. 
