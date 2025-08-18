# aulas-segundo-info-etec
Repositório para gerenciar códigos da disciplina de Computacao em nuvem

import java.util.Scanner;

public class Cadastro {

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        // Instanciando 3 objetos da classe Pessoa
        Pessoa registro1 = new Pessoa();
        Pessoa registro2 = new Pessoa();
        Pessoa registro3 = new Pessoa();

        // Coletando dados para o primeiro registro
        System.out.println("Cadastro da Primeira Pessoa:");
        System.out.print("Digite o código: ");
        registro1.setCodigo(scanner.nextInt());
        scanner.nextLine(); // Consome a nova linha
        System.out.print("Digite o nome: ");
        registro1.setNome(scanner.nextLine());
        System.out.print("Digite a idade: ");
        registro1.setIdade(scanner.nextInt());

        // Coletando dados para o segundo registro
        System.out.println("\nCadastro da Segunda Pessoa:");
        System.out.print("Digite o código: ");
        registro2.setCodigo(scanner.nextInt());
        scanner.nextLine(); // Consome a nova linha
        System.out.print("Digite o nome: ");
        registro2.setNome(scanner.nextLine());
        System.out.print("Digite a idade: ");
        registro2.setIdade(scanner.nextInt());

        // Coletando dados para o terceiro registro
        System.out.println("\nCadastro da Terceira Pessoa:");
        System.out.print("Digite o código: ");
        registro3.setCodigo(scanner.nextInt());
        scanner.nextLine(); // Consome a nova linha
        System.out.print("Digite o nome: ");
        registro3.setNome(scanner.nextLine());
        System.out.print("Digite a idade: ");
        registro3.setIdade(scanner.nextInt());

        // Determinando a pessoa mais velha
        String nomeMaisVelho = "";
        int idadeMaisVelha = 0;

        if (registro1.getIdade() > idadeMaisVelha) {
            idadeMaisVelha = registro1.getIdade();
            nomeMaisVelho = registro1.getNome();
        }

        if (registro2.getIdade() > idadeMaisVelha) {
            idadeMaisVelha = registro2.getIdade();
            nomeMaisVelho = registro2.getNome();
        }

        if (registro3.getIdade() > idadeMaisVelha) {
            idadeMaisVelha = registro3.getIdade();
            nomeMaisVelho = registro3.getNome();
        }

        // Imprimindo o resultado
        System.out.println("\n--- Resultado ---");
        System.out.println("A pessoa mais velha é: " + nomeMaisVelho);
        
        scanner.close();
    }
}
