# Unity Component Copier

A Unity Editor tool to copy components from one GameObject to another – excluding `Transform`.  
Includes an advanced Smart Override Mode that remaps object references between hierarchies.  

---

## ✨ Features
- Copy all components from a source GameObject to a target GameObject (except `Transform`)
- Preview which components will be copied before applying
- Select/deselect individual components
- Option to overwrite existing components of the same type, or add them as new
- Include or skip disabled components
- **Smart Override Mode**:
  - Copies values and remaps object references from the source hierarchy to the target hierarchy by relative path
  - Keeps existing references when no match is found to avoid broken links

---

## 📥 Installation
1. Create a folder named `Editor` in your Unity project (if it doesn’t exist).
2. Place the script inside:
   ```plaintext
   Assets/Editor/ComponentCopierWindow.cs
   ```
3. In Unity, open the window via **Tools → Component Copier**.

---

## 🛠 Usage
1. Open **Tools → Component Copier** from the Unity menu.
2. Drag a **Source GameObject** and a **Target GameObject** into the fields.
3. Click **Preview** to see which components can be copied.
4. Toggle selection of the components you want.
5. Press **Copy Components**.
6. (Optional) Enable **Smart Override Mode** to remap references automatically.

---

## 📸 Preview

_Add your screenshots or GIFs here to showcase the tool in action._

Example placeholders:

![Preview Window](docs/images/preview-window.png)  
*Component Copier window inside Unity Editor*

![Copy in Action](docs/images/copy-action.gif)  
*Copying multiple components with Smart Override Mode enabled*

---

## 💡 Example Use Cases
- Duplicate a prefab setup with all its scripts and serialized values
- Replace an old GameObject with a new one while preserving its components
- Quickly clone setup-heavy GameObjects without manual reference assignment

---

## ⚠️ Notes
- `Transform` and `RectTransform` are never copied
- Smart Override Mode relies on hierarchy paths. If the target hierarchy differs, unmatched references will remain unchanged

---

## 📜 License
MIT License – free to use in personal or commercial projects.
