# laba6
Console.WriteLine("Введите количество строк");
int a = Convert.ToInt32(Console.ReadLine());
Console.WriteLine("Введите количество столбцов");
int b = Convert.ToInt32(Console.ReadLine());
int[,] mass = new int[a, b];
for (int i = 0; i < a; i++)
{
    for (int j = 0; j < b; j++)
    {
        Console.WriteLine("Введите элементы массива");
        mass[i, j] = Convert.ToInt32(Console.ReadLine());
    }
}
int sum = 0;
for (int i = 0; i < a; i++)
{
    for (int j = 0; j < b; j++)
    {
        if (mass[i, j] < 0 && mass[i, j] % 2 != 0)
        {
            sum = Math.Abs(mass[i,j]) + sum;
        }
    }
}
Console.WriteLine(sum);
