---
title: Compatibilidad entre versiones de 32 y 64 bits de Office
ms.date: 04/27/2016
ms.audience: ITPro
ms.assetid: ff49dc9e-daf8-43cf-8802-51c2537ed561
description: Descubra cómo la versión de 32 bits de Office es compatible con de 64 bits.
localization_priority: Priority
ms.openlocfilehash: b03323b37b242c9992c47cd737ae54f3f9bbf2ca
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359825"
---
# <a name="compatibility-between-the-32-bit-and-64-bit-versions-of-office"></a>Compatibilidad entre versiones de 32 y 64 bits de Office

Descubra cómo la versión de 32 bits de Office es compatible con de 64 bits.
  
Las aplicaciones de Office están disponibles en versiones de 32 y 64 bits. 
  
Las versiones de 64 bits de Office permiten desplazar más datos para obtener una mayor capacidad, por ejemplo, al trabajar con números grandes en Microsoft Excel 2010. Al escribir código de 32 bits, puede usar la versión de 64 bits de Office sin cambios. Sin embargo, al escribir el código de 64 bits, debe asegurarse de que el código contiene palabras clave específicas y constantes de compilación condicional para asegurarse de que el código es compatible con la versión anterior de Office y que el código correcto se ejecuta si se combinan códigos de 32 y 64 bits.
  
Visual Basic para Aplicaciones 7.0 (VBA 7) se publicó en las versiones de 64 bits de Office y funciona tanto con aplicaciones de 32 como de 64 bits. Los cambios descritos en este artículo solo se aplican a las versiones de 64 bits de Office. Usar las versiones de 32 bits de Microsoft Office le permite utilizar soluciones integradas en versiones anteriores de Office sin realizar modificaciones.
  
> [!NOTE]
> De forma predeterminada, cuando se instala una versión de 64 bits de Office, también se instala la versión de 32 bits con el sistema de 64 bits. Debe seleccionar explícitamente la opción de instalación de la versión de 64 bits de Microsoft Office. 
  
En VBA 7, se deben actualizar las instrucciones existentes de la API de Windows (instrucciones **Declarar**) para que funcione con la versión de 64 bits. Además, se deben actualizar los punteros de dirección y los controladores de ventanas en los tipos definidos por el usuario que usan estas instrucciones. Esto se describe en detalle en este artículo, así como también los problemas de compatibilidad entre las versiones de 32 y 64 bits y las soluciones recomendadas. 
  
## <a name="comparing-32-bit-and-64-bit-systems"></a>Comparación de los sistemas de 32 y 64 bits
<a name="odc_office_Compatibility32bit64bit_Comparing32BitSystemsto64BitSystems"> </a>

Las aplicaciones integradas con las versiones de 64 bits de Office pueden hacer referencia a espacios de direcciones más grandes que las versiones de 32 bits. Esto significa que puede usar más memoria física para datos que antes, lo que probablemente reduzca la sobrecarga utilizada en la entrada y salida de datos de la memoria física
  
Además de hacer referencia a ubicaciones específicas (denominadas punteros) en la memoria física, también puede usar direcciones para hacer referencia a los identificadores de ventanas (denominados controladores). El tamaño (en bytes) del puntero o controlador depende de si usa un sistema de 32 o 64 bits. 
  
Si desea ejecutar las soluciones existentes con las versiones de 64 bits de Office, tenga en cuenta lo siguiente:
  
- Los procesos nativos de 64 bits de Office no pueden cargar archivos binarios de 32 bits. Este será un problema habitual cuando se tengan ya controles Microsoft ActiveX y complementos.
    
- Anteriormente, VBA no tenía un tipo de datos de punteros, por lo que se tenían que usar variables de 32 bits para almacenar punteros y controladores. Ahora, estas variables truncan los valores de 64 bits devueltos por las llamadas a la API al usar instrucciones **Declarar**. 
    
## <a name="vba-7-code-base"></a>Base del código de VBA 7
<a name="odc_office_Compatibility32bit64bit_IntroducingVBA7CodeBase"> </a>

VBA 7 reemplaza la base del código VBA en Office 2007 y versiones anteriores. VBA 7 se encuentra disponible tanto en la versión de 32 como en la de 64 bits de Office. Ofrece dos constantes de compilación condicional: 
  
- **VBA7**: ayuda a garantizar la compatibilidad con versiones anteriores del código al comprobar si la aplicación usa VBA 7 o la versión anterior. 
    
- **Win64**: comprueba si el código se ejecuta en 32 o 64 bits. 
    
Con algunas excepciones, las macros de un documento que funcionan en la versión de 32 bits de la aplicación también funcionan en la versión de 64 bits.
  
## <a name="activex-control-and-com-add-in-compatibility"></a>Compatibilidad de controles ActiveX y complementos COM
<a name="odc_office_Compatibility32bit64bit_ActiveXControlCOMAddinCompatibility"> </a>

Los controles ActiveX de 32 bits existentes no son compatibles con las versiones de 64 bits de Office. Para controles ActiveX y objetos COM:
  
- Si se dispone del código fuente, puede generar una versión de 64 bits.
- Si no cuenta con el código fuente, póngase en contacto con el proveedor para obtener una versión actualizada.
    
Los procesos nativos de 64 bits de Office no pueden cargar archivos binarios de 32 bits. Esto incluye los controles comunes de **MSComCtl** (TabStrip, Toolbar, StatusBar, ProgressBar, TreeView, ListViews, ImageList, Slider, ImageComboBox) y los controles de **MSComCt2** (Animation, UpDown, MonthView, DateTimePicker, FlatScrollBar). Estos controles se instalaron con versiones de 32 bits de Office anteriores a Office 2010. Deberá buscar una alternativa para las soluciones de VBA existentes que usan estos controles al migrar el código a las versiones de 64 bits de Office. 
  
## <a name="api-compatibility"></a>Compatibilidad de API
<a name="odc_office_Compatibility32bit64bit_ApplicationProgrammingInterfaceCompatibility"> </a>

La combinación de las bibliotecas de VBA y de tipos ofrece una gran variedad de funcionalidad para crear aplicaciones de Office. Sin embargo, a veces debe comunicarse directamente con el sistema operativo y otros componentes, como cuando administra la memoria o los procesos al trabajar con elementos de la interfaz de usuario, tales como controles y ventanas o cuando se modifica el registro de Windows. En estos casos, la mejor opción es usar una de las funciones externas incrustadas en archivos DLL. Para ello en VBA, realice llamadas a la API con instrucciones **Declarar**. 
  
> [!NOTE]
> Microsoft proporciona un archivo Win32API.txt con 1 500 instrucciones **Declarar** y una herramienta para copiar la que desee en el código. Sin embargo, estas instrucciones son para sistemas de 32 bits y deben convertirse a 64 bits con la información que se describe más adelante en este artículo. Las instrucciones **Declarar** existentes no se compilarán en VBA de 64 bits hasta que hayan sido marcadas como seguras para 64 bits a través del atributo **PtrSafe**. Encontrará ejemplos de este tipo de conversión en el sitio web de Jan Karel Pieterse [ https://www.jkp-ads.com/articles/apideclarations.asp ](https://www.jkp-ads.com/articles/apideclarations.asp)sobre Excel MVP. La [Guía del usuario de Office Code Compatibility Inspector](https://technet.microsoft.com/es-ES/library/ee833946%28office.14%29.aspx) es una herramienta útil para inspeccionar la sintaxis de las instrucciones **Declarar** de la API para el atributo **PtrSafe**, si es necesario, y el tipo de valor devuelto correspondiente. 
  
Las instrucciones **Declarar** se verán como algunas de las siguientes, dependiendo de si se llama a una subrutina (que no tiene valor devuelto) o a una función (que sí tiene un valor devuelto). 
  
```vb
Public/Private Declare Sub SubName Lib "LibName" Alias "AliasName" (argument list)
Public/Private Declare Function FunctionName Lib "Libname" alias "aliasname" (argument list) As Type

```

La función **SubName** o **FunctionName** se reemplaza por el nombre real del procedimiento en el archivo DLL y representa el nombre que se usa cuando se llama al procedimiento desde el código de VBA. También puede especificar un argumento **AliasName** para el nombre del procedimiento. El nombre del archivo DLL que contiene el procedimiento al que se llama se coloca a continuación de la palabra clave **Lib**. Y por último, la lista de argumentos contiene los parámetros y los tipos de datos que se deben pasar al procedimiento. 
  
La siguiente instrucción **Declarar** abre una *subclave* en el registro de Windows y reemplaza su valor. 
  
```vb
Declare Function RegOpenKeyA Lib "advapi32.dll" (ByVal Key As Long, ByVal SubKey As String, NewKey As Long) As Long
```

La entrada Windows.h (controlador de la ventana) de la función **RegOpenKeyA** es la siguiente: 
  
```vb
LONG RegOpenKeyA ( HKEY hKey, LPCSTR lpSubKey, HKEY *phkResult );
```

En Visual C y Microsoft Visual C++, el ejemplo anterior compila correctamente tanto para 32 como para 64-bits. Esto es porque HKEY está definido como un puntero, cuyo tamaño refleja el tamaño de la memoria de la plataforma en la que se compila el código.
  
En versiones anteriores de VBA, no había ningún tipo de datos específico del puntero así que se utilizó el tipo de datos **Long**. Además, dado que el tipo de datos **Long** siempre es de 32 bits, este se interrumpe cuando se utiliza en un sistema con memoria de 64 bits ya que los 32 bits superiores pueden truncarse o podrían sobrescribir otras direcciones de memoria. Cualquiera de estas situaciones puede causar comportamientos impredecibles o bloqueos del sistema. 
  
Para resolver esto, VBA incluye un verdadero tipo de datos *puntero*: **LongPtr**. Este nuevo tipo de datos le permite escribir la instrucción **Declarar** original correctamente como: 
  
```vb
Declare PtrSafe Function RegOpenKeyA Lib "advapire32.dll" (ByVal hKey as LongPtr, ByVal lpSubKey As String, phkResult As LongPtr) As Long
```

Este tipo de datos y el nuevo atributo **PtrSafe** le permiten utilizar esta instrucción **Declarar** en sistemas de 32 o 64 bits. El atributo **PtrSafe** le indica al compilador de VBA que la instrucción **Declarar** está destinada a la versión de 64 bits de Office. Sin este atributo, al usar la instrucción **Declarar** en un sistema de 64 bits se producirá un error en tiempo de compilación. El atributo **PtrSafe** es opcional, en la versión de 32 bits de Office. Esto permite que las instrucciones **Declarar** existentes funcionen de manera habitual. 
  
La siguiente tabla proporciona más información sobre el nuevo calificador y el tipo de datos, así como otro tipo de datos, dos operadores de conversión y tres funciones.
  
|Tipo|Item|Descripción|
|:-----|:-----|:-----|
|Calificador  <br/> |**PtrSafe** <br/> |Indica que la instrucción **Declarar** es compatible con 64 bits. Este atributo es obligatorio en sistemas de 64 bits.  <br/> |
|Tipo de datos  <br/> |**LongPtr** <br/> |Un tipo de datos variable que es un tipo de datos de 4 bytes en versiones de 32 bits y un tipo de datos de 8 bytes en versiones de 64 bits de Microsoft Office. Esta es la manera recomendada de declarar un puntero o un controlador para un código nuevo, pero también para el código heredado si se tiene que ejecutar en la versión de 64 bits de Office. Solo es compatible en el tiempo de ejecución de VBA 7 de 32 y 64 bits. Tenga en cuenta que puede asignarle valores numéricos, pero no tipos numéricos.  <br/> |
|Tipo de datos  <br/> |**LongLong** <br/> |Este es un tipo de datos de 8 bytes que solo está disponible en versiones de 64 bits de Microsoft Office. Puede asignar valores numéricos, pero no tipos numéricos (para evitar truncamiento).  <br/> |
|Operador de conversión  <br/> |**CLngPtr** <br/> |Convierte una expresión sencilla en un tipo de datos **LongPtr**.  <br/> |
|Operador de conversión  <br/> |**CLngLng** <br/> |Convierte una expresión sencilla en un tipo de datos **LongLong**.  <br/> |
|Función  <br/> |**VarPtr** <br/> |Convertidor Variant. Devuelve un **LongPtr** en versiones de 64 bits y un **Long** en versiones de 32 bits (4 bytes).<br/> |
|Función  <br/> |**ObjPtr** <br/> |Convertidor Object. Devuelve un **LongPtr** en versiones de 64 bits y un **Long** en versiones de 32 bits (4 bytes).<br/> |
|Función  <br/> |**StrPtr** <br/> |Convertidor String. Devuelve un **LongPtr** en versiones de 64 bits y un **Long** en versiones de 32 bits (4 bytes).<br/> |
   
El siguiente ejemplo muestra cómo usar algunos de estos elementos en una instrucción **Declarar**. 
  
```vb
Declare PtrSafe Function RegOpenKeyA Lib "advapi32.dll" (ByVal Key As LongPtr, ByVal SubKey As String, NewKey As LongPtr) As Long
```

Tenga en cuenta que se asume que las instrucciones **Declarar** sin el atributo **PtrSafe** no son compatibles con la versión de 64 bits de Office. 
  
Existen dos constantes de compilación condicional: **VBA7** y **Win64**. Para garantizar la compatibilidad con versiones anteriores de Microsoft Office, se utiliza la constante **VBA7** (esto es lo más habitual) para evitar que el código de 64 bits se use en la versión anterior de Office. Para todo código que sea diferente de la versión de 32 y la de 64 bits, como por ejemplo, llamar a una API de matemáticas que utiliza **LongLong** para su versión de 64 bits y **Long** para su versión de 32 bits, se usa la constante **Win64**. El siguiente código muestra el uso de estas dos constantes. 
  
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

En resumen, si escribe código de 64 bits y desea usarlo en versiones anteriores de Office, tendrá que usar la constante de compilación condicional **VBA7**. Sin embargo, si escribe código de 32 bits en Office, ese código funciona como en versiones anteriores de Office sin necesidad de usar la constante de compilación. Si desea asegurarse de que está usando instrucciones de 32 bits para versiones de 32 bits e instrucciones de 64 bits para versiones de 64 bits, la mejor opción es usar la constante de compilación condicional **Win64**. 
  
## <a name="using-conditional-compilation-attributes"></a>Uso de atributos de compilación condicional
<a name="odc_office_Compatibility32bit64bit_UsingConditionalCompilationAttributes"> </a>

El siguiente ejemplo muestra el código VBA escrito para 32 bits que debe actualizarse. Observe los tipos de datos en el código heredado que se actualizan para usar **LongPtr** ya que hacen referencia a punteros o controladores. 
  
### <a name="vba-code-written-for-32-bit-versions"></a>Código VBA escrito para versiones de 32 bits
  
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

### <a name="vba-code-rewritten-for-64-bit-versions"></a>Código VBA reescrito para versiones de 64 bits
  
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

#### <a name="when-should-i-use-the-64-bit-version-of-office"></a>¿Cuándo debería usar la versión de 64 bits de Office?
  
Depende, en gran medida, de la aplicación host (Word, Excel, etc.) que utiliza. Por ejemplo, Excel es capaz de manejar hojas de cálculo mucho más grandes con la versión de 64 bits de Microsoft Office.
  
#### <a name="can-i-install-64-bit-and-32-bit-versions-of-office-side-by-side"></a>¿Puedo instalar las versiones de 32 y 64 bits de Office en paralelo?
  
No.
  
#### <a name="when-should-i-convert-long-parameters-to-longptr"></a>¿Cuándo debo convertir los parámetros Long a LongPtr?
  
Debe comprobar la documentación de la API de Windows en Microsoft Developers Network para la función que desea llamar. Es necesario convertir los controladores y punteros a **LongPtr**. Por ejemplo, la documentación de [RegOpenKeyA](https://msdn.microsoft.com/library/c8a590f2-3249-437f-a320-c7443d42b792.aspx) proporciona la siguiente firma: 
  
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
|hKey [in]  <br/> |Un *controlador* a una clave del registro abierta.  <br/> |
|lpSubKey [in, opcional]  <br/> |El nombre de la subclave del registro que se abrirá.  <br/> |
|ulOptions  <br/> |Este parámetro está reservado y debe ser cero.  <br/> |
|samDesired [in]  <br/> |Máscara que especifica los derechos de acceso deseados a la clave.  <br/> |
|phkResult [out]  <br/> |Un *puntero* a una variable que recibe un controlador a la clave abierta.  <br/> |
   
En [Win32API_PtrSafe.txt](https://www.microsoft.com/downloads/details.aspx?displaylang=en&amp;FamilyID=035b72a5-eef9-4baf-8dbc-63fbd2dd982b), la instrucción **Declarar** se define como: 
  
```vb
Declare PtrSafe Function RegOpenKeyEx Lib "advapi32.dll" Alias "RegOpenKeyExA" (ByVal hKey As LongPtr , ByVal lpSubKey As String, ByVal ulOptions As Long, ByVal samDesired As Long, phkResult As LongPtr ) As Long
```

#### <a name="should-i-convert-pointers-and-handles-in-structures"></a>¿Debo convertir punteros y controladores en estructuras?
  
Sí. Consulte el tipo **MSG** en Win32API_PtrSafe.txt: 
  
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
  
Debe usar estas funciones para recuperar punteros a cadenas, variables y objetos, respectivamente. En la versión de 64 bits de Office, estas funciones devuelven un parámetro **LongPtr** de 64 bits, que se puede pasar a las instrucciones **Declarar**. El uso de estas funciones no ha cambiado de versiones anteriores de VBA. La única diferencia es que ahora devuelven un parámetro **LongPtr**.
  
## <a name="see-also"></a>Vea también
<a name="odc_office_Compatibility32bit64bit_AdditionalResources"> </a>

- [Componentes de la Instrucción Declarar](https://msdn.microsoft.com/library/office/aa671659.aspx)
    

