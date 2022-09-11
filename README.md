# PSP-assignment
#include <math.h>
#include <stdio.h>
#include <string.h>
#define R 8.314
#define F 96485
int main() {
  char electrode1[50], electrode2[50];
  int feos, feic, Cuous, Curic, Zn, Ni, H, K, Li, Ca, Na, Mg, Al, Cr, Ag, Pt,
      Au_3, Au_1;
  char Lithium[50] = "Li+";
  char Potasium[10] = "K+";
  char Calcium[10] = "Ca+2";
  char Sodium[50] = "Na+";
  char Magnesium[50] = "Mg+2";
  char Alluminium[50] = "Al+3";
  char Zinc[10] = "Zn+2";
  char Chromium[50] = "Cr+3";
  char Ferrous[10] = "Fe+2";
  char Nickel[10] = "Ni+2";
  char Ferric[10] = "Fe+3";
  char Hydrogen[10] = "H+";
  char Cuprous[10] = "Cu+2";
  char cupric[10] = "Cu+";
  char Silver[10] = "Ag+";
  char Platinum[10] = "Pt+2";
  char Gold_3[10] = "Au+3";
  char Gold_1[10] = "Au+";
  int e, f, n, flag;
  double c, d, T, C1, C2, EO_Cell, E_Cell;
  printf("Standard electrode potential values of some elements at 25 degree "
         "are given below \n");
  printf("1.  Li+  ⇌ Li : E0 = -3.04V\n");
  printf("2.  K+   ⇌ K  : E0 = -2.92V \n");
  printf("3.  Ca+2 ⇌ Ca : E0 = -2.87V \n");
  printf("4.  Na+  ⇌ Na : E0 = -2.71V \n");
  printf("5.  Mg+2 ⇌ Mg : E0 = -2.36V \n");
  printf("6.  Al+3 ⇌ Al : E0 = -1.66V \n");
  printf("7.  Zn+2 ⇌ Zn : E0 = -0.76V \n");
  printf("8.  Cr+3 ⇌ Cr : E0 = -0.74V \n");
  printf("9.  Fe+2 ⇌ Fe : E0 = -0.41V \n");
  printf("10. Ni+2 ⇌ Ni : E0 = -0.25V \n");
  printf("11. Fe+3 ⇌ Fe : E0 = -0.04V \n");
  printf("12. H+   ⇌ H2 : E0 =  0V    \n");
  printf("13. Cu+2 ⇌ Cu : E0 = 0.34V \n");
  printf("14. Cu+  ⇌ Cu : E0 = 0.52V  \n");
  printf("15. Ag+  ⇌ Ag : E0 = 0.80V  \n");
  printf("16. Pt+2 ⇌ Pt : E0 = 1.18V  \n");
  printf("17. Au+3 ⇌ Au : E0 = 1.52V  \n");
  printf("18. Au+  ⇌ Au : E0 = 1.83V  \n");
  printf("Enter electrode1 : ");
  scanf("%s", electrode1);
  Li = strcmp(electrode1, Lithium);
  K = strcmp(electrode1, Potasium);
  Ca = strcmp(electrode1, Calcium);
  Na = strcmp(electrode1, Sodium);
  Mg = strcmp(electrode1, Magnesium);
  Al = strcmp(electrode1, Alluminium);
  Zn = strcmp(electrode1, Zinc);
  Cr = strcmp(electrode1, Chromium);
  feos = strcmp(electrode1, Ferrous);
  Ni = strcmp(electrode1, Nickel);
  feic = strcmp(electrode1, Ferric);
  H = strcmp(electrode1, Hydrogen);
  Cuous = strcmp(electrode1, Cuprous);
  Curic = strcmp(electrode1, cupric);
  Ag = strcmp(electrode1, Silver);
  Pt = strcmp(electrode1, Platinum);
  Au_3 = strcmp(electrode1, Gold_3);
  Au_1 = strcmp(electrode1, Gold_1);
  if (Li == 0) {
    c = -3.04;
    e = 1;
  } else if (K == 0) {
    c = -2.92;
    e = 1;
  } else if (Ca == 0) {
    c = -2.87;
    e = 2;
  } else if (Na == 0) {
    c = -2.71;
    e = 1;
  } else if (Mg == 0) {
    c = -2.36;
    e = 2;
  } else if (Al == 0) {
    c = -1.66;
    e = 3;
  } else if (Zn == 0) {
    c = -0.76;
    e = 2;
  } else if (Cr == 0) {
    c = -0.74;
    e = 3;
  } else if (feos == 0) {
    c = -0.44;
    e = 2;
  } else if (Ni == 0) {
    c = -0.25;
    e = 2;
  } else if (feic == 0) {
    c = -0.04;
    e = 3;
  } else if (H == 0) {
    c = 0;
    e = 1;
  } else if (Cuous == 0) {
    c = 0.34;
    e = 2;
  } else if (Curic == 0) {
    c = 0.52;
    e = 1;
  } else if (Ag == 0) {
    c = 0.80;
    e = 1;
  } else if (Pt == 0) {
    c = 1.18;
    e = 2;
  } else if (Au_3 == 0) {
    c = 1.52;
    e = 3;
  } else if (Au_1 == 0) {
    c = 1.83;
    e = 1;
  } else {
    printf("Enter correct Ion ");
  }

  printf("Enter electrode2 : ");
  scanf("%s", electrode2);
  Li = strcmp(electrode2, Lithium);
  K = strcmp(electrode2, Potasium);
  Ca = strcmp(electrode2, Calcium);
  Na = strcmp(electrode2, Sodium);
  Mg = strcmp(electrode2, Magnesium);
  Al = strcmp(electrode2, Alluminium);
  Zn = strcmp(electrode2, Zinc);
  feos = strcmp(electrode2, Ferrous);
  Ni = strcmp(electrode2, Nickel);
  feic = strcmp(electrode2, Ferric);
  H = strcmp(electrode2, Hydrogen);
  Cuous = strcmp(electrode2, Cuprous);
  Curic = strcmp(electrode2, cupric);
  Ag = strcmp(electrode2, Silver);
  Pt = strcmp(electrode2, Platinum);
  Au_3 = strcmp(electrode2, Gold_3);
  Au_1 = strcmp(electrode2, Gold_1);

  if (Li == 0) {
    d = -3.04;
    f = 1;
  } else if (K == 0) {
    d = -2.92;
    f = 1;
  } else if (Ca == 0) {
    d = -2.87;
    f = 2;
  } else if (Na == 0) {
    d = -2.71;
    f = 1;
  } else if (Mg == 0) {
    d = -2.36;
    f = 2;
  } else if (Al == 0) {
    d = -1.66;
    f = 3;
  } else if (Zn == 0) {
    d = -0.76;
    f = 2;
  } else if (Cr == 0) {
    c = -0.74;
    f = 3;
  } else if (feos == 0) {
    d = -0.44;
    f = 2;
  } else if (Ni == 0) {
    d = -0.25;
    f = 2;
  } else if (feic == 0) {
    d = -0.04;
    f = 3;
  } else if (H == 0) {
    d = 0;
    f = 1;
  } else if (Cuous == 0) {
    d = 0.34;
    f = 2;
  } else if (Curic == 0) {
    d = 0.52;
    f = 1;
  } else if (Ag == 0) {
    d = 0.80;
    f = 1;
  } else if (Pt == 0) {
    d = 1.18;
    f = 2;
  } else if (Au_3 == 0) {
    d = 1.52;
    f = 3;
  } else if (Au_1 == 0) {
    d = 1.83;
    f = 1;
  } else {
    printf("Enter correct Ion ");
  }

  printf(" <--------------------------------------------- >");
  printf("\n");
  if (c > d) {
    printf("cathode : ");
    puts(electrode1);
    printf("Anode : ");
    puts(electrode2);
    EO_Cell = c - d;
  } else if (c < d) {
    printf("cathode : ");
    puts(electrode2);
    printf("Anode : ");
    puts(electrode1);
    EO_Cell = d - c;
  }

  printf("EO cell = %lfV \n", EO_Cell);
  n = (e > f) ? e : f;
  flag = 1;
  while (flag) // (flag = 1)
  {
    if (n % e == 0 && n % f == 0) {
      printf("Number of electrons used in the reaction is %d. \n", n);
      break;
    }
    ++n; // pre-increment n
  }
  printf("Enter the value of Temperature in kelivn\n");
  scanf("%lf", &T);
  printf("Concentration of anode :");
  scanf("%lf", &C1);
  printf("Concentration of cathode : ");
  scanf("%lf", &C2);
  E_Cell = (EO_Cell - (2.303 * R * T * log10(C1 / C2)) / (n * F));
  printf("Electrode potential of the cell =  %lfV", E_Cell);
  return 0;
}
