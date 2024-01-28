# car-Price-Predictions
check project: https://stvy-predict-your-car-price.herokuapp.com/

# Installation - Linux
Set up a virtual environment:

# Create a virtual environment
python3 -m venv venv
Set up a virtual environment:

# Activate the virtual environment
source venv/bin/activate
Install dependencies:

pip install -r requirements.txt


# Installation - Windows

To set up and activate a virtual environment for Python on Windows, you can use the following steps:

Step 1: Install virtualenv (if not already installed):
Open a command prompt and run the following command:

pip install virtualenv
Step 2: Create a virtual environment:
Choose or create a directory for your project. Open a command prompt in that directory and run:

python -m venv venv
Replace venv with the desired name for your virtual environment.

Step 3: Activate the virtual environment:
Navigate to the directory of your project using the command prompt. Then, use the following command to activate the virtual environment:

venv\Scripts\activate
You should see the prompt change to indicate that the virtual environment is now active.

Step 4: Install packages within the virtual environment:
With the virtual environment active, you can use pip to install Python packages, and they will be isolated within the virtual environment. For example:

pip install package_name
Step 5: Deactivate the virtual environment:
When you're done working in the virtual environment, you can deactivate it using the following command:

deactivate
This will return you to the global Python environment.

Remember to activate the virtual environment every time you work on your project. If you use a different command prompt, you'll need to activate the virtual environment in that new instance.

These steps should help you set up and work within a virtual environment on Windows.

# If you get UnauthorizedAccess Access on Step 3

venv\Scripts\activate

venv\Scripts\activate : File E:\Python Projects\car-Price-Predictions\venv\Scripts\Activate.ps1 cannot be loaded
because running scripts is disabled on this system. For more information, see about_Execution_Policies at
https:/go.microsoft.com/fwlink/?LinkID=135170.
At line:1 char:1
+ venv\Scripts\activate
+ ~~~~~~~~~~~~~~~~~~~~~
    + CategoryInfo          : SecurityError: (:) [], PSSecurityException
    + FullyQualifiedErrorId : UnauthorizedAccess

The error you're encountering is related to PowerShell script execution policies. By default, PowerShell restricts running scripts to enhance security. You can modify the execution policy to allow running scripts. Here's how you can change it:

Open a PowerShell session with administrative privileges. Right-click on the PowerShell icon and choose "Run as Administrator."

Check the current execution policy:

Get-ExecutionPolicy
If the output is Restricted, you need to change the policy. To change it to RemoteSigned (which allows local scripts but requires downloaded scripts to be signed), run the following command:

Set-ExecutionPolicy RemoteSigned
Confirm the change by entering Y and pressing Enter.

Try activating your virtual environment again:

.\venv\Scripts\Activate
This should resolve the issue. Keep in mind that changing the execution policy can introduce security risks, so make sure you understand the implications and only run scripts from trusted sources.

If you encounter issues, you can revert the execution policy to its original state after you're done working in your virtual environment:

powershell
Copy code
Set-ExecutionPolicy Restricted
Remember to run this command with administrative privileges as well.
