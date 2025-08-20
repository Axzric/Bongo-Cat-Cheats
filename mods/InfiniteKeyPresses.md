# 🎵 Bongo Cat - Infinite Key Presses Mod

This modification for **Bongo Cat** (available on [Steam](https://store.steampowered.com/app/3419430/Bongo_Cat/)) allows you to gain **massive key points** by editing the game assembly with **dnSpy**.

> [!IMPORTANT]  
> This project is for **educational purposes only**. Modifying game files may violate the game's **Terms of Service**. Proceed at your own risk.

---

## 📋 Requirements

- [Bongo Cat](https://store.steampowered.com/app/3419430/Bongo_Cat/) installed  
- [dnSpy](https://github.com/dnSpy/dnSpy/releases) (.NET debugger and assembly editor)  

---

## 🛠️ Steps to Apply the Modification

### 1. Locate the Game Assembly

Default path:
```ps1
C:\Program Files (x86)\Steam\steamapps\common\BongoCat\BongoCat_Data\Managed
```

### 2. Open the Assembly in dnSpy

1. Launch **dnSpy**  
2. Go to `File > Open...` and select **Assembly-CSharp.dll** from the `Managed` folder  

### 3. Find the Target Code

In the assembly explorer:

1. Expand `Assembly-CSharp`  
2. Locate the **namespace** `BongoCat`  
3. Open the `GlobalKeyHook` class  
4. Find the following line of code:  

```csharp
this._keysDown += GlobalKeyHook.IsDown.Count((bool x) => x);
```

### 4. Modify the Code

Right-click the method and choose **Edit Method (C#)**.  
Replace it with:  

```csharp
this._keysDown += GlobalKeyHook.IsDown.Count((bool x) => x) * 10000;
```

### 5. Save the Changes

- Click **Compile** to confirm the edit  
- Then go to `File > Save Module` to apply the modification  

---

## 🎯 Result

After applying this modification, each key press will count as **thousands of presses**, granting you effectively infinite points.

> [!NOTE]  
> - You can adjust the multiplier value (`10000`) to your preference.
