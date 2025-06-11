package Biblioteca_2_fase;


import java.util.InputMismatchException;
import java.util.Scanner;

public class Main {

    public static void main(String[] args) {
        Scanner scan = new Scanner(System.in);
        int opcaoUsuario = 0;
        Biblioteca biblioteca = new Biblioteca();

        do{
            System.out.println("__________MENU__________"+"\n1) Adicionar livro"+"\n2) Adicionar revista"+
                    "\n3) Exibir livros"+"\n4) Exibir revistas"+"\n5) Excluir livro"+"\n6) Excluir revista"+"\n7) Pesquisar livros por gênero"+
                    "\n8) Pesquisar revista por código"+"\n9) Sair do sistema");
            System.out.println("Selecione uma opção: ");
            opcaoUsuario = scan.nextInt();

            try {

                switch (opcaoUsuario){

                    case 1:
                        biblioteca.adicionarLivro(scan);
                        break;
                    case 2:
                        biblioteca.adicionarRevista(scan);
                        break;
                    case 3:
                        biblioteca.listarLivros();
                        break;
                    case 4:
                        biblioteca.listarRevistas();
                        break;
                    case 5:
                        biblioteca.removerLivro(scan);
                        break;
                    case 6:
                        biblioteca.removerRevista(scan);
                        break;
                    case 7:
                        biblioteca.pesquisarLivro(scan);
                        break;
                    case 8:
                        biblioteca.pesquisarRevista(scan);
                        break;
                    case 9:
                        System.out.println("Saindo do sistema");
                        break;
                    default:
                        System.out.println("Opção inválida, tente novamente...");


                }

            }catch (InputMismatchException e){
                System.out.println("Opção inválida, tente novamente... ");
            }

        }while(opcaoUsuario != 9);


    }
}
