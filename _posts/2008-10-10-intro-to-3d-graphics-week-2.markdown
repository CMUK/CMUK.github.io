---
date: 2008-10-10 11:19:03+00:00
title: Intro to 3d Graphics Week 2
categories:
  - Intro to 3D Graphics
tags:
  - C++
  - Class
  - Maths
  - Programming
  - Vectors
---

This week i have been implementing a Vector class in C++. This was fairly easy once i understood the class and passing in one parameter instead of both vectors as parameters. After that it was just putting the maths i did last week on vectors into code. I made it console based but will try and implement it into GDI+ and use the draw string to display it on screen. Below is some code from my Vector.cpp class:

<blockquote>
//Basic addition method returning the calculated vector to output in the main
Vector Vector::Add(Vector rhs)
{
return Vector(rhs._x + _x,rhs._y + _y,rhs._z + _z);
}</blockquote>

Back in the main class

<blockquote>
void test_addition()
{
	Vector result;

    std::cout << "addition" << std::endl;
    std::cout << "---------" << std::endl;

    Vector a1(3.0f, 4.0f, 5.0f);
    Vector a2(3.0f, 2.0f, 1.0f);
    result = a1.Add(a2); // Here its passing in Vector a2 to the add method in in the Vector class and storing the calculation in result
    std::cout << result <<"\n";

</blockquote>

<blockquote>
//Used to output the vector in main
std::ostream& operator<<(std::ostream& out, const Vector& vec)
{
	return out << "<" << vec._x << ", " << vec._y << ", " << vec._z <" << std::endl;
}
</blockquote>

Here is my CrossProduct method

<blockquote>
Vector Vector::CrossProduct(Vector v)
{
	float cross_x = ((_y*v._z) -(_z*v._y));
	float cross_y = ((_z*v._x) -(_x*v._z));
	float cross_z = ((_x*v._y) -(_y*v._x));

    return Vector(cross_x,cross_y,cross_z);

}

</blockquote>
