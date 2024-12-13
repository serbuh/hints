
C|A
-|-
pip show `<module>` | Show installed `<module>` version 
pip index versions `<module>` | Show available `<module>` version 
pip install `<module>`==`<version>` | Install `<module>` of version `<version>` 
pip unisntall `<module>` | Uninstall `<module>` 
pip list | list the available packages (venv local + system packages) 
pip list --local | list the available packages (venv local only) 
pip freeze | list all the packages (in a requirements.txt format) 
pip freeze > requirements.txt | create requirements file 
pip download -r requirements.txt -d downloads/ | Save all the requirements as a whl files to the folder 

### Install all whl in the folder [windows.bat]
```for %x in (*.whl) do python -m pip install %x```

### Troubleshoot
Problem:  
In case of `[SSL: CERTIFICATE_VERIFY_FAILED]`  
Solution:
```
python -m pip install --upgrade pip --trusted-host pypi.org --trusted-host pypi.python.org --trusted-host files.pythonhosted.org
```
