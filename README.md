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
