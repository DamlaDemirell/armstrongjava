# 
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {

        System.out.println("Basamak sayılarının toplamını hesaplayan programdır.");
        // Basamak Sayısı Bulma İşlemi
        // 2451 / 10 = 245
        // 245 / 10 = 24
        // 24 / 10 = 2
        // 2 / 10 = 0
        // 0 / 10 = 0
        Scanner input = new Scanner(System.in);
        int number, tempNumber, numberCounter=0,total=0,basamakDegeri;
        System.out.print("Bir sayı giriniz:");
        number = input.nextInt();
        tempNumber = number;
        while (tempNumber != 0)
        {
            tempNumber = tempNumber / 10;
            numberCounter++;
        }
        System.out.println("Basamak sayısı" + numberCounter);
        tempNumber = number;
        while(tempNumber !=0)
        {
            basamakDegeri = tempNumber % 10;
            total += basamakDegeri;
            tempNumber = tempNumber / 10;
        }
        System.out.println("Basamak Sayiların Toplmaı: "+ total);

    }
}
