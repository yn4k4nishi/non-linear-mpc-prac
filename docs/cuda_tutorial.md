## tutorial
```PowerShell
PS C:\Users\ynakanishi> nvidia-smi.exe
Sun Mar 14 12:59:41 2021
+-----------------------------------------------------------------------------+
| NVIDIA-SMI 470.05       Driver Version: 470.05       CUDA Version: 11.3     |
|-------------------------------+----------------------+----------------------+
| GPU  Name            TCC/WDDM | Bus-Id        Disp.A | Volatile Uncorr. ECC |
| Fan  Temp  Perf  Pwr:Usage/Cap|         Memory-Usage | GPU-Util  Compute M. |
|                               |                      |               MIG M. |
|===============================+======================+======================|
|   0  NVIDIA GeForce ... WDDM  | 00000000:09:00.0  On |                  N/A |
| 24%   54C    P0    31W / 120W |   1395MiB /  6144MiB |     12%      Default |
|                               |                      |                  N/A |
+-------------------------------+----------------------+----------------------+

+-----------------------------------------------------------------------------+
| Processes:                                                                  |
|  GPU   GI   CI        PID   Type   Process name                  GPU Memory |
|        ID   ID                                                   Usage      |
|=============================================================================|
|    0   N/A  N/A      1460    C+G   Insufficient Permissions        N/A      |
|    0   N/A  N/A      1976    C+G   ...Container\nvcontainer.exe    N/A      |
|    0   N/A  N/A      3088    C+G   Insufficient Permissions        N/A      |
|    0   N/A  N/A      7380      C   ...oice\NVIDIA RTX Voice.exe    N/A      |
|    0   N/A  N/A      8012    C+G   C:\Windows\explorer.exe         N/A      |
|    0   N/A  N/A      8972    C+G   ...artMenuExperienceHost.exe    N/A      |
|    0   N/A  N/A      9312    C+G   ...ekyb3d8bbwe\YourPhone.exe    N/A      |
|    0   N/A  N/A      9724    C+G   ...5n1h2txyewy\SearchApp.exe    N/A      |
|    0   N/A  N/A     10204    C+G   ...y\ShellExperienceHost.exe    N/A      |
|    0   N/A  N/A     10632    C+G   ...5n1h2txyewy\SearchApp.exe    N/A      |
|    0   N/A  N/A     10684    C+G   ...cw5n1h2txyewy\LockApp.exe    N/A      |
|    0   N/A  N/A     11796    C+G   ...perience\NVIDIA Share.exe    N/A      |
|    0   N/A  N/A     11944    C+G   ...me\Application\chrome.exe    N/A      |
|    0   N/A  N/A     12048    C+G   ...2txyewy\TextInputHost.exe    N/A      |
|    0   N/A  N/A     12696    C+G   ...icrosoft VS Code\Code.exe    N/A      |
|    0   N/A  N/A     14020    C+G   ...lack\app-4.13.0\slack.exe    N/A      |
|    0   N/A  N/A     14400    C+G   ...d\app-0.0.309\Discord.exe    N/A      |
|    0   N/A  N/A     15020    C+G   ...8wekyb3d8bbwe\Cortana.exe    N/A      |
|    0   N/A  N/A     15428    C+G   ...pp\AutodeskDesktopApp.exe    N/A      |
|    0   N/A  N/A     16036    C+G   ...bBrowser\AcWebBrowser.exe    N/A      |
+-----------------------------------------------------------------------------+
```
