package Biblioteca_2_fase;

import java.util.Objects;

public class Revista extends Material{

    private int numero;

    public Revista(String autor, String titulo, int numero) {
        super(autor, titulo);
        this.numero = numero;
    }

    public int getNumero() {
        return numero;
    }

    @Override
    public boolean equals(Object o) {
        if (o == null || getClass() != o.getClass()) return false;
        Revista revista = (Revista) o;
        return numero == revista.numero;
    }

    @Override
    public int hashCode() {
        return Objects.hashCode(numero);
    }
}
