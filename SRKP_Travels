#include <iostream>
#include<fstream>
#include<iomanip>
#include<windows.h>
using namespace std;

void menu();

class ManageMenu
{
protected:
	string userName;
public:
      ManageMenu()    //constructor
      {
    	  system("color 0B");//change terminal colour
    	  cout<< "\n\n\n\n\n\n\n\n\n\t Enter Your Name to Continue as Admin: ";
    	  cin>>userName;
    	  system("CLS");
    	  menu();
      }
      ~ManageMenu(){} ;

};

class Customers
{
public:
	int age,mobileNo,menuBack;
	static int custId;
	string name,address,gender;
	char all[999];

	void getDetails(){
		ofstream out("old -Customer.txt",ios:: app);
		{
		cout<<"\nEnter Customer Id: ";
		cin>>custId;
		cout<<"\nEnter Name: ";
		cin>>name;
		cout<<"\nEnter Address: ";
		cin>>address;
		cout<<"\nEnter Gender: ";
		cin>>gender;
		cout<<"\nEnter Age: ";
		cin>>age;
		cout<<"\nEnter Mobile Number: ";
		cin>>mobileNo;
	}
	out << "\nCustomer Id: "<< custId <<"\nName: " << name << "\nAddress: " << address <<"\nGender: " << gender << "\nAge: "<< age << "\nMobile Number: " << mobileNo <<endl;
	out.close();
	cout<<"\nSAVED /nNOTE: We have saved your record for future purposes\n"<<endl;
	}
	void showDetails()  //to show old cust details
	{
	ifstream in("old-customer.txt");
		{
			if(!in)
			{
			    cout<< "File Error" << endl;
		    }
		    while(!in.eof()){
		    	in.getline(all,999);
		    	cout<<all<<endl;
		    }
		    in.close();
		}
	}
};
int Customers :: custId;

class Cabs
{
public:
		int cabChoice;
		int kilometers;
		float cabCost;
		static float lastCabCost;



		void cabDetails(){
			cout<<"Welcome to SRKP Cabs \n"<<endl;
			cout<<"We have collaborated with fastest safest and smartest cab service around the Country"<<endl;
			cout<<"1. Rent a standard Cab - Rs10/km"<<endl;
			cout<<"2. Rent a Luxury Cab - Rs 20/km"<<endl;


	        cout << "\nEnter another key to back or," << endl;

			cout<<"/n To calculate the fare of the cab"<<endl;
			cout<<"Enter type of cab of your choice"<<endl;
			cin>>cabChoice;
			cout<<"Enter distance(km) you have to travel"<<endl;
			cin>>kilometers;

			int hireCab;

			if (cabChoice == 1)
			{
				cabCost=kilometers*10;
				cout<<"Your journey cost ="<<cabCost <<"rupees for Standard Cab"<<endl;
				cout<<"Press 1 to select this Cab: or";
				cout<<"Press 2 to select another Cab: ";
				cin>>hireCab;

				system("CLS"); //to clear system terminal

				if(hireCab==1){
					lastCabCost = cabCost;
					cout<<"/nYou have Successfully hired a Standard Cab"<<endl;
					cout<<"Go back to menu & take your reciept"<<endl;
				}
				else if(hireCab==2){
					cabDetails();
				}
				else{
					cout<<"Invalid input! Redirecting you to prevoius menu \n Please wait!"<<endl;
					Sleep(999);
					system("CLS");
					cabDetails();
				}

			}
			else if(cabChoice==2){
				cabCost=kilometers*20;
				cout<<"Your journey cost ="<<cabCost <<"rupees for Standard Cab"<<endl;
				cout<<"Press 1 to select this Cab: or";
				cout<<"Press 2 to select another Cab: ";
				cin>>hireCab;

				system("CLS"); //to clear system terminal

				if(hireCab==1){
				lastCabCost = cabCost;
				cout<<"/nYou have Successfully hired a Luxury Cab"<<endl;
				cout<<"Go back to menu & take your reciept"<<endl;
				}
				else if(hireCab==2)
				{
					cabDetails();
				}
				else{
				cout<<"Invalid input! Redirecting you to prevoius menu \n Please wait!"<<endl;
				Sleep(1100);
				system("CLS");
				cabDetails();
				}

			}
			else{
				cout<<"Invalid input! Redirecting you to the previous menu"<<endl;
				Sleep(1100);
				system("CLS");
				menu();
			    }
			cout<<"\nPress 1 to redirect to Main memu: ";
			cin>>hireCab;
			system("CLS");
			if(hireCab==1){
				menu();
			}
			else{
				menu();
			}
		}
};

float Cabs::lastCabCost;

class Booking
{
public:
	int hotelChoice;
	static float hotelCost;
	int packChoice;
    int gotoMenu;

	void Hotels()
	{
		string hotelNo[]={"ARYAN RESIDENCY" , "SAURYA INN" ,"GOLDEN IRIS" , "SONNET"};
		for(int i=0;i<4;i++)
		{
			cout<<(i+1) <<": Hotel"<< hotelNo[i] <<endl;
		}
		cout<<"Currently we are collaborated with above hotels!"<<endl;
		cout<<"Press any key to go back or\n Enter your choice of the hotel to book: ";
		cin>>hotelChoice;

		system("CLS");

		if(hotelChoice == 1){
			cout<<"------Welcome to HOTEL ARYAN RESIDENCY-------\n"<<endl;
			cout<<"The Garden ,food and beverage .Enjoy all you can drink,Stay cool and get chilled in the summer sun "<<endl;
			cout<<"Packages offered by ARYAN RESIDENCY:\n" <<endl;
			cout<<"1.Standard Package"<<endl;
			cout<<"\tAll basic facilities you need just for: Rs.10000 "<< endl;
			cout<<"2.Premium Package"<<endl;
			cout<<"\tEnjoy Premium at : Rs.20000 "<< endl;
			cout<<"3.Luxury Package"<<endl;
			cout<<"\tLive a Luxury at ARYAN RESISDENCY : Rs.30000 "<< endl;

			cout<<"\nPress another key to go back or\n Enter Package number you want to book"<<endl;
			cin>>packChoice;

			if(packChoice==1){
				hotelCost=10000;
				cout<<"You have successfully booked Standard Package at ARYAN RESIDENCY"<<endl;
				cout<<"Go to menu and take your reciept"<<endl;
			}
			else if(packChoice==2){
				    hotelCost=20000;
					cout<<"You have successfully booked Premium Package at ARYAN RESIDENCY"<<endl;
					cout<<"Go to menu and take your reciept"<<endl;
						}
			else if(packChoice==3){
					hotelCost=30000;
					cout<<"You have successfully booked Luxury Package at ARYAN RESIDENCY"<<endl;
					cout<<"Go to menu and take your reciept"<<endl;
						}
			else{
				cout<<"Invalid input! Redirecting you to the previous menu"<<endl;
						Sleep(1100);
						system("CLS");
						Hotels();

						}

			cout<<"/nPress 1 to redirect to Main memu: ";
						cin>>gotoMenu;
						system("CLS");
						if(gotoMenu==1){
							menu();
						}
						else{
							menu();
						}

		}
		else if(hotelChoice == 2){
						cout<<"------Welcome to HOTEL SAURYA INN-------\n"<<endl;
						cout<<"Swimming Pool || Cafe ||Free WIFI || Family Rooms || Restro & Bar"<<endl;
						cout<<"Packages offered by SAURYA INN :\n" <<endl;
						cout<<"1.Family Package"<<endl;
						cout<<"\tRs.10000/Night "<< endl;
						cout<<"2.Couple Package"<<endl;
						cout<<"\tRs.20000/Night "<< endl;
						cout<<"3.Single Package"<<endl;
						cout<<"\tRs.30000/Night "<< endl;

						cout<<"\nPress another key to go back or\n Enter Package number you want to book"<<endl;
						cin>>packChoice;

						if(packChoice==1){
							hotelCost=10000;
							cout<<"You have successfully booked Family Package at SAURYA INN"<<endl;
							cout<<"Go to menu and take your receipt"<<endl;
						}
						else if(packChoice==2){
								hotelCost=20000;
								cout<<"You have successfully booked Couple Package at SAURYA INN"<<endl;
								cout<<"Go to menu and take your receipt"<<endl;
									}
						else if(packChoice==3){
								hotelCost=30000;
								cout<<"You have successfully booked Single Package at SAURYA INN"<<endl;
								cout<<"Go to menu and take your receipt"<<endl;
									}
						else{
							cout<<"Invalid input! Redirecting you to the previous menu"<<endl;
									Sleep(1100);
									system("CLS");
									Hotels();

								}

					cout<<"/nPress 1 to redirect to Main memu: ";
								cin>>gotoMenu;
								system("CLS");
								if(gotoMenu==1){
									menu();
								}
								else{
									menu();
								}

				       }
		else if(hotelChoice == 3){
								cout<<"------Welcome to HOTEL GOLDEN IRIS-------\n"<<endl;
								cout<<"Gym || Cafe ||Free WIFI || Couple friendly Rooms || Beauty Parlour"<<endl;
								cout<<"Packages offered by SAURYA INN :\n" <<endl;
								cout<<"1.Family Package"<<endl;
								cout<<"\tRs.10000/Night "<< endl;
								cout<<"2.Couple Package"<<endl;
								cout<<"\tRs.20000/Night "<< endl;
								cout<<"3.Single Package"<<endl;
								cout<<"\tRs.30000/Night "<< endl;

								cout<<"\nPress another key to go back or\n Enter Package number you want to book"<<endl;
								cin>>packChoice;

								if(packChoice==1){
									hotelCost=10000;
									cout<<"You have successfully booked Family Package at GOLDEN IRIS"<<endl;
									cout<<"Go to menu and take your receipt"<<endl;
								}
								else if(packChoice==2){
										hotelCost=20000;
										cout<<"You have successfully booked Couple Package at GOLDEN IRIS"<<endl;
										cout<<"Go to menu and take your receipt"<<endl;
											}
								else if(packChoice==3){
										hotelCost=30000;
										cout<<"You have successfully booked Single Package at GOLDEN IRIS"<<endl;
										cout<<"Go to menu and take your receipt"<<endl;
											}
								else{
									cout<<"Invalid input! Redirecting you to the previous menu"<<endl;
											Sleep(1100);
											system("CLS");
											Hotels();

										}

							cout<<"/nPress 1 to redirect to Main memu: ";
										cin>>gotoMenu;
										system("CLS");
										if(gotoMenu==1){
											menu();
										}
										else{
											menu();
										}

						                }

	else if(hotelChoice  == 4)
	{
	            cout << "-------WELCOME TO HOTEL SONNET-------\n" << endl;

	            cout << "The Garden, food and beverage. Enjoy all you can drink, Stay cool and get chilled in the summer sun." << endl;

	            cout << "Packages offered by SONNET:\n" << endl;

	            cout << "1. Standard Pack" << endl;
	            cout << "\tAll basic facilities you need just for: Rs.5000.00" << endl;
	            cout << "2. Premium Pack" << endl;
	            cout << "\tEnjoy Premium: Rs.10000.00" << endl;
	            cout << "3. Luxury Pack" << endl;
	            cout << "\tLive a Luxury at Avendra: Rs.15000.00" << endl;


	            cout << "\nPress another key to back or\nEnter Package number you want to book: ";
	            cin >> packChoice;

	            if (packChoice == 1){
	                hotelCost = 5000.00;
	                cout << "\nYou have successfully booked Standard Pack at SONNET" << endl;
	                cout << "Goto Menu and take the receipt" << endl;
	            }
	            else if (packChoice == 2){
	                hotelCost = 10000.00;
	                cout << "\nYou have successfully booked Premium Pack at SONNET" << endl;
	                cout << "Goto Menu and take the receipt" << endl;
	            }
	            else if (packChoice == 3){
	                hotelCost = 15000.00;
	                cout << "\nYou have successfully booked Luxury Pack at SONNET" << endl;
	                cout << "Goto Menu to take the receipt" << endl;
	            }
	            else{
	                cout << "Invalid Input! Redirecting to Previous Menu \nPlease Wait!" << endl;
	                Sleep(1100);
	                system("CLS");
	                Hotels();

	            }

	            cout << "\nPress 1 to Redirect Main Menu: ";
	            cin >> gotoMenu;
	            system("CLS");
	            if(gotoMenu == 1){
	                menu();
	            }
	            else{
	                menu();
	            }

	}
	}
};

float Booking :: hotelCost;
class Billing : public Booking ,Cabs,Customers
{
public:
	void printBill()
	{
		ofstream outf("reciept.txt");
		{
			outf << "-----ARYAN RESIDENCY--------" << endl;
			outf <<"------REciept----------------" <<endl;
			outf<<"______________________________" <<endl;

			outf<<"Customer ID: "<<Customers :: custId <<endl<<endl;
			outf<<"Description\t\t Total" <<endl;
			outf<<"Hotel cost:\t\t "<<fixed <<setprecision(2)<< Booking::hotelCost <<endl;
			outf<<"Travel(cab) cost:\t "<< fixed <<setprecision(2)<< Cabs ::lastCabCost <<endl;

			outf<<"______________________________" <<endl;
			outf<<"Total Charge:\t\t "<<fixed <<setprecision(2)<< Booking::hotelCost+Cabs::lastCabCost <<endl;
			outf<<"______________________________" <<endl;
			outf<<"--------THANK YOU------"<<endl;
		}
		outf.close();

		}
	void showBill(){
			ifstream inf("reciept.txt");
			{
				if(!inf)
				{
				    cout<< "File Opening Error" << endl;
			    }
			    while(!inf.eof()){
			    	inf.getline(all,999);
			    	cout<<all<<endl;
			    }

		}
			inf.close();

	}


};
void menu(){
	int mainChoice;
	int inChoice;
	int gotoMenu;

	cout<<"\t\t         ABC TRAVELS \n"<<endl ;
	cout<< "---------------Main Menu--------------------"<<endl;

	cout<<"\t _____________________"<<endl;
	cout<<"\t|\t\t\t\t\t|"<<endl;
	cout<<"\t|\tCustomer Management  -> 1\t|" <<endl;
	cout<<"\t|\tCab Management       -> 2\t|" <<endl;
	cout<<"\t|\tBookings Management  -> 3\t|" <<endl;
	cout<<"\t|\tCharges & Bills      -> 4\t|" <<endl;
	cout<<"\t|\tExit                 -> 5\t|" <<endl;
	cout<<"\t|\t\t\t\t\t|"<<endl;
	cout<<"\t _____________________"<<endl;

	cout<<"\nEnter Your Choice: ";
	cin>>mainChoice;

	system("CLS");

	Customers a1;
	Cabs a2;
	Booking a3;
	Billing a4;

	if(mainChoice ==1){
		cout<<"--------Customers------\n" <<endl;
		cout<<"1. Enter New Customer" << endl;
		cout<<"2. See Old Customers" <<endl;

		cout<<"\nEnter your Choice: ";
		cin>>inChoice;
		system("CLS");
		if(inChoice==1){
			a1.getDetails();
		}
		else if(inChoice == 2){
			a1.showDetails();
		}
		else{
			cout<<"Invalid input! Redirecting you to the previous menu"<<endl;
			Sleep(1100);
			system("CLS");
			menu();
		}
		cout<<"/nPress 1 to redirect to Main memu: ";
		cin>>gotoMenu;
		system("CLS");
		if(gotoMenu==1){
			menu();
		}
		else{
			menu();
		}
		}
	else if(mainChoice == 2){
		a2.cabDetails();
	}
	else if(mainChoice == 3){
		cout<<"---> Book a Luxury Hotel using the System <---" <<endl;
		a3.Hotels();
	}
	else if (mainChoice == 4){
		cout<<"---> Get your Reciept <---"<<endl;
		a4.printBill();

		cout<< "Your receipt is already printed you can get it from file path\n "<<endl;
		cout<< "to display your reciept on the screen ,Enter 1: or Enter any key to go back to main menu: "<<endl;

		cin>>gotoMenu;

		if(gotoMenu==1){
			system("CLS");
			a4.showBill();
			cout<<"\nPress 1 to redirect to main menu" <<endl;
			cin>>gotoMenu;
			system("CLS");
			if(gotoMenu==1){
				menu();
			}
			else{
				menu();
			}

		}
		else if (mainChoice == 5)
		{
			cout<<"---GOOD BYE---"<<endl;
			Sleep(999);
			system("CLS");
			menu();
		}
		else{
			cout<<"Invalid input! Redirecting you to the previous menu"<<endl;
			Sleep(1100);
			system("CLS");
			menu();

		}

	}
}
int main()
{
    ManageMenu startObj;
    return 0;
}
