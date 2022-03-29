# Testing

## Running Tests
-  Make sure the backend is running before running your unit tests.
- Open up a new terminal window and `cd repoPath/API/api-core/Tests`
- Make sure python is installed if not install it [here](https://www.python.org/downloads/)
- To install pytest, run `pip install pytest` or `python -m pip install pytest` or `py -m pip install pytest`.
- Change the from_email and username in EmailClient.cs to your Gordon email and the password to your Gordon password.
- To run the tests, run `pytest` or `python -m pytest` or `py -m pytest`
- If you get an SSLError when running the tests, comment out line 7 in pytest_components.py where it says `return requests.get(fullUrl)` and uncomment line 9 where it says `return requests.get(fullUrl, verify=False)` and run the tests again
