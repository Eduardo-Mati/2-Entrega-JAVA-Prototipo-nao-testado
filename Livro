package Biblioteca_2_fase;

import java.util.Objects;

public class Livro extends Material{

    private Genero genero;

    public Livro(String Autor,String Titulo,Genero genero) {
        super(Autor,Titulo);
        this.genero = genero;

    }

    public Genero getGenero() {
        return genero;
    }

    @Override
    public boolean equals(Object o) {
        if (!(o instanceof Livro livro)) return false;
        return genero == livro.genero;
    }

    @Override
    public int hashCode() {
        return Objects.hashCode(genero);
    }
}
