package Biblioteca_2_fase;


import java.util.ArrayList;
import java.util.InputMismatchException;
import java.util.Scanner;

public class Biblioteca {
    Scanner scan = new Scanner(System.in);

    private ArrayList<Livro> livros;
    private ArrayList<Revista> revistas;

    public Biblioteca(){
        this.livros = new ArrayList<>();
        this.revistas = new ArrayList<>();
    }

    public void adicionarLivro(Scanner scan){
        System.out.println("Digite o autor do livro: ");
        scan.nextLine();
        String autor = scan.nextLine();
        System.out.println("Digite o título do livro: ");
        String titulo = scan.nextLine();
        Genero genero = null;

        System.out.println("Selecione o gênero do livro: "+"\n1) Ação "+"\n2) Aventura"+"\n3) Romance"+
                "\n4) Terror"+"\n5) Suspense"+"\n6) Informátivo");
        System.out.println("Selecione uma opção: ");
        int opcaoUsuario = scan.nextInt();

        try{

            switch (opcaoUsuario){

                case 1:
                    genero = Genero.AÇÃO;
                    break;
                case 2:
                    genero = Genero.AVENTURA;
                    break;
                case 3:
                    genero = Genero.ROMANCE;
                    break;
                case 4:
                    genero = Genero.TERROR;
                    break;
                case 5:
                    genero = Genero.SUSPENSE;
                    break;
                case 6:
                    genero = Genero.INFORMÁTIVO;
                    break;
                default:
                    System.out.println("Opção inválida, tente novamente...");
            }


        }catch (InputMismatchException e){
            System.out.println("Opção inválida, tente novamente...");
        }
        if(livros.contains(titulo)){
            System.out.println("Livro já cadastrado, tente novamente...");
        }else {
            Livro livro1 = new Livro(autor, titulo, genero);
            System.out.println("Livro adicionado com sucesso!!!");
            livros.add(livro1);
        }
    }

    public void removerLivro(Scanner scan){
        if(livros.isEmpty()){
            System.out.println("Não há livros cadastrados.");
        }else {
            System.out.println("Digite o título do livro que você deseja remover: ");
            scan.nextLine();
            String tituloRemove = scan.nextLine();

            for (Livro livro : livros) {
                if (livro.getTitulo().equalsIgnoreCase(tituloRemove)) {
                    livros.remove(livro);
                    System.out.println("Livro removido com sucesso!!!");
                }
            }
        }
    }

    public void adicionarRevista(Scanner scan){

        System.out.println("Digite o autor da revista: ");
        scan.nextLine();
        String autorRevista = scan.nextLine();
        System.out.println("Digite o título da revista: ");
        String tituloRevista = scan.nextLine();
        System.out.println("Digite o número da revista: ");
        int numeroRevista = scan.nextInt();

        Boolean livroExistente = false;
        for (Revista revista : revistas){

            if(revista.getTitulo().equals(revista)){
                livroExistente = true;
            }
        }

        if(livroExistente == true){
            System.out.println("Livro já cadastrado, tente novamente...");
        }else {
            Revista revista1 = new Revista(autorRevista, tituloRevista,numeroRevista);
            revistas.add(revista1);
            System.out.println("Revista adicionada com sucesso!!!");
        }

    }

    public void removerRevista(Scanner scan){

        if(revistas.isEmpty()){
            System.out.println("Não há revistas a serem removidas.");

        }else{
            System.out.println("Digite a revista que você quer remover: ");
            String tituloRemove = scan.nextLine();
            for (Revista revista : revistas){
                if (revista.getTitulo().equalsIgnoreCase(tituloRemove)){
                    revistas.remove(revista);
                    System.out.println("Revista removida com sucesso!!!");
                }

            }
        }
    }

    public void listarLivros(){

       if(livros.isEmpty()){
           System.out.println("Não há livros cadastrados.");
       }else{
           for(Livro livro : livros){
               System.out.println(livro);
               System.out.println("Gênero = " + livro.getGenero());;
           }
       }
    }

    public void listarRevistas(){

        if(revistas.isEmpty()){
            System.out.println("Não há revistas cadastradas.");
        }else{
            for(Revista revista : revistas){
                System.out.println(revista);
                System.out.println("Código = "+ revista.getNumero());
            }
        }
    }

    public void pesquisarLivro(Scanner scan){

        if(livros.isEmpty()){
            System.out.println("Não há livros cadastrados.");
        }else {
            System.out.println("Selecione o gênero do livro que você deseja pesquisar: " + "\n1) Ação " + "\n2) Aventura" + "\n3) Romance" +
                    "\n4) Terror" + "\n5) Suspense" + "\n6) Informátivo");
            System.out.println("Selecione uma opção: ");
            int opcaoUsuario = scan.nextInt();
            Genero generoPesquisa = null;


            try {

                switch (opcaoUsuario) {

                    case 1:
                        generoPesquisa = Genero.AÇÃO;
                        break;
                    case 2:
                        generoPesquisa = Genero.AVENTURA;
                        break;
                    case 3:
                        generoPesquisa = Genero.ROMANCE;
                        break;
                    case 4:
                        generoPesquisa = Genero.TERROR;
                        break;
                    case 5:
                        generoPesquisa = Genero.SUSPENSE;
                        break;
                    case 6:
                        generoPesquisa = Genero.INFORMÁTIVO;
                        break;
                    default:
                        System.out.println("Opção inválida, tente novamente...");
                }


            } catch (InputMismatchException e) {
                System.out.println("Opção inválida, tente novamente...");
            }

            for (Livro livro : livros) {
                if (livro.getGenero().equals(generoPesquisa)) {
                    System.out.println(livro);
                }
            }
        }
    }
    public void pesquisarRevista(Scanner scan){

        System.out.println("Digite o código da revista");
        int codigoPesquisa = scan.nextInt();

        for(Revista revista : revistas){
            if(revista.getNumero() == codigoPesquisa){
                System.out.println(revista);
            }
        }
    }
}
