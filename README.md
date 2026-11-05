<p align="center">
  <img src="assets/ZaticoLogic_banner.png"
       alt="ZaticoLogic - Simulador de Lógica Combinacional"
       width="100%">
</p>


# ZaticoLogic — Simulador de Lógica Combinacional


[Última Versión](https://github.com/ajmartostorres-hub/ZATICOLOGIC/releases)
[Descargar Ejecutable](https://github.com/ajmartostorres-hub/ZATICOLOGIC/releases)
[Licencia](LICENSE)
[Python](https://www.python.org/)

ZaticoLogic es una aplicación de escritorio para Windows y Linux pensada para el aula: permite introducir una función lógica, una tabla de verdad o un circuito de puertas y obtener al instante todas las demás representaciones.

Utiliza un motor de simplificación propio basado en el método de **Quine-McCluskey** (al estilo de Logic Friday) y un editor visual de circuitos con simulación en tiempo real, sin necesidad de configuraciones avanzadas ni entornos de programación.

## 📥 Descarga e Instalación (.exe y .deb)

No necesitas instalar Python ni configurar dependencias.

1. **Accede a las versiones oficiales:**
   Dirígete a la sección de [Lanzamientos / Releases](https://github.com/ajmartostorres-hub/ZATICOLOGIC/releases).
2. **Descarga el archivo de tu sistema:**
   - Windows: `ZaticoLogic.exe`
   - Linux (Debian, Ubuntu, Linux Mint…): `zaticologic_1.0_all.deb`
3. **Ejecuta la aplicación:**
   - Windows: haz doble clic sobre `ZaticoLogic.exe`.
   - Linux: instala el paquete con doble clic o desde una terminal con
     ```bash
     sudo apt install ./zaticologic_1.0_all.deb
     ```
     y ábrelo desde el menú de aplicaciones.

### 🛡️ Nota sobre la advertencia de Microsoft Defender SmartScreen

Al ejecutar un archivo `.exe` descargado de GitHub que no cuenta con un certificado digital comercial de pago, es normal que Windows muestre la advertencia **"Windows protegió su PC"**.

**¿Cómo omitir esta advertencia?**

1. Haz clic en el enlace **"Más información"** (*More info*) en la ventana de SmartScreen.
2. Haz clic en el botón **"Ejecutar de todos modos"** (*Run anyway*).
3. La aplicación se abrirá con normalidad.

## ✨ Características Principales

- **Tres formas de introducir el dato:**
  - **Función lógica:** con notación de clase (`A·B' + C`) o con operadores y funciones (`AND`, `OR`, `NOT`, `NAND(A,B,C)`, `XOR`, `XNOR`…).
  - **Tabla de verdad:** de 1 a 6 variables, con salidas 0, 1 o X (indiferente) y relleno rápido por mintérminos.
  - **Circuito lógico:** editor visual de arrastrar y soltar con puertas AND, OR, NAND, NOR, XOR y XNOR de 1 a 4 entradas, NOT y BUF.
- **Simplificación automática:** expresiones mínimas SOP (suma de productos) y POS (producto de sumas) mediante Quine-McCluskey, con la lista de implicantes primos.
- **Formas canónicas:** mintérminos Σm, maxtérminos ΠM e indiferencias, con las formas canónicas SOP y POS completas.
- **Mapas de Karnaugh:** de 1 a 6 variables en código Gray, con los grupos de unos (SOP) o de ceros (POS) marcados en colores.
- **Circuitos generados:** dibujo automático del circuito del dato y de los circuitos SOP y POS mínimos, editables en el editor.
- **Simulación en tiempo real:** al pulsar sobre las entradas cambian de valor y los cables se colorean según la señal que llevan.
- **Resultados al instante:** todo se recalcula mientras escribes o modificas la tabla o el circuito.

## 💻 Requisitos del Sistema

- **Sistema operativo:** Windows 7, Windows 10, Windows 11 (64 bits) o Linux (Debian, Ubuntu o derivadas).
- **Conexión a Internet:** no es necesaria; el programa funciona totalmente sin conexión.
- **Espacio libre en disco:** ~30 MB.

## 🛠️ Tecnologías Internas

- **Interfaz gráfica:** Python 3 + Tkinter (incluido en Python, sin dependencias externas)
- **Motor lógico:** analizador de expresiones y simplificación por Quine-McCluskey con búsqueda exacta de la cobertura mínima
- **Gráficos:** dibujo vectorial de puertas, circuitos, tablas y mapas de Karnaugh sobre `tk.Canvas`

### Ejecutar desde el código fuente

```bash
python logica.py
```

| Archivo | Contenido |
|---|---|
| `logica.py` | Ventana principal y modos de entrada |
| `motor_logico.py` | Motor: expresiones, tablas de verdad, Quine-McCluskey y circuitos |
| `editor_circuito.py` | Editor visual de circuitos con simulación |
| `dibujo_circuito.py` | Dibujo automático de circuitos |
| `karnaugh.py` | Mapas de Karnaugh |
| `widgets.py` | Tema visual y componentes de la interfaz |
| `recursos/` | Iconos de la aplicación |

## 📜 Licencia y Créditos

- **Licencia:** distribuido bajo la licencia GNU General Public License v3.0 o posterior (GPLv3+).
- **Autor:** Alfonso José Martos Torres (@ajmt_00)
