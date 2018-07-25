---
title: Obtener acceso a DLL en Excel
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
keywords:
- acceder a dll [excel 2007], DLL [Excel 2007], acceder en Excel
localization_priority: Normal
ms.assetid: e2bfd6ea-efa3-45c1-a5b8-2ccb8650c6ab
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: bfb562b6bbe824124c6b5a691745d076720ee004
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815638"
---
# <a name="access-dlls-in-excel"></a>Obtener acceso a DLL en Excel

**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio 
  
Puede obtener acceso a una función DLL o comando en Microsoft Excel de varias formas:
  
- A trav�s del m�dulo de códigoMicrosoft Visual Basic para aplicaciones (VBA) en el que la función o el comando est� disponible mediante una instrucci�n **Declare**. 
    
- A trav�s de una hoja de macros XLM con las funciones **CALL** o **REGISTER**. 
    
- Directamente desde la hoja de cálculo o de un elemento personalizado de la interfaz de usuario (IU).
    
Esta documentaci�n no trata las funciones XLM. Se recomienda que use uno de los dos enfoques.
  
Para acceder directamente desde la hoja de cálculo o desde un elemento personalizado de la interfaz de usuario, la función o el comando se debe registrar primero con Excel. Para obtener información sobre el registro de comandos y funciones, consulte [Acceso al códigoXLL en Excel](accessing-xll-code-in-excel.md).
  
## <a name="calling-dll-functions-and-commands-from-vba"></a>Llamar a funciones y comandos DLL desde VBA

Puede acceder a funciones y comandos DLL de VBA con la instrucci�n **Declare**. Esta instrucci�n tiene una sintaxis para los comandos y otra para las funciones. 
  
- **Sintaxis 1: comandos**
    
  ```vb
  [Public | Private] Declare Sub name Lib "libname" [Alias "aliasname"] [([arglist])]
  ```

- **Sintaxis 2: funciones**
    
  ```vb
  [Public | Private] Declare Function name Lib "libname" [Alias "aliasname"] [([arglist])] [As type]
  ```

Las palabras clave opcionales **Public** y **Private** especifican el �mbito de la función importada: todo el proyecto de Visual Basic o el m�dulo de Visual Basic, respectivamente. El nombre es el nombre que quiere usar en el códigoVBA. Si esto difiere del nombre del DLL, debe usar el especificador de Alias "aliasname" y proporcionar el nombre de la función como exportada por el DLL. Si quiere acceder a una función DLL por referencia para un n�mero ordinal DLL, debe proporcionar un nombre de alias, que es el ordinal con el prefijo **#**.
  
Los comandos deben devolver **void**. Las funciones deben devolver tipos que VBA pueda reconocer **ByVal**. Esto significa que algunos tipos se devuelven m�s f�cilmente modificando los argumentos locales: cadenas, matrices, tipos definidos por el usuario y objetos.
  
> [!NOTE]
> VBA no puede comprobar que la lista de argumentos y el retorno que se indica en el m�dulo de Visual Basic son los mismos seg�n la codificaci�n de DLL. Debe comprobar usted mismo con cuidado, ya que un error podr�a provocar el bloqueo de Excel. 
  
Cuando la referencia o el puntero no pasan los argumentos de la función o del comando, deben ir precedidos por la palabra clave **ByVal** en la declaraci�n **arglist**. Cuando una función de C o C++ toma argumentos de puntero o una función de C++ toma argumentos de referencia, deben pasar **ByRef**. La palabra clave **ByRef** se puede omitir de las listas de argumentos porque es el valor predeterminado en VBA. 
  
### <a name="argument-types-in-cc-and-vba"></a>Tipos de argumento en C/C++ y VBA

Debe tener en cuenta lo siguiente cuando se comparan las declaraciones de tipos de argumentos en C o C++ y VBA.
  
- Se pasa un **String** de VBA como un puntero a una estructura BSTR de cadena de bytes al pasar ByVal, y como un puntero a un puntero al pasar **ByRef**.
    
- **Variant** de VBA que contiene una cadena se pasa como puntero a una estructura BSTR de cadena de caracteres anchos Unicode al pasar **ByVal**, y como un puntero a un puntero al pasar **ByRef**.
    
- **Integer** de VBA es un tipo de 16 bits equivalente a un signed short en C/C++. 
    
- **Long** de VBA es un tipo de 32 bits equivalente a un signed int en C/C++. 
    
- Tanto VBA como C/C++ permiten la definici�n de tipos de datos definidos por el usuario, con las instrucciones **Type** y **struct** respectivamente. 
    
- Tanto VBA como C/C++ admiten el tipo de datos **Variant**, definidos para C/C++ en los archivos de encabezado de Windows OLE/COM como VARIANT. 
    
- Las matrices VBA son OLE **SafeArrays**, definidas para C/C++ en los archivos de encabezado de Windows OLE/COM como **SAFEARRAY**.
    
- El tipo de datos **Currency** de VBA se pasa como estructura de tipo **CY**, definido en el archivo wtypes.h del archivo de encabezado Windows, cuando pasa **ByVal**, y como un puntero para este cuando pasa **ByRef**.
    
En VBA, los elementos de los tipos de datos definidos por el usuario se empaquetan en l�mites de 4 bytes mientras que, en Visual Studio, de forma predeterminada, se empaquetan en l�mites de 8 bytes. Por lo tanto, debe incluir la definición de la estructura de C/C++ en un bloque `#pragma pack(4) … #pragma pack()` para evitar que los elementos estén alineados de forma incorrecta. 
  
El siguiente es un ejemplo de definiciones de tipo de usuario equivalente.
  
```vb
Type VB_User_Type
    i As Integer
    d As Double
    s As String
End Type

```

```cpp
#pragma pack(4)
struct C_user_type
{
    short iVal;
    double dVal;
    BSTR bstr; // VBA String type is a byte string
}
#pragma pack() // restore default

```

VBA admite una amplia gama de valores, en algunos casos, m�s de los que admite Excel. El doble de VBA es compatible con IEEE y admite n�meros por debajo de lo normal redondeados hacia abajo a cero en la hoja de cálculo. El tipo **Date** de VBA puede representar fechas anteriores al uno de enero de 0100 con fechas serializadas negativas. Excel solo permite fechas serializadas mayores o iguales a cero. El tipo **Currency** de VBA, un entero escalado de 64 bits, puede alcanzar una precisi�n no admitida por los dobles de 8 bytes y, por lo tanto, no coinciden en la hoja de cálculo. 
  
Excel solo pasa las variantes de los siguientes tipos a una función definida por el usuario de VBA.
  
|**Tipo de datos VBA**|**Marcas de bits de tipo Variant de C/C++**|**Descripción**|
|:-----|:-----|:-----|
|Doble  <br/> |**VT_R8** <br/> ||
|Booleano  <br/> |**VT_BOOL** <br/> ||
|Fecha  <br/> |**VT_DATE** <br/> ||
|String  <br/> |**VT_BSTR** <br/> |Cadena de bytes Bstr OLE  <br/> |
|Range  <br/> |**VT_DISPATCH** <br/> |Referencias de celda y de rango  <br/> |
|Variante que contiene una matriz  <br/> |**VT_ARRAY** | **VT_VARIANT** <br/> |Matrices literales  <br/> |
|Ccy  <br/> |**VT_CY** <br/> |Entero de 64 bits que se escala para permitir cuatro posiciones decimales de precisi�n.  <br/> |
|Variante que contiene un error  <br/> |**VT_ERROR** <br/> ||
||**VT_EMPTY** <br/> |Celdas vac�as o argumentos omitidos  <br/> |
   
Puede comprobar el tipo de una variante pasada en VBA con **VarType**, excepto que la función devuelve el tipo de los valores del rango cuando se llama con referencias. Para determinar si una **Variant** es un objeto de referencia **Range**, puede usar la función **IsObject**. 
  
Puede crear **Variants** que contenga matrices de variantes en VBA desde **Range** asignando la propiedad **Value** a **Variant**. Las celdas del rango de origen que tengan formato de moneda est�ndar para la configuraci�n regional en vigor en el momento, se convierten en elementos de matriz de tipo **Currency**. Las celdas con formato como fechas se convierten en elementos de la matriz de tipo **Date**. Las celdas que contienen cadenas se convierten en variantes **BSTR** de caracteres anchos. Las celdas que contienen errores se convierten en **Variants** de tipo **VT_ERROR**. Las celdas que contienen **Boolean** **True** o **False** se convierten en **Variants** de tipo **VT_BOOL**. 
  
> [!NOTE]
> **Variant** almacena **True** como -1 y **False** como 0. Los n�meros sin formato como fechas o cantidades de moneda se convierten en variantes de tipo **VT_R8**. 
  
### <a name="variant-and-string-arguments"></a>Variante y argumentos de cadena

Excel funciona internamente con cadenas de caracteres anchos Unicode. Cuando se declara una función definida por el usuario VBA como que toma un argumento **String**, Excel convierte la cadena proporcionada en una cadena de bytes de forma espec�fica de la configuraci�n regional. Si quiere que la función se pase a una cadena Unicode, la función definida por el usuario VBA debe aceptar **Variant** en lugar de un argumento **String**. Luego, la función DLL la cadena de car�cter ancho BSTR **Variant** VBA. 
  
Para devolver las cadenas Unicode a VBA desde un DLL, debe modificar un argumento de cadena **Variant** local. Para que funcione, debe declarar la función DLL que toma un puntero en **Variant** y en el códigode C/C++, y declarar el argumento en el códigoVBA como  `ByRef varg As Variant`. Debe liberar la memoria de cadena antigua y el nuevo valor de cadena creado con las funciones de cadena OLE Bstr solo en DLL.
  
Para devolver una cadena de bytes a VBA desde un DLL, debe modificar un argumento BSTR de cadena de bytes local. Para que funcione, debe declarar la función DLL que toma un puntero para un puntero en BSTR y en el códigode C/C++, y declarar el argumento en el códigoVBA como **ByRef varg As String**.
  
Solo debe gestionar las cadenas que se pasan de estas formas desde VBA con las funciones de cadena OLE BSTR para evitar problemas relacionados con la memoria. Por ejemplo, debe llamar a **SysFreeString** para liberar la memoria antes de sobrescribir la cadena pasada, y **SysAllocStringByteLen** o **SysAllocStringLen** para asignar espacio para una nueva cadena. 
  
Puede crear errores de hoja de cálculo de Excel como **Variants** en VBA con la función **CVerr** con argumentos, como se muestra en la siguiente tabla. Los errores de la hoja de cálculo tambi�n se pueden devolver a VBA desde un DLL con **Variants** de tipo **VT_ERROR**y con los siguientes valores en el campo **ulVal**. 
  
|**Error**|**Valor Variant ulVal**|**Argumento CVerr**|
|:-----|:-----|:-----|
|#NULL!  <br/> |2148141008  <br/> |2000  <br/> |
|#DIV/0!  <br/> |2148141015  <br/> |2007  <br/> |
|#VALUE!  <br/> |2148141023  <br/> |2015  <br/> |
|#REF!  <br/> |2148141031  <br/> |2023  <br/> |
|#NAME?  <br/> |2148141037  <br/> |2029  <br/> |
|#NUM!  <br/> |2148141044  <br/> |2036  <br/> |
|#N/A  <br/> |2148141050  <br/> |2042  <br/> |
   
Tenga en cuenta que el valor **ulVal** variante dado equivale al valor de argumento **CVerr** más x800A0000 hexadecimal. 
  
## <a name="calling-dll-functions-directly-from-the-worksheet"></a>Llamar a funciones DLL directamente desde la hoja de cálculo

No puede acceder a funciones DLL de Win32 desde la hoja de cálculo sin, por ejemplo, usar VBA o XLM como interfaces, o sin dejar que Excel conozca la función, sus argumentos y el tipo devuelto por adelantado. Este proceso se denomina registro.
  
Las formas en que se puede acceder a las funciones de un DLL en la hoja de cálculo son las siguientes:
  
- Declarar la función de VBA como descrita anteriormente y acceder a ella a trav�s de una función definida por el usuario VBA.
    
- Llamar a la función DLL con CALL en una hoja de macros XLM y acceder a ella a trav�s de una función definida por el usuario XLM.
    
- Usar un comando XLM o VBA para llamar a la función **REGISTER** de XML, que proporciona la información que Excel necesita para reconocer la función cuando se introduce en una celda de la hoja de cálculo. 
    
- Convertir el DLL en un XLL y registrar la función con la función **xlfRegister** de la API de C cuando se activa XLL. 
    
El cuarto enfoque es independiente: el códigoque registra las funciones y el códigode función se incluyen en el mismo proyecto de código. Realizar cambios en el complemento no implica realizar cambios a una hoja de XLM o en un m�dulo de códigoVBA. Para hacerlo de manera administrada manteni�ndose dentro de las capacidades de la API de C, debe convertir el DLL en un XLL y cargar el complemento resultante con Administrador de complementos. Esto permite que Excel llame a una función que expone el DLL cuando se carga o activa el complemento, desde el que puede registrar todas las funciones que contiene el XLL y realizar cualquier otra inicializaci�n del DLL.
  
## <a name="calling-dll-commands-directly-from-excel"></a>Llamar a los comandos DLL directamente desde Excel

No se puede acceder directamente a los comandos del DLL de Win32 desde los men�s y los cuadros de di�logo de Excel sin que haya una interfaz, como VBA, o sin los comandos que se registran con antelaci�n.
  
Las formas en las que acceder a los comandos de un DLL son las siguientes:
  
- Declarar el comando de VBA, como se describi� anteriormente, y acceder a �l a trav�s de una macro de VBA.
    
- Llamar al comando DLL con **CALL** en una hoja de macros XLM y acceder a �l a trav�s de una macro XLM. 
    
- Usar un comando XLM o VBA para llamar a la función **REGISTER** de XML, que proporciona la información que Excel necesita para reconocer el comando cuando se introduce en un cuadro de di�logo que se espera el nombre de un comando de macros. 
    
- Convertir el DLL en un XLL y registrar el comando mediante la función **xlfRegister** de la API de C. 
    
Como se ha explicado anteriormente, en el contexto de las funciones DLL, el cuarto enfoque es el m�s independiente ya que mantiene el códigode registro cerca del códigode comando. Para ello, debe convertir el DLL en un XLL y cargar el complemento resultante con el Administrador de complementos. Registrar los comandos de esta manera tambi�n le permite adjuntar el comando a un elemento de la interfaz de usuario, como un men� personalizado, o configurar una captura de eventos que llame al comando en una pulsaci�n de tecla determinada u otro evento.
  
Excel asume que todos los comandos XLL registrados con Excel tienen el siguiente formato.
  
```cpp
int WINAPI my_xll_cmd(void)
{
// Function code...
    return 1;
}
```

> [!NOTE]
> Excel omite el valor devuelto a menos que se le llame desde una hoja de macros XLM, en cuyo caso el valor devuelto se convierte a **TRUE** o **FALSE**. Por lo tanto, debe devolver 1 si el comando se ejecuta correctamente y 0 si tiene errores o el usuario lo cancela. 
  
## <a name="dll-memory-and-multiple-dll-instances"></a>Memoria de DLL e instancias de varios DLL

Cuando una aplicación carga un DLL, el códigoejecutable del DLL se carga en el mont�n global para que se pueda ejecutar, y se asigna espacio en el mont�n global para las estructuras de datos. Windows usa la asignaci�n de memoria para que estas �reas de memoria aparezcan como si estuvieran en el proceso de la aplicación, para que esta pueda acceder a ella.
  
Si una segunda aplicación carga el DLL, Windows no crea otra copia del códigoejecutable de DLL, ya que la memoria es de solo lectura. Windows asigna la memoria de códigoejecutable de DLL a los procesos de ambas aplicaciones. Sin embargo, asigna un segundo espacio para una copia privada de las estructuras de datos del DLL y asigna esta copia solo al segundo proceso. Esto garantiza que ninguna aplicación interfiere con los datos del DLL de la otra.
  
Esto significa que los desarrolladores de DLL no tienen que preocuparse de las variables globales y est�ticas ni de las estructuras de datos a las que acceden varias aplicaciones, o m�s de una instancia de la misma aplicación. Cada instancia de cada aplicación obtiene su propia copia de los datos del DLL.
  
Los desarrolladores de DLL no tienen que preocuparse por la misma instancia de una aplicación que llama al DLL varias veces desde distintos subprocesos, ya que esto puede provocar la contenci�n de los datos de esa instancia. Para obtener m�s información, consulte [administración de memoria en Excel](memory-management-in-excel.md).
  
## <a name="see-also"></a>Vea también

- [Desarrollar DLL](developing-dlls.md) 
- [Llamar a Excel desde el archivo DLL o XLL](calling-into-excel-from-the-dll-or-xll.md)

