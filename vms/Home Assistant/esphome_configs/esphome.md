## Install

See [Manual Installation Guide](https://esphome.io/guides/installing_esphome.html) To install on dev system or use built in ESPHome WebUI builder (not tested)

## ESPHome venv Setup Guide for Windows

This guide walks you through creating and activating a Python virtual environment (venv) for ESPHome on Windows.

### Prerequisites

- Windows 10 or 11
- Python 3.8 or later installed and added to your PATH
- (Optional) Git installed for cloning repositories

### Steps

1. **Open PowerShell or Command Prompt as Administrator**  
   Press `Win + X`, then choose **Windows PowerShell (Admin)** or **Command Prompt (Admin)**.

2. **Verify Python Installation**  
   ```powershell
   python --version
   ```  
   Ensure the output shows at least Python 3.8.

3. **Navigate to Your Workspace Directory**  
   Choose or create a directory for your ESPHome projects:
   ```powershell
   mkdir %USERPROFILE%\esphome
   cd %USERPROFILE%\esphome
   ```

4. **Create the Virtual Environment**  
   ```powershell
   python -m venv esphome-env
   ```

5. **Activate the Virtual Environment**  
   ```powershell
   .\esphome-env\Scripts\Activate.ps1
   ```  
   - If you encounter an execution policy error, run:
     ```powershell
     Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope CurrentUser
     ```
     and then re-activate.

6. **Upgrade pip**  
   ```powershell
   pip install --upgrade pip
   ```

7. **Install ESPHome**  
   ```powershell
   pip install esphome
   ```

8. **Verify ESPHome Installation**  
   ```powershell
   esphome version
   ```  
   You should see the installed ESPHome version.

9. **Initialize a New ESPHome Project**  
   ```powershell
   esphome mydevice.yaml wizard
   ```

10. **Run the ESPHome Dashboard**  
    ```powershell
    esphome dashboard .
    ```  
    Then open [http://localhost:6052](http://localhost:6052) in your browser.

## Tips

- To deactivate the venv:  
  ```powershell
  deactivate
  ```
- To reactivate later, navigate to your workspace and run the activation command again.

---

*End of Guide.*

## ESPHome Commands

- Compile: ```esphome compile config.yaml --device COM<number>```
- Compile & Flash: ```esphome run config.yaml --device COM<number>```

**Ensure Driver's are Installed for the respective board!**