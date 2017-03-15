#AHMAD FAJRI RAHMAN
#165150301111014
#no_1

#include <iostream>
using namespace std;
typedef struct polinom{
	int bilangan, pangkat;
	char x;};
polinom pol1[5], pol2[6], pol3[2];
polinom penambahan[8], pengalian[5*2], penurunan[5];
int i = 0, ik = 0, ikur = 0;
void fpol1(){
	pol1[0].bilangan = 6;
	pol1[0].x = 'x';
	pol1[0].pangkat = 8;
	pol1[1].bilangan = 8;
	pol1[1].x = 'x';
	pol1[1].pangkat = 7;
	pol1[2].bilangan = 5;
	pol1[2].x = 'x';
	pol1[2].pangkat = 5;
	pol1[3].bilangan = 1;
	pol1[3].x = 'x';
	pol1[3].pangkat = 3;
	pol1[4].bilangan = 15;}
void fpol2(){
	pol2[0].bilangan = 3;
	pol2[0].x = 'x';
	pol2[0].pangkat = 9;
	pol2[1].bilangan = 4;
	pol2[1].x = 'x';
	pol2[1].pangkat = 7;
	pol2[2].bilangan = 3;
	pol2[2].x = 'x';
	pol2[2].pangkat = 4;
	pol2[3].bilangan = 2;
	pol2[3].x = 'x';
	pol2[3].pangkat = 3;
	pol2[4].bilangan = 2;
	pol2[4].x = 'x';
	pol2[4].pangkat = 2;
	pol2[5].bilangan = 10;}
void fpol3(){
	pol3[0].bilangan = 1;
	pol3[0].x = 'x';
	pol3[0].pangkat = 2;
	pol3[1].bilangan = 5;}
void pengisian_Polinom() {
	fpol1();
	fpol2();
	fpol3();}
void penjumlahan() {
	for (int a = 0; a < sizeof(pol1) / sizeof(polinom); a++){
		for (int b = 0; b < sizeof(pol2) / sizeof(polinom); b++){
			if (pol1[a].pangkat == pol2[b].pangkat){
				penambahan[i].bilangan = pol1[a].bilangan + pol2[b].bilangan;
				penambahan[i].x = pol1[a].x;
				penambahan[i].pangkat = pol1[a].pangkat;
				i++;}}}
	for (int a = 0; a < sizeof(pol1) / sizeof(polinom); a++){
		if (pol1[a].pangkat != penambahan[0].pangkat){
			if (pol1[a].pangkat != penambahan[1].pangkat){
				if (pol1[a].pangkat != penambahan[2].pangkat){
					penambahan[i].bilangan = pol1[a].bilangan;
					penambahan[i].x = pol1[a].x;
					penambahan[i].pangkat = pol1[a].pangkat;
					i++;}}}}
	for (int a = 0; a < sizeof(pol2) / sizeof(polinom); a++){
		if (pol2[a].pangkat != penambahan[0].pangkat){
			if (pol2[a].pangkat != penambahan[1].pangkat){
				if (pol2[a].pangkat != penambahan[2].pangkat){
					penambahan[i].bilangan = pol2[a].bilangan;
					penambahan[i].x = pol2[a].x;
					penambahan[i].pangkat = pol2[a].pangkat;
					i++;}}}}
	for (i = 0; i < sizeof(penambahan) / sizeof(polinom); i++){
		cout << penambahan[i].bilangan << penambahan[i].x << penambahan[i].pangkat << " + ";}
	cout << endl;}
void pengurangan() {
	for (int a = 0; a < sizeof(pol1) / sizeof(polinom); a++){
		for (int b = 0; b < sizeof(pol2) / sizeof(polinom); b++){
			if (pol1[a].pangkat == pol2[b].pangkat){
				penambahan[ikur].bilangan = pol1[a].bilangan - pol2[b].bilangan;
				penambahan[ikur].x = pol1[a].x;
				penambahan[ikur].pangkat = pol1[a].pangkat;
				ikur++;}}}
	for (int a = 0; a < sizeof(pol1) / sizeof(polinom); a++){
		if (pol1[a].pangkat != penambahan[0].pangkat){
			if (pol1[a].pangkat != penambahan[1].pangkat){
				if (pol1[a].pangkat != penambahan[2].pangkat){
					penambahan[ikur].bilangan = pol1[a].bilangan;
					penambahan[ikur].x = pol1[a].x;
					penambahan[ikur].pangkat = pol1[a].pangkat;
					ikur++;}}}}
	for (int a = 0; a < sizeof(pol2) / sizeof(polinom); a++){
		if (pol2[a].pangkat != penambahan[0].pangkat){
			if (pol2[a].pangkat != penambahan[1].pangkat){
				if (pol2[a].pangkat != penambahan[2].pangkat){
					penambahan[ikur].bilangan = pol2[a].bilangan;
					penambahan[ikur].x = pol2[a].x;
					penambahan[ikur].pangkat = pol2[a].pangkat;
					ikur++;}}}}
	for (ikur = 0; ikur < sizeof(penambahan) / sizeof(polinom); ikur++){
		cout << penambahan[ikur].bilangan << penambahan[ikur].x << penambahan[ikur].pangkat << " + ";}
	cout << endl;}
void perkalian(){
	for (int a = 0; a < sizeof(pol1) / sizeof(
                                           polinom); a++){
		for (int b = 0; b < sizeof(pol3) / sizeof(
                                            polinom); b++){
			pengalian[ik].bilangan = pol1[a].bilangan * pol3[b].bilangan;
			pengalian[ik].x = pol1[a].x;
			pengalian[ik].pangkat = pol1[a].pangkat + pol3[b].pangkat;
			ik++;}}
	for (ik = 0; ik < sizeof(pengalian) / sizeof(
                                         polinom); ik++){
		if (pengalian[ik].pangkat == 2){
			pengalian[ik].x = 'x';}
		cout << pengalian[ik].bilangan << pengalian[ik].x << pengalian[ik].pangkat << " + ";}
	cout << endl;}
void turunan(){
	for (int a = 0; a < sizeof(pol2)/sizeof(polinom); a++){
		if (pol2[a].pangkat == 0){
			break;}
		else{
			penurunan[a].bilangan = pol2[a].bilangan * pol2[a].pangkat;
			penurunan[a].x = 'x';
			penurunan[a].pangkat = pol2[a].pangkat - 1;}}
	for (int a = 0; a < sizeof(penurunan) / sizeof(polinom); a++){
		cout << penurunan[a].bilangan << penurunan[a].x << penurunan[a].pangkat << " + ";}}
int main(){
    cout << "P1 = 6x^8 + 8x^7 + 5x^5+ x^3 + 15" << endl;
    cout << "P2 = 3x^9 + 4x^7 + 3x^4 + 2xP^3 + 2x^2 + 10" << endl;
    cout << "P3 = x^2 + 5" << endl;
	pengisian_Polinom();
	cout << "Hasil Penjumlahan : " << endl;
	penjumlahan();
	cout << "Hasil Pengurangan : " << endl;
	pengurangan();
	cout << "Hasil Perkalian   : " << endl;
	perkalian();
	cout << "Hasil Penurunan   : " << endl;
	turunan();}
