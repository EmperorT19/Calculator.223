# Calculator.223
using System;

namespace calculator
{
    internal class Program

    {
        static void Main(string[] args)
        {
            bool isRunning = true;
            while (isRunning)
            {
                try
                {
                    Console.Write("Enter number1: ");
                    double num1 = Convert.ToDouble(Console.ReadLine());

                    Console.Write("Enter number2: ");
                    double num2 = Convert.ToDouble(Console.ReadLine());

                    Console.Write("Choose operation(+ or - or * or /): ");
                    string operation = Console.ReadLine();

                    if (operation == "+")
                    {
                        Console.WriteLine(num1 + num2);
                        break;
                    }
                    else if (operation == "-")
                    {
                        Console.WriteLine(num1 - num2);
                        break;
                    }
                    else if (operation == "/")
                    {
                        Console.WriteLine(num1 / num2);
                        if (num2 == 0)
                        {
                            Console.WriteLine("infinity");
                            break;
                        }
                    }
                    else if (operation == "*")
                    {
                        Console.WriteLine(num1 * num2);
                        break;
                    }
                    else
                    {
                        Console.WriteLine("Wrong operator");
                        Console.WriteLine();
                        continue;
                    }

                }
                catch
                {
                    Console.WriteLine("Wrong input. Try Again");
                    continue;
                }
            }
            Console.ReadKey();
        }
    }
}
