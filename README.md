# VEICULOCARRO
package Automovel
public class Carro implements Veiculo{

	private String marca;
	private String modelo;
	private int velocidade;
	private int marcha;
	private boolean ligado; 
	
	@Override
	public void ligar() {
		if(this.ligado==false && this.marcha==0)
			this.ligado=true;
		else
			System.out.println("Erro! Verifique a marcha e se o carro já esta ligado");
		
	}

	@Override
	public void desligar() {
		if(this.ligado==true && this.marcha==0 && this.velocidade==0)
			this.ligado=false;
		else
			System.out.println("Erro! Verifique a marchar se o carro esta desligado e parado");
		
	}

	@Override
	public void acelerar() {
		if(this.ligado==true && this.marcha!=0)
			this.velocidade++;
		else
			System.out.println("Erro! Verifique a marcha e se o carro esta ligado");
			
	}

	@Override
	public void freiar() {
		if(this.ligado==true && this.velocidade>0)
			this.velocidade--;
		else
			System.out.println("Erro! Verifique a velocidade e se o carro esta ligado" );
	}

	@Override
	public void trocarMarcha() {
		this.marcha++;
		
	}

	public String getMarca() {
		return marca;
	}

	public void setMarca(String marca) {
		this.marca = marca;
	}

	public String getModelo() {
		return modelo;
	}

	public void setModelo(String modelo) {
		this.modelo = modelo;
	}

	public int getVelocidade() {
		return velocidade;
	}

	public int getMarcha() {
		return marcha;
	}

	public boolean getLigado() {
		return ligado;
	}
		} 
	
