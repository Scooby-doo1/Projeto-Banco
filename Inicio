package Estudo;

import java.util.Scanner;

public class Inicio {

    private static int contadorConvencional = 0;
    private static int contadorPreferencial = 0;
    private static int contadorBlack = 0;

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        while (true) {
            System.out.println("Escolha uma operação:");
            System.out.println("1. Retirar ficha");
            System.out.println("2. Chamar próximo");
            System.out.println("3. Sair");
            System.out.print("Escolha uma opção: ");
            int opcao = scanner.nextInt();

            switch (opcao) {
                case 1:
                    retirarFicha(scanner);
                    break;
                case 2:
                    chamarProximo();
                    break;
                case 3:
                    System.out.println("Saindo...");
                    scanner.close();
                    return;
                default:
                    System.out.println("Opção inválida. Tente novamente.");
            }
        }
    }

    private static void retirarFicha(Scanner scanner) {
        System.out.println("\nEscolha o tipo de ficha:");
        System.out.println("1 - Convencional");
        System.out.println("2 - Preferencial");
        System.out.println("3 - Black");
        System.out.print("Escolha uma opção:");
        int tipoFicha = scanner.nextInt();

        if (tipoFicha == 1) {
            contadorConvencional++;
            System.out.println("Você retirou a ficha convencional número: " + contadorConvencional);
        } else if (tipoFicha == 2) {
            contadorPreferencial++;
            System.out.println("Você retirou a ficha preferencial número: " + contadorPreferencial);
        } else if (tipoFicha == 3) {
            contadorBlack++;
            System.out.println("Você retirou a ficha black número: " + contadorBlack);
        } else {
            System.out.println("Tipo de ficha inválido. Tente novamente.");
        }

        exibirEstatisticas();
    }

    private static void chamarProximo() {
    	//Se contador for maior que 0 Chama pessoa Black primeiro e depois Preferencial
        if (contadorBlack > 0) {
            System.out.println("Chamando pessoa black número: " + contadorBlack);
            contadorBlack--;
        } else if (contadorPreferencial > 0) {
            System.out.println("Chamando pessoa preferencial número: " + contadorPreferencial);
            contadorPreferencial--;
        } else if (contadorConvencional > 0) {
            System.out.println("Chamando pessoa convencional número: " + contadorConvencional);
            contadorConvencional--;
        } else {
            System.out.println("Não há pessoas na fila.");
        }

        exibirEstatisticas();
    }

    private static void exibirEstatisticas() {
        System.out.println("Fichas:");
        System.out.println("\nNúmero de pessoas na fila convencional: " + contadorConvencional);
        System.out.println("Número de pessoas na fila preferencial: " + contadorPreferencial);
        System.out.println("Número de pessoas na fila black: " + contadorBlack + "\n");
    }
}
