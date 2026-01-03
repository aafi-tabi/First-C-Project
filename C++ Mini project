    #include<iostream>
    #include<string>
    #include<iomanip>
    using namespace std;

    struct restaurant{
        int ID;
        string name;
        float rating;
        string best_food;
        string location;
    };

    struct ride_info{
        int ID;
        string name;
        float price;
    };

    void artGallery();
    void park();
    void restaurant_menu();
    void fruit_shop();
    void vegetable_shop();
    void bank();
    void home();

    float withdrawal_amount;
    bool again = false;
    float pay;
    float change;
    bool p_visit = false;
    bool r_visit = false;
    float total = 0;
    bool py = true;
    int visit_option;

    // Function to print a line of dashes
    void printDashes(int length) {
        for(int i=0;i<length;i++){
            cout << "-";
        }
        cout << endl;
    }


    void home(){
        if(again == false){
            cout << "╔═════════════════════════════════════════╗" << endl;
            cout << "║     🐾🏠WELCOME TO YOUR HOME!🏠🐾       ║" << endl;
            cout << "╚═════════════════════════════════════════╝" << endl;
            cout<<"================================="<<endl<<endl;
            cout<<"Today you will:"<<endl;
            cout<<endl;
            cout<<"1 - Go to Bank to withdraw money"<<endl;
            cout<<"2 - Visit Vegetable Shop to buy vegetables"<<endl;
            cout<<"3 - Visit Fruit Shop to buy fruits"<<endl;
            cout<<"4 - Go to Restaurant to eat food"<<endl;
            cout<<"5 - Visit Park to enjoy rides"<<endl;
            cout<<"6 - Visit Art Gallary to view art"<<endl;
            cout<<endl;
            cout<<"🎉 Let's start your day! 🎉"<<endl<<endl;
            cout << "Press Enter to continue...";
            cin.ignore();
            cin.get();
            cout<<endl<<endl;
            bank();
        }else if(again == true){
            cout<<"╔═══════════════════════════════════════╗"<<endl;
            cout<<"║     WELCOME BACK TO YOUR HOME!🏠      ║"<<endl;
            cout<<"╚═══════════════════════════════════════╝"<<endl;
            cout<<"================================"<<endl;
            cout<<"\n🎊 Day Complete! 🎊\n";
            cout<<endl;
        }
    }

    void dayReview(){
    float money_spent = 35000 - withdrawal_amount;
    
    cout<<endl;
    cout<<"╔════════════════════════════════════════╗"<<endl;
    cout<<"║       🎊 YOUR DAY SUMMARY 🎊           ║"<<endl;
    cout<<"╚════════════════════════════════════════╝"<<endl;
    cout << endl;
    
    cout<<"💰 FINANCIAL REPORT:"<<endl;
    cout<<"   Bank Balance    : 35000"<<endl;
    cout<<"   Money Withdrawn : "<<35000 - money_spent<<endl;
    cout<<"   Money Spent     : "<<money_spent<<endl;
    cout<<"   Remaining       : "<<withdrawal_amount<<endl;
    cout<<endl;
    
    cout<<"📍 PLACES YOU VISITED TODAY:"<<endl;
    cout<<"✓ Bank"<<endl;
    cout<<"✓ Vegetable Shop"<<endl;
    cout<<"✓ Fruit Shop" << endl;
    cout<<"✓ Art Gallary" << endl;
    if(r_visit) 
        cout << "✓ Restaurant" << endl;
    if(p_visit)
        cout << "✓ Park" << endl;
    cout << endl;
    
    cout << "🎯 STATUS: ";
    if(withdrawal_amount > 5000){
        cout << "Excellent Money Management! 💎" << endl;
    }else if(withdrawal_amount > 2000){
        cout << "Good Spending! 👍" << endl;
    }else if(withdrawal_amount > 0){
        cout << "Almost Done! 😊" << endl;
    }else{
        cout << "All Spent! 🎉" << endl;
    }
    cout << endl;
    
    cout<<"╔════════════════════════════════════════╗"<<endl;
    cout<<"║    Thank You For Your Day With Us!     ║"<<endl;
    cout<<"╚════════════════════════════════════════╝"<<endl;
    cout<<"Press Enter to continue to go back to bank.";
    cin.ignore();
    cin.get();
    
    bank();
}

    void bank(){
        float balance = 35000;
        if(again == false){
            cout<<"╔════════════════════════════════════╗"<<endl;
            cout<<"║        💰 WELCOME TO BANK 💸       ║"<<endl;
            cout<<"╚════════════════════════════════════╝"<<endl;
            cout<<"Your bank balance  = "<<balance<<endl;
            cout<<"How much you want to withdraw?"<<endl;
            cin>>withdrawal_amount;
            while(withdrawal_amount > balance || withdrawal_amount < 0){
                printDashes(23); // prints 23 dashes
                cout<<"You are exceeding your limit"<<endl;
                cout<<"Try Again"<<endl;
                cout<<"Enter amount to withdraw "<<endl;
                cin>>withdrawal_amount;
            }
            cout<<"Amount withdrawn successfully"<<endl;
            balance -= withdrawal_amount;
            cout<<"Remaining balance = "<<balance<<endl;
            cout<<endl<<endl;
            cout<<"Press Enter to continue...";
            cin.ignore();
            cin.get();
            vegetable_shop(); 
        }else if(again == true){
            cout<<"╔════════════════════════════════════╗"<<endl;
            cout<<"║        WELCOME BACK TO BANK 💸     ║"<<endl;
            cout<<"╚════════════════════════════════════╝"<<endl;
            cout<<"You are back in bank"<<endl;
            withdrawal_amount = 0;
            cout<<"Your bank balance  = "<<withdrawal_amount<<endl;
            cout<<"Now, go back to your home to continue your day!"<<endl;
            cout<<"Press Enter to continue to go back to home.";
            cin.ignore();
            cin.get();
            home();
        }
    }

    void vegetable_shop(){
        char choice = 'Y';
        int total_quantity = 0;
        int option;

        string vege_name[] = {"Potato","Tomato","Onion","Cabbage","Carrot"};
        float vege_price[] = {80, 120, 100, 150, 90};

        int vege_length = sizeof(vege_name)/sizeof(vege_name[0]);

        cout<<"╔════════════════════════════════════╗"<<endl;
        cout<<"║    🥕 FRESH VEGETABLE SHOP 🥬      ║"<<endl;
        cout<<"╚════════════════════════════════════╝"<<endl;
        int qua;
        int quantity[5] = {0,0,0,0,0};

        do{
            do{
                do{
                   cout << "Press the number to select a vegetable:" << endl;
                    cout << left << setw(5) << "No." 
                    << setw(15) << "Name" 
                    << setw(10) << "Price" << endl;
                    printDashes(30);

                    for(int i = 0; i < vege_length; i++){
                        cout << left << setw(5) << i+1
                        << setw(15) << vege_name[i]
                        << setw(10) << vege_price[i] 
                        << endl;
                    }

                    cin>>option;
                    cout<<"________________________________"<<endl;
                    string vege_header[] = {"Name", "Qua", "Total"};
                    int vegeheader_len = sizeof(vege_header)/sizeof(vege_header[0]);
                    

                    if(option == 1){
                        float p_price = vege_price[0];
                        float p_total = 0;
                        cout<<"How much Quantity of Potato you want?"<<endl;
                        cin>>qua;
                        total_quantity += qua;
                        quantity[option-1] += qua;
                        p_total = p_price * qua;
                        total += p_total; 
                        for(int i=0; i<vegeheader_len ; i++){
                            cout<<vege_header[i]<<"\t";
                        }
                        cout<<endl;
                        cout<<vege_name[option-1]<<"\t"<<qua<<"\t"<<p_total<<endl;
                    }else if(option == 2){
                        float t_price = vege_price[1];
                        float t_total = 0;
                        cout<<"How much Quantity of Tomato you want?"<<endl;
                        cin>>qua;
                        total_quantity += qua;
                        quantity[option-1] += qua;
                        t_total = t_price * qua;
                        total += t_total; 
                        for(int i=0; i<vegeheader_len ; i++){
                            cout<<vege_header[i]<<"\t";
                        }
                        cout<<endl;
                        cout<<vege_name[option-1]<<"\t"<<qua<<"\t"<<t_total<<endl;
                    }
                    else if(option == 3){
                        float o_price = vege_price[2];
                        float o_total = 0;
                        cout<<"How much Quantity of Onion you want?"<<endl;
                        cin>>qua;
                        total_quantity += qua;
                        quantity[option-1] += qua;
                        o_total = o_price * qua;
                        total += o_total; 
                        for(int i=0; i<vegeheader_len ; i++){
                            cout<<vege_header[i]<<"\t";
                        }
                        cout<<endl;
                        cout<<vege_name[option-1]<<"\t"<<qua<<"\t"<<o_total<<endl;
                    }
                    else if(option == 4){
                        float c_price = vege_price[3];
                        float c_total = 0;
                        cout<<"How much Quantity of Cabbage you want?"<<endl;
                        cin>>qua;
                        total_quantity += qua;
                        quantity[option-1] += qua;
                        c_total = c_price * qua;
                        total += c_total; 
                        for(int i=0; i<vegeheader_len ; i++){
                            cout<<vege_header[i]<<"\t";
                        }
                        cout<<endl;
                        cout<<vege_name[option-1]<<"\t"<<qua<<"\t"<<c_total<<endl;
                    }
                    else if(option == 5){
                        float ca_price = vege_price[4];
                        float ca_total = 0;
                        cout<<"How much Quantity of Carrot you want?"<<endl;
                        cin>>qua;
                        total_quantity += qua;
                        quantity[option-1] += qua;
                        ca_total = ca_price * qua;
                        total += ca_total; 
                        for(int i=0; i<vegeheader_len ; i++){
                            cout<<vege_header[i]<<"\t";
                        }
                        cout<<endl;
                        cout<<vege_name[option-1]<<"\t"<<qua<<"\t"<<ca_total<<endl;
                    }
                    else{
                        cout<<"Invalid Option"<<endl;
                        cout<<"Try again"<<endl;
                    }
                }while(!(option >= 1 && option <= 5));

                cout<<"Do you want to buy another vegetable? (Y/N)"<<endl;
                cin>>choice;
                cout<<endl;
                cout<<"    <-------->    "<<endl;

            }while(choice == 'Y' || choice == 'y');
            
            do{
                cout<<endl;
                string bill_header[] = {"Sr", "Item Name", "Quantity", "Price"};
                int bill_len = sizeof(bill_header)/sizeof(bill_header[0]);

                cout<<left<<setw(5)<<bill_header[0]
                    <<setw(20)<<bill_header[1]
                    <<setw(10)<<bill_header[2]
                    <<setw(10)<<bill_header[3]<<endl;
                    printDashes(50);

                for(int i= 0; i<vege_length; i++){
                    if(quantity[i] > 0){
                        cout<<left<<setw(5)<<i+1
                            <<setw(20)<<vege_name[i]
                            <<setw(10)<<quantity[i]
                            <<setw(10)<<fixed<<setprecision(2)<<vege_price[i] * quantity[i]
                            <<endl;
                    }
                }

                printDashes(41);
                cout<<setw(25)<<"Total"<<setw(10)<<total_quantity<<setw(10)<<total<<endl;
                printDashes(41);
                cout<<"Enter an amount to pay:"<<endl;
                cin>>pay;
                
                if(total > withdrawal_amount){
                    printDashes(32);
                    cout<<"You do not have enough balance to pay the bill"<<endl;
                    cout<<"Shop again"<<endl;
                }
                else if(pay < total){
                    printDashes(32);
                    cout<<"Payment insufficient!"<<endl;
                    cout<<"Bill is "<<total<<" but you paid "<<pay<<endl;
                    cout<<"Please pay again"<<endl;
                    py = false;
                }
                else{
                    change = pay - total;
                    cout<<"Change returned = "<<change<<endl;
                    cout<<"Payment successful"<<endl;
                    py = true;
                }
            }while(py == false);
        }while(total > withdrawal_amount);

        withdrawal_amount -= total;
        cout<<"Remaining balance in bank = "<<withdrawal_amount<<endl;
        printDashes(37); 
        if(withdrawal_amount > 0){
            cout<<"    <-------->    "<<endl;
            cout<<endl;
            cout << "Press Enter to continue to Fruit Shop...";
            cin.ignore();
            cin.get();
            fruit_shop();
        }else{
            cout<<"You have no remaining balance to continue your day"<<endl;
            cout<<"    <-------->    "<<endl;
            again = true;
            bank();
        }
    }

    void fruit_shop(){
        py = true;
        char choice = 'Y';
        int total_quantity = 0;
        total = 0;
        change = 0;
        int qua;
        int option;
        int quantity[5] = {0,0,0,0,0};

        string fruit_name[] = {"Apple","Banana","Orange","Mango","Grapes"};
        float fruit_price[] = {200, 80, 150, 250, 180};

        int fruit_length = sizeof(fruit_name)/sizeof(fruit_name[0]);

        cout<<"╔════════════════════════════════════╗"<<endl;
        cout<<"║          🍌 FRUIT SHOP 🍓          ║"<<endl;
        cout<<"╚════════════════════════════════════╝"<<endl;
        
        do{
            do{
                do{
                    cout << "Press the corresponding number to select a fruit:" << endl;

                    cout<<left<<setw(5)<<"No." 
                    <<setw(15)<<"Name" 
                    <<setw(10)<<"Price"<< endl;
                    printDashes(30);

                    for(int i=0; i<fruit_length; i++){
                        cout<<left<< setw(5) << i+1
                        <<setw(15)<<fruit_name[i]
                        <<setw(10)<<fruit_price[i] 
                        <<endl;
                    }
                    cin>>option;
                    cout<<"________________________________"<<endl;

                    string fruit_header[] = {"Name", "Qua", "Total"};
                    int fruitheader_len = sizeof(fruit_header)/sizeof(fruit_header[0]);
                    
                    if(option == 1){
                        float a_price = fruit_price[0];
                        float a_total = 0;
                        cout<<"How much Quantity of Apple you want?"<<endl;
                        cin>>qua;
                        total_quantity += qua;
                        quantity[option-1] += qua;
                        a_total = a_price * qua;
                        total += a_total; 
                        for(int i=0; i<fruitheader_len ; i++){
                            cout<<fruit_header[i]<<"\t";
                        }
                        cout<<endl;
                        cout<<fruit_name[option-1]<<"\t"<<qua<<"\t"<<a_total<<endl;

                    }
                    else if(option == 2){
                        float b_price = fruit_price[1];
                        float b_total = 0;
                        cout<<"How much Quantity of Banana you want?"<<endl;
                        cin>>qua;
                        total_quantity += qua;
                        quantity[option-1] += qua;
                        b_total = b_price * qua;
                        total += b_total; 
                        for(int i=0; i<fruitheader_len ; i++){
                            cout<<fruit_header[i]<<"\t";
                        }
                        cout<<endl;
                        cout<<fruit_name[option-1]<<"\t"<<qua<<"\t"<<b_total<<endl;
                    }
                    else if(option == 3){
                        float o_price = fruit_price[2];
                        float o_total = 0;
                        cout<<"How much Quantity of Orange you want?"<<endl;
                        cin>>qua;
                        total_quantity += qua;
                        quantity[option-1] += qua;
                        o_total = o_price * qua;
                        total += o_total; 
                        for(int i=0; i<fruitheader_len ; i++){
                            cout<<fruit_header[i]<<"\t";
                        }
                        cout<<endl;
                        cout<<fruit_name[option-1]<<"\t"<<qua<<"\t"<<o_total<<endl;
                    }
                    else if(option == 4){
                        float m_price = fruit_price[3];
                        float m_total = 0;
                        cout<<"How much Quantity of Mango you want?"<<endl;
                        cin>>qua;
                        total_quantity += qua;
                        quantity[option-1] += qua;
                        m_total = m_price * qua;
                        total += m_total; 
                        for(int i=0; i<fruitheader_len ; i++){
                            cout<<fruit_header[i]<<"\t";
                        }
                        cout<<endl;
                        cout<<fruit_name[option-1]<<"\t"<<qua<<"\t"<<m_total<<endl;
                    }
                    else if(option == 5){
                        float g_price = fruit_price[4];
                        float g_total = 0;
                        cout<<"How much Quantity of Grapes you want?"<<endl;
                        cin>>qua;
                        total_quantity += qua;
                        quantity[option-1] += qua;
                        g_total = g_price * qua;
                        total += g_total; 
                        for(int i=0; i<fruitheader_len ; i++){
                            cout<<fruit_header[i]<<"\t";
                        }
                        cout<<endl;
                        cout<<fruit_name[option-1]<<"\t"<<qua<<"\t"<<g_total<<endl;
                    }
                    else{
                        cout<<"Invalid Option"<<endl;
                        cout<<"Try again"<<endl;
                    }
                }while(!(option >= 1 && option <= 5));

                cout<<"Do you want to buy another fruit? (Y/N)"<<endl;
                cin>>choice;
                cout<<"    <-------->    "<<endl;

            }while(choice == 'Y' || choice == 'y');

            do{
                cout<<endl;
                string bill_header[] = {"Sr", "Name", "Qua", "Price"};
                int bill_len = sizeof(bill_header) / sizeof(bill_header[0]);

                for(int i=0; i<bill_len; i++) {
                cout<<setw(10)<<bill_header[i];
                }
                cout<<endl;

                for(int i=0; i<fruit_length; i++) {
                    if(quantity[i] > 0) {
                        cout<<setw(10) << i + 1
                        <<setw(10)<<fruit_name[i]
                        <<setw(10)<<quantity[i]
                        <<setw(10)<<fruit_price[i] * quantity[i]
                        <<endl;
                    }
                }

                printDashes(41); 
                cout<<setw(20)<<"Total"<<setw(10)<<total_quantity<<setw(10)<<total<<endl;
                printDashes(41); 
                cout << endl;

                cout<<"Enter an amount to pay:"<<endl;
                cin>>pay;
                
                if(total > withdrawal_amount){
                    printDashes(32);
                    cout<<"You do not have enough balance to pay the bill"<<endl;
                    cout<<"Shop again"<<endl;
                }
                else if(pay < total){
                    printDashes(32);
                    cout<<"Payment insufficient!"<<endl;
                    cout<<"Bill is "<<total<<" but you paid "<<pay<<endl;
                    cout<<"Please pay again"<<endl;
                    py = false;
                }
                else{
                    change = pay - total;
                    cout<<"Change returned = "<<change<<endl;
                    cout<<"Payment successful"<<endl;
                    py = true;
                }
            }while(py == false);
        }while(total > withdrawal_amount);

        withdrawal_amount -= total;
        cout<<"Remaining balance in bank = "<<withdrawal_amount<<endl;
        cout<<"    <-------->    "<<endl; 
        cout<<endl;
 
        if(withdrawal_amount > 0){
            cout << "Press Enter to continue...";
            cin.ignore();
            cin.get();
            do{
                cout<<"Do you want to visit Restaurant or Park?"<<endl;
                cout<<"Choose one option:"<<endl;
                cout<<"1 - Restaurant"<<endl;
                cout<<"2 - Park"<<endl;
                cin>>visit_option;
                if(visit_option == 1){
                    restaurant_menu();
                }else if(visit_option == 2){
                    park();
                }
            }while(visit_option != 1 && visit_option != 2);

        }else{
            cout<<"You have no remaining balance to continue your day"<<endl;
            cout<<"    <-------->    "<<endl;
            cout<<endl<<endl;
            again = true;
            bank();
        }
    }

    void restaurant_menu(){
        r_visit = true;
        py = true;
        total = 0;
        change = 0;
        int option;
        int opt;
        int size_option;

        cout<<"╔════════════════════════════════════╗"<<endl;
        cout<<"║     🍽️  RESTAURANT PLAZA 🍽️         ║"<<endl;
        cout<<"╚════════════════════════════════════╝"<<endl;
        
        do{
            do{
                cout<<"Choose from following resturants:"<<endl;
                cout<<endl;

                restaurant r1 = {1, "Fast Food Restaurant", 4.5, "Zinger Burger", "Downtown"};
                restaurant r2 = {2, "Traditional Pakistani Restaurant", 4.7, "Chicken Biryani", "Uptown"};
                restaurant r3 = {3, "Fine Dining Restaurant", 4.6, "Alfredo Pasta", "Midtown"};

                cout<<"+----+----------------------------------+--------+------------------+-----------+"<<endl;
                cout<<"| ID | Name                             | Rating | Best Food        | Location  |"<<endl;
                cout<<"+----+----------------------------------+--------+------------------+-----------+"<<endl;

                cout << "| " << setw(2) << r1.ID << " | "
                    <<setw(30) << left << r1.name << "   | "
                    <<setw(6) << r1.rating << " | "
                    <<setw(16) << r1.best_food << " | "
                    <<setw(9) << r1.location << " |"<<endl;
                cout << "+----+----------------------------------+--------+------------------+-----------+" << endl;

                cout << "| " << setw(2) << r2.ID << " | "
                    <<setw(30) << left << r2.name << " | "
                    <<setw(6) << r2.rating << " | "
                    <<setw(16) << r2.best_food << " | "
                    <<setw(9) << r2.location << " |"<<endl;
                cout << "+----+----------------------------------+--------+------------------+-----------+" << endl;

                cout << "| " << setw(2) << r3.ID << " | "
                    << setw(30) << left << r3.name << "   | "
                    << setw(6) << r3.rating << " | "
                    << setw(16) << r3.best_food << " | "
                    << setw(9) << r3.location << " |" << endl;
                cout << "+----+----------------------------------+--------+------------------+-----------+" << endl;
                            
                cout<<"Enter an ID to choose a resturant:"<<endl;
                cin>>option;

                if(option == 1){
                    int menu[5][3] = {
                        {350, 450, 550},
                        {300, 400, 500},
                        {250, 350, 450},
                        {600, 900, 1200},
                        {300, 400, 500}
                    };
                    string header[] = {"Small", "Medium", "Large"};
                    string food[] = {"Zinger Burger", "Chicken shawarma", "French Fries", "Chicken Pizza", "Club sandwich"};
                    int header_len = sizeof(header)/sizeof(header[0]);
                    int food_len = sizeof(food)/sizeof(food[0]);
                    
                    
                    cout<<"You have selected Fast Food Restaurant"<<endl;
                    cout<<"___ Here's a menu ___"<<endl;
                    cout<<"Press No."<<endl;
                    cout << "+----+-----------------------+-------+-------+-------+" << endl;
                    cout << "| No | Food                  | Small | Medium| Large |" << endl;
                    cout << "+----+-----------------------+-------+-------+-------+" << endl;

                    for(int i = 0; i < food_len; i++) {
                    cout << "| " << setw(2) << i+1 << " | " << setw(21) << food[i] << " | ";
                        for(int j = 0; j < 3; j++) {
                            cout << setw(5) << menu[i][j] << " | ";
                        }
                    cout << endl;
                    cout << "+----+-----------------------+-------+-------+-------+" << endl;
                    }
                
                    
                    do{
                        cin>>opt;
                        if(opt >= 1 && opt <= 5){
                            do{
                                cout<<"Select size: 1 - Small, 2 - Medium, 3 - Large"<<endl;
                                cin>>size_option;
                                if(size_option >= 1 && size_option <= 3){
                                    float food_price = menu[opt-1][size_option-1];
                                    total += food_price;
                                    cout<<"________________________________"<<endl;
                                    cout<<setw(20)<<"Food"<<setw(15)<<"Size"<<setw(15)<<"Total"<<endl;
                                    cout<<setw(20)<<food[opt-1]<<setw(15)<<header[size_option-1]<<setw(15)<<food_price<<endl;
                                    cout<<"________________________________"<<endl;
                                }
                                else{
                                    cout<<"Invalid size selection"<<endl;
                                    cout<<"Try again"<<endl;
                                }
                            }while(!(size_option >= 1 && size_option <= 3));
                        }
                        else{
                            cout<<"Invalid food selection"<<endl;
                            cout<<"Try again"<<endl;
                        }
                    }while(!(opt >= 1 && opt <= 5));
                }
                else if(option == 2){
                    int menu[5][3] = {
                        {500, 650, 800},
                        {450, 600, 750},
                        {400, 550, 700},
                        {600, 850, 1100},
                        {350, 500, 650}
                    };
                    string header[] = {"Small", "Medium", "Large"};
                    string food[] = {"Chicken Biryani", "Seekh Kebab", "Chapli Kebab", "Nihari", "Karahi Chicken"};
                    int header_len = sizeof(header)/sizeof(header[0]);
                    int food_len = sizeof(food)/sizeof(food[0]);
                    
                    cout<<"You have selected Traditional Pakistani Restaurant"<<endl;
                    cout<<"___ Here's a menu ___"<<endl;
                    cout<<"Press No."<<endl;
                    cout << "+----+-----------------------+-------+-------+-------+" << endl;
                    cout << "| No | Food                  | Small | Medium| Large |" << endl;
                    cout << "+----+-----------------------+-------+-------+-------+" << endl;

                    for(int i = 0; i < food_len; i++) {
                    cout << "| " << setw(2) << i+1 << " | " << setw(21) << food[i] << " | ";
                        for(int j = 0; j < 3; j++) {
                            cout << setw(5) << menu[i][j] << " | ";
                        }
                    cout << endl;
                    cout << "+----+-----------------------+-------+-------+-------+" << endl;
                    }
                    
                    do{
                        cin>>opt;
                        if(opt >= 1 && opt <= 5){
                            do{
                                cout<<"Select size: 1 - Small, 2 - Medium, 3 - Large"<<endl;
                                cin>>size_option;
                                if(size_option >= 1 && size_option <= 3){
                                    float food_price = menu[opt-1][size_option-1];
                                    total += food_price;
                                    cout<<"________________________________"<<endl;
                                    cout<<setw(20)<<"Food"<<setw(15)<<"Size"<<setw(15)<<"Total"<<endl;
                                    cout<<setw(20)<<food[opt-1]<<setw(15)<<header[size_option-1]<<setw(15)<<food_price<<endl;
                                    cout<<"________________________________"<<endl;
                                }
                                else{
                                    cout<<"Invalid size selection"<<endl;
                                    cout<<"Try again"<<endl;
                                }
                            }while(!(size_option >= 1 && size_option <= 3));
                        }
                        else{
                            cout<<"Invalid food selection"<<endl;
                            cout<<"Try again"<<endl;
                        }
                    }while(!(opt >= 1 && opt <= 5));
                }
                else if(option == 3){
                    int menu[5][3] = {
                        {700, 900, 1100},
                        {650, 850, 1050},
                        {600, 800, 1000},
                        {750, 950, 1150},
                        {500, 700, 900}
                    };
                    string header[] = {"Small", "Medium", "Large"};
                    string food[] = {"Alfredo Pasta", "Grilled Salmon", "Steak", "Lobster Tail", "Caesar Salad"};
                    int header_len = sizeof(header)/sizeof(header[0]);
                    int food_len = sizeof(food)/sizeof(food[0]);
                    
                    cout<<"You have selected Fine Dining Restaurant"<<endl;
                    cout<<"___ Here's a menu ___"<<endl;
                    cout<<"Press No."<<endl;
                    cout << "+----+-----------------------+-------+-------+-------+" << endl;
                    cout << "| No | Food                  | Small | Medium| Large |" << endl;
                    cout << "+----+-----------------------+-------+-------+-------+" << endl;

                    for(int i = 0; i < food_len; i++) {
                    cout << "| " << setw(2) << i+1 << " | " << setw(21) << food[i] << " | ";
                        for(int j = 0; j < 3; j++) {
                            cout << setw(5) << menu[i][j] << " | ";
                        }
                    cout << endl;
                    cout << "+----+-----------------------+-------+-------+-------+" << endl;
                    }
                    
                    do{
                        cin>>opt;
                        if(opt >= 1 && opt <= 5){
                            do{
                                cout<<"Select size: 1 - Small, 2 - Medium, 3 - Large"<<endl;
                                cin>>size_option;
                                if(size_option >= 1 && size_option <= 3){
                                    float food_price = menu[opt-1][size_option-1];
                                    total += food_price;
                                    cout<<"________________________________"<<endl;
                                    cout<<setw(20)<<"Food"<<setw(15)<<"Size"<<setw(15)<<"Total"<<endl;
                                    cout<<setw(20)<<food[opt-1]<<setw(15)<<header[size_option-1]<<setw(15)<<food_price<<endl;
                                    cout<<"________________________________"<<endl;
                                }
                                else{
                                    cout<<"Invalid size selection"<<endl;
                                    cout<<"Try again"<<endl;
                                }
                            }while(!(size_option >= 1 && size_option <= 3));
                        }
                        else{
                            cout<<"Invalid food selection"<<endl;
                            cout<<"Try again"<<endl;
                        }
                    }while(!(opt >= 1 && opt <= 5));
                }
                else{
                    cout<<"Invalid restaurant selection"<<endl;
                    cout<<"Try again"<<endl;
                }
            }while(!(option >= 1 && option <= 3));
            
            do{
                cout<<endl;
                cout << "+-----------------------------------+" << endl;
                cout << "| Total bill: " << setw(21) << total << " |" << endl;
                cout << "+-----------------------------------+" << endl << endl;


                cout<<"Enter an amount to pay:"<<endl;
                cin>>pay;
                
                if(total > withdrawal_amount){
                    cout<<"You do not have enough balance to pay the bill"<<endl;
                    cout<<"Shop again"<<endl;
                }
                else if(pay < total){
                    cout<<"Payment insufficient!"<<endl;
                    cout<<"Bill is "<<total<<" but you paid "<<pay<<endl;
                    cout<<"Please pay again"<<endl;
                    py = false;
                }
                else{
                    change = pay - total;
                    cout<<"Change returned = "<<change<<endl;
                    cout<<"Payment successful"<<endl;
                    py = true;
                }
            }while(py == false);
        }while(total > withdrawal_amount);
        
        withdrawal_amount -= total;
        cout<<"Remaining balance in bank = "<<withdrawal_amount<<endl;
        cout<<"    <-------->    "<<endl; 
        cout<<endl;


        if(withdrawal_amount > 0){
            cout << "Press Enter to continue...";
            cin.ignore();
            cin.get();
            cout<<endl<<endl;
            artGallery();
        }else{
            cout<<"You have no remaining balance to continue your day"<<endl;
            again = true;
            bank();
        }
    }

    void park(){
        p_visit = true;
        py = true;
        int id;
        float total = 0;
        char choice = 'Y';
        int take[5] = {0,0,0,0,0};
        string header[] = {"ID", "Name", "Tickets No.", "Price"};
        int header_len = sizeof(header)/sizeof(header[0]);
        

        cout << "╔════════════════════════════════════╗" << endl;
        cout << "║       🎡 ADVENTURE PARK 🎢         ║" << endl;
        cout << "╚════════════════════════════════════╝" << endl;
        
        ride_info p1 = {1, "Roller Coaster", 50};
        ride_info p2 = {2, "Ferris Wheel", 75}; 
        ride_info p3 = {3, "Swing Ride", 100};
        ride_info p4 = {4, "Water Slide", 150};
        ride_info p5 = {5, "Go-Karts", 200};

        int ride_id[5] = {p1.ID, p2.ID, p3.ID, p4.ID, p5.ID};
        string ride_name[5] = {p1.name, p2.name, p3.name, p4.name, p5.name};
        float ride_price[5] = {p1.price, p2.price, p3.price, p4.price, p5.price};
        
        do{
            cout<<"Here are the available rides:"<<endl;
            do{
                do{
                     cout << "+------------------------------------------------------+" << endl;

                    cout << "| " << left << setw(5) << "ID(5)"
                    << " | " << setw(30) << "Ride Name(30)"
                    << " | " << setw(10) << "Price(10)" << " |" << endl;

                    cout << "+------------------------------------------------------+" << endl;

                    for (int i = 0; i < 5; i++) {
                    cout << "| " << left << setw(5) << ride_id[i]
                    << " | " << setw(30) << ride_name[i]
                    << " | " << setw(10) << fixed << setprecision(2) << ride_price[i] << " |" << endl;

                    cout << "+------------------------------------------------------+" << endl;
                }

                    cout<<"Enter the ID of ride you want to visit:"<<endl;
                    cin>>id;

                    if(id >= 1 && id <= 5){
                        if(id == 1){
                            cout<<"You have selected Roller Coaster. Enjoy your ride!"<<endl;
                            cout<<endl;
                            take[0]++;
                            float p1_price = take[0] * p1.price;
                            total += p1_price;
                            for(int i=0; i<header_len; i++){
                                if(i == 1){
                                cout<<header[i]<<"\t\t";
                                }else{
                                    cout<<header[i]<<"\t";
                                }
                            }
                            cout<<endl; 
                            cout<<p1.ID<<"\t"<<p1.name<<"\t\t"<<take[0]<<"\t"<<p1_price<<endl;
                            again = false;
                            
                        }
                        else if(id == 2){
                            cout<<"You have selected Ferris Wheel. Enjoy your ride!"<<endl;
                            cout<<endl;
                            take[1]++;
                            float p2_price = take[1] * p2.price;
                            total += p2_price;
                            for(int i=0; i<header_len; i++){
                                if(i == 1){
                                cout<<header[i]<<"\t\t";
                                }else{
                                    cout<<header[i]<<"\t";
                                }
                            }
                            cout<<endl; 
                            cout<<p2.ID<<"\t"<<p2.name<<"\t\t"<<take[1]<<"\t"<<p2_price<<endl;
                            again = false;
                        }
                        else if(id == 3){
                            cout<<"You have selected Swing Ride. Enjoy your ride!"<<endl;
                            cout<<endl;
                            take[2]++;
                            float p3_price = take[2] * p3.price;
                            total += p3_price;
                            for(int i=0; i<header_len; i++){
                                if(i == 1){
                                cout<<header[i]<<"\t\t";
                                }else{
                                    cout<<header[i]<<"\t";
                                }
                            }
                            cout<<endl; 
                            cout<<p3.ID<<"\t"<<p3.name<<"\t\t"<<take[2]<<"\t"<<p3_price<<endl;
                            again = false;
                        }
                        else if(id == 4){
                            cout<<"You have selected Water Slide. Enjoy your ride!"<<endl;
                            cout<<endl;
                            take[3]++;
                            float p4_price = take[3] * p4.price;
                            total += p4_price;
                            for(int i=0; i<header_len; i++){
                                if(i == 1){
                                cout<<header[i]<<"\t\t";
                                }else{
                                    cout<<header[i]<<"\t";
                                }
                            }
                            cout<<endl; 
                            cout<<p4.ID<<"\t"<<p4.name<<"\t\t"<<take[3]<<"\t"<<p4_price<<endl;
                            again = false;
                        }
                        else if(id == 5){
                            cout<<"You have selected Go-Karts. Enjoy your ride!"<<endl;
                            cout<<endl;
                            take[4]++;
                            float p5_price = take[4] * p5.price;
                            total += p5_price;
                            for(int i=0; i<header_len; i++){
                                if(i == 1){
                                cout<<header[i]<<"\t\t";
                                }else{
                                    cout<<header[i]<<"\t";
                                }
                            }
                            cout<<endl; 
                            cout<<p5.ID<<"\t"<<p5.name<<"\t\t"<<take[4]<<"\t"<<p5_price<<endl;
                            again = false;
                        }
                    }
                    else{
                        cout<<"Invalid ride selection"<<endl;
                        cout<<"Try again"<<endl;
                    }
                }while(!(id >= 1 && id <= 5));
                
                cout<<"Do you want another ride?(Y/N)"<<endl;
                cin>>choice;
                cout<<"    <-------->    "<<endl<<endl;
            }while(choice == 'Y' || choice == 'y');
            do{
                cout<<endl;
                for(int i = 0; i < header_len; i++){
                if(i == 1) 
                    cout<<setw(20)<<header[i];
                else 
                    cout<<setw(15)<<header[i];
                }
                cout << endl;
                printDashes(60); 
                int total_quantity = 0;

                for(int i =0;i<5; i++){
                    if(take[i] > 0){
                        float item_total = ride_price[i] * take[i];
                        total_quantity += take[i];
                        cout << setw(15) << ride_id[i]
                        << setw(20) << ride_name[i]
                        << setw(15) << take[i]
                        << setw(15) << fixed << setprecision(2) << item_total
                        << endl;
                    }
                }

                printDashes(60); 
                    cout << setw(25) << "Total" 
                    << setw(10) <<total_quantity 
                    << setw(10) << fixed << setprecision(2) << total 
                    << endl;
                printDashes(60); 
                cout << endl;
                cout<<"Enter an amount to pay:"<<endl;
                cin>>pay;
                
                if(total > withdrawal_amount){
                    printDashes(32);
                    cout<<"You do not have enough balance to pay the bill"<<endl;
                    cout<<"Visit again"<<endl;
                }
                else if(pay < total){
                    printDashes(32);
                    cout<<"Payment insufficient!"<<endl;
                    cout<<"Bill is "<<total<<" but you paid "<<pay<<endl;
                    cout<<"Please pay again"<<endl;
                    py = false;
                }
                else{
                    change = pay - total;
                    cout<<"Change returned = "<<change<<endl;
                    cout<<"Payment successful"<<endl;
                    py = true;
                }
            }while(py == false);
        }while(total > withdrawal_amount);

        withdrawal_amount -= total;
        cout<<"Remaining balance in bank = "<<withdrawal_amount<<endl;
        printDashes(32); 
        cout<<"Enjoy your visit!"<<endl;
        cout<<"    <-------->    "<<endl;
        cout<<endl;
        again = true;

        if(withdrawal_amount > 0){
            cout << "Press Enter to continue...";
            cin.ignore();
            cin.get();
            cout<<endl<<endl;
            if(r_visit == false){
                do{
                    cout<<"Do you want to go to resturant or art gallary?"<<endl;
                    cout<<"1 - Resturant"<<endl;
                    cout<<"2 - Art gallary"<<endl;
                    cin>>visit_option;
                    if(visit_option == 1){
                        restaurant_menu();
                    }else if(visit_option == 2){
                        artGallery();
                    }
                    else{
                        cout<<"Invalid Option"<<endl;
                    }
                }while(visit_option != 1 && visit_option != 2);
            }else if(r_visit == true){
                artGallery();
            }
        }else{
            printDashes(32);
            cout<<"You have no remaining balance to continue your day"<<endl;
            again = true;
            bank();
        }
    }

    void artGallery(){ 
    bool vt1 = false;
    bool vt2 = false;
    bool vt3 = false;
    py = true;
    change = 0;
    total = 0;  
    char choice = 'Y';
    int opt;
    pay = 0;
    again = false;
    float price = 0;
    int option;
    string ticket_type[] = {"Standard Ticket", "Premium Ticket", "VIP Ticket"};
    string header[] = {"Ticket Type", "Price"};
    int len = sizeof(ticket_type)/sizeof(ticket_type[0]);
    float prices[] = {100, 200, 300};

    string art1[] = {"Abstract Painting", "Digital Art", "Street Art"};
    string art2[] = {"Renaissance Painting", "Baroque Sculpture", "Neoclassical Drawing"};
    string art3[] = {"Marble Sculpture", "Bronze Statue", "Wooden Carving"};
    float rating1[3] = {0,0,0};
    float rating2[3] = {0,0,0};
    float rating3[3] = {0,0,0};
    int art_len = sizeof(art1)/sizeof(art1[0]); 

    cout << "╔════════════════════════════════════╗" << endl;
    cout << "║     🎨 ART GALLERY MUSEUM 🖼️        ║" << endl;
    cout << "╚════════════════════════════════════╝" << endl;
    do{
        do{
            cout << "Choose from the following ticket options:" << endl;
            cout << "-----------------------------------------------" << endl;
            cout << "Option\t" << header[0] << "\t\t" << header[1] << endl;
            cout << "-----------------------------------------------" << endl;

            for(int i=0; i<len; i++){
                cout << i+1 << "\t" << ticket_type[i] << "\t\t" << prices[i] << endl;
            }
            cout << "-----------------------------------------------" << endl;
            cin>>option;

            if(option == 1){
                cout<<"You have selected Standard Ticket."<<endl<<"Enjoy your visit!"<<endl<<endl; 
                price = prices[0];
                again = false;
            }else if(option == 2){
                cout<<"You have selected Premium Ticket."<<endl<<"Enjoy your visit!"<<endl<<endl; 
                price = prices[1];
                again = false;
            }else if(option == 3){
                cout<<"You have selected VIP Ticket."<<endl<<"Enjoy your visit!"<<endl<<endl;
                price = prices[2];
                again = false;
            }else{
                again = true;
                cout<<"Invalid ticket option"<<endl;
            }
        }while (again == true);

        cout<<"Enjoy your visit to the Art Gallery!"<<endl;
        printDashes(37);
        do{
            cout<<"Ticket Price: "<<price<<endl;
            cout<<"Enter an amount to pay:"<<endl;
            cin>>pay;
            if(pay >= price){
                change = pay - price;
                cout<<"Change returned = "<<change<<endl;
                cout<<"Payment successful"<<endl;
                py = true;
            }else if(pay < price){
                printDashes(32);
                cout<<"Payment insufficient!"<<endl;
                cout<<"Bill is "<<price<<" but you paid "<<pay<<endl;
                cout<<"Please pay again"<<endl;
                py = false;
                
            }else{
                printDashes(32);
                cout<<"You do not have enough balance to pay for the ticket"<<endl;
            }
        }while(py == false);
    }while(withdrawal_amount < total);
    printDashes(32);
    withdrawal_amount -= price;
    cout<<"Remaining balance in bank = "<<withdrawal_amount<<endl;
    printDashes(32);
    cout<<endl;

    while((choice == 'Y' || choice == 'y') && (vt1 == false || vt2 == false || vt3 == false)){
        do{
            cout<<"Choose from the following exhibitions to visit:"<<endl;
            cout<<"1 - Modern Art Exhibition"<<endl;
            cout<<"2 - Classical Art Exhibition"<<endl;
            cout<<"3 - Sculpture Exhibition"<<endl;
            cin>>opt;
            if(opt == 1 && vt1 == false){
                vt1 = true;
                cout<<"You have selected Modern Art Exhibition."<<endl<<"Enjoy your visit!"<<endl<<endl;
                again = false;
                cout<<"Rate the following art pieces from 1 to 5:"<<endl;
                for(int i=0; i<art_len; i++){
                    do {
                        cout << setw(20) << left << art1[i] << ": ";
                        cin >> rating1[i];
                        if(!(rating1[i] >= 1 && rating1[i] <= 5)){
                            cout << "Invalid rating. Enter a number from 1 to 5.\n";
                        }
                    } while(!(rating1[i] >= 1 && rating1[i] <= 5));
                }
            }else if(opt == 2 && vt2 == false){
                vt2 = true;
                cout<<"You have selected Classical Art Exhibition."<<endl<<"Enjoy your visit!"<<endl<<endl;
                again = false;
                cout<<"Rate the following art pieces from 1 to 5:"<<endl;
                for(int i=0; i<art_len; i++){
                    do {
                        cout << setw(20) << left << art2[i] << ": ";
                        cin >> rating2[i];
                        if(!(rating2[i] >= 1 && rating2[i] <= 5)){
                            cout << "Invalid rating. Enter a number from 1 to 5.\n";
                        }
                    } while(!(rating2[i] >= 1 && rating2[i] <= 5));
                }
            }else if(opt == 3 && vt3 == false){
                vt3 = true;
                cout<<"You have selected Sculpture Exhibition."<<endl<<"Enjoy your visit!"<<endl<<endl;
                again = false;
                cout<<"Rate the following art pieces from 1 to 5:"<<endl;
                for(int i=0; i<art_len; i++){
                    do {
                        cout << setw(20) << left << art3[i] << ": ";
                        cin >> rating3[i];
                        if(!(rating3[i] >= 1 && rating3[i] <= 5)){
                            cout << "Invalid rating. Enter a number from 1 to 5.\n";
                        }
                    } while(!(rating3[i] >= 1 && rating3[i] <= 5));
                }
            }else{
                if(!(opt >=1 && opt <=3)){
                    cout<<"Invalid exhibition selection"<<endl;
                    cout<<"Try again"<<endl;
                    again = true;
                }else if(vt1 == true || vt2 == true || vt3 == true){
                    cout<<"You have already visited this exhibition"<<endl;
                }
            }
        }while(!(opt >=1 && opt <=3));
        printDashes(32);

        if(vt1 == true && vt2 == true && vt3 == true){
            cout<<"You have visited all exhibitions"<<endl;
        }else{
            cout<<"Do You want to visit another exhibition? (Y/N)"<<endl;
            cin>>choice;
        }
    }
    cout<<endl;
    string rating_header[] = {"Art Piece", "Rating"};
    int header_len = sizeof(rating_header)/sizeof(rating_header[0]);
    
    for (int i = 0; i < header_len; i++) {
        if(i == 0){
            cout<<left<<setw(25)<<rating_header[i];
        }else{
            cout<<left<<setw(10)<<rating_header[i];
        }
    }
    cout<<endl;

    for(int i=0; i<art_len; i++){
        if(rating1[i] > 0){
            cout<<left<<setw(25)<<art1[i];
            for(int j=0; j<rating1[i]; j++) 
                cout<<"⭐";
            cout<<endl;
        }

        if(rating2[i] > 0){
            cout<<left<<setw(25)<<art2[i];
            for(int j=0; j<rating2[i]; j++) 
                cout<<"⭐";
            cout<<endl;
        }

        if(rating3[i] > 0){
            cout<<left<<setw(25)<<art3[i];
            for(int j=0; j<rating3[i]; j++) 
                cout<<"⭐";
            cout<<endl;
        }
    }

    again = true;
    printDashes(32);
    cout<<"Thank you for visiting the Art Gallery!"<<endl;
    cout<<"    <-------->    "<<endl;
    cout<<endl;

    cout<<"Press Enter to continue...";
    cin.ignore();
    cin.get();

    dayReview();
}

    int main(){
        home();
        return 0;
    }
