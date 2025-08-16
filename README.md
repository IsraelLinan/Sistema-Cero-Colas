# Sistema-Cero-Colas
Sistema de Escritorio para la Gestión Integral del Hospital, diseñado para optimizar y acelerar los procesos internos, reducir tiempos de atención y mejorar la experiencia tanto de pacientes como del personal administrativo y médico.

1. Módulo de Admisión
•	Registro de pacientes para atención: Captura los datos del paciente, asi como la asignación de número de turno. 
•	Gestión de Citas: Almacena la información para su atención.
•	Generación de Reportes: Reportes y filtrado de admisiones diarias por especialidad y consultorio.

2. Módulo de Sala de Espera
•	Visualización en Tiempo Real: Panel de turnos y tiempos de espera actualizados al instante.
•	Llamado Automático a Pacientes: Sistema de anuncios mediante pantallas o altavoces.
•	Prioridad Dinámica: Reordenamiento de turnos según urgencia o criterios definidos.
•	Histórico de Espera: Registro de tiempos de espera por paciente y servicio.
•	Ventana publicitaria: Colocar video promocional del Hospital.

3. Módulo de Consultoría
•	Visualización de consultorios: Vista independiente de cada consultorio.
•	Visualización de atención: Libre o Ocupado
•	Función Llamado: Llamar y Re-Llamar a un paciente en específico.
•	Comunicación Interna: Mensajería segura entre médicos, administrativos y pacientes.

4. Dashboard interactivo
•  Muestra los principales KPIs del negocio.

![Screenshot_1](https://github.com/user-attachments/assets/7af11c23-5892-4978-a636-34ccec96226d)
![Screenshot_2](https://github.com/user-attachments/assets/543e8fd5-21cc-44fb-80fc-5ef5dcf4382f)
![Screenshot_3](https://github.com/user-attachments/assets/021fa779-22e8-4596-8145-02587467927a)
![Screenshot_4](https://github.com/user-attachments/assets/33ceb2f6-a403-4f43-899c-1e70869a5e13)
![Screenshot_5](https://github.com/user-attachments/assets/99892b02-12f2-40b7-9fcc-fb360549e208)
![Screenshot_6](https://github.com/user-attachments/assets/916f724a-9bf5-464c-aba8-82c71892aac7)
![Screenshot_7](https://github.com/user-attachments/assets/5c2bda93-627c-440c-8ce9-17759b4bd420)
![Screenshot_8](https://github.com/user-attachments/assets/3f753231-2b15-4591-9df4-7a9f4ea3b8ed)
![Screenshot_9](https://github.com/user-attachments/assets/c3982412-04f7-494d-b7dc-8c23632855c3)

# Tecnologías Usadas en el proyecto

Python 3.x: Todo el sistema está desarrollado en Python, utilizando características modernas como f-strings, type hints (parcialmente), y programación orientada a objetos.

# Interfaz Gráfica (GUI)

Tkinter:
Librería principal para todas las interfaces de escritorio
Uso avanzado de:
Frames, Labels, Entries, Buttons
Widgets personalizados (Treeview, Scrollbars, Canvas)
Gestión de eventos y bindings

Ttk (Themed Tkinter):
Para componentes estilizados (Comboboxes, Treeviews modernos)
Uso de estilos personalizados (Modern.Treeview)

PIL/Pillow:
Manipulación de imágenes para logos
ImageTk para integración con Tkinter

# Base de Datos

PostgreSQL:
Sistema de base de datos principal
Esquema con tablas: pacientes, especialidades, pacientes_especialidades, ultimos_llamados

Psycopg2:
Adaptador PostgreSQL para Python
Conexiones con pool (SimpleConnectionPool)
Cursors especializados (RealDictCursor, DictCursor)

# Librerías Especializadas

Pyttsx3:
Síntesis de voz para anuncios en sala de espera y consultorios
Configuración de voces en español

ReportLab:
Generación de reportes PDF profesionales
Creación de tablas estilizadas con headers/colores

TKCalendar:
Widget de calendario para selección de fechas en reportes
Streamlit (Dashboard):
Framework para aplicaciones web/data dashboard
Integración con Plotly para gráficos interactivos

Plotly:
Visualización de datos (gráficos de barras, heatmaps)
Integrado en el dashboard

# Patrones y Técnicas Avanzadas

Programación Multihilo:
threading para tareas concurrentes (actualización de datos en segundo plano)
Mecanismos de sincronización para acceso a recursos compartidos

POO (Programación Orientada a Objetos):
Diseño modular con clases para cada módulo (ModuloAdmision, ModuloConsultorio, etc.)
Herencia, encapsulamiento y abstracción

Gestión de Estilos Modernos:
Sistema centralizado de colores (COLORS)
Funciones factory para componentes UI (create_modern_button())
Diseño responsive con grid() y pack()

Seguridad:
Bcrypt para hashing de contraseñas
Validación de entradas de usuario

# Características Destacadas
1.Sistema Modular: Cada componente (admisiones, consultorios, etc.) es independiente.

2.Diseño Responsive: Interfaces que se adaptan a diferentes resoluciones.

3.Actualización en Tiempo Real: Datos sincronizados cada 3 segundos.

4.Accesibilidad: Soporte de texto a voz (TTS) para anuncios.

5.Reporting Avanzado:
Exportación a PDF/CSV

6.Dashboard interactivo con métricas clave (SLAs, tiempos de espera)
Seguridad Robustecida:
Autenticación de usuarios
Validación de inputs
Pool de conexiones a BD

