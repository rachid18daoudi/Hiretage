# Hiretage

public class Article
{
    public string designation;
    public double prix;
}
public Article(string designation,double prix)
{
    this.designation=designation;
    this.prix=prix;
}
public override string ToString()
{
    return this.designation+" "+this.prix;
}
public class Livre :Article
{
    public string isbn;
    public int nbrpages;
}
public Livre(string designation,double prix,string isbn,int nbrpages):base(designation,prix)
{
    this.isbn=isbn;
    this.nbrpages=nbrpages;
}
public override string ToString()
{
    return base.ToString+" "+this.isbn+" "+this.nbrpages;
}
class Disque : Article
{
    private string label ;
}
public Disque(string designation,double prix,string label):base(designation,prix)
{
    this.label=label;
}
public override string ToString()
{
    return base.ToString+" "+this.label;
}
public class Video :Article
{
    private int duree;
    
}
public duree(string designation,double prix,int duree):base(designation,prix)
{
    this.duree=duree;
}
public override string ToString()
{
    return base.ToString+" "+this.duree;
}
class programme
{
    static Void Mais(){
        Article article = new Article("Le Figaro", 100);
        Console.WriteLine(article);
        Livre livre = new Livre("Programmation", 200, "BN101202", 320);
        Console.WriteLine(livre);
        Disque disque = new Disque("Rock", 450, "Metallica");
        Console.WriteLine(disque);
        Video video = new Video("Java", 450, 12.5);
        Console.WriteLine(video);
        Console.WriteLine();
    }
    
}
