# KDVTutar-
KDV Tutarı Hesaplayan Program
Java ile kullanıcıdan alınan para değerinin KDV'li fiyatını ve KDV tutarını hesaplayıp ekrana bastıran programı yazın.

(Not : KDV tutarını 18% olarak alın)

KDV'siz Fiyat = 10;

KDV'li Fiyat = 11.8;

KDV tutarı = 1.8;

Ödev
Eğer girilen tutar 0 ve 1000 TL arasında ise KDV oranı %18 , tutar 1000 TL'den büyük ise KDV oranını %8 olarak KDV tutarı hesaplayan programı yazınız.

import java.util.Scanner;

public class Main {

    public static void main(String[] args) {
        // variables
        double price, kdvRate, kdvPrice, total;
        Scanner input = new Scanner(System.in);
        System.out.println("Ucret tutarini giriniz : ");
        price = input.nextDouble();
        if(price>=0 && price<=1000){
            kdvRate=0.18;

            kdvPrice = price*kdvRate;
            System.out.println("KDV'siz tutar : " + price);
            System.out.println("KDV'siz orani : " + kdvRate);
            System.out.println("KDV tutari : " + kdvPrice);
            total = price +kdvPrice;
            System.out.println(" KDV'li tutar : " +total);
        } else {
            kdvRate=0.08;

            kdvPrice = price*kdvRate;
            System.out.println("KDV'siz tutar : " + price);
            System.out.println("KDV'siz orani : " + kdvRate);
            System.out.println("KDV tutari : " + kdvPrice);
            total = price +kdvPrice;
            System.out.println(" KDV'li tutar : " +total);
        }
    }
}
