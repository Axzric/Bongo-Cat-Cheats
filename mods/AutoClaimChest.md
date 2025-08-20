# 🎵 Bongo Cat - Auto Claim Chest Mod

This modification for **Bongo Cat** (available on [Steam](https://store.steampowered.com/app/3419430/Bongo_Cat/)) enables **automatic chest claiming** by editing the game assembly with **dnSpy**.

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

### 3. Find the Target Method

In the assembly explorer:

1. Expand `Assembly-CSharp`  
2. Navigate to `BongoCat -> Shop -> TimerUpdate()`  
3. Right-click inside the method and select **Edit Method (C#)**  

### 4. Modify the Code

Replace the relevant section with:

```csharp
_shopItem.Buy();
```

### 5. Save the Changes

- Click **Compile** to confirm the edit  
- Then go to `File > Save Module` to apply the modification  
- Replace the original `Assembly-CSharp.dll` in the `Managed` folder  

---

## 📸 Example

Your modified method should look similar to this:  

![Example](../images/Example.png)

---

## 🎯 Result

After applying this modification, chests will be **automatically claimed** without manual interaction.

> [!NOTE]  
> Ensure you edit the correct section inside `TimerUpdate()`, otherwise the modification will not function.
