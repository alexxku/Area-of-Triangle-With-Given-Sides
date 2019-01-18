# Area-of-Triangle-With-Given-Sides
Using C# console application, create a program that calculates the area of a triangle with given sides.

using System;

namespace AreaTriangleGivenSides
{
    class Program
    { 
        static void Main(string[] args)
        {
            Program function = new Program ();

            //Variables.
            double a, b, c, p, A;

            //Ask user for input.
            Console.WriteLine("Enter the three sides of the triangle. ");
            Console.WriteLine();
            Console.Write("Side a: ");
            a = Convert.ToInt32(Console.ReadLine());
            Console.Write("Side b: ");
            b = Convert.ToInt32(Console.ReadLine());
            Console.Write("Side c: ");
            c = Convert.ToInt32(Console.ReadLine());
            Console.WriteLine();

            //Calculate sides and Area.
            p = function.sides(a, b, c);
            A = Math.Sqrt((p * (p - a)) * (p * (p - b)) * (p*(p - c)));

            //Display answer.
            Console.WriteLine($"Area= {A}");
            Console.ReadLine();

        }

       public double sides(double x, double y, double z)
        {
            return (x + y + z) / 2;
        }
    }
}
