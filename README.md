# Lego Shape Generator
 
## Overview
Lego Shape Generator Application is designed to create and visualize Lego Shapes Assembly on a canvas, in a 3D space. It consists of 3 Dynamically-Linked Libraries(DLLs) : Geometry, LegoShapeFactory and Lego. It is a interactive desktop appication where you can view and change the assembly according to your requirements.
 
## File Structure
The application is structured into three main components:
 
### 1. Geometry DLL
#### Files:
- **Point2D.h/cpp**: Defines a 3D point class with x, y, and z coordinates.
    - `Point2D(double inX, double inY)`: Constructor for Point2D.
    - `~Point2D()`: Destructor for Point2D.
    - `double x() const`: Returns the x-coordinate of the point.
    - `double y() const`: Returns the y-coordinate of the point.
    - `void setX(double inX)`: Sets the x-coordinate of the point.
    - `void setY(double inY)`: Sets the y-coordinate of the point.

- **Point3D.h/cpp**: Defines a 3D point class with x, y, and z coordinates.
    - `Point3D(double inX, double inY, double inZ = 0)`: Constructor for Point3D.
    - `~Point3D()`: Destructor for Point3D.
    - `double x() const`: Returns the x-coordinate of the point.
    - `double y() const`: Returns the y-coordinate of the point.
    - `double z() const`: Returns the z-coordinate of the point.
    - `void setX(double inX)`: Sets the x-coordinate of the point.
    - `void setY(double inY)`: Sets the y-coordinate of the point.
    - `void setZ(double inZ)`: Sets the z-coordinate of the point.
 
- **Triangle.h/cpp**: Represents a 3D triangle using three Point3D vertices.
    - `Triangle(Point3D p1, Point3D p2, Point3D p3)`: Constructor for Triangle.
    - `~Triangle()`: Destructor for Triangle.
    - `Point3D p1() const`: Returns the first vertex of the triangle.
    - `Point3D p2() const`: Returns the second vertex of the triangle.
    - `Point3D p3() const`: Returns the third vertex of the triangle.
 
- **Triangulation.h/cpp**: Manages a collection of triangles forming a 3D mesh.
    - `Triangulation(const std::vector<Triangle>& inTriangles)`: Constructor for Triangulation.
    - `~Triangulation()`: Destructor for Triangulation.
    - `std::vector<Triangle> getTriangles() const`: Returns the collection of triangles.
 
### 2. Lego Shape Factory DLL
#### Files:
- **LegoShapeFactory.h/cpp**: Provides a base class for creating different Lego shapes.
    - `LegoShapeFactory()`: Constructor for LegoShapeFactory class.
    - Following classes inherit LegoShapeFactory class.
- **Cross.h/cpp**
    - `Cross()` Private constructor for cross shape generation.
    - `~Cross()`
    - `static Cube* getCube(float side)`: Function to get shape because the constuctor is private;
- **Cube.h/cpp**
- **Cuboid.h/cpp**
- **Cylinder.h/cpp**
- **CuboQuarto.h/cpp**
- **Quarto.h/cpp**

- **Reader.h/cpp** This is a reader class file for reading the STL file for the specified shape. You can create your own shape in Inventor and export it as STL file and later you can add it inside our Lego Shape Generator Project.
 
### 3. Application Lego
#### Files:
- **Lego.h/cpp**: Main application class utilizing Qt for the user interface.
    - `Lego(QWindow* parent = nullptr)`: Constructor for the Lego class.
    - `~Lego()`: Destructor for the Lego class.
    - `void setupUi()`: Sets up the user interface.
    - `void setConnections()`;
    - `void setupUi()`;
    - `void newSpace()`;
    - `void copySelectedShape()`;
    - `void pasteSelectedShape()`;
    - `void translateSelectedShape()`;
    - `void rotateSelectedShape()`;
    - `void removeSelectedShape()`;
    - `void colorSelectedShape()`;
    - `void resetSpace()`;
    - `void placeCube()`;
    - `void placeCuboid()`;
    - `void placeCylinder()`;
    - `void placeQuarto()`;
    - `void placeCuboQuarto()`;
    - `void placeCross()`;
    - `void increaseCount(std::string compareStr)`;
 
- **OpenGLWindow.h/cpp**: Handles rendering and OpenGL integration.
 
### 5. Software Tools
 
1. `C++`: The primary programming language for the application.
 
2. `QT`: The Qt framework is utilized for the development of the graphical user interface (GUI) components.
 
3. `OpenGL`: OpenGL is employed for rendering 3D graphics, enhancing the visualization capabilities of the application.
 
4. `Visual Studio`: The project is developed and built using the Visual Studio integrated development environment.
 
5. `Git`: Git is used for version control and collaborative development, allowing for easy tracking of changes and contributions.
