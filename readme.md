`npm run dist-win` - works fine   
`npm i extract-file-icon`   
`npm run dist-win` - node-gyp error   
Downgrading electron to from 11.3.0 to 11.2.3 fixes this error, but why? :(   
`npm i electron@11.2.3`   
`npm run dist-win` - works fine   

```log
PS D:\Fishie\Desktop\test> npm run dist-win

> test@1.0.0 dist-win
> electron-builder

  • electron-builder  version=22.9.1 os=10.0.19042
  • description is missed in the package.json  appPackageFile=D:\Fishie\Desktop\test\package.json
  • writing effective config  file=dist\builder-effective-config.yaml
  • rebuilding native dependencies  dependencies=extract-file-icon@0.3.2 platform=win32 arch=x64
  ⨯ cannot execute  cause=exit status 1
                    errorOut=npm ERR! code 1
    npm ERR! path D:\Fishie\Desktop\test\node_modules\extract-file-icon
    npm ERR! command failed
    npm ERR! command C:\Windows\system32\cmd.exe /d /s /c npm run rebuild
    npm ERR! > extract-file-icon@0.3.2 rebuild
    npm ERR! > node-gyp rebuild
    npm ERR! gyp info it worked if it ends with ok
    npm ERR! gyp info using node-gyp@7.1.2
    npm ERR! gyp info using node@14.16.0 | win32 | x64
    npm ERR! gyp info find Python using Python version 2.7.18 found at "C:\Python27\python.exe"
    npm ERR! gyp info find VS using VS2017 (15.9.28307.1401) found at:
    npm ERR! gyp info find VS "C:\Program Files (x86)\Microsoft Visual Studio\2017\BuildTools"
    npm ERR! gyp info find VS run with --verbose for detailed information
    npm ERR! gyp info spawn C:\Python27\python.exe
    npm ERR! gyp info spawn args [
    npm ERR! gyp info spawn args   'C:\\Users\\Fishie\\AppData\\Roaming\\npm\\node_modules\\npm\\node_modules\\node-gyp\\gyp\\gyp_main.py',
    npm ERR! gyp info spawn args   'binding.gyp',
    npm ERR! gyp info spawn args   '-f',
    npm ERR! gyp info spawn args   'msvs',
    npm ERR! gyp info spawn args   '-I',
    npm ERR! gyp info spawn args   'D:\\Fishie\\Desktop\\test\\node_modules\\extract-file-icon\\build\\config.gypi',
    npm ERR! gyp info spawn args   '-I',
    npm ERR! gyp info spawn args   'C:\\Users\\Fishie\\AppData\\Roaming\\npm\\node_modules\\npm\\node_modules\\node-gyp\\addon.gypi',
    npm ERR! gyp info spawn args   '-I',
    npm ERR! gyp info spawn args   'C:\\Users\\Fishie\\.electron-gyp\\11.3.0\\common.gypi',
    npm ERR! gyp info spawn args   '-Dlibrary=shared_library',
    npm ERR! gyp info spawn args   '-Dvisibility=default',
    npm ERR! gyp info spawn args   '-Dnode_root_dir=C:\\Users\\Fishie\\.electron-gyp\\11.3.0',
    npm ERR! gyp info spawn args   '-Dnode_gyp_dir=C:\\Users\\Fishie\\AppData\\Roaming\\npm\\node_modules\\npm\\node_modules\\node-gyp',
    npm ERR! gyp info spawn args   '-Dnode_lib_file=C:\\\\Users\\\\Fishie\\\\.electron-gyp\\\\11.3.0\\\\<(target_arch)\\\\node.lib',
    npm ERR! gyp info spawn args   '-Dmodule_root_dir=D:\\Fishie\\Desktop\\test\\node_modules\\extract-file-icon',
    npm ERR! gyp info spawn args   '-Dnode_engine=v8',
    npm ERR! gyp info spawn args   '--depth=.',
    npm ERR! gyp info spawn args   '--no-parallel',
    npm ERR! gyp info spawn args   '--generator-output',
    npm ERR! gyp info spawn args   'D:\\Fishie\\Desktop\\test\\node_modules\\extract-file-icon\\build',
    npm ERR! gyp info spawn args   '-Goutput_dir=.'
    npm ERR! gyp info spawn args ]
    npm ERR! gyp: C:\Users\Fishie\.electron-gyp\11.3.0\common.gypi not found (cwd: D:\Fishie\Desktop\test\node_modules\extract-file-icon) while reading includes of binding.gyp while trying to load binding.gyp
    npm ERR! gyp ERR! configure error
    npm ERR! gyp ERR! stack Error: `gyp` failed with exit code: 1
    npm ERR! gyp ERR! stack     at ChildProcess.onCpExit (C:\Users\Fishie\AppData\Roaming\npm\node_modules\npm\node_modules\node-gyp\lib\configure.js:351:16)
    npm ERR! gyp ERR! stack     at ChildProcess.emit (events.js:315:20)
    npm ERR! gyp ERR! stack     at Process.ChildProcess._handle.onexit (internal/child_process.js:277:12)
    npm ERR! gyp ERR! System Windows_NT 10.0.19042
    npm ERR! gyp ERR! command "C:\\Program Files\\nodejs\\node.exe" "C:\\Users\\Fishie\\AppData\\Roaming\\npm\\node_modules\\npm\\node_modules\\node-gyp\\bin\\node-gyp.js" "rebuild"
    npm ERR! gyp ERR! cwd D:\Fishie\Desktop\test\node_modules\extract-file-icon
    npm ERR! gyp ERR! node -v v14.16.0
    npm ERR! gyp ERR! node-gyp -v v7.1.2
    npm ERR! gyp ERR! not ok
    npm ERR! npm ERR! code 1
    npm ERR! npm ERR! path D:\Fishie\Desktop\test\node_modules\extract-file-icon
    npm ERR! npm ERR! command failed
    npm ERR! npm ERR! command C:\Windows\system32\cmd.exe /d /s /c node-gyp rebuild
    npm ERR!
    npm ERR! npm ERR! A complete log of this run can be found in:
    npm ERR! npm ERR!     C:\Users\Fishie\AppData\Local\npm-cache\_logs\2021-02-26T18_59_30_356Z-debug.log

    npm ERR! A complete log of this run can be found in:
    npm ERR!     C:\Users\Fishie\AppData\Local\npm-cache\_logs\2021-02-26T18_59_30_379Z-debug.log

                    command='C:\Program Files\nodejs\node.exe' 'C:\Users\Fishie\AppData\Roaming\npm\node_modules\npm\bin\npm-cli.js' rebuild extract-file-icon@0.3.2
                    workingDir=
npm ERR! code 1
npm ERR! path D:\Fishie\Desktop\test
npm ERR! command failed
npm ERR! command C:\Windows\system32\cmd.exe /d /s /c electron-builder

npm ERR! A complete log of this run can be found in:
npm ERR!     C:\Users\Fishie\AppData\Local\npm-cache\_logs\2021-02-26T18_59_30_420Z-debug.log
PS D:\Fishie\Desktop\test>
```
