# 🧩 Blok Logikasi

## MIT App Inventor Komponentlar

### 📦 UI Components

```
Screen1 (Main Screen)
├─ HorizontalArrangement (Top Navigation)
│  ├─ SearchButton
│  └─ MenuButton
│
├─ ScrollView (Main Content)
│  └─ VerticalArrangement
│     ├─ HorizontalArrangement (File Categories)
│     │  ├─ ImageButton (Tasvirlar)
│     │  ├─ ImageButton (Videolar)
│     │  ├─ ImageButton (Audio)
│     │  ├─ ImageButton (Hujjatlar)
│     │  ├─ ImageButton (Yuklab)
│     │  └─ ImageButton (APK)
│     │
│     ├─ Label (Oxirgi Fayllar)
│     ├─ HorizontalScrollArrangement (Recent Files)
│     │  └─ (Dynamically created cards)
│     │
│     ├─ Label (Xotira)
│     └─ VerticalArrangement (Storage Items)
│        ├─ ListViewItem (Ichki xotira)
│        ├─ ListViewItem (SD-karta)
│        ├─ ListViewItem (OneDrive)
│        ├─ ListViewItem (Google Drive)
│        └─ ListViewItem (Tarmog)
```

---

## 🔧 Extensions

### TaifunFile
```
Purpose: Xotira hajmini va fayllarni o'qish
Methods:
- TotalBytes() - Jami byte
- FreeSpace() - Bo'sh joy
- List() - Fayllar ro'yxati
```

### ActivityStarter
```
Purpose: Boshqa app'larni ochish
Methods:
- StartActivity() - App ochish
```

---

## 📝 Block Logic

### 1. Screen Initialize
```
When Screen1.Initialize
├─ Set background color (Dark)
├─ Load storage info (TaifunFile)
├─ Display categories
└─ Load recent files
```

### 2. Category Button Click
```
When ImageButton.Click (e.g., Tasvirlar)
├─ Call TaifunFile.ListFiles(/DCIM/Camera)
├─ Filter by .jpg, .png, .jpeg
├─ Display in list view
└─ Show file count
```

### 3. Storage Display
```
When Screen1.Initialize
├─ Get Internal Storage
│  ├─ TaifunFile.TotalBytes("/storage/emulated/0")
│  ├─ TaifunFile.FreeSpace("/storage/emulated/0")
│  └─ Calculate percentage
├─ Get SD Card
│  └─ Similar logic
└─ Display all storages
```

### 4. Recent Files
```
When App Starts
├─ Get file list from common directories
├─ Sort by modification date (newest first)
├─ Take 4 recent files
├─ Create image cards dynamically
└─ Add to scroll view
```

### 5. Search Function
```
When SearchButton.Click
├─ Show text input dialog
├─ Get search query
├─ Filter files by name
└─ Display results
```

---

## 📊 Data Flow

```
User Opens App
    ↓
Screen1.Initialize
    ├─ Load Storage Data (TaifunFile)
    ├─ Display Categories
    ├─ Load Recent Files
    └─ Display Storage Items
    ↓
User Clicks Category
    ├─ Filter Files
    ├─ List Files
    └─ Display in ListView
    ↓
User Clicks Storage Item
    ├─ Open File Manager
    └─ Navigate to folder
    ↓
User Searches
    ├─ Filter Files
    └─ Display Results
```

---

## 🔑 Key Variables

```
global storageList = list()
global recentFiles = list()
global selectedCategory = text (default: "")
global searchQuery = text (default: "")
global internalStorageUsed = number
global internalStorageTotal = number
global internalStoragePercent = number
```

---

## ⚙️ Procedures

### `GetStorageInfo()`
- Input: Storage path (text)
- Output: Storage info (list with used/total/percent)
- Logic: Use TaifunFile to get sizes

### `ListFiles(path, filter)`
- Input: Directory path (text), file filter (text)
- Output: File list (list)
- Logic: Recursively list files

### `CreateRecentFiles()`
- Input: None
- Output: Display recent files
- Logic: Get files from common directories, sort by date

### `DisplayStorageItems()`
- Input: None
- Output: Display storage info
- Logic: Create UI elements for each storage

### `FormatBytes(bytes)`
- Input: Number of bytes (number)
- Output: Formatted string (KB, MB, GB)
- Logic: Divide by 1024 and format

