import 'dart:io';

int toplama(int sayi, int sayi2) {
  return sayi + sayi2;
}

int cikarma(int sayi, int sayi2) {
  return sayi - sayi2;
}

int carpma(int sayi, int sayi2) {
  return sayi * sayi2;
}

double bolme(double sayi, double sayi2) {
  return sayi / sayi2;
}

void main() {
  bool devam = true;
  while (devam) {
    print("Yapmak istediğiniz işlemi seçiniz!");
    print("1 - Toplama");
    print("2 - Çıkarma");
    print("3 - Çarpma");
    print("4 - Bölme");
    int? secim = int.parse(stdin.readLineSync()!);

    print("Sırayla sayıları giriniz : ");
    double? sayi = double.parse(stdin.readLineSync()!);
    double? sayi2 = double.parse(stdin.readLineSync()!);

    switch (secim) {
      case 1:
        print("Sonuç: ${toplama(sayi.toInt(), sayi2.toInt())}");
        break;
      case 2:
        print("Sonuç: ${cikarma(sayi.toInt(), sayi2.toInt())}");
        break;
      case 3:
        print("Sonuç: ${carpma(sayi.toInt(), sayi2.toInt())}");
        break;
      case 4:
        if (sayi2 != 0) {
          print("Sonuç: ${bolme(sayi, sayi2)}");
        } else {
          print("Bir sayı sıfıra bölünemez.");
        }
        break;
      default:
        print("Böyle bir işlem bulunmamaktadır.");
    }

    print("Başka bir işlem yapmak istiyor musunuz? (E/H)");
    String cevap = stdin.readLineSync()!;
    if (cevap.toUpperCase() != "E") {
      devam = false;
    }
  }
}
# Hesap-Makinesi
