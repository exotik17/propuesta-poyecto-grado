# Meditrack
## Validacion y verificacion con casos de uso

## **Registrar paciente**
**Actor:** Recepcionista  
**Descripción:** Permite registrar nuevos pacientes en el sistema, ingresando datos personales y de contacto.  

**Validación:**  
- Se validan campos obligatorios (nombre, documento, teléfono, correo).  
- El correo debe tener formato válido y el documento no debe existir previamente.  

**Verificación:**  
- Se confirma que los datos queden correctamente almacenados y accesibles en la base de datos.  
- El sistema notifica que el registro fue exitoso.  

---

## **Iniciar sesión**
**Actor:** Administrador / Recepcionista / Médico  
**Descripción:** Permite a los usuarios autenticarse según su rol.  

**Validación:**  
- Se verifica que el usuario y contraseña sean válidos.  
- Se bloquea la cuenta tras múltiples intentos fallidos.  

**Verificación:**  
- El sistema redirige al panel correspondiente según el rol.  
- Solo usuarios registrados pueden acceder.  

---

## **Agendar cita médica**
**Actor:** Recepcionista / Paciente  
**Descripción:** Permite registrar una nueva cita médica con fecha, hora y médico asignado.  

**Validación:**  
- Se comprueba disponibilidad del médico en la fecha y hora seleccionada.  
- Se evita el cruce de horarios.  

**Verificación:**  
- La cita queda registrada correctamente en la base de datos.  
- El paciente y el médico reciben confirmación de la reserva.  

---

## **Consultar citas**
**Actor:** Paciente / Recepcionista / Médico  
**Descripción:** Permite visualizar el historial y próximas citas agendadas.  

**Validación:**  
- Se verifica que el usuario tenga permisos para visualizar la información.  

**Verificación:**  
- El sistema muestra la información completa y actualizada.  
- Se garantiza que las citas mostradas correspondan al usuario correcto.  

---

## **Cancelar cita médica**
**Actor:** Paciente / Recepcionista  
**Descripción:** Permite cancelar una cita médica previamente agendada.  

**Validación:**  
- Se verifica que la cita exista y esté activa.  
- No puede cancelarse una cita pasada o ya atendida.  

**Verificación:**  
- El sistema actualiza el estado de la cita a “Cancelada”.  
- El médico recibe la notificación de cancelación.  

---

## **Registrar médico**
**Actor:** Administrador  
**Descripción:** Permite añadir médicos al sistema con su información profesional y horarios de atención.  

**Validación:**  
- Se verifica que el nombre, especialidad y horario sean válidos.  
- No se permiten médicos duplicados.  

**Verificación:**  
- El médico aparece disponible para asignación de citas.  
- Los datos quedan almacenados correctamente.  

---

## **Consultar disponibilidad médica**
**Actor:** Recepcionista / Paciente  
**Descripción:** Permite verificar los horarios disponibles de los médicos para agendar citas.  

**Validación:**  
- Se comprueba que el médico tenga agenda activa.  

**Verificación:**  
- El sistema muestra correctamente los espacios libres.  
- Se evita mostrar horarios ya reservados.  

---


