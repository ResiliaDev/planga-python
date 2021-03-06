Planga Python Wrapper:
======================

[![Planga](https://img.shields.io/badge/%F0%9F%98%8E%20planga-chat-ff00ff.svg)](http://www.planga.io/)
[![Planga Docs](https://img.shields.io/badge/planga-docs-lightgrey.svg)](http://www.planga.io/docs)

[![PyPI](https://img.shields.io/pypi/v/planga.svg)](https://pypi.org/project/planga/)
=![PyPI - Python Version](https://img.shields.io/pypi/pyversions/planga.svg)](https://pypi.org/project/planga/)



**Example usage:**


```python
from planga import *

conf = PlangaConfiguration(
        public_api_id="foobar",
        private_api_key="ePxoM3OTkW1z6j84JDurqw",
        conversation_id="general",
        current_user_id="1234",
        current_user_name="Bob",
        container_id="my_container_div"
    )

snippet = Planga.get_planga_snippet(conf)
```


**Setup:**


* Install Twine: `pip install twine`


**Requirements:**


* [Python](https://www.python.org/) >= 2.7.x.
* [pip](http://www.pip-installer.org)
* virtualenv (Optional)


**Build and Deploy new package:**


* run `python3 setup.py sdist bdist_wheel`
* run `twine upload --repository-url https://test.pypi.org/legacy/ dist/* --skip-existing`


**Installing the new package:**


* run `python -m pip install jwcrypto`
* run `python -m pip install --index-url https://test.pypi.org/simple/ planga`

Installing jwcrypto manually is only necessary when uploading the planga wrapper to test.pypi.org. The installation tool will attempt to install jwcrypto from test.pypi.org as well, which fails. Having jwcrypto pre-installed allows the installation of the planga wrapper to finish successfully.

**Deploy to live Pypi:**

* run `twine upload dist/* --skip-existing`

For information on how to package for PiPy:
[https://packaging.python.org/tutorials/packaging-projects/](https://packaging.python.org/tutorials/packaging-projects/)
