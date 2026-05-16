
# 🦓 **Habitat Simulation**

## 🔍 **Overview**
This repository is a **JavaFX application** initially developed as coursework at **King’s College London**. I’ve been expanding and refining it beyond the original requirements. The simulation models a dynamic habitat environment with **complex food chain interactions**, including multiple species with distinct behaviours, **predator-prey relationships, genetic evolution** and **environmental influences like disease**.

## 🌟 **Features**
- 🦊 **Simulates predator-prey interactions** with distinct hunting behaviors.
- 🌿 **Implements plant consumption mechanics** for herbivores.
- 🦠 **Includes disease spread** among species.
- 🧬 **Genetic inheritance and mutations** affecting evolution.
- ⏳ **Age-based predator behavior**.
- 🛠️ **Extensible object-oriented design** with reusable logic.

## ⚙️ **Installation**
To install this project, follow these steps:
1. **Clone the repository:**
   ```bash
   git clone https://github.com/thomas-trotter/habitat-simulation.git
   ```
2. **Navigate to the project directory:**
   ```bash
   cd habitat-simulation
   ```
3. **Ensure you have Java and JavaFX installed:**
   - **Install Java (JDK 17 or later):** [Download here](https://jdk.java.net/)
   - **Install JavaFX SDK:** [Download here](https://gluonhq.com/products/javafx/)
4. **Configure JavaFX** in your IDE (e.g., IntelliJ IDEA or Eclipse).
5. **Build the project using Maven or Gradle:**
   ```bash
   mvn clean install
   ```
   or
   ```bash
   gradle build
   ```

## 🚀 **Usage**
To run the JavaFX application, use:
```bash
mvn javafx:run
```
or
```bash
java --module-path /path/to/javafx-sdk/lib --add-modules javafx.controls,javafx.fxml -jar target/your-app.jar
```
After running the command, the **JavaFX window should launch, displaying the habitat simulation.**

## 🗂️ **Repository Structure**
``` graphql
habitat-simulation/                  
├── src/
│   ├── main/
│   │   └── java/
│   │       ├── com/tomtrotter/habitatsimulation/
│   │       |   ├── application/             
│   │       |   │   └── Main.java               
│   │       |   ├── core/                  
│   │       |   │   ├── domain/             
│   │       |   │   │   ├── Animal.java          
│   │       |   │   │   ├── Disease.java     
│   │       |   │   │   ├── Organism.java        
│   │       |   │   │   ├── Plant.java           
│   │       |   │   │   ├── Predator.java        
│   │       |   │   │   └── Prey.java            
|   |       |   ├── simulation/
│   │       |   │   ├── entities/           
│   │       |   │   │   ├── Deer.java        
│   │       |   │   │   ├── Hare.java            
│   │       |   │   │   ├── Leopard.java       
│   │       |   │   │   ├── Tiger.java           
│   │       |   │   │   └── WildBoar.java        
│   │       |   │   ├── environment/         
|   |       |   |   |   ├── Counter.java         
│   │       |   │   │   ├── Field.java           
│   │       |   │   │   ├── FieldStats.java     
│   │       |   │   │   └── Location.java        
│   │       |   │   ├── factory/            
│   │       |   │   │   └── OrganismFactory.java 
│   │       |   │   ├── genetics/          
|   |       |   |   |   ├── attributes/        
|   |       |   |   |   |   ├── AttributeDefinition.java         
│   │       |   │   │   |   ├── Attributes.java               
│   │       |   │   │   |   └── GeneticAttributeManager.java  
|   |       |   |   |   ├── builder/
|   |       |   |   |   |   └── GeneticsBuilder.java         
|   |       |   |   |   ├── core/
|   |       |   |   |   |   └── Genetics.java        
|   |       |   |   |   └── mutation/
|   |       |   |   |       ├── BooleanRandomizeMutation.java
|   |       |   |   |       ├── BooleanToggleMutation.java
|   |       |   |   |       ├── DoubleIncrementMutation.java
|   |       |   |   |       ├── IntegerIncrementMutation.java
|   |       |   |   |       ├── MutationFactory.java
|   |       |   |   |       ├── MutationStrategy.java
|   |       |   |   |       └── MutationType.java 
|   |       |   |   ├── simulation/
|   |       |   |   |   └── Simulator.java
|   |       |   |   └── state/
|   |       |   |       └── SimulatorState.java
|   |       |   ├── ui/
│   │       |   │   ├── base/
|   |       |   |   |   └── BaseView.java
│   │       |   │   ├── canvas/
|   |       |   |   |   └── FieldCanvas.java
│   │       |   │   ├── components/
|   |       |   |   |   ├── SectionBuilder.java
|   |       |   |   |   └── UIFactory.java
│   │       |   │   ├── screens/
|   |       |   |   |   ├── SettingsView.java
|   |       |   |   |   └── SimulatorView.java
|   |       |   |   └── state/
│   │       |   │       └── ViewState.java  
│   │       |   └── util/             
│   │       |       └── Randomizer.java      
|   |       └── module-info.java
│   └── test/
│       └── java/
│           └── com/tomtrotter/habitatsimulation/
│               ├── core/domain/              
│               │   ├── AnimalTest.java
│               │   ├── ConcreteAnimalTest.java
│               │   ├── DiseaseTest.java
│               │   ├── OrganismTest.java
│               │   ├── PlantTest.java
│               │   ├── PredatorTest.java
│               │   └── PreyTest.java           
│               ├── simulation/
│               │   ├── genetics/
│               |   |   └── GeneticsTest.java  
│               │   └── simulation/
│               |       └── SimulatorTests.java    
│               └── ui/
│                   └── FieldCanvasTests.java 
├── LICENSE
├── pom.xml
└── README.md 
```

## 🧪 **Testing**
Run the test suite using the following command:
```sh
mvn test
```
or
```sh
gradle test
```
**JUnit tests cover:**
- ✔️ Animal behaviour logic
- ✔️ Hunting mechanisms
- ✔️ Plant consumption
- ✔️ Breeding mechanics
- ✔️ Disease spread
- ✔️ Genetic inheritance

## 🔮 **Improvements**
Future improvements and features include:
- 📈 **See the average characteristic** of each species.
- 🦌 **Additional species-specific traits** (e.g., movement patterns, field of view).
- 🌦️ **Seasonal changes affecting food availability and survival rates.**

## 📜 **License**
This project operates under the **GNU General Public License v3.0**. The **[LICENSE](https://choosealicense.com/licenses/gpl-3.0/)** file provides details.

