# HomeWork2
static void Main(string[] args)
        
        {
            Console.WriteLine("Выберите одно из доступных заданий: ");
            Console.WriteLine("Задание 1.");
            Console.WriteLine("Задание 2.");
            Console.WriteLine("Задание 3.");
            Console.WriteLine("Задание 4.");

            int number = int.Parse(Console.ReadLine());
            Console.Clear();
            switch (number)
            {
                case 1:
                    
                    Console.WriteLine("Задание 1. Написать метод, возвращающий минимальное из трёх чисел.");
                    Task1();
                    break;

                case 2:

                    Console.WriteLine("Задание 2. С клавиатуры вводятся числа, пока не будет введен 0. Подсчитать сумму всех нечетных положительных чисел.");
                    Task2(); 
                    break;

                case 3:

                    Console.WriteLine("Задание 3. Написать метод подсчета количества цифр числа.");
                    Task3(); 
                    break;

                case 4:

                    Console.WriteLine("Задание 4. Реализовать метод проверки логина и пароля. На вход метода подается логин и пароль. На выходе истина, если прошел авторизацию, и ложь, если не прошел (Логин: root, Password: GeekBrains). Используя метод проверки логина и пароля, написать программу: пользователь вводит логин и пароль, программа пропускает его дальше или не пропускает. С помощью цикла do while ограничить ввод пароля тремя попытками.");
                    Task4();
                    break;

                default:

                    Console.WriteLine("Введен некорректный номер задачи.");
                    break;
            }

        }

        static void Task1()// ЗАДАНИЕ 1  Написать метод, возвращающий минимальное из трёх чисел.
        {
            
            Console.WriteLine("Введите три целых числа.");

            Console.Write("Введите первое число: ");
            int x = int.Parse(Console.ReadLine());

            Console.Write("Введите второе число: ");
            int y = int.Parse(Console.ReadLine());

            Console.Write("Введите третье число: ");
            int z = int.Parse(Console.ReadLine());


            int min;
            if (x < y && x < z)
            {
                min = x;
            }
            else if (y < x && y < z)
            {
                min = y;
            }
            else
            {
                min = z;
            }
            Console.WriteLine("Наименьшее число: " + min);
            Console.ReadLine();
        }

        static void Task2() //С клавиатуры вводятся числа, пока не будет введен 0. Подсчитать сумму всех нечетных положительных чисел.
        {
            Console.WriteLine("Вводите целые числа: ");
            int sum = 0;
            int num = 0;
            
            do
            {
                num = int.Parse(Console.ReadLine());
                if (num > 0 && num % 2 == 1)
                    sum += num;

            }
            while (num != 0);

            Console.WriteLine("Сумма нечетных положительных чисел:  " + sum);
        }

        static void Task3() //Написать метод подсчета количества цифр числа.
        {
            Console.Write("Введите число: ");
            Console.WriteLine("Количество цифр числа: " + count(Console.ReadLine()));
            Console.ReadKey();
        }

        static int count(string s)
        {
            return s.Length;

        }
        static void Task4()//Реализовать метод проверки логина и пароля. На вход метода подается логин и пароль. На выходе истина, если прошел авторизацию, и ложь, если не прошел (Логин: root, Password: GeekBrains). Используя метод проверки логина и пароля, написать программу: пользователь вводит логин и пароль, программа пропускает его дальше или не пропускает. С помощью цикла do while ограничить ввод пароля тремя попытками.
        {
            string login = "root";
            string password = "GeekBrains";

            int count = 0;
            do
            {
                Console.Write("Введите логин: ");
                string checkLogin = Console.ReadLine();

                Console.Write("Введите пароль: ");
                string checkPassword = Console.ReadLine();


                if (login == checkLogin && password == checkPassword)
                {

                    Console.WriteLine("Добро пожаловать!");
                    Console.ReadLine();
                    break;
                }
                Console.WriteLine("Неверный логин или пароль.");
                Console.ReadLine();
                ++count;
            } while (count < 3);

        }
