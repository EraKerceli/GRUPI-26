#include <iostream>
#include <string>
using namespace std;

void miresevini() {
    cout << "Miresevini ne dyqanin tone te luleve!\n";
}

void paraqitLule() {
    cout << "\nLlojet e luleve dhe cmimet per cope:\n";
    cout << "1. Trendafil - 3 EUR\n";
    cout << "2. Tulipan - 2 EUR\n";
    cout << "3. Orkide - 5 EUR\n";
    cout << "4. Zambak - 4 EUR\n";
}

int formoBuqete(bool zbritje) {
    cout << "\nZgjidhni lule per te formuar buqeten tuaj. Kur te perfundoni, shtypni 0.\n";
    paraqitLule();
    int zgjedhja, sasia, cmimiBuqete = 0;

    do {
        cout << "Zgjidhni lulen (1-4 ose 0 per te perfunduar): ";
        cin >> zgjedhja;

        if (zgjedhja >= 1 && zgjedhja <= 4) {
            cout << "Sa copa deshironi?: ";
            cin >> sasia;

            switch (zgjedhja) {
            case 1:
                cmimiBuqete += sasia * 3;
                break;
            case 2:
                cmimiBuqete += sasia * 2;
                break;
            case 3:
                cmimiBuqete += sasia * 5;
                break;
            case 4:
                cmimiBuqete += sasia * 4;
                break;
            default:
                break;
            }
        }
    } while (zgjedhja != 0);

    if (zbritje) {
        cout << "Si klient per here te pare, keni fituar 10% zbritje!\n";
        cmimiBuqete -= (cmimiBuqete * 0.10); // 10% zbritje
    }

    cout << "Cmimi i buqetes: " << cmimiBuqete << " EUR\n";
    return cmimiBuqete;
}

void ofertaShenValentin() {
    cout << "\nOferta per Shen Valentin: \n";
    cout << "Nese bleni nje buqete, fitoni nje kartoline dhe nje byzylyk falas!\n";
    cout << "Cmimet e buqetave te gatshme:\n";
    cout << "1. Buqete e vogel - 10 EUR\n";
    cout << "2. Buqete e madhe - 20 EUR\n";
}

void zgjedhLuleFalas(int numriLuleve) {
    cout << "\nZgjidhni " << numriLuleve << " lule falas.\n";
    paraqitLule();
    int zgjedhja;

    for (int i = 0; i < numriLuleve; i++) {
        cout << "Zgjidh lulen (1-4): ";
        cin >> zgjedhja;

        switch (zgjedhja) {
        case 1:
            cout << "Zgjodhet Trendafil.\n";
            break;
        case 2:
            cout << "Zgjodhet Tulipan.\n";
            break;
        case 3:
            cout << "Zgjodhet Orkide.\n";
            break;
        case 4:
            cout << "Zgjodhet Zambak.\n";
            break;
        default:
            cout << "Zgjedhje e pavlefshme!\n";
            i--; // Përsërit këtë raund
            break;
        }
    }
}

void oferta2plus2(bool zbritje) {
    cout << "\nOferta 2+2 falas: \n";
    cout << "Nese bleni nje cope Trendafil dhe nje Tulipan, mund te zgjidhni dy lule te tjera falas!\n";

    int cmimiOferta = 3 + 2;
    if (zbritje) {
        cmimiOferta -= (cmimiOferta * 0.10); // 10% zbritje
    }

    cout << "Cmimi per Trendafil dhe Tulipan: " << cmimiOferta << " EUR\n";

    string deshironFalas;
    cout << "Deshironi te zgjidhni dy lule falas? (po/jo): ";
    cin >> deshironFalas;

    if (deshironFalas == "po") {
        zgjedhLuleFalas(2);
    }
}

int main() {
    miresevini();
    paraqitLule();

    string klientIPare;
    cout << "\nA jeni klient per here te pare? (po/jo): ";
    cin >> klientIPare;

    bool zbritje = false;
    int cmimiFinal = 0;
    if (klientIPare == "po") {
        cout << "Si klient per here te pare, mund te formoni nje buqete dhe fitoni 10% zbritje!\n";
        zbritje = true;
        cmimiFinal += formoBuqete(zbritje);
    }
    else {
        cout << "Zbritja nuk vlen per klientet e rregullt.\n";
    }

    string ofertaSV;
    cout << "\nDeshironi oferten per Shen Valentin? (po/jo): ";
    cin >> ofertaSV;

    if (ofertaSV == "po") {
        ofertaShenValentin();
        int zgjedhjaBuqetes;
        cout << "Zgjidhni nje nga buqetat e gatshme (1-2): ";
        cin >> zgjedhjaBuqetes;

        if (zgjedhjaBuqetes == 1) {
            cmimiFinal += (zbritje ? 9 : 10);
        }
        else if (zgjedhjaBuqetes == 2) {
            cmimiFinal += (zbritje ? 18 : 20);
        }

        cout << "Oferta perfshin nje kartoline dhe nje byzylyk falas!\n";
    }
    else {
        string oferta22;
        cout << "\nDeshironi oferten 2+2 falas? (po/jo): ";
        cin >> oferta22;

        if (oferta22 == "po") {
            oferta2plus2(zbritje);
            cmimiFinal += (zbritje ? 4.5 : 5); // 3 EUR Trendafil + 2 EUR Tulipan me zbritje
        }
    }

    cout << "\nCmimi total: " << cmimiFinal << " EUR\n";

    if (cmimiFinal >= 20) {
        cout << "Urime! Keni fituar transport falas!\n";
    }
    else {
        cout << "Transporti nuk eshte falas per blerje nen 20 EUR.\n";
    }

    cout << "\nFaleminderit qe zgjodhet dyqanin tone te luleve!\n";
    return 0;
}
