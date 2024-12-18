
# PCB-Tools Installation Guide for Blender Python

This guide outlines the steps to install `PCB-Tools` and its dependencies within Blender's bundled Python environment.

---

## Steps:

### 1. Locate Blender's Python Executable
1. Open Blender.
2. Go to `Scripting` tab and open the Python console.
3. Run the following command to locate Blender's Python executable:
   ```python
   import sys
   print(sys.executable)
   ```
   Example output:
   ```
   C:\Program Files\Blender Foundation\Blender 4.3\4.3\python\bin\python.exe
   ```

### 2. Clone the PCB-Tools Repository
1. Open your terminal or command prompt.
2. Clone the `PCB-Tools` repository:
   ```bash
   git clone https://github.com/curtacircuitos/pcb-tools.git
   ```
3. Navigate to the cloned repository:
   ```bash
   cd pcb-tools
   ```

### 3. Install Dependencies

!!! The package should be installed on Blender's python environment, so you can install it using the system's Python on the Blender environment path or manage path. !!!

Run the following command to install the required dependencies:
```bash
"C:\Program Files\Blender Foundation\Blender 4.3\4.3\python\bin\python.exe" -m pip install -r requirements.txt --target "C:\Program Files\Blender Foundation\Blender 4.3\4.3\python\lib\site-packages"
```

### 4. Install PCB-Tools
Run the following command to install the `PCB-Tools` package:
```bash
"C:\Program Files\Blender Foundation\Blender 4.3\4.3\python\bin\python.exe" -m pip install . --target "C:\Program Files\Blender Foundation\Blender 4.3\4.3\python\lib\site-packages"
```

---

## Verify Installation
1. Open Blender and navigate to the `Scripting` tab.
2. Open the Python console and run the following commands:
   ```python
   import cairocffi
   import gerber
   print("PCB-Tools and dependencies installed successfully!")
   ```

If there are no errors, the installation is successful.

---

## Notes:
- Ensure that the paths in the commands match your Blender installation path.
- The `--target` option explicitly installs the packages in Blender's Python site-packages directory.
- If you face issues, ensure you have sufficient permissions and run the command prompt as an administrator.

---

Enjoy using `PCB-Tools` in Blender!
