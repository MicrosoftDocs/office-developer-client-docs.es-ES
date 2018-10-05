---
title: Compatibilidad entre versiones de 32 y 64 bits de Office
ms.date: 04/27/2016
ms.audience: ITPro
localization_priority: Normal
ms.assetid: ff49dc9e-daf8-43cf-8802-51c2537ed561
description: Descubra cómo la versión de 32 bits de Office es compatible con la versión de 64 bits de Office.
ms.openlocfilehash: eeff11f11d4f2595b7111c0233703d09b1c46651
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25390943"
---
# <a name="compatibility-between-the-32-bit-and-64-bit-versions-of-office"></a>Compatibilidad entre versiones de 32 y 64 bits de Office

Descubra cómo la versión de 32 bits de Office es compatible con la versión de 64 bits de Office.
  
Las aplicaciones de Office están disponibles en versiones de 32 bits y 64 bits. 
  
Las versiones de 64 bits de Office permiten mover los datos más de una mayor capacidad de, por ejemplo, cuando se trabaja con un gran número de Microsoft Excel 2010. Al escribir código de 32 bits, puede usar la versión de 64 bits de Office sin cambios. Sin embargo, cuando se escribe código de 64 bits, debe asegurarse de que el código contiene palabras clave específicas y las constantes de compilación condicional para asegurarse de que el código es compatible con la versión anterior de Office y que se está ejecutando el código correcto si se mezclar código de 32 bits y 64 bits.
  
Visual Basic para aplicaciones 7.0 (VBA 7) está publicado en las versiones de 64 bits para Office y funciona con aplicaciones de 32 bits y 64 bits. Los cambios que se describen en este artículo se aplican sólo a las versiones de 64 bits de Office. Con las versiones de 32 bits de habilitar Microsoft Office utilizar soluciones creadas en versiones anteriores de Office sin modificaciones aún más.
  
> [!NOTE]
> De forma predeterminada, al instalar una versión de 64 bits de Office, se instala también la versión de 32 bits se instala junto con el sistema de 64 bits. Debe seleccionar explícitamente la opción de instalación de la versión de Microsoft Office de 64 bits. 
  
En VBA 7, debe actualizar las instrucciones de API de Windows (instrucciones**Declare** ) existentes para que funcione con la versión de 64 bits. Además, debe actualizar punteros de dirección y mostrar los identificadores de ventana en tipos definidos por el usuario que se usan por estas instrucciones. Esto se describe con más detalle en este artículo, así como problemas de compatibilidad entre las versiones de 32 bits y 64 bits y soluciones sugeridas. 
  
## <a name="comparing-32-bit-and-64-bit-systems"></a>Comparación de los sistemas de 32 bits y 64 bits
<a name="odc_office_Compatibility32bit64bit_Comparing32BitSystemsto64BitSystems"> </a>

Las aplicaciones creadas con las versiones de 64 bits de Office pueden hacer referencia a los espacios de direcciones mayores que las versiones de 32 bits. Esto significa que se puede usar más memoria física para los datos que antes, puede reducir la sobrecarga de empleado en mover datos dentro y fuera de la memoria física
  
Además de hacer referencia a ubicaciones específicas (conocidas como punteros) en la memoria física, también puede utilizar direcciones para hacer referencia a identificadores de ventana para mostrar (conocidos como identificadores). El tamaño (en bytes) del puntero o identificador depende de si está utilizando un sistema de 32 bits o 64 bits. 
  
Si desea ejecutar las soluciones existentes con las versiones de 64 bits de Office, tenga en cuenta de las siguientes opciones:
  
- Procesos de 64 bits nativos de Office no pueden cargar los archivos binarios de 32 bits. Esto se espera que un problema común cuando haya existentes controles Microsoft ActiveX y complementos existentes.
    
- VBA anteriormente no tiene un tipo de datos de puntero, por lo que había que usar variables de 32 bits para almacenar punteros e identificadores. Estas variables ahora truncan valores de 64 bits devueltos por llamadas a la API cuando se usa instrucciones **Declare** . 
    
## <a name="vba-7-code-base"></a>Base de código VBA 7
<a name="odc_office_Compatibility32bit64bit_IntroducingVBA7CodeBase"> </a>

VBA 7 reemplaza el código VBA que se base en Office 2007 y versiones anteriores. 7 de VBA está disponible en las versiones de 32 bits y 64 bits de Office. Proporciona dos constantes de compilación condicional: 
  
- **VBA7** - ayuda a garantizar la compatibilidad con versiones anteriores del código mediante la comprobación de si la aplicación usa VBA 7 o la versión anterior de VBA. 
    
- **Win64** Comprueba si se ejecuta el código como 32 bits o 64 bits. 
    
Con algunas excepciones, las macros de un documento que funcionan en la versión de 32 bits de la aplicación también funcionan con la versión de 64 bits.
  
## <a name="activex-control-and-com-add-in-compatibility"></a>Control ActiveX y compatibilidad de complementos COM
<a name="odc_office_Compatibility32bit64bit_ActiveXControlCOMAddinCompatibility"> </a>

Existentes controles ActiveX de 32 bits, no son compatibles con las versiones de 64 bits de Office. Para los controles ActiveX y los objetos COM:
  
- Si dispone del código fuente, generar una versión de 64 bits usted mismo.
- Si no dispone del código fuente, póngase en contacto con el proveedor para obtener una versión actualizada.
    
Procesos de 64 bits nativos de Office no pueden cargar los archivos binarios de 32 bits. Esto incluye los controles comunes de **MSComCtl** (TabStrip, la barra de herramientas, barra de estado, ProgressBar, TreeView, controles ListView por, ImageList, control deslizante, ImageComboBox) y los controles de **MSComCt2** (animación, UpDown, MonthView, DateTimePicker, FlatScrollBar). Estos controles se instalaron con versiones de 32 bits de Office anteriores a Office 2010. Debe encontrar una alternativa para las soluciones VBA existentes que usan estos controles al migrar el código a las versiones de 64 bits de Office. 
  
## <a name="api-compatibility"></a>Compatibilidad de API
<a name="odc_office_Compatibility32bit64bit_ApplicationProgrammingInterfaceCompatibility"> </a>

La combinación de las bibliotecas de VBA y tipo le ofrece una gran cantidad de funcionalidad para crear aplicaciones de Office. Sin embargo, en ocasiones, se debe comunicar directamente con el sistema operativo y otros componentes, por ejemplo, al administrar memoria o procesos, cuando se trabaja con controles y ventanas de linke de elementos de la interfaz de usuario, o cuando se modifica el registro de Windows. En estos escenarios, la mejor opción es utilizar una de las funciones externas que están incrustadas en archivos DLL. Puede hacerlo en VBA mediante la realización de llamadas a API utilizando instrucciones **Declare** . 
  
> [!NOTE]
> Microsoft proporciona un archivo Win32API.txt que contiene las instrucciones Declare 1.500 y una herramienta para copiar la instrucción **Declare** que desee en el código. Sin embargo, estas instrucciones son para sistemas de 32 bits y se debe convertir a 64 bits mediante el uso de la información que se trata más adelante en este artículo. Las instrucciones **Declare** existentes no se compilan en VBA de 64 bits hasta que haya marcado como seguros para 64 bits mediante el atributo **PtrSafe** . Puede encontrar ejemplos de este tipo de conversión en el sitio Web del Excel MVP Jan Karel Pieterse en [https://www.jkp-ads.com/articles/apideclarations.asp](https://www.jkp-ads.com/articles/apideclarations.asp). La [Guía de usuario del Inspector de compatibilidad de código de Office](https://technet.microsoft.com/en-us/library/ee833946%28office.14%29.aspx) es una herramienta muy útil para inspeccionar la sintaxis de instrucciones **Declare** de API para el atributo **PtrSafe** , si es necesario, y el correspondiente tipo de valor devuelto. 
  
Instrucciones **Declare** se parecen a uno de los siguientes, dependiendo de si se está llamando a una subrutina (que no tiene ningún valor devuelto) o una función (que tiene un valor devuelto). 
  
```vb
Public/Private Declare Sub SubName Lib "LibName" Alias "AliasName" (argument list)
Public/Private Declare Function FunctionName Lib "Libname" alias "aliasname" (argument list) As Type

```

La función de **nombre secundario** o **nombrefunción** se ha reemplazado por el nombre real del procedimiento en el archivo DLL y representa el nombre que se usa cuando se llama al procedimiento desde el código VBA. También puede especificar un argumento **nombreAlias** para el nombre del procedimiento. El nombre del archivo DLL que contiene el procedimiento que se llama sigue la palabra clave **Lib** . Y, por último, la lista de argumentos contiene los parámetros y los tipos de datos que se deben pasar al procedimiento. 
  
La instrucción **Declare** siguiente abre una *subclave* en el registro de Windows y reemplaza su valor. 
  
```vb
Declare Function RegOpenKeyA Lib "advapi32.dll" (ByVal Key As Long, ByVal SubKey As String, NewKey As Long) As Long
```

La entrada de Windows.h (identificador de ventana) para la función **RegOpenKeyA** es la siguiente: 
  
```vb
LONG RegOpenKeyA ( HKEY hKey, LPCSTR lpSubKey, HKEY *phkResult );
```

En Visual C y Microsoft Visual C++, en el ejemplo anterior se compila correctamente para 32 bits y 64 bits. Esto es debido a que HKEY se define como un puntero, cuyo tamaño refleja el tamaño de la memoria de la plataforma que el código se compila en.
  
En versiones anteriores de VBA, se ha producido ningún tipo de datos de puntero específicos por lo que se usó el tipo de datos **Long** . Y debido a que el tipo de datos **Long** es siempre este saltos cuando se usa en un sistema con memoria de 64 bits porque los superiores 32 bits se pueden truncar o es posible que sobrescribir otras direcciones de memoria de 32 bits. Cualquiera de estas situaciones puede provocar bloqueos imprevisibles de comportamiento o del sistema. 
  
Para resolver este problema, VBA incluye un tipo de datos es true *puntero* : **LongPtr**. Este nuevo tipo de datos le permite escribir la instrucción **Declare** original correctamente como: 
  
```vb
Declare PtrSafe Function RegOpenKeyA Lib "advapire32.dll" (ByVal hKey as LongPtr, ByVal lpSubKey As String, phkResult As LongPtr) As Long
```

Este tipo de datos y el nuevo atributo **PtrSafe** permiten utilizar esta instrucción **Declare** en sistemas de 32 bits o 64 bits. El atributo **PtrSafe** indica que el compilador VBA que la instrucción **Declare** está destinada a la versión de 64 bits de Office. Sin este atributo, el uso de la instrucción **Declare** en un sistema de 64 bits, se producirá un error en tiempo de compilación. El atributo **PtrSafe** es opcional en la versión de 32 bits de Office. Esto permite que las instrucciones **Declare** existentes para que funcione como siempre lo han. 
  
En la siguiente tabla se proporciona más información acerca del nuevo calificador y datos typeas así como otro tipo de datos, dos operadores de conversión y tres funciones.
  
|Tipo|Elemento|Descripción|
|:-----|:-----|:-----|
|Calificador  <br/> |**PtrSafe** <br/> |Indica que la instrucción **Declare** es compatible con 64 bits. Este atributo es obligatorio en sistemas de 64 bits.<br/> |
|Tipo de datos  <br/> |**LongPtr** <br/> |Un tipo de datos de la variable que es un tipo de datos de 4 bytes en las versiones de 32 bits y un tipo de datos de 8 bytes en las versiones de 64 bits de Microsoft Office. Esta es la manera recomendada de declaración de un puntero o un identificador para el nuevo código, sino también para el código heredado si tiene que ejecutar en la versión de 64 bits de Office. Sólo se admite en el tiempo de ejecución de VBA 7 de 32 bits y 64 bits. Tenga en cuenta que puede asignar valores numéricos a ella pero tipos no numéricos.  <br/> |
|Tipo de datos  <br/> |**LongLong** <br/> |Este es un tipo de datos de 8 bytes que sólo está disponible en versiones de 64 bits de Microsoft Office. Puede asignar valores numéricos pero tipos no numéricos (para evitar el truncamiento).  <br/> |
|Operador de conversión  <br/> |**CLngPtr** <br/> |Convierte una expresión simple en un tipo de datos **LongPtr**.  <br/> |
|Operador de conversión  <br/> |**CLngLng** <br/> |Convierte una expresión simple en un tipo de datos **LongLong**.  <br/> |
|Funci?n  <br/> |**VarPtr** <br/> |Convertidor de datos Variant. Devuelve un tipo de datos **LongPtr** en versiones de 64 bits y **Long** en versiones de 32 bits (4 bytes).<br/> |
|Funci?n  <br/> |**ObjPtr** <br/> |Convertidor de objetos. Devuelve un tipo de datos **LongPtr** en versiones de 64 bits y **Long** en versiones de 32 bits (4 bytes).<br/> |
|Funci?n  <br/> |**StrPtr** <br/> |Convertidor de cadena. Devuelve un tipo de datos **LongPtr** en versiones de 64 bits y **Long** en versiones de 32 bits (4 bytes).<br/> |
   
El siguiente ejemplo muestra cómo usar algunos de estos elementos en una instrucción **Declare**. 
  
```vb
Declare PtrSafe Function RegOpenKeyA Lib "advapi32.dll" (ByVal Key As LongPtr, ByVal SubKey As String, NewKey As LongPtr) As Long
```

Tenga en cuenta las instrucciones **Declare** sin el atributo **PtrSafe** se supone que no sea compatible con la versión de 64 bits de Office. 
  
Hay dos constantes de compilación condicional: **VBA7** y **Win64**. Para garantizar la compatibilidad con versiones anteriores con versiones anteriores de Microsoft Office, utiliza la constante de **VBA7** (Esto es el caso más típico) para evitar que el código de 64 bits que se usa en la versión anterior de Office. Para que el código sea diferente entre la versión de 32 bits y la versión de 64 bits, como una llamada a un coprocesador API que usa **LongLong** para su versión de 64 bits y **largo** para su versión de 32 bits, utilice la constante **Win64** . El siguiente código muestra el uso de estas dos constantes. 
  
```vb
#if Win64 then
   Declare PtrSafe Function MyMathFunc Lib "User32" (ByVal N As LongLong) As LongLong
#else
   Declare Function MyMathFunc Lib "User32" (ByVal N As Long) As Long
#end if
#if VBA7 then
   Declare PtrSafe Sub MessageBeep Lib "User32" (ByVal N AS Long)
#else
   Declare Sub MessageBeep Lib "User32" (ByVal N AS Long)
#end if
```

En resumen, si escribir código de 64 bits y va a utilizar en las versiones anteriores de Office, que desea usar la constante de compilación condicional **VBA7** . Sin embargo, si escribe un código de 32 bits en Office, ese código funciona como se encuentra en las versiones anteriores de Office sin necesidad de la constante de compilación. Si desea asegurarse de que está utilizando instrucciones de 32 bits para las versiones de 32 bits y 64 bits de instrucciones para las versiones de 64 bits, la mejor opción es usar la constante de compilación condicional **Win64** . 
  
## <a name="using-conditional-compilation-attributes"></a>Uso de atributos de compilación condicional
<a name="odc_office_Compatibility32bit64bit_UsingConditionalCompilationAttributes"> </a>

En el ejemplo siguiente se muestra el código de VBA escrito para 32 bits que deben actualizarse. Tenga en cuenta los tipos de datos en el código heredado que se actualizan para utilizar **LongPtr** , ya que hacen referencia a punteros o identificadores. 
  
### <a name="vba-code-written-for-32-bit-versions"></a>Código de VBA escrito para versiones de 32 bits
  
```vb
Declare Function SHBrowseForFolder Lib "shell32.dll" _
  Alias "SHBrowseForFolderA" (lpBrowseInfo As BROWSEINFO) As Long
  
Public Type BROWSEINFO
  hOwner As Long
  pidlRoot As Long
  pszDisplayName As String
  lpszTitle As String
  ulFlags As Long
  lpfn As Long
  lParam As Long
  iImage As Long
End Type
```

### <a name="vba-code-rewritten-for-64-bit-versions"></a>Código VBA que se modificó para versiones de 64 bits
  
```vb
#if VBA7 then    ' VBA7 
Declare PtrSafe Function SHBrowseForFolder Lib "shell32.dll" _
  Alias "SHBrowseForFolderA" (lpBrowseInfo As BROWSEINFO) As Long
Public Type BROWSEINFO
  hOwner As LongPtr
  pidlRoot As Long
  pszDisplayName As String
  lpszTitle As String
  ulFlags As Long
  lpfn As LongPtr
  lParam As LongPtr
  iImage As Long
End Type
 
#else    ' Downlevel when using previous version of VBA7
Declare Function SHBrowseForFolder Lib "shell32.dll" _
  Alias "SHBrowseForFolderA" (lpBrowseInfo As BROWSEINFO) As Long
Public Type BROWSEINFO
  hOwner As Long
  pidlRoot As Long
  pszDisplayName As String
  lpszTitle As String
  ulFlags As Long
  lpfn As Long
  lParam As Long
  iImage As Long
End Type
 
#end if
Sub TestSHBrowseForFolder ()
    Dim bInfo As BROWSEINFO
    Dim pidList As Long
    bInfo.pidlRoot = 0&amp;
    bInfo.ulFlags = &amp;H1
    pidList = SHBrowseForFolder(bInfo)
End Sub
```

<a name="odc_office_Compatibility32bit64bit_FrequentlyAskedQuestions"> </a>

## <a name="frequently-asked-questions"></a>Preguntas más frecuentes

#### <a name="when-should-i-use-the-64-bit-version-of-office"></a>¿Cuándo debo usar la versión de 64 bits de Office?
  
Esto es más una cuestión de la aplicación host (Excel, Word etc.) que está utilizando. Por ejemplo, Excel es capaz de controlar mucho más grandes hojas de cálculo con la versión de 64 bits de Microsoft Office.
  
#### <a name="can-i-install-64-bit-and-32-bit-versions-of-office-side-by-side"></a>¿Puedo instalar versiones de 32 bits y de 64 bits de Office en paralelo?
  
No.
  
#### <a name="when-should-i-convert-long-parameters-to-longptr"></a>¿Cuándo debo convertir parámetros largos a LongPtr?
  
Debe consultar la documentación de API de Windows en la red de programadores de Microsoft para la función que desea llamar. Punteros y controladores necesitan que se va a convertir a **LongPtr**. Por ejemplo, la documentación de [RegOpenKeyA](https://msdn.microsoft.com/library/c8a590f2-3249-437f-a320-c7443d42b792.aspx) proporciona la siguiente firma: 
  
```cs
LONG WINAPI RegOpenKeyEx(
  __in        HKEY hKey,
  __in_opt    LPCTSTR lpSubKey,
  __reserved  DWORD ulOptions,
  __in        REGSAM samDesired,
  __out       PHKEY phkResult
);
```

Los parámetros se definen como:
  
|Parámetro|Descripción|
|:-----|:-----|
|hKey [in]  <br/> |*Controlar* a una clave del registro abierta.  <br/> |
|lpSubKey [entrada, opcional]  <br/> |El nombre de la subclave del registro que se va a abrir.  <br/> |
|ulOptions  <br/> |Este parámetro está reservado y debe ser cero.  <br/> |
|samDesired [in]  <br/> |Máscara que especifica los derechos de acceso que desee a la clave.  <br/> |
|phkResult [out]  <br/> |Un *puntero* a una variable que recibe un identificador de la clave abierta.  <br/> |
   
En [Win32API_PtrSafe.txt](https://www.microsoft.com/downloads/details.aspx?displaylang=en&amp;FamilyID=035b72a5-eef9-4baf-8dbc-63fbd2dd982b), la instrucción **Declare** se define como: 
  
```vb
Declare PtrSafe Function RegOpenKeyEx Lib "advapi32.dll" Alias "RegOpenKeyExA" (ByVal hKey As LongPtr , ByVal lpSubKey As String, ByVal ulOptions As Long, ByVal samDesired As Long, phkResult As LongPtr ) As Long
```

#### <a name="should-i-convert-pointers-and-handles-in-structures"></a>¿Debo convertir punteros e identificadores en estructuras?
  
Sí. Vea el tipo de **mensaje** en Win32API_PtrSafe.txt: 
  
```vb
Type MSG
    hwnd As LongPtr 
    message As Long
    wParam As LongPtr 
    lParam As LongPtr 
    time As Long
    pt As POINTAPI
End TypeF
```

#### <a name="when-should-i-use-strptr-varpt-and-objptr"></a>¿Cuándo debo usar strptr, varpt y objptr?
  
Debe utilizar estas funciones para recuperar punteros a cadenas, variables y objetos, respectivamente. En la versión de 64 bits de Office, estas funciones devolverán de 64 bits **LongPtr**, que se puede pasar a las instrucciones **Declare** . El uso de estas funciones no ha cambiado desde las versiones anteriores de VBA. La única diferencia es que ahora devuelven un **LongPtr**.
  
## <a name="see-also"></a>Vea también
<a name="odc_office_Compatibility32bit64bit_AdditionalResources"> </a>

- [Anatomía de una instrucción Declare](https://msdn.microsoft.com/library/office/aa671659.aspx)
    

