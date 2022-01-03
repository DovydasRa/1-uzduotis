#include <iostream>

using namespace std;

int main()
{
    string diena, menuo;
    int metai, d, m, klaidadiena = 0, klaidamenuo = 0;
    string dienos[] = {"1st", "2nd", "3rd", "4th", "5th", "6th", "7th", "8th", "9th", "10th", "11th", "12th", "13th", "14th", "15th", "16th", "17th", "18th", "19th", "20th", "21st", "22nd", "23rd", "24th", "25th", "26th", "27th", "28th", "29th", "30th", "31st"};
    string menesiai[] = {"Jan", "Feb", "Mar", "Apr", "May", "Jun", "Jul", "Aug", "Sep", "Oct", "Nov", "Dec"};
    cout << "Iveskite dienos skaiciu (pvz.: 20th): "; cin >> diena;
    for (int i=0; i<=30; i++)
    if (diena == dienos[i])
    {
    cout << "Iveskite menesio sutrumpinta pavadinima (pvz.: Oct): "; cin >> menuo;
    for (int i=0; i<=11; i++)
    if (menuo == menesiai[i])
    {
    cout << "Iveskite metu skaiciu (pvz.: 2052): "; cin >> metai;
    if (metai < 1900)
    {
        cout << "Rasykite naujesne data nei 1900." << endl;
    }
    else if (metai > 2100)
    {klaidadiena = klaidadiena + 1;
        if (klaidadiena == 31)
        {
            cout << "Klaidingai ivesta diena." << endl;
        }
        cout << "Rasykite senesne data nei 2100." << endl;
    }
    else
    {
        for (int i=0; i<=30; i++)
            if (diena == dienos[i])
            {
                d = i + 1;
            }
        for (int i=0; i<=11; i++)
            if (menuo == menesiai[i])
            {
                m = i + 1;
            }
    cout << " " << endl;
    cout << "Irasyta data skaiciais: " << metai << "-" << m << "-" << d << endl;
    }
    }
    else
    {
        klaidamenuo = klaidamenuo + 1;
        if (klaidamenuo == 12)
        {
            cout << "Klaidingai ivestas menuo." << endl;
        }
    }
    }
    else
    {
        klaidadiena = klaidadiena + 1;
        if (klaidadiena == 31)
        {
            cout << "Klaidingai ivesta diena." << endl;
        }
    }
    return 0;
}
