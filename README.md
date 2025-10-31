# imc-portal
Nombre del Proyecto: Cálculo Web de IMC
## 📌 Diagrama de Caso de Uso (PlantUML)

```plantuml
@startuml
actor Cliente
actor Especialista
actor SistemaIMC as "Sistema IMC"

Cliente --> (Registrarse)
Cliente --> (Iniciar sesión)
Cliente --> (Calcular IMC)
Cliente --> (Ver resultado de IMC)

Especialista --> (Iniciar sesión)
Especialista --> (Ver pacientes asignados)
Especialista --> (Ver historial de IMC)

SistemaIMC --> (Asignar cliente a especialista)
SistemaIMC --> (Guardar cálculo de IMC)

(Registrarse) .down.> (Asignar cliente a especialista) : <<incluye>>
(Calcular IMC) .down.> (Guardar cálculo de IMC) : <<incluye>>
@enduml
