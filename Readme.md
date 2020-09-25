## Inofficial/Experimental Oculus Unity Integration as a package

The Oculus Unity Integration is officially available from the Oculus homepage and the Unity AssetStore:
https://developer.oculus.com/downloads/package/unity-integration/

### How to Use

**Option 1:** Add the git package to your manifest.json:  
```"com.oculus.integration": "https://github.com/needle-mirror/com.oculus.integration.inofficial.git#package",```

**Option 2:** In Unity, open the Package Manager Window,   
click "+ > Add package from git url" and paste  
```https://github.com/needle-mirror/com.oculus.integration.inofficial.git#package```

### Known Issues

First and foremost, the Oculus SDK License Agreement is not quite clear if "turning this into a package" counts as "derivative works from any SDK or its component" (section 1.2.1); no functionality of the SDK(s) has been changed, it's mostly reordering of folders plus adding AsmDefs.  
Please let me know if having this as a public package is an issue, and I'll remove it.

Additional known issues:
- some unclear cross references between samples (e.g. if you import a sample you might be missing assets that are in another sample)
- some of the "update logic" that the Oculus Integration does is enabling/disabling the plugin files inside the package; this does not work since packages are immutable by default. If you need this behaviour please embed the package.
- the package structure is not "final" in the sense that there is no Runtime/Editor folder yet. Tried to stick to the original structure to make future updates easier.

### Contact

[@hybridherbst](https://twitter.com/hybridherbst)