# ece240

LAB 2
    
    
    int select;
    while (select != 4)
    {

        printf("1: Enter int\n");
        printf("2: Enter char\n");
        printf("3: Enter double\n");
        printf("4: To Quit\n\n");

        printf("Enter Choice: ");
        scanf("%d", &select);

        if (select != 1 && select !=2 && select !=3 && select!=4)
        {
            printf("Error: Invalid choice!\n");
        }
        
        

        if (select == 1)
        {
            int x;
            printf("Enter an integer (0-15): ");
            scanf("%d", &x);

            if (x >= 0 && x <= 15)
            {
                for (int j = 0; j < 5; j++)
                {
                    setOnBoardLEDs(x);
                    usleep(500000);
                    setOnBoardLEDs(0);
                    usleep(500000);
                }
            }

            else
            {
                printf("Error: Value outside of range!\n");
            }
        }

        if (select == 2)
        {


            int i;
            printf("Enter a ASCII character 0 - F: ");
            scanf("%x", &i);

            if (i < 0 || i > 15)
            {
                printf("Error: Value outside of range!\n");
			}
            else
            { 
                for (int j = 0; j < 5; j++)
                {
                    setOnBoardLEDs(i);
                    usleep(500000);
                    setOnBoardLEDs(0);
                    usleep(500000);
                }
             }   
          
        }


        if (select == 3)
        {
            double Dub;
            printf("Enter a double: ");
            scanf("%lf", &Dub);
            double D2 = Dub + 0.5;
            int y = (int)D2; // Will properly round the double value up or down
            
            
            if (y < 0 || y > 15)
            {
                printf("Error: Value outside of range!\n");
            }
            else
            {
                for (int j = 0; j < 5; j++)
                {
                    setOnBoardLEDs(y);
                    usleep(500000);
                    setOnBoardLEDs(0);
                    usleep(500000);
                }
            }
        }


        if (select == 4)
        {
            exit(0);
        }

    }

