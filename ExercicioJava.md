
package atividadeaula6;

import java.util.Scanner;

public class AtividadeAula6 {
    public static void main(String[] args) {
        Scanner leia = new Scanner(System.in);
        
        float totalIdade = 0, totalAltura = 0, totalPeso = 0, idade, altura, peso;
        int numPessoas = 0, numOlhosVerdesCabeloLouros = 0, numMasc = 0, numFem = 0;
        String sexo, corOlho, corCabelo;
        double mediaIdade, mediaPeso, mediaAltura, porcentagemMulheres, porcentagemHomens ;
        String continuar = "sim";

        while (continuar.equalsIgnoreCase("sim")) {
        System.out.println("Informe seu sexo (Masculino/Feminino):  ");
        sexo = leia.next();
            
        System.out.println("Informe a cor dos seus olhos (Azul/Verde/Castanho):  ");
        corOlho = leia.next();
            
        System.out.println("Informe a cor do seu cabelo (Louro/Castanho/Preto):  ");
        corCabelo = leia.next();
            
        System.out.println("Informe sua idade:  ");
        idade = leia.nextFloat();
            
        System.out.println("Informe sua altura:  ");
        altura = leia.nextFloat();
            
        System.out.println("Informe seu peso:  ");
        peso = leia.nextFloat();
            
            
        totalIdade += idade;
        totalPeso += peso;
        totalAltura += altura;
        numPessoas++;
            
           
        if (sexo.equalsIgnoreCase("feminino")) {
           numFem++;
        }else if (sexo.equalsIgnoreCase("masculino")) {
            numMasc++;
        }
            
            
        if (corOlho.equalsIgnoreCase("verde") && corCabelo.equalsIgnoreCase("louro")) {
            numOlhosVerdesCabeloLouros++;
        }

            
        System.out.println("Deseja adicionar mais uma pessoa? (Sim/Não)");
        continuar = leia.next();
        }

        
        mediaIdade = totalIdade / numPessoas;
        mediaPeso = totalPeso / numPessoas;
        mediaAltura = totalAltura / numPessoas;

        
        porcentagemMulheres = (numFem / (double) numPessoas) * 100;
        porcentagemHomens = (numMasc / (double) numPessoas) * 100;

        System.out.println("Resultados da pesquisa:");
        System.out.println("Média da idade: " + mediaIdade);
        System.out.println("Média do peso: " + mediaPeso);
        System.out.println("Média da altura: " + mediaAltura);
        System.out.println("Porcentagem de pessoas do sexo feminino: " + porcentagemMulheres + "%");
        System.out.println("Porcentagem de pessoas do sexo masculino: " + porcentagemHomens + "%");
        System.out.println("Número de pessoas com olhos verdes e cabelos louros: " + numOlhosVerdesCabeloLouros);
    }
}
