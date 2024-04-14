# How to hot reload C# mods in Stardew Valley on macOS  
Download and install the latest .NET SDK [here](https://dotnet.microsoft.com/en-us/download).  
Make sure that the `dotnet` command works in your preferred shell.  
  
Open the .csproj file for your mod and add the following properties in the PropertyGroup setting:  
     `     <PropertyGroup>`  
        `          ...`  
        `          <RunWorkingDirectory>/Applications/Stardew Valley.app/Contents/MacOS/</RunWorkingDirectory>`  
        `          <RunCommand>/Applications/Stardew Valley.app/Contents/MacOS/StardewModdingAPI</RunCommand>`  
        `          <RunArguments>-mode dryrun</RunArguments>`  
        `          ...`  
      `     </PropertyGroup>`  
      
Open a terminal at your project folder and execute the following command:  
     `dotnet watch --project <project-name>.csproj run`  
  
Now, any changes made in your project should trigger a hot reload in Stardew Valley. (press `CTRL + R` to force hot reload)  
  
*You CANNOT debug with hot reload on macOS.
