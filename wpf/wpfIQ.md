### 1. What is MVVM.
- MVVM = Model + View + ViewModel
    - Model → Data
    - View → UI
    - ViewModel → Logic + binding
- It separates UI and business logic.
### 2. Data Binding.
- Connects UI with data.
```aspx
<TextBox Text="{Binding Name}" />
```
- Types of Data Binding
  - OneWay → Data → UI
  - TwoWay → Data ↔ UI
  - OneTime → Load once
  - OneWayToSource → UI → Data
### 3. What is Dependency Property?
- A special property used in WPF.
- Advanced property used for WPF features.
  - Binding
  - Styling
  - Animation
```C#
public static readonly DependencyProperty MyProperty =
DependencyProperty.Register("My", typeof(string), typeof(MyClass));
```
### 4. What is Routed Event?
- Routed Event is a specialized type of event that can travel through the element hierarchy (the visual tree).
- Imagine a Button that contains an Image and a TextBlock. Without routed events, if you clicked the text, only the TextBlock would know.
Because of Bubbling, the click event "bubbles up" from the TextBlock to the Button, allowing the button to trigger its logic regardless of which internal part you actually touched.
- Bubbling : Travels up the tree from the source to the root (Window).
- Tunneling : Travels down the tree from the root to the source.
- Direct :	Only fires on the element itself (like a standard .NET event).
### 5. Dispatcher 
- Dispatcher is the manager of the UI thread's work queue. Since WPF uses a Single-Threaded Affinity (STA) model, only the thread that created a UI element (the "UI thread") is allowed to modify it.
- ### 6. 
