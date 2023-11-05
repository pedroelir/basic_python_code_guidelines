# Setting Up Black and Pylint in PyCharm

1. **Install Python:**
   - Download and install Python from the [official website](https://www.python.org/downloads/).

2. **Install PyCharm:**
   - Download and install PyCharm from the [official website](https://www.jetbrains.com/pycharm/download/).

3. **Open Your Project in PyCharm:**
   - Open your Python project in PyCharm.

4. **Create a Virtual Environment:**
   - Set up a Python virtual environment for your project within PyCharm. You can do this by going to `File` > `Settings` (or `PyCharm` > `Preferences` on macOS) and then selecting `Python Interpreter`. Click the gear icon and choose "Add...". Create a new virtual environment for your project.

5. **Install Black and Pylint:**
   - Activate your virtual environment in the terminal within PyCharm. You can use the terminal located at the bottom of the PyCharm window.
   - Install Black and Pylint using pip:
     ```shell
     pip install black pylint
     ```

6. **Configure Black with Line Length 120 in PyCharm:**
   - In PyCharm, go to `File` > `Settings`.
   - Under `Tools`, select `Black`, and in the `Use Black Formatter:` section, make sure To check "On code reformat" and optionally "On save" checkboxes.
   - In the **Settings:** field, add `--line-length=120`.
   - Click "OK" to save the changes.

7. **Configure Pylint with Line Length 120 in PyCharm:**
   - In the same `Settings` window, under `Tools`, select `External Tools`, click the `+` button to add a new tool.
   - Add the fill the following field as follow:
      - **Name:** `Pylint`
      - **Pogram:** `$PyInterpreterDirectory$\pylint`
      - **Arguments:** `$FilePath$ --max-line-length=120`
      - **Working directory:** `$ProjectFileDir$`
   - Click "OK" to save the changes.

8. **Apply Changes and Restart:**
   - Click "Apply" and then "OK" to save the settings.
   - Restart PyCharm to ensure the changes take effect.