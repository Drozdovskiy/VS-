class Calculators
{
    static void Main()
    {
        Console.WriteLine("Выберите операцию:");
        Console.WriteLine("1 - Сложение");
        Console.WriteLine("2 - Вычитание");
        Console.WriteLine("3 - Умножение");
        Console.WriteLine("4 - Деление");

        int choice = int.Parse(Console.ReadLine());

        Console.Write("Введите первое число: ");
        double a = double.Parse(Console.ReadLine());

        Console.Write("Введите второе число: ");
        double b = double.Parse(Console.ReadLine());

        double i = 0;

        switch (choice)
        {
            case 1:
                i = a + b;
                Console.WriteLine($"Результат сложения: {i}");
                break;
            case 2:
                i = a - b;
                Console.WriteLine($"Результат вычитания: {i}");
                break;
            case 3:
                i = a * b;
                Console.WriteLine($"Результат умножения: {i}");
                break;
            case 4:
                if (a != 0)
                {
                    i = a / b;
                    Console.WriteLine($"Результат деления: {i}");
                }
                else
                {
                    Console.WriteLine("Ошибка: деление на ноль!");
                }
                break;
            default:
                Console.WriteLine("Неверный выбор операции.");
                break;
        }

        Console.WriteLine("Нажмите любую кнопку для выхода:");
        Console.ReadKey();
    }
}
