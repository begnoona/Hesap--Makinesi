import java.util.Scanner;

public class hesap {

    static int plus(int a,int b){
    
        int result=a+b;
        
        System.out.println("toplama: "+result);
        
        return result;
        
    }
    static int sub(int a,int b){
    
        int result= b-a;
        
        System.out.println("çıkarma: "+result);
        
        return result;
    }
    static int imp(int a,int b){
        int result=a*b;
        System.out.println("çarpma: "+result);
        return result;
    }
    static int divide(int a, int b){
        int result=a/b;
        System.out.println("Bölme: "+result);
        return result;
    }
    static int behaved(int a,int b){
        int result=1;
        for(int i=1;i<=b;i++){
            result*=a;
        }
        System.out.println("üs alma: "+result);
        return result;
    }
    static int mod(int a,int b){
        int result=a%b;
        System.out.println("mod alma: "+result);
        return result;
    }

    public static void main(String[] args) {
        Scanner input=new Scanner(System.in);
        int select;
        String menu="1- Toplama İşlemi\n"
                + "2- Çıkarma İşlemi\n"
                + "3- Çarpma İşlemi\n"
                + "4- Bölme işlemi\n"
                + "5- Üslü Sayı Hesaplama\n"
                + "6- Mod Alma\n"
                + "0- Çıkış Yap";
        while(true){
            System.out.println(menu);
            System.out.println("Bir işlem seçiniz: ");
            select=input.nextInt();
            if(select==0){
                break;
            }
            System.out.println("ilk sayı: ");
            int a =input.nextInt();
            System.out.println("ikinci sayı: ");
            int b =input.nextInt();
            switch (select){
                case 1:
                    plus(a,b);
                    break;
                case 2:
                    sub(a,b);
                    break;
                case 3:
                    imp(a,b);
                    break;
                case 4:
                    if(b==0){
                        System.out.println("Bir sayı sıfıra bölünemez.");
                    }else{
                        divide(a,b);
                    }
                    break;
                case 5:
                    behaved(a,b);
                    break;
                case 6:
                    mod(a,b);
                    break;
                default:
                    System.out.println("Geçersiz bir işlem girdiniz");
                    break;




            }
        }



    }
}
