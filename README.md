# proyecto-herencia-act-3

Clase base: Vehiculo
public class Vehiculo {
    protected String marca;
    protected int año;

    public Vehiculo(String marca, int año) {
        this.marca = marca;
        this.año = año;
    }

    public void mostrarInformacion() {
        System.out.println("Marca: " + marca);
        System.out.println("Año: " + año);
    }
}

Clase derivada: Automovil
public class Automovil extends Vehiculo {
    private int puertas;

    public Automovil(String marca, int año, int puertas) {
        super(marca, año);
        this.puertas = puertas;
    }

    @Override
    public void mostrarInformacion() {
        super.mostrarInformacion();
        System.out.println("Puertas: " + puertas);
    }

    public void encenderRadio() {
        System.out.println("Radio encendida.");
    }
}

Clase derivada: Motocicleta
public class Motocicleta extends Vehiculo {
    private int cilindrada;

    public Motocicleta(String marca, int año, int cilindrada) {
        super(marca, año);
        this.cilindrada = cilindrada;
    }

    @Override
    public void mostrarInformacion() {
        super.mostrarInformacion();
        System.out.println("Cilindrada: " + cilindrada + " cc");
    }

    public void hacerCaballito() {
        System.out.println("La motocicleta realiza un caballito.");
    }
}

Programa principal
public class Principal {
    public static void main(String[] args) {

        Automovil auto = new Automovil("Toyota", 2024, 4);
        Motocicleta moto = new Motocicleta("Yamaha", 2023, 600);

        System.out.println("=== Automóvil ===");
        auto.mostrarInformacion();
        auto.encenderRadio();

        System.out.println("\n=== Motocicleta ===");
        moto.mostrarInformacion();
        moto.hacerCaballito();
    }
}

git init
git add .
git commit -m "Actividad Formativa 3 - Herencia"
git branch desarrollo
git checkout desarrollo
git push origin desarrollo
