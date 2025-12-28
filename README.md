# ⚡ React Native & Expo Mastery Guide (A-Z)

Welcome to the ultimate React Native and Expo quick-reference guide. This document covers essential components, hardware APIs, and best practices for building professional mobile applications.

---

## 🏗️ 1. Core Components (The UI Foundation)

### ⏹️ **View**
The most fundamental component for building a UI (like HTML's `div`).
- `style`: Applies layout and design (Flexbox, shadows, colors).
- `pointerEvents`: Determines if the view should be touchable ('auto', 'none', 'box-none').
- `onLayout`: Gets the exact dimensions and position of the view.

### 📝 **Text**
Essential for displaying any string of text.
- `numberOfLines`: Truncates text after a set number of lines.
- `selectable`: Allows users to select and copy text.
- `adjustsFontSizeToFit`: Dynamically scales font size to fit the container.

### ⌨️ **TextInput**
Captures user data from the keyboard.
- `value`: Holds the current string (controlled via state).
- `onChangeText`: Callback function triggered on every keystroke.
- `keyboardType`: Sets keyboard style (`numeric`, `email-address`, `phone-pad`).
- `secureTextEntry`: Hides characters for password fields.
- `autoFocus`: Automatically opens the keyboard on mount.

### 🔘 **TouchableOpacity & Pressable**
Handles all touch interactions and button behaviors.
- `onPress`: Fires on a single tap.
- `onLongPress`: Fires when held for a specific duration.
- `activeOpacity`: Determines transparency during touch (e.g., 0.7).
- `hitSlop`: Expands the clickable area beyond the visual boundaries.
- `android_ripple`: (Pressable only) Adds the native Android wave effect.

---

## 📊 2. List & Scroll Management

### 📜 **FlatList**
High-performance tool for rendering large lists.
- `data`: The array of data to be displayed.
- `renderItem`: Takes an item and returns a component.
- `keyExtractor`: Assigns a unique ID to each item for efficient rendering.
- `onEndReached`: Triggers a function for infinite scrolling/pagination.
- `ListEmptyComponent`: Shows a fallback UI when the list is empty.

### 🎡 **ScrollView**
Best for small, fixed-length scrollable content.
- `keyboardShouldPersistTaps`: Ensures buttons work even when the keyboard is open.
- `horizontal`: Enables side-to-side scrolling.

---

## 🚀 3. Expo-Specific Hardware & APIs

| Feature | Description & Key Props |
| :--- | :--- |
| **SQLite** | Offline storage. Use `db.transaction()` for SQL queries. |
| **Location** | GPS tracking. Use `getCurrentPositionAsync()` for Lat/Long. |
| **Camera** | Barcode/QR scanning via `onBarCodeScanned`. |
| **Haptics** | Physical vibration feedback via `Haptics.impactAsync()`. |
| **Sharing** | Native share dialog for reports/files via `Sharing.shareAsync()`. |
| **FileSystem** | Read/Write local files using `FileSystem.documentDirectory`. |

---

## 🛠️ 4. Advanced System APIs

* **Keyboard**: Use `Keyboard.dismiss()` to hide the keyboard manually.
* **Platform**: Detect OS using `Platform.OS === 'ios'`.
* **Modal**: Overlay UI with `animationType="slide"` and `statusBarTranslucent`.
* **StatusBar**: Control top bar style with `barStyle="light-content"`.

---

## 💡 5. Professional Best Practices

1.  **Keyboard Management**: Always wrap forms in `KeyboardAvoidingView` to prevent UI overlap.
2.  **SafeArea**: Use `SafeAreaView` from `react-native-safe-area-context` to handle notches.
3.  **Performance**: Optimize lists by using `React.memo` for list items.
4.  **Icons**: Utilize `@expo/vector-icons` for scalable, high-quality UI symbols.

---
*Created with ❤️ for React Native Developers.*
