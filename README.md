# Welcome to Streamlit Cookies Controller 🍪

[![PyPI][pypi_badge]][pypi_link]
[![Download][pypi_download_badge]][pypi_link]
[![GitHub][github_badge]][github_link]
[![GitHub license][license_badge]][license_link]
[![GitHub issues][issue_badge]][issue_link]
[![GitHub pull requests][pull_badge]][pull_link]

Control client browser cookie for the site.

## What is Streamlit Cookie Controller?
`streamlit-cookies-controller` let you

- get cookie(s)
- set cookie
- remove cookie

from/to the client browser.
It use [universal-cookie](https://www.npmjs.com/package/universal-cookie) package to access the cookies.


## Installation
Open a terminal and run:
``` terminal
pip install streamlit-cookies-controller
```


## Quickstart
Create a new file example.py
``` python
import streamlit as st
from streamlit_cookies_controller import CookieController

st.set_page_config('Cookie QuickStart', '🍪', layout='wide')

controller = CookieController()

# Set a cookie
controller.set('cookie_name', 'testing')
st.write(st.session_state)

# Get all cookies
cookies = controller.getAll()
st.write(cookies)

# Get a cookie
cookie = controller.get('cookie_name')
st.write(cookie)

# Remove a cookie
controller.remove('cookie_name')
st.write(st.session_state)
```
Run the streamlit app
``` terminal
streamlit run example.py
```


## Change Log
### Version 0.0.1
- Initial release
### Version 0.0.2
- return None when there is no cookie with the given name instead of throw error
### Version 0.0.3
Remove `Test1` in frontend due to it is flikkering on streamlit v1.32.0


[pypi_badge]: https://img.shields.io/pypi/v/streamlit-cookies-controller.svg
[pypi_link]: https://pypi.org/project/streamlit-cookies-controller
[pypi_download_badge]: https://static.pepy.tech/badge/streamlit-cookies-controller
[github_badge]: https://badgen.net/badge/icon/GitHub?icon=github&color=black&label
[github_link]: https://github.com/NathanChen198/streamlit-cookies-controller
[license_badge]: https://img.shields.io/badge/Licence-MIT-gr.svg
[license_link]: https://github.com/NathanChen198/streamlit-cookies-controller/blob/main/LICENSE
[issue_badge]: https://img.shields.io/github/issues/NathanChen198/streamlit-cookies-controller
[issue_link]: https://github.com/NathanChen198/streamlit-cookies-controller/issues
[pull_badge]: https://img.shields.io/github/issues-pr/NathanChen198/streamlit-cookies-controller
[pull_link]: https://github.com/NathanChen198/streamlit-cookies-controller/pulls
