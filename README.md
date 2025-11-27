package ZAD_BOOK;

	public class book {
	
	private String Zaglavie;
	private String Avtor;
	private int stranici;
	private double cena;
	public book() {
		this.setZaglavie("Pod IGoto");
	   this. setAvtor("Vazov");
	   this. setStranici(12);
	   this. setCena(0);
	}

	public book(String Zaglavie, String Avtor, int	 stranici, double cena) {
	    
	    setZaglavie(Zaglavie);
	    setAvtor(Avtor);
	    setStranici(stranici);
	    setCena(cena);
	}


public void setZaglavie(String Zaglavie) {
	if(Zaglavie.length()>40)
	throw new IllegalArgumentException("Long Title!");
    this.Zaglavie = Zaglavie;
}

public void setAvtor(String Avtor) {
	if(Avtor.length()>30)
	throw new IllegalArgumentException("Long name of the Author!");
    this.Avtor = Avtor;
}

public void setStranici(int stranici) {
	if(stranici<0)
		throw new IllegalArgumentException("Invalid Pages!");
    this.stranici = stranici;
}

public void setCena(double cena) {
	if(cena<0)
	throw new IllegalArgumentException("Invalid Price!");
    this.cena = cena;
}
public void cutPages(int stranici) {
	if(this.stranici<=stranici)
		this.stranici=0;
	else
		this.stranici-=stranici;
}
// Методи за достъп (getter-и)


public String getZaglavie() {
    return this.Zaglavie;
}

public String getAvtor() {
    return this.Avtor;
}

public double getStranici() {
    return this.stranici;
}

public double getCena() {
    return this.cena;
}

@Override
public String toString() {
	return "book [Zaglavie=" + Zaglavie + ", Avtor=" + Avtor + ", stranici=" + stranici + ", cena=" + cena + "]";
}




}
