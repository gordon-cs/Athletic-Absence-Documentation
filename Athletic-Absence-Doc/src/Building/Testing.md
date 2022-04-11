# Testing

## Running Tests
-  Make sure the backend is running before running your unit tests.
- Open up a new terminal window and `cd repoPath/API/api-core/Tests`
- Make sure python is installed if not install it [here](https://www.python.org/downloads/)
- To install pytest, run `pip install pytest` or `python -m pip install pytest` or `py -m pip install pytest`.
- Change the fromEmail in test_emails.py to your Gordon email and the password to your Gordon password.
- To run the tests, run `pytest` or `python -m pytest` or `py -m pytest`
- If you get an SSLError when running the tests, comment out line 7 in pytest_components.py where it says `return requests.get(fullUrl)` and line 13 where it says `return requests.post(fullUrl, data = data, headers = {'Content-Type': 'application/json'})` and uncomment line 9 where it says `return requests.get(fullUrl, verify=False)` and line 15 where it says `return requests.post(fullUrl, data = data, headers = {'Content-Type': 'application/json'}, verify=False)` and run the tests again
