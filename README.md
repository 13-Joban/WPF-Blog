
_Hey there 🖐, glad you visited my blog this is my first time I am writing about what i have learned so without wasting your precious time lets gets Started 🚀.
In this tutorial, i will share my experience about creating an application in **WPF** using C# which creates rectangle, circle and triangle with given input parameters._

### What actually is WPF ?
Windows Presentation Foundation (WPF), a UI framework that is resolution-independent and uses a vector-based rendering engine, built to take advantage of modern graphics hardware. WPF provides a comprehensive set of application-development features that include Extensible Application Markup Language (XAML), controls, data binding, layout, 2D and 3D graphics, animation, styles, templates, documents, media, text, and typography. WPF is part of .NET, so you can build applications that incorporate other elements of the .NET API.

### Markup and code-behind
WPF lets you develop an application using both markup and code-behind, an experience with which ASP.NET developers should be familiar. You generally use XAML markup to implement the appearance of an application while using managed programming languages (code-behind) to implement its behavior. This separation of appearance and behavior has the following benefits:

-Development and maintenance costs are reduced because appearance-specific markup isn't tightly coupled with behavior-specific code.

-Development is more efficient because designers can implement an application's appearance simultaneously with developers who are implementing the application's behavior.

## Markup
XAML is an XML-based markup language that implements an application's appearance declaratively. You typically use it to define windows, dialog boxes, pages, and user controls, and to fill them with controls, shapes, and graphics.

The following example uses XAML to implement the appearance of a window that contains a single button:
![beautify-picture (1)](https://user-images.githubusercontent.com/74794315/216296218-014acfd2-4bb2-484a-8a19-fdb3c389bff4.png)


The following figure shows the user interface (UI) that is defined by the XAML in the previous example:

![markup-window-button.png]({{site.baseurl}}/_posts/markup-window-button.png)


## Code Behind
The main behavior of an application is to implement the functionality that responds to user interactions. For example clicking a menu or button, and calling business logic and data access logic in response. In WPF, this behavior is implemented in code that is associated with markup. This type of code is known as code-behind. The following example shows the updated markup from the previous example and the code-behind:

![markup-window-button-clicked.png]({{site.baseurl}}/_posts/markup-window-button-clicked.png)


That's enough for introduction lets deep dive into our main task that means creating an application in  WPF using C# 

## Step 1 Install Visual Studio 
The Visual Studio IDE is a creative launching pad that you can use to edit, debug, and build code, and then publish an app. Over and above the standard editor and debugger that most IDEs provide, Visual Studio includes compilers, code completion tools, graphical designers, and many more features to enhance the software development process.
Visit https://visualstudio.microsoft.com/

_Hope you are along  with me_
## Step 2 Setup of project

1. Open Visual Studio.

2. Select Create a new project.

![vs-create-new-project.png](./_posts/vs-create-new-project.png)

3.In the Search for templates box, type wpf, and then press Enter.

4. In the code language dropdown, choose C# or Visual Basic.

5. In the templates list, select WPF Application and then select Next.

![vs-template-search.png]({{site.baseurl}}/_posts/vs-template-search.png)

6.In the Configure your new project window, do the following:

a. In the Project name box, enter Names.
b. Select the Place solution and project in the same directory check box.
c.Optionally, choose a different Location to save your code.
d.Select the Next button.

### Important parts of Visual Studio

![vs-main-window.png]({{site.baseurl}}/_posts/vs-main-window.png)


1. Solution Explorer

All of your project files, code, windows, resources, will appear in this pane.

2. Properties

This pane shows property settings you can configure based on the item selected. For example, if you select an item from Solution Explorer, you'll see property settings related to the file. If you select an object in the Designer, you'll see settings for that item.

3. Toolbox

The toolbox contains all of the controls you can add to a form. To add a control to the current form, double-click a control or drag-and-drop the control.

4. XAML designer

This is the designer for a XAML document. It's interactive and you can drag-and-drop objects from the Toolbox. By selecting and moving items in the designer, you can visually compose the user interface (UI) for your app.

5.XAML code editor

This is the XAML code editor for a XAML document. The XAML code editor is a way to craft your UI by hand without a designer. The designer may infer the values of properties on a control when the control is added in the designer. The XAML code editor gives you a lot more control.

## Step 3 Coding and Examining Output

## XAML (MainWindow.xaml)

![Screenshot (651).png]({{site.baseurl}}/_posts/Screenshot (651).png)


Let's break down this XAML code to understand it better. XAML is simply XML that can be processed by the compilers that WPF uses. It describes the WPF UI and interacts with .NET code. To understand XAML, you should, at a minimum, be familiar with the basics of XML.

### 1. Grid

A Grid is a very powerful and useful Layout in WPF. It enables you to arrange children elements in cells defined by rows and columns. In fact, when we add a new XAML document or create a new WPF Project in Visual Studio, Visual Studio automatically adds a Grid as the first container inside the window element.

### 2. Rectangle

The Rectangle object represents a rectangle shape and draws a rectangle with the given height and width. The Width and Height properties of the Rectangle class represent the width and height of a rectangle. The Fill property fills the interior of a rectangle. The Stroke property sets the color and StrokeThickness represents the width of the outer line of a rectangle.

****Note : We will be using Ellipse object for Circle and Polygon object for Triangle

### 3. Ellipse

The Ellipse object represents an ellipse shape and draws an ellipse with the given height and width. The Width and Height properties of the Ellipse class represent the width and height of an ellipse. The Fill property fills the interior of an ellipse. The Stroke property sets the color and StrokeThickness represents the width of the outer line of an ellipse.

### 4. Polygon

A polygon is a series of connected lines which is a closed shape. A closed shape is a shape that has same start point and end point.

The Polygon object represents a polygon shape and draws a polygon for the given connected points. The Fill property fills the interior of an ellipse. The Stroke property sets the color and StrokeThickness represents the width of the outer line of an ellipse. The Points property of the Polygon represents a collection of Point that defines the points in a polygon. 

### 5. StackPanel

A StackPanel places child elements in a vertical or horizontal stack. It is one of the popular panels because of its simplicity. By default, a StackPanel's child element grows from the top of the panel to the bottom, in other words in vertical orientation. We can control the position of elements using HorizontalAlignment or VerticalAlignment and control the spacing using margin and padding properties.

### 6. Slider Control

The Slider element in XAML represents a WPF Slider control.
**Slider Control Properties**

The Width and Height property represent the width and the height of the control. The Name property represents name of the control, which is a unique identifier of the control. The Background property is used to set the background color of the control. The Minimum and Maximum properties represent the minimum and maximum values of the slider range.

**_That's all we need in our XAML now head over to Code Behind for implementing the Click event handlers_**

## Code Behind (MainWindow.xaml.c#)
