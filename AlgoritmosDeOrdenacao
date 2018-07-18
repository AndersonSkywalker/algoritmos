package algoritmosdeordenacao;

import java.util.Scanner;

public class AlgoritmosDeOrdenacao {

    //Bubble Sort
    public static void bubbleSort(int vet[]) {
        int aux;
        boolean controle;
        for (int i = 0; i < vet.length; i++) {
            controle = true;
            for (int j = 0; j < vet.length - 1; j++) {
                if (vet[j] > vet[j + 1]) {
                    aux = vet[j];
                    vet[j] = vet[j + 1];
                    vet[j + 1] = aux;
                    controle = false;
                }
            }
            if (controle) {
                break;
            }
        }
    }

    //insertionSort
    public static void insertionSort(int vetor[]) {
        int j;
        int key;
        int i;

        for (j = 1; j < vetor.length; j++) {
            key = vetor[j];
            for (i = j - 1; (i >= 0) && (vetor[i] > key); i--) {
                vetor[i + 1] = vetor[i];
            }
            vetor[i + 1] = key;
        }
    }

    //selectionSort
    public static void selectionSort(int[] vet) {
        for (int fixo = 0; fixo < vet.length - 1; fixo++) {
            int menor = fixo;

            for (int i = menor + 1; i < vet.length; i++) {
                if (vet[i] < vet[menor]) {
                    menor = i;
                }
            }
            if (menor != fixo) {
                int t = vet[fixo];
                vet[fixo] = vet[menor];
                vet[menor] = t;
            }
        }
    }

    //quickSort
    private static void quickSort(int[] vetor, int inicio, int fim) {
        if (inicio < fim) {
            int posicaoPivo = separar(vetor, inicio, fim);
            quickSort(vetor, inicio, posicaoPivo - 1);
            quickSort(vetor, posicaoPivo + 1, fim);
        }
    }

    //quickSortSeparar
    private static int separar(int[] vetor, int inicio, int fim) {
        int pivo = vetor[inicio];
        int i = inicio + 1, f = fim;
        while (i <= f) {
            if (vetor[i] <= pivo) {
                i++;
            } else if (pivo < vetor[f]) {
                f--;
            } else {
                int troca = vetor[i];
                vetor[i] = vetor[f];
                vetor[f] = troca;
                i++;
                f--;
            }
        }
        vetor[inicio] = vetor[f];
        vetor[f] = pivo;
        return f;
    }

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        //Leitura do tamno do vetor
        int tamanho = sc.nextInt();
        //vetor recebendo o tamanho
        int[] vet = new int[tamanho];
        //Leitura dos dados
        for (int i = 0; i < vet.length; i++) {
            vet[i] = sc.nextInt();
        }
        //Chamando método bolha
        //bubbleSort(vet);

        //Chamada método insertionSort
        //insertionSort(vet);
        //Chamada método quickSort
        //quickSort(vet, 0, (vet.length - 1));
        //Chamada método selectionSort
        //selectionSort(vet);
        //Exibição no console
        for (int i = 0; i < vet.length; i++) {
            if (i == vet.length - 1) {
                System.out.println(vet[i]);
            } else {
                System.out.print(vet[i] + " ");
            }
        }
    }
}
