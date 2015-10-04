# homework2
package Friends;

import java.util.ArrayList;

import java.util.List;
import java.util.Scanner;

/**
 * Created by Princess Of Persia on 03/10/2015.
 */
public class Personne {
    private String Nom;
    private String Prenom;
    private String Nationalite;
    private int Age;
    public List<Personne> Amis = new ArrayList<>();
    public List<Personne> MesAmis = new ArrayList<>();
    public List<Personne> AmisAlgerien = new ArrayList<>();
    public List<Personne> AmisEtrangers = new ArrayList<>();

    Scanner scanner = new Scanner(System.in);

    public void Compte(){
        System.out.println("pour cree un compte vous devez remplir les champs suivant:");
        Scanner scanner = new Scanner(System.in);
        System.out.print("Ercis Ton Nom\t");
        String Nom = scanner.nextLine();
        System.out.print("Ecris Ton Prenom\t");
        String Prenom = scanner.nextLine();
        System.out.print("Ecris Ta Nationalite\t");
        String nationalite = scanner.nextLine();
        System.out.print("Ecris Ton Age\t");
        int age = scanner.nextInt();
    }

    public Personne(){}

    public Personne(String LastName,String FirstName, String Nationality, int Age){
        this.Nom = LastName;
        this.Prenom = FirstName;
        this.Nationalite = Nationality;
        this.Age = Age;
    }


    public void setNom(String nom) {
        Nom = nom;
    }

    public String getNom() {
        return Nom;
    }

    public void setPrenom(String prenom) {
        Prenom = prenom;
    }

    public String getPrenom() {
        return Prenom;
    }

    public void setNationalite(String nationalite) {
        Nationalite = nationalite;
    }

    public String getNationalite() {
        return Nationalite;
    }

    public void setAge(int age) {
        Age = age;
    }

    public int getAge() {
        return Age;
    }

    public void CreeListAmis(){

        Amis.add(new Personne("Sihem","Bousseta","Algerienne",20));
        Amis.add(new Personne("Ilyes","Hammadi","Algerien",21));
        Amis.add(new Personne("Nadia","Maghraoui","Algerienne",20));
        Amis.add(new Personne("Djalil","Fortas","Algerien",20));
        Amis.add(new Personne("David","Montgomrie","Americain",22));
        Amis.add(new Personne("Marten","Mister","Francais",26));
        Amis.add(new Personne("Ally","jones","Anglaise",21));
        Amis.add(new Personne("Miley","Forchten","Italienne",18));
    }

    public void AjouterAmis(){
        System.out.println("quel amis veux tu ajouter?");
        int choix = scanner.nextInt();

            switch (choix) {
                case 1:
                    MesAmis.add(Amis.get(0));
                    Amis.remove(0);
                    break;
                case 2:
                    MesAmis.add(Amis.get(1));
                    Amis.remove(1);
                    break;
                case 3:
                    MesAmis.add(Amis.get(2));
                    Amis.remove(2);
                    break;
                case 4:
                    MesAmis.add(Amis.get(3));
                    Amis.remove(3);
                    break;
                case 5:
                    MesAmis.add(Amis.get(4));
                    Amis.remove(4);
                    break;
                case 6:
                    MesAmis.add(Amis.get(5));
                    Amis.remove(5);
                    break;
                case 7:
                    MesAmis.add(Amis.get(6));
                    Amis.remove(6);
                    break;
                case 8:
                    MesAmis.add(Amis.get(7));
                    Amis.remove(7);
                    break;

            }



    }

    public void MaListAmis(){
        MesAmis.add(new Personne("Hichem","Med","Algerien",20));
        MesAmis.add(new Personne("Hadjer","Bezghoud","Algerienne",19));
        MesAmis.add( new Personne("Maria","chris","americaine",28));
    }

    public void afficheListAmisPourAjouter(){
        for (int i = 0; i < Amis.size(); i++) {

            System.out.println(i + 1 + " " + Amis.get(i).getNom() + " " + Amis.get(i).getPrenom() + " " + Amis.get(i).getNationalite() + " " + Amis.get(i).getAge());
        }
    }

    public void afficheMaListAmis(){
        for (int i = 0; i < MesAmis.size(); i++) {

            System.out.println(i + 1 + " " + MesAmis.get(i).getNom() + " " + MesAmis.get(i).getPrenom() + " " + MesAmis.get(i).getNationalite()+" "+MesAmis.get(i).getAge());

        }
    }

    public void DifferentsAmis(){
        for (int i = 0; i < MesAmis.size(); i++) {

            String p = MesAmis.get(i).getNationalite();
            if (p == "Algerien" || p == "Algerienne")
                AmisAlgerien.add(MesAmis.get(i));
            else AmisEtrangers.add(MesAmis.get(i));
        }
    }

    public void AmisEtrangers() {

        for (int i = 0; i <AmisEtrangers.size() ; i++) {
            System.out.println(i+1+" "+AmisEtrangers.get(i).getNom()+" "+AmisEtrangers.get(i).getPrenom()+" "+AmisEtrangers.get(i).getNationalite()+" "+AmisEtrangers.get(i).getAge());
        }
    }

    public void AmisAlgeriens(){
        for (int i = 0; i <AmisAlgerien.size() ; i++) {
            System.out.println(i+1+" "+AmisAlgerien.get(i).getNom()+" "+AmisAlgerien.get(i).getPrenom()+" "+AmisAlgerien.get(i).getNationalite()+" "+AmisAlgerien.get(i).getAge());
        }

    }

}
