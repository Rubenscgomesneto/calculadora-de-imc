package teste.executavel;

import java.text.DecimalFormat;
import javax.swing.JOptionPane;

public class imc {

	public static void main(String[] args) {
		DecimalFormat formatador = new DecimalFormat("0.0");
		String peso = JOptionPane.showInputDialog(" Informe seu peso?");
		String altura = JOptionPane.showInputDialog(" Informe sua altura?");

		double pesoNumero = Double.parseDouble(peso);
		double alturaNumero = Double.parseDouble(altura);
		double imc = (double) (pesoNumero / (alturaNumero * alturaNumero));

		JOptionPane.showMessageDialog(null, " Seu IMC é : " + formatador.format(imc));
		if (imc < 18.6) {
			JOptionPane.showMessageDialog(null, " Abaixo do peso ");

		} else if (imc >= 18.6 && imc <= 24.9) {
			JOptionPane.showMessageDialog(null, " peso normal");

		} else if (imc >= 25 && imc <= 29.9) {
			JOptionPane.showMessageDialog(null, " sobre peso");

		} else if (imc >= 30 && imc <= 34.9) {
			JOptionPane.showMessageDialog(null, " Obesidade grau 1");

		} else if (imc >= 35 && imc <= 39.9) {
			JOptionPane.showMessageDialog(null, " Obesidade grau 2");

		} else if (imc >= 40) {
			JOptionPane.showMessageDialog(null, " Obesidade grau 3");

		}

	}
}
