using System;

class Program
{
    static void Main(string[] args)
    {
        Random rand = new Random();
        int playerHealth = 100;
        int playerEnergy = 100;

        int enemyHealth = 150;
        int enemyEnergy = 150;

        int action;

        while (true)
        {
            // Игровое меню
            Console.Clear();

            Console.WriteLine(@"       Жизни игрока: {0}                    Жизни вируса: {1}", playerHealth, enemyHealth);
            Console.WriteLine(@"       Энергия игрока: {0}                  Энергия вируса: {1}", playerEnergy, enemyEnergy);

            Console.WriteLine();

            Console.WriteLine("1. Установить обновление стандартного антивируса (20 урона, -20 энергии)");
            Console.WriteLine("2. Использовать свинью Касперского (30 урона, -30 энергии)");
            Console.WriteLine("3. Выпить кофе 3 в 1 (+30 энергии)");
            Console.WriteLine("4. Заказать пиццу (+40 жизни, -20 энергии)");
            Console.WriteLine("5. Ультимейт: переустановить Windows (100 урона, -110 энергии)\n");
            Console.WriteLine("Введите номер скилла:");


            // Проверка победы
            if (playerHealth <= 0)
            {
                Console.WriteLine("Вирус выиграл!");
                Console.WriteLine("     _______\n    | Игрок |\n    |  RIP  |\n    |       |\n    |_______|");
                Console.ReadLine();
                break;
            }
            if (enemyHealth <= 0)
            {
                Console.WriteLine("Игрок выиграл");
                Console.WriteLine("     _______\n    | Вирус |\n    |  RIP  |\n    |       |\n    |_______|");
                Console.ReadLine();
                break;
            }

            // Описание скиллов игрока
            action = int.Parse(Console.ReadLine());

            if (action == 1)
            {
                if (playerEnergy >= 10)
                {
                    enemyHealth -= 20;
                    playerEnergy -= 20;
                    Console.WriteLine("Игрок устанавливает обновление стандартного антивируса! Вы наносите 20 урона!\n");
                }
                else
                {
                    Console.WriteLine("Не достаточно энергии, пропуск хода!\n");
                }
            }

            if (action == 2)
            {
                if (playerEnergy >= 40)
                {
                    enemyHealth -= 30;
                    playerEnergy -= 40;
                    Console.WriteLine("Игрок слышит визг свиньи Касперского! Вы наносите 30 урона!\n");
                }
                else
                {
                    Console.WriteLine("Недостаточно энергии, пропуск хода!\n");
                }
            }

            if (action == 3)
            {
                if (playerEnergy <= 130)
                    {

                    playerEnergy += 30;
                    Console.WriteLine("Игрок заварил себе кофе 3 в 1 в гейзерной кофеварке! Вы получаете 30 энергии!\n"); 
                    }
                else
                {
                    Console.WriteLine("Так много кофе нельзя, а то будет инфаркт. Пропуск хода!\n");
                }
                
            }

            if (action == 4)
            {
                if (playerEnergy >= 20)
                {
                    if (playerHealth <= 60)
                    {
                        playerHealth += 40;
                        playerEnergy -= 20;
                        Console.WriteLine("Игрок заказал себе пиццу с ананасами. Вирус в шоке! Вы получаете 30 очков жизни!\n");
                    }
                    else
                    {
                        Console.WriteLine("Переизбыток жизни! Вы не можете быть таким живучим!\n");
                    }
                }
                else
                {
                    Console.WriteLine("Недостаточно энергии, пропуск хода!\n");
                }
            }

            if (action == 5)
            {
                if (playerEnergy >= 110)
                {
                    enemyHealth -= 100;
                    playerEnergy -= 110;
                    Console.WriteLine("Переустановка Windows! Вы наносите 100 урона!\n");
                }
                else
                {
                    Console.WriteLine("Недостаточно энергии, пропуск хода!\n");
                }
            }

            // Описание работы скиллов противника
            action = rand.Next(1, 8);

            if (action == 1)
            {
                if (enemyEnergy >= 10)
                {
                    playerHealth -= 40;
                    enemyEnergy -= 20;
                    Console.WriteLine("Вирус нашел ваши паспортные данные и слил их в Darknet, вы получаете 40 урона!\n");
                }
                else
                {
                    Console.WriteLine("Вирус истощен и пойман Касперским. Он пропускает ход!\n");
                }
            }

            if (action == 2)
            {
                if (enemyEnergy >= 10)
                {
                    playerHealth -= 20;
                    enemyEnergy -= 10;
                    Console.WriteLine("Вирус атаковал брандмауер! Вы получаете 20 урона!\n");
                }
                else
                {
                    Console.WriteLine("Вирус истощен и пойман Касперским. Он пропускает ход!\n");
                }
            }

            if (action == 3)
            {
                enemyEnergy += 30;
                Console.WriteLine("Вирус загрузил майнер. Он получает 30 энергии!\n");
            }

            if (action == 4)
            {
                if (enemyEnergy >= 20)
                {
                    enemyHealth += 30;
                    enemyEnergy -= 20;
                    Console.WriteLine("Вирус скачал обновление! Он получает 30 очков жизни!\n");
                }
                else
                {
                    Console.WriteLine("Вирус истощен и пойман Касперским. Он пропускает ход!\n");
                }
            }
            if (action == 5)
            {
                if (enemyEnergy >= 10)
                {
                    playerHealth -= 10;
                    enemyEnergy -= 10;
                    Console.WriteLine("Вирус удалил значок \"Пуск\". Вы получаете 10 урона!\n");
                }
            }
            if (action == 6)
            {
                if (enemyEnergy >= 10)
                {
                    playerHealth -= 10;
                    enemyEnergy -= 10;
                    Console.WriteLine("Вирус удалил значок \"Мой компьютер\". Вы получаете 10 урона!\n");
                }
            }
            if (action == 7)
            {
                enemyEnergy += 40;
                enemyHealth += 10;

                Console.WriteLine("Вирус эволюционировал. Теперь он Троянский. Вирус получает 10 очков жизни и 40 энергии!\n");

            }

            Console.WriteLine("Нажмите Enter для продолжения...");
            Console.ReadLine();
        }
    }
}
