# 🩺 DermaTech — Sistema Web de Gestión Clínica Dermatológica

![Estado del Proyecto](https://img.shields.io/badge/Estado-En%20Desarrollo-yellow)
![Metodología](https://img.shields.io/badge/Metodología-Ágil%20%2F%20Scrum-blue)
![Licencia](https://img.shields.io/badge/Licencia-MIT-green)

---

## 📋 Descripción General

**DermaTech** es una plataforma web clínica orientada a la gestión integral de consultas dermatológicas. El sistema centraliza el agendamiento de citas, el manejo de historias clínicas digitales, la emisión de recetas y el seguimiento visual de tratamientos, tanto para pacientes como para médicos y administradores.

Este repositorio contiene el desarrollo del sistema bajo una metodología **ágil (Scrum)**, con requisitos definidos como **Historias de Usuario** priorizadas por valor de negocio.

---

## 🎯 Objetivos del Proyecto

- Digitalizar y centralizar los procesos clínicos de la clínica DermaTech.
- Mejorar la experiencia del paciente mediante autogestión de citas y notificaciones.
- Proveer a los médicos herramientas digitales para consulta, diagnóstico y seguimiento.
- Reducir el ausentismo, el papeleo y los errores administrativos.

---

## 👥 Roles del Sistema

| Rol | Descripción |
|---|---|
| 🧑‍💼 **Administrador** | Gestiona perfiles de médicos, horarios y configuración del sistema |
| 🩺 **Médico Dermatólogo** | Accede a historias clínicas, emite recetas y sube imágenes de lesiones |
| 🧑‍⚕️ **Paciente Registrado** | Agenda/cancela citas, recibe recordatorios y realiza pagos en línea |
| 🌐 **Visitante** | Explora el catálogo público de tratamientos |

---

## 📌 Backlog de Historias de Usuario

| ID | Historia | Módulo | Prioridad |
|---|---|---|---|
| US-01 | Autenticación y Acceso Seguro | Seguridad y Control de Acceso | 🔴 Alta |
| US-02 | Agendamiento de Citas Dermatológicas | Gestión de Citas y Calendario | 🔴 Alta |
| US-03 | Visualización del Historial Clínico | Gestión de Historias Clínicas | 🔴 Alta |
| US-04 | Emisión de Recetas Digitales | Historias Clínicas / Farmacia | 🟡 Media |
| US-05 | Reprogramación y Cancelación de Citas | Gestión de Citas y Calendario | 🔴 Alta |
| US-06 | Notificaciones y Recordatorios de Citas | Notificaciones | 🟡 Media |
| US-07 | Gestión de Perfiles de Médicos y Horarios | Administración del Sistema | 🔴 Alta |
| US-08 | Carga de Imágenes de Lesiones Dermatológicas | Gestión de Historias Clínicas | 🟡 Media |
| US-09 | Catálogo Informativo de Tratamientos | Portal Público / Catálogo | 🟢 Baja |
| US-10 | Pago de Consultas en Línea | Facturación y Pagos | 🟡 Media |

---

## 🗂️ Detalle de Historias de Usuario

<details>
<summary><strong>US-01 · Autenticación y Acceso Seguro</strong></summary>

**Como** paciente registrado en la clínica DermaTech,  
**Quiero** iniciar sesión ingresando mi correo electrónico y contraseña,  
**Para** acceder a mi perfil privado, historial clínico y gestionar mis citas de forma segura.

**Criterios de Aceptación:**
- [ ] El acceso se concede solo si las credenciales coinciden con la base de datos.
- [ ] Mensaje genérico de error ("Credenciales incorrectas") sin especificar el campo fallido.
- [ ] Bloqueo temporal de 15 minutos tras 3 intentos fallidos consecutivos.
- [ ] La contraseña viaja cifrada y se valida mediante hash seguro en el servidor.

</details>

<details>
<summary><strong>US-02 · Agendamiento de Citas Dermatológicas</strong></summary>

**Como** paciente de DermaTech,  
**Quiero** visualizar un calendario interactivo con horarios disponibles,  
**Para** agendar una cita en el horario que mejor se ajuste a mi disponibilidad.

**Criterios de Aceptación:**
- [ ] Solo se muestran bloques de tiempo (30 min) no reservados previamente.
- [ ] Menú desplegable para seleccionar al médico especialista antes de ver el calendario.
- [ ] Confirmación final y envío automático de correo con detalles de la cita.
- [ ] No se permiten fechas pasadas ni citas con menos de 2 horas de anticipación.

</details>

<details>
<summary><strong>US-03 · Visualización del Historial Clínico</strong></summary>

**Como** médico dermatólogo,  
**Quiero** acceder al historial clínico detallado de mis pacientes,  
**Para** tomar decisiones médicas informadas durante la consulta.

**Criterios de Aceptación:**
- [ ] Acceso restringido al médico asignado o al director médico.
- [ ] Búsqueda de pacientes por número de cédula o apellidos.
- [ ] Registros ordenados cronológicamente de más reciente a más antiguo.

</details>

<details>
<summary><strong>US-04 · Emisión de Recetas Digitales</strong></summary>

**Como** médico dermatólogo,  
**Quiero** generar y enviar recetas médicas digitales al correo del paciente,  
**Para** eliminar el uso de papel y evitar errores de caligrafía.

**Criterios de Aceptación:**
- [ ] Receta generada en PDF con logotipo, datos del médico y número de registro profesional.
- [ ] Autocompletado de medicamentos y cremas dermatológicas comunes.
- [ ] Envío automático al correo del paciente al emitir la receta.

</details>

<details>
<summary><strong>US-05 · Reprogramación y Cancelación de Citas</strong></summary>

**Como** paciente de DermaTech,  
**Quiero** cancelar o reprogramar citas desde mi panel de usuario,  
**Para** gestionar imprevistos sin necesidad de llamar a la clínica.

**Criterios de Aceptación:**
- [ ] Solo se permite cancelar/reprogramar con al menos 24 horas de anticipación.
- [ ] El bloque liberado vuelve a estar disponible en el calendario de forma inmediata.
- [ ] El médico recibe notificación del cambio en su agenda.

</details>

<details>
<summary><strong>US-06 · Notificaciones y Recordatorios de Citas</strong></summary>

**Como** paciente agendado,  
**Quiero** recibir recordatorios automáticos por correo electrónico,  
**Para** no olvidar la fecha y hora de mi consulta.

**Criterios de Aceptación:**
- [ ] Recordatorio enviado automáticamente 24 horas antes de la cita.
- [ ] El correo incluye fecha, hora, especialista, dirección y recomendaciones previas.

</details>

<details>
<summary><strong>US-07 · Gestión de Perfiles de Médicos y Horarios</strong></summary>

**Como** administrador del sistema,  
**Quiero** configurar perfiles de dermatólogos, especialidades y horarios,  
**Para** que el calendario refleje la disponibilidad real de los profesionales.

**Criterios de Aceptación:**
- [ ] CRUD completo de perfiles médicos (crear, leer, actualizar, desactivar).
- [ ] Opción para bloquear días festivos, vacaciones o permisos médicos.

</details>

<details>
<summary><strong>US-08 · Carga de Imágenes de Lesiones Dermatológicas</strong></summary>

**Como** médico dermatólogo,  
**Quiero** adjuntar fotografías de lesiones cutáneas al expediente digital del paciente,  
**Para** llevar un seguimiento visual objetivo de la evolución del tratamiento.

**Criterios de Aceptación:**
- [ ] Formatos soportados: JPG y PNG, máximo 5MB por archivo.
- [ ] Cada imagen queda registrada automáticamente con la fecha de la consulta.
- [ ] Sección "Evolución Visual" con galería de imágenes en el historial del paciente.

</details>

<details>
<summary><strong>US-09 · Catálogo Informativo de Tratamientos</strong></summary>

**Como** visitante de la página web,  
**Quiero** explorar un catálogo de tratamientos dermatológicos,  
**Para** informarme antes de agendar una cita.

**Criterios de Aceptación:**
- [ ] Catálogo dividido en categorías claras (Dermatología Clínica, Estética, etc.).
- [ ] Ficha de tratamiento con descripción, duración y botón "Agendar cita para este tratamiento".

</details>

<details>
<summary><strong>US-10 · Pago de Consultas en Línea</strong></summary>

**Como** paciente de DermaTech,  
**Quiero** pagar mi consulta a través de una pasarela segura con tarjeta,  
**Para** confirmar mi cita sin trámites presenciales en recepción.

**Criterios de Aceptación:**
- [ ] Redirección a pasarela de pagos autorizada con retorno del estado de la transacción.
- [ ] Estado de la cita cambia de "Pendiente" a "Confirmada" solo tras pago exitoso.
- [ ] Generación y envío de comprobante de pago digital al correo del paciente.

</details>

---

## 🏗️ Módulos del Sistema

```
DermaTech/
├── 🔐 Seguridad y Control de Acceso      (US-01)
├── 📅 Gestión de Citas y Calendario       (US-02, US-05)
├── 📁 Gestión de Historias Clínicas       (US-03, US-04, US-08)
├── 🔔 Notificaciones                      (US-06)
├── ⚙️  Administración del Sistema          (US-07)
├── 🌐 Portal Público / Catálogo           (US-09)
└── 💳 Facturación y Pagos                 (US-10)
```

---

## 🚀 Estado del Sprint

> ⚙️ *Actualizar según avance del equipo*

| Sprint | Historias incluidas | Estado |
|---|---|---|
| Sprint 1 | US-01, US-07 | 🔲 Por iniciar |
| Sprint 2 | US-02, US-05 | 🔲 Por iniciar |
| Sprint 3 | US-03, US-06 | 🔲 Por iniciar |
| Sprint 4 | US-04, US-08, US-10 | 🔲 Por iniciar |
| Sprint 5 | US-09 | 🔲 Por iniciar |

---

## 🤝 Contribución

1. Haz un fork del repositorio.
2. Crea una rama con el ID de la historia: `git checkout -b feature/US-01-autenticacion`
3. Realiza tus cambios y haz commit: `git commit -m "feat(US-01): implementar login seguro"`
4. Abre un Pull Request hacia `develop` describiendo los cambios.

---

## 📄 Licencia

Este proyecto está bajo la licencia **MIT**. Consulta el archivo `LICENSE` para más detalles.

---

<p align="center">Desarrollado con ❤️ para la clínica <strong>DermaTech</strong></p>