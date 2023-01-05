# example_pkg_nsulliv3
This 'package' was created following the Python package tutorial [here](https://packaging.python.org/en/latest/tutorials/packaging-projects/).

Steps used to create the package, push to Test PyPi and then install from Test PyPi:
1. Create a repo with a README and MIT license on GitHub.
2. Clone into a databricks repo. (If not done already, make sure to add one's GitHub username and PAT in the databricks user credentials section before proceeding to the next step.)
3. Create all the necessary additional files on databricks and push to GitHub.
4. Go to the GitHub repo and open it in codespaces (which has Python installed on its engine image).
5. Once in codespaces, in the terminal run the additional commands in the terminal to pip install build, build the dist/ and push to Test PyPi (in this case).
6. Check that the package is [available on Test PyPi](https://test.pypi.org/project/example-pkg-nsulliv3/).
7. Open up a Python notebook anywhere on databricks and run: `!pip install --index-url https://test.pypi.org/simple/ --no-deps example_pkg_nsulliv3`
8. Next run: 
```
from example_pkg_nsulliv3 import example
example.add_one(2)
```

If all the steps were correctly followed, this should yield a printed output of 3.
