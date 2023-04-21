//dotnet new console
//dotnet run
//Первое задание(1)
//Напишите программу, которая принимает на вход пятизначное число и проверяет, является ли оно палиндромом.
using System;

public class Program
{
    public static void Main()
    {
        Console.WriteLine("Введите пятизначное число:");
        string input = Console.ReadLine();

        if (input.Length != 5)
        {
            Console.WriteLine("Некорректный ввод. Введите пятизначное число.");
            return;
        }

        bool isPalindrome = true;
        for (int i = 0; i < input.Length / 2; i++)
        {
            if (input[i] != input[input.Length - i - 1])
            {
                isPalindrome = false;
                break;
            }
        }

        if (isPalindrome)
        {
            Console.WriteLine("Число является палиндромом.");
        }
        else
        {
            Console.WriteLine("Число не является палиндромом.");
        }
    }
}
//Задание два(2)
//Напишите программу, которая принимает на вход координаты двух точек и находит расстояние между ними в 3D пространстве.
using System;

public class Program
{
    public static void Main()
    {
        Console.WriteLine("Введите координаты двух точек в 3D пространстве:");
        Console.Write("x1: ");
        double x1 = double.Parse(Console.ReadLine());
        Console.Write("y1: ");
        double y1 = double.Parse(Console.ReadLine());
        Console.Write("z1: ");
        double z1 = double.Parse(Console.ReadLine());
        Console.Write("x2: ");
        double x2 = double.Parse(Console.ReadLine());
        Console.Write("y2: ");
        double y2 = double.Parse(Console.ReadLine());
        Console.Write("z2: ");
        double z2 = double.Parse(Console.ReadLine());

        double distance = Math.Sqrt(Math.Pow(x2 - x1, 2) + Math.Pow(y2 - y1, 2) + Math.Pow(z2 - z1, 2));

        Console.WriteLine("Расстояние между точками: " + distance);
    }
}
//Задание три(3)
//Напишите программу, которая принимает на вход число (N) и выдаёт таблицу кубов чисел от 1 до N.
using System;

public class Program
{
    public static void Main()
    {
        Console.WriteLine("Введите число N для построения таблицы кубов чисел от 1 до N:");
        int n = int.Parse(Console.ReadLine());

        Console.WriteLine("Таблица кубов чисел от 1 до " + n + ":");
        Console.WriteLine("------------------");

        for (int i = 1; i <= n; i++)
        {
            Console.WriteLine(i + " в кубе = " + (int)Math.Pow(i, 3));
        }
    }
}
