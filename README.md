# Par1_programacion2
class Libro {
private String titulo;
private String autor;
private String propietario;
private double precio;

public Libro(String titulo, String autor) {
this.titulo = titulo;
this.autor = autor;
}
public String getTitulo() {
return titulo;
}
public void setTitulo(String titulo) {
 this.titulo = titulo;
}
public String getAutor() {
return autor;
}
public void setAutor(String autor) {
this.autor = autor;
}
public String getPropietario() {
return propietario;
}
public void setPropietario(String propietario) {
this.propietario = propietario;
}
public double getPrecio() {
return precio;
}
public void setPrecio(double precio) {
this.precio = precio;
}
public void imprimirInfo() {
System.out.println("Título: " + titulo);
System.out.println("Autor: " + autor);
System.out.println("Precio: " + precio);
System.out.println("Propietario: " + propietario);
}
}

class LibroTexto extends Libro {
private String curso;

public LibroTexto(String titulo, String autor, String curso) {
super(titulo, autor);
this.curso = curso;
}
public String getCurso() {
return curso;
}
public void setCurso(String curso) {
this.curso = curso;
}
public void imprimirInfo() {
super.imprimirInfo();
System.out.println("Curso: " + curso);
}
}

class LibroTextoInstitucion extends LibroTexto {
private String facultad;

public LibroTextoInstitucion(String titulo, String autor, String curso, String facultad) {
super(titulo, autor, curso);
 this.facultad = facultad;
}

public String getFacultad() {
return facultad; }

public void setFacultad(String facultad) {
this.facultad = facultad;
}

public void imprimirInfo() {
super.imprimirInfo();
System.out.println("Facultad: " + facultad);
    }
}

class Novela extends Libro {
private String tipo;

public Novela(String titulo, String autor, String tipo) {
super(titulo, autor);
this.tipo = tipo;
}
public String getTipo() {
return tipo;
}
public void setTipo(String tipo) {
this.tipo = tipo;
}
public void imprimirInfo() {
super.imprimirInfo();
System.out.println("Tipo: " + tipo);
}
}
public class Main {
public static void main(String[] args) {
// Objeto de la clase LibroTextoInstitucion
LibroTextoInstitucion libroTextoInstitucion = new LibroTextoInstitucion(
 " Matematicas 2 ", "Luis Fernando Mosquera ", "Matemáticas", "Facultad Ingenierias");
libroTextoInstitucion.setPropietario("Zamira Tamayo Moritz");
libroTextoInstitucion.setPrecio(150000);
libroTextoInstitucion.imprimirInfo();

System.out.println();
// Objeto de la clase Novela
Novela novela = new Novela("Romper el circulo ", "Collen hoover", "Ciencia Ficción" );
novela.setPropietario("Zamira Tamayo Moritz");
novela.setPrecio(90000);
novela.imprimirInfo();
}
}
