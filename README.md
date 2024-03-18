### Installing Mediapipe using Python Environment

If you encounter an error while trying to install Mediapipe using pip, it might be due to compatibility issues with your Python version. Mediapipe Python officially supports versions 3.7 to 3.10 on certain operating systems.

To troubleshoot installation issues, you can refer to the [Mediapipe documentation](https://mediapipe.readthedocs.io/en/latest/getting_started/troubleshooting.html#:~:text=after%20running%20pip%20install%20mediapipe,x86_64%20macOS%2010.15%2B).

### Installing Python with Pyenv

If your Python version is outside the supported range, you can try installing a compatible version. The easiest way to manage Python versions is by using Pyenv. Follow these steps to install Pyenv:

1. **Install Pyenv**:
   
   ```bash
   brew install pyenv
   ```

2. **Install Python**:

   Once Pyenv is installed, you can install a compatible Python version:

   ```bash
   pyenv install 3.7
   ```

   Replace `3.7` with the version you need.

3. **Set Python Version**:

   Set the installed Python version as the active version:

   ```bash
   pyenv global 3.7
   ```

4. **Add Python to PATH**:

   Ensure that the installed Python is added to your PATH variable. You can do this by editing your shell configuration file (`~/.bashrc`, `~/.zshrc`, etc.) and adding the following line:

   ```bash
   export PATH="/Users/shivakhatri/.pyenv/versions/3.7/bin:$PATH"
   ```

   Alternatively, you can use the following command:

   ```bash
   export PATH="$(pyenv root)/shims:$PATH"
   ```

   This will automatically include all versions managed by Pyenv in your PATH.

5. **Set Pip Alias**:(optional)

   You can create an alias for pip to point to the correct pip version associated with the installed Python version:

   ```bash
   alias pip='/Users/shivakhatri/.pyenv/versions/3.7.17/bin/pip'
   ```

   Adding this alias will ensure that when you use the `pip` command, it will use the correct version associated with Python 3.7.17.

6. **Verify Installation**:

   Verify that the correct Python version is now active:

   ```bash
   python --version
   ```

   This should display the Python version you installed with Pyenv.

7. **Install Mediapipe**:

   Now that you have the correct Python version installed and active, you can install Mediapipe using the newly aliased pip command:

   ```bash
   pip install mediapipe
   ```

By following these steps, you should now be able to install Mediapipe successfully within your Python environment managed by Pyenv, using the correct version of pip associated with Python 3.7.17.
