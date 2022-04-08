# Building for Production
Our site (Both the API and UI) is on the `CS-Athletics.gordon.edu`, and the built files are deployed at `D:\Sites`, under the name `AthleticAbsenceAPI` and `AthleticsAbsenceUI` respectively.

Both the frontend and API are deployed manually.

## API
[Connect to the VM](./ConnectingToVM.md)

If you need to clone the repository, the Visual Studio publish profile will need to be remade. 

 - Open Visual Studio 2019
 - You want to select `Build` -> `Publish AthleticForm` 
 - You might see a folder publish profile already created, but if not:
    - Create a new publish profile
    - Within "Pick a publish target" select Folder and browse to `D:\Sites\AthleticAbsenceAPI` (If the API folder doesn't exist, publish should create it automatically).
    - Select pubish. 
Visual Studio should build the project to the selected path

## UI
If needed, clone the repository

 - Open Git Bash in `<repository path>\athletic-form-ui`
 - Run `npm run build` to build the project in this directory. This will create files in `build/`
 - Move (or copy) `build/` to `D:\Sites` and rename to `AthleticAbsenceUI`

 At this point, you should be able to browse to `https://AthleticAbsence.gordon.edu` and log in!

