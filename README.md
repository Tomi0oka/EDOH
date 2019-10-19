# PowerShell Notebook

This PowerShell module lets you automate the PowerShell notebooks you can create in the Azure Data Studio. Check out the *SQL DBA with A Beard* [PowerShell Notebooks in Azure Data Studio](https://sqldbawithabeard.com/2019/10/17/powershell-notebooks-in-azure-data-studio/).

This module includes the function `Invoke-PowerShellNotebook` which enables you to run the *cells* inside the PowerShell notebook.

# A PowerShell Notebook with Cells

Below is a PowerShell Notebook with three cells, each containing a PowerShell "script".

![](./media/ADSPowerShellNoteBook.png)

Notice the second cell has the results of running `get-process | select company, name, handles -first 10`


# Automate the PowerShell Notebook

![](./media/InvokePowerShellNotebook.png)

# Bonus Points: Using the `-AsExcel` switch

`Invoke-PowerShellNotebook` sports an `AsExcel` switch. This lets you execute each cell in the PowerShell notebook and the function exports the results to a separate sheet in an Excel file.

![](./media/InvokePowerShellNotebookAsExcel.png)

You need to have the PowerShell `ImportExcel` module installed. The module is on the PowerShell Gallery, use `Install-Module ImportExcel` to install it on you machine.