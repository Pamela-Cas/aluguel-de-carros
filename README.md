# Aluguel de Carros

Boas-vindas ao repositório do projeto `Aluguel de Carros`

# Requisitos do Projeto

A empresa do coração em que você trabalha está desenvolvendo um sistema para controlar o aluguel de carros, e você foi o primeiro contratado para iniciar o desenvolvimento do sistema.

O `Rent Cars` está dividido em partes orgainzadas. Em `Model` você vai encontrar as classes bases que devem seguir a seguinte hierarquia:

- `Vehicle.cs` descreve uma classe **abstrata** base para os veículos.
  - `Car.cs` descreve uma classe derivada para **carros**.
  - `Truck.cs` descreve uma classe derivada para **caminhões**.
  - `Motorcycle.cs` descreve uma classe derivada para **motos**.

- `Person.cs` descreve uma classe **abstrata** base para as pessoas clientes do sistema.
  - `PhysicalPerson.cs` descreve uma classe derivada para **pessoas físicas**.
  - `LegalPerson.cs` descreve uma classe derivada para **pessoas jurídicas**.

- `Rent.cs` descreve a classe para um aluguel entre uma **pessoa** e um **veículo**.

## 1. Crie uma `Struct` para as **Cores**

<details>

<summary> Mais informações
</summary>

Crie sua lógica em src/RentCars/Types/Structs/Color.cs

**O que será testado:**

 - A struct deve conter o campo <code>Name</code> do tipo <code>string</code>
 - A struct deve conter o campo <code>Hex</code> do tipo <code>string</code>
 - Os atributos devem ser públicos.

</details>

## 2. Crie um enum `FuelType`
<details>

<summary> Mais informações
</summary>

Crie sua lógica em src/RentCars/Types/Enums/FuelType.cs

**O que será testado:**

  - O enum deve conter o campo <code>Alcohol</code> com valor 10
  - O enum deve conter o campo <code>Gasoline</code> com valor 20
  - O enum deve conter o campo <code>Flex</code> com valor 30
  - O enum deve conter o campo <code>Diesel</code> com valor 40
  - O enum deve conter o campo <code>Electric</code> com valor 50
  - O enum deve conter o campo <code>Hybrid</code> com valor 60


</details>

## 3. Crie a classe `Vehicle`

<details>

<summary> Mais informações
</summary>

Crie sua lógica em src/RentCars/Models/Vehicle.cs

A classe deve conter os campos comuns à um veículo.

**O que será testado:**

- A classe deve ter as seguintes propriedades:
  - <code>Brand</code> que deve ser do tipo <code>string</code>, ter valor padrão igual à "", deve ter get e set;
  - <code>Model</code> que deve ser do tipo <code>string</code>, ter valor padrão igual à "", deve ter get e set;
  - <code>Price</code> que deve ser do tipo <code>decimal</code>, deve ter get e  set;
  - <code>Fuel</code> que deve ser do tipo <code>FuelType</code>, deve ter get e set;
  - <code>EngineCapacity</code> que deve ser do tipo <code>int</code>, deve ter get e set;
  - <code>MainColor</code> que deve ser do tipo <code>Color</code>, deve ter get e set;
  - <code>Year</code> que deve ser do tipo <code>int</code>, deve ter get e set;
  - <code>PricePerDay</code> que deve ser do tipo <code>double</code>, deve ter get e set;
  - <code>IsRented</code> que deve ser do tipo <code>bool</code>, ter valor padrão igual à false, deve ter get e set;

</details>

## 4. Crie um enum `BrakeType`

<details>

<summary> Mais informações
</summary>

Crie sua lógica em src/RentCars/Types/Enums/BreakeType.cs

**O que será testado:**

  - O enum deve conter o campo <code>Chamber</code> com valor 1
  - O enum deve conter o campo <code>Disc</code> com valor 2
  - O enum deve conter o campo <code>Drum</code> com valor 3

</details>

## 5. Crie um enum `TractionType`

<details>

<summary> Mais informações
</summary>

Crie sua lógica em src/RentCars/Types/Enums/TractionType.cs

**O que será testado:**

  - O enum deve conter o campo <code>FrontWheelDrive</code> com valor 0
  - O enum deve conter o campo <code>RearWheelDrive</code> com valor 1
  - O enum deve conter o campo <code>AllWheelDrive</code> com valor 2

</details>

## 6. Faça a classe `Car` herdar de `Vehicle`

<details>

<summary> Mais informações
</summary>

Crie sua lógica em src/RentCars/Models/Car.cs

Adicione a herança da classe Vehicle
Adicione novos campos específicos de Car

**O que será testado:**

- A classe deve ter as seguintes propriedades:
  - <code>Seats</code> que deve ser do tipo <code>Int</code>;
  - <code>Doors</code> que deve ser do tipo <code>Int</code>;
  - <code>Traction</code> que deve ser do tipo <code>TractionType</code>;
  - <code>FrontBrake</code> que deve ser do tipo <code>BrakeType</code>;
  - <code>RearBrake</code> que deve ser do tipo <code>BrakeType</code>;

</details>

## 7. Faça a classe `Motorcycle` herdar de `Vehicle`

<details>

<summary> Mais informações
</summary>

Crie sua lógica em src/RentCars/Models/Motorcycle.cs

Adicione a herança da classe Vehicle

Adicione novos campos específicos de Motorcycle

**O que será testado:**

- A classe deve ter as seguintes propriedades:
  - <code>SeatHeight</code> que deve ser do tipo <code>double</code>;
  - <code>FrontBrake</code> que deve ser do tipo <code>BrakeType</code>;
  - <code>RearBrake</code> que deve ser do tipo <code>BrakeType</code>;

</details>

## 8. Faça a classe `PickupTruck` herdar de `Car`

<details>

<summary> Mais informações
</summary>

Crie sua lógica em src/RentCars/Models/PickupTruck.cs

Adicione a herança da classe Vehicle

Adicione novos campos específicos de PickupTruck

**O que será testado:**
- A classe deve ter as seguintes propriedades:
  - <code>LoadCapacity</code> que deve ser do tipo <code>double</code>;
</details>


## 9. Crie um enum `RentStatus`

<details>

<summary> Mais informações
</summary>

Crie sua lógica em src/RentCars/Types/Enums/RentStatus.cs

**O que será testado:**
  - O enum deve conter o campo <code>Confirmed</code> com valor 0
  - O enum deve conter o campo <code>Finished</code> com valor 1
  - O enum deve conter o campo <code>Canceled</code> com valor igual ao <code>Finished</code>

</details>

## 10. Crie o construtor de `Rent` seguindo as regras de negócio

<details>

<summary> Mais informações
</summary>

Crie sua lógica em src/RentCars/Models/Rent.cs

**O que será testado:**
O construtor deve receber uma instância de <code>Vehicle</code>, uma de <code>Person</code> e um valor <code>inteiro</code> com os dias alugados.

  - Para calcular o atributo <code>Price</code> deve-se seguir a seguinte regra:
  - Para pessoas fisícas o preço deve ser o preço por dia do veículo * os dias alugados.
  - Para pessoas jurídicas o preço deve ser o preço por dia do veículo * os dias alugados com <code>10% de desconto</code>.

  - O status inicial deve ser <code>RentStatus.Confirmed</code>

  - O construtor deve alterar o atributo <code>IsRented</code> do veículo para <code>true</code>.
  - O construtor deve alterar o atributo <code>Debit</code> da pessoa para o Preço calculado.

</details>

## Bônus (não avaliativo) - Implemente os métodos de `cancelar` e `finalizar` um aluguel

<details>

<summary> Mais informações
</summary>

Crie sua lógica em src/RentCars/Types/Models/Rent.cs

**O que será testado:**
  - O método <code>Rent.Cancel()</code> deve cancelar um aluguel
    - O <code>Status</code> deve ser alterado para <code>RentStatus.Cancelled</code>

  - O método <code>Rent.Finish()</code> deve finalizar um aluguel
    - O <code>Status</code> deve ser alterado para <code>RentStatus.Finished</code>

</details>
