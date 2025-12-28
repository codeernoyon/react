# 📱 React Native & Expo: The Complete A-Z Reference Guide

This document provides a detailed breakdown of the most essential React Native and Expo components, including their properties and use cases.

---

## 🏗️ 1. View (The Structural Container)
The `View` is the most fundamental component for building a UI. It acts as a container that supports layout with Flexbox, style, and touch handling.

**A-Z Properties:**
* **`style`**: Used for all layout and visual styling (Flexbox, Width, Height, Margin, Padding, Colors).
* **`pointerEvents`**: Controls whether the View can be the target of touch events (`'auto'`, `'none'`, `'box-none'`, `'box-only'`).
* **`onLayout`**: Invoked on mount and layout changes to get the exact `x`, `y`, `width`, and `height` of the view.
-   **`nativeID`**: A unique identifier for the view, often used for automation or connecting with native code.
-   **`accessible`**: If `true`, indicates the view is an accessibility element (groups children for screen readers).
-   **`collapsable`**: (Android Only) Optimization to remove a view from the hierarchy if it only used for layout.

---

## 📝 2. Text (Displaying Content)
The `Text` component is the only way to display strings in React Native. It supports nesting, styling, and touch handling.

**A-Z Properties:**
* **`numberOfLines`**: Truncates the text with an ellipsis (...) after a specific number of lines.
* **`selectable`**: Allows the user to select and copy the text (true/false).
* **`onPress / onLongPress`**: Functions triggered when the user taps or holds the text.
-   **`ellipsizeMode`**: Determines where the ellipsis appears (`'head'`, `'middle'`, `'tail'`, `'clip'`).
-   **`adjustsFontSizeToFit`**: Scales the font size down automatically to fit the container dimensions.
-   **`selectionColor`**: Changes the highlight color when the text is selected.

---

## ⌨️ 3. TextInput (Data Input)
A foundation component for inputting text into the app via a keyboard.

**A-Z Properties:**
* **`value`**: The string value to show for the text input (Controlled component).
* **`onChangeText`**: Callback that is called when the text input's text changes.
* **`placeholder`**: Text that appears when the input is empty.
* **`keyboardType`**: Determines which keyboard to open (`'numeric'`, `'email-address'`, `'phone-pad'`, `'default'`).
* **`secureTextEntry`**: If `true`, the text input obscures the text entered (for passwords).
* **`autoFocus`**: If `true`, focuses the input on `componentDidMount`.
* **`maxLength`**: Limits the maximum number of characters that can be entered.
* **`multiline`**: If `true`, the text input can be multiple lines.
* **`editable`**: If `false`, text is not editable (Read-only).
* **`onSubmitEditing`**: Callback that is called when the keyboard's submit button is pressed.
* **`keyboardAppearance`**: (iOS Only) Determines the color of the keyboard (`'default'`, `'light'`, `'dark'`).

---

## 🔘 4. TouchableOpacity & Pressable (Interactions)
These are used to make any component "clickable" with visual feedback.

**A-Z Properties:**
* **`onPress`**: Called when the touch is released (standard click).
* **`onLongPress`**: Called if the user holds the touch for a certain duration.
* **`activeOpacity`**: (TouchableOpacity) Sets the transparency level when touched (0 to 1).
* **`disabled`**: If `true`, disable all interactions for this component.
* **`hitSlop`**: Defines how far your touch can be from the button and still trigger a press.
* **`pressRetentionOffset`**: How far your finger can move away before the press is cancelled.
* **`android_ripple`**: (Pressable Only) Configures the native Android ripple effect colors.

---

## 📜 5. FlatList (High-Performance Lists)
The best way to render a large scrollable list of data efficiently.

**A-Z Properties:**
* **`data`**: An array of data to be rendered.
* **`renderItem`**: A function that takes an item from data and returns a component.
* **`keyExtractor`**: Used to extract a unique key for a given item (for performance).
* **`numColumns`**: Multiple columns can only be rendered with `horizontal={false}`.
* **`onRefresh / refreshing`**: Standard "Pull to Refresh" functionality.
* **`onEndReached`**: Called when the scroll position gets close to the end of the data.
* **`ListHeaderComponent / ListFooterComponent`**: Rendered at the very top and bottom of the list.
* **`ListEmptyComponent`**: Rendered when the list is empty.

---

## 📦 6. Modal (Overlay Windows)
A simple way to present content above an enclosing view.

**A-Z Properties:**
* **`visible`**: Controls whether the modal is currently showing.
* **`animationType`**: Controls how the modal animates (`'none'`, `'slide'`, `'fade'`).
* **`transparent`**: If `true`, the modal will render over a transparent background.
* **`statusBarTranslucent`**: (Android Only) Determines whether the modal should go under the system status bar.
* **`onRequestClose`**: (Android Only) Function called when the user presses the hardware back button.

---

## 🎡 7. ScrollView (Generic Scrolling)
A generic scrolling container that can host multiple components and views.

**A-Z Properties:**
* **`horizontal`**: When `true`, the ScrollView's children are arranged horizontally.
* **`showsVerticalScrollIndicator`**: Displays or hides the scroll bar.
* **`keyboardShouldPersistTaps`**: Determines when the keyboard should stay up after a tap (`'always'`, `'never'`, `'handled'`).
* **`contentContainerStyle`**: Styling for the actual scrollable content area.

---

## 🚀 8. Expo Extra APIs (Hardware & System)

| Feature | API Name | Usage |
| :--- | :--- | :--- |
| **Haptics** | `expo-haptics` | Physical vibration feedback: `impactAsync(ImpactFeedbackStyle.Light)`. |
| **SQLite** | `expo-sqlite` | Local database for offline storage: `db.transaction(tx => ...)`. |
| **Sharing** | `expo-sharing` | Open native sharing menu for files/links: `shareAsync(url)`. |
| **Location** | `expo-location` | Get user's coordinates: `getCurrentPositionAsync({})`. |
| **Camera** | `expo-camera` | QR Code and Barcode scanning via `onBarCodeScanned`. |
| **FileSystem** | `expo-file-system` | Create, read, and write files locally: `writeAsStringAsync()`. |

---

## 🛠️ 9. Advanced Hooks & System APIs

* **`useState`**: To manage your dynamic data (e.g., input values).
* **`useEffect`**: For fetching data or setting up listeners.
* **`useRef`**: To persist values or directly access a component (e.g., focusing a TextInput).
* **`Keyboard.dismiss()`**: A static method to close the keyboard programmatically.
* **`Platform.OS`**: To write platform-specific code (`'ios'` or `'android'`).

---
*Maintained for React Native Learning 🚀*
