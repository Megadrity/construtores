Telefone:
public abstract class Telefone{
 public Integer codigodopais;
 public Integer ddd;
 public Decimal numero;

    public Telefone(Integer codigodopais, Integer ddd, Decimal numero){ 
      this.codigodopais = codigodopais;
      this.ddd = ddd;
      this.numero = numero;
    }

    public Telefone(){} // Adicionando um construtor padrão vazio

    public Integer getcodigodopais(){
        return codigodopais; 
    }
     public void setcodigodopais(Integer codigodopais) {
        this.codigodopais = codigodopais;
    }
    public Integer getddd(){
        return ddd; 
    }
     public void setddd(Integer ddd) {
        this.ddd = ddd;
    }
     public Decimal getnumero(){
        return numero; 
    }
     public void setnumero(Decimal numero){
        this.numero = numero;
    }

}
Smartphone:
public virtual class Smartphone extends Telefone{
  public String marca;
  public String modelo; 
  public Boolean internet;
  public Decimal preco;

  public Smartphone(String marca, String modelo, Boolean internet, Decimal preco, Integer codigodopais, Integer ddd, Decimal numero){ 
    super(codigodopais, ddd, numero);
    this.marca = marca;
    this.modelo = modelo;
    this.internet = internet;
    this.preco = preco;
  }

  public Smartphone(){}

  public String getmarca(){
    return marca; 
  }

  public void setmarca(String marca){
    this.marca = marca;
  }

  public String getmodelo(){
    return modelo; 
  }

  public void setmodelo(String modelo) {
    this.modelo = modelo;
  }

  public Boolean getinternet(){
    return internet; 
  }

  public void setinternet(Boolean internet) {
    this.internet = internet;
  }

  public Decimal getpreco(){
    return preco; 
  }

  public void setpreco(Decimal preco) {
    this.preco = preco;
  }

  public void exibirDados(){ 
    System.debug('O número do Smartphone é: ' + getnumero());
    System.debug('A marca do Smartphone é: ' + marca);
    System.debug('A modelo do Smartphone é: ' + modelo);
    System.debug('É 5G: ' + internet);
    System.debug('O preço do Smartphone é: ' + preco);
  }

  public void exibirDadosTelefone(){
    System.debug('Número do telefone: ' + getnumero());
  }
}
