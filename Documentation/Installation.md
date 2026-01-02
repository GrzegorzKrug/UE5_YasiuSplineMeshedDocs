\page install Installation


# 1. Download and Extract the Plugin
1. Download the ZIP file containing the plugin.
2. Locate your Unreal Engine project folder on your computer.
3. Inside your project folder, create a new folder named **Plugins** if it doesn’t already exist.  
   - Example path: `YourProject/Plugins/`
4. Extract (unzip) the downloaded plugin ZIP **into the Plugins folder**.

Your folder structure should look like this:
```
YourProject
├── Content
├── Source
└── Plugins
	└── PluginName (plugin files into this folder)
```

---

# 2. C++ Dependency
Add dependency to your project in build file: `ProjectName.Build.cs`
```cs
   PrivateDependencyModuleNames.AddRange(new string[] { "YasiuSplineMeshed" });
```

# 3. (Check or) Enable the Plugin in Unreal Engine
1. Open your Unreal Engine project.
2. In the top menu, select **Edit → Plugins**.
3. Use the search bar to find **Yasiu Spline Meshed**.
4. Check the box to enable the plugin.
   - If changed Unreal Engine may ask you to restart the editor.


---

# Dependencies
- Plugin: **YasiuMath**

---

## 3. Finished!
After the editor restarts, the **Yasiu Spline Meshed** plugin is installed and ready to use.



