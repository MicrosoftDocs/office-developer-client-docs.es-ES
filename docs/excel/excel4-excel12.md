---
title: Excel4/Excel12
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Excel12
- Excel4
keywords:
- función excel4 [excel 2007],Función Excel12 [Excel 2007]
localization_priority: Normal
ms.assetid: 2404f10d-8641-4ee6-a909-1c5a26610f80
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 7c3af5f380ae4144890b1f7b486a61a05c19de74
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429449"
---
# <a name="excel4excel12"></a>Excel4/Excel12

**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio 
  
Llama a una función interna de hoja de cálculo de Microsoft Excel, una función o un comando de hoja de macros, o una función o un comando especial solo XLL, desde un dll/XLL o un recurso de código.
  
Todas las versiones recientes de Excel **admiten Excel4**. A partir de Excel 2007, **se admite Excel12.** 
  
Solo se puede llamar a estas funciones cuando Excel ha pasado el control a la DLL o XLL. También se pueden llamar cuando Excel ha pasado el control indirectamente a través de una llamada a Visual Basic para Aplicaciones (VBA). No se pueden llamar en ningún otro momento. Por ejemplo, no se pueden llamar durante llamadas a la función [DllMain](https://docs.microsoft.com/windows/desktop/dlls/dllmain) u otras veces cuando el sistema operativo ha llamado a la DLL o desde un subproceso creado por la DLL. 
  
Las [funciones Excel4v y Excel12v](excel4v-excel12v.md) aceptan sus argumentos como una matriz, mientras que las funciones **de Excel4** y **Excel12** aceptan sus argumentos como una lista de longitud variable en la pila. En el resto de aspectos, **Excel4** se comporta igual que **Excel4v** y **Excel12** se comporta igual que **Excel12v**.
  
```cs
int Excel4(int iFunction, LPXLOPER pxRes, int iCount, LPXLOPER argument1, ...);
int Excel12(int iFunction, LPXLOPER12 pxRes, int iCount, LPXLOPER12 argument1, ...);
```

## <a name="parameters"></a>Parámetros

 _iFunction_ (**int**)
  
Número que indica el comando, la función o la función especial a la que desea llamar. Para obtener una lista de los valores  _válidos de iFunction,_ vea la sección comentarios siguiente. 
  
 _pxRes_ (**LPXLOPER** o **LPXLOPER12**)
  
Puntero a un **XLOPER** (con **Excel4)** o **XLOPER12** (con **Excel12)** que contendrán el resultado de la función evaluada.
  
 _iCount_ (**int**)
  
Número de argumentos subsiguientes que se pasarán a la función. En versiones de Excel hasta 2003, puede ser cualquier número entre 0 y 30. A partir de Excel 2007, puede ser cualquier número entre 0 y 255.
  
 _argument1, ..._ (**LPXLOPER** o **LPXLOPER12**)
  
Argumentos opcionales de la función. Todos los argumentos deben ser punteros a **los valores XLOPER** **o XLOPER12.** 
  
## <a name="return-value"></a>Valor devuelto

Devuelve uno de los siguientes valores enteros (**int**).
  
|**Valor**|**Código de devolución**|**Descripción**|
|:-----|:-----|:-----|
|0  <br/> |**xlretSuccess** <br/> |Se ha llamado correctamente a la función. Esto no significa que la función no devuelva un valor de error de Excel; para averiguarlo, debes ver el tipo y el valor del parámetro  _pxRes_ resultante.  <br/> |
|1   <br/> |**xlretAbort** <br/> |El comando o la función finalizaron de forma anómala (anulación interna). Esto puede ocurrir si una hoja de macros XLM se cierra llamando a **CLOSE** o si Excel no tiene memoria. Si Excel devuelve este error, la función de llamada debe salir inmediatamente. La DLL solo puede llamar **a xlFree** antes de salir. No se permiten todas las demás llamadas a la API de C. El usuario puede guardar cualquier trabajo de forma interactiva mediante el comando **Guardar** del **menú** Archivo.  <br/> |
|2   <br/> |**xlretInvXlfn** <br/> |Se proporcionó un número de función no válido. Si usa constantes del archivo de encabezado Xlcall.h, esto no debería ocurrir a menos que llame a algo que no sea compatible con la versión de Excel que está ejecutando.  <br/> |
|4   <br/> |**xlretInvCount** <br/> |Se especificó un número de argumentos no válido. En versiones hasta Excel 2003, el número máximo de argumentos que puede tomar cualquier función es 30. A partir de Excel 2007, el número máximo es 255. Algunos requieren un número fijo o mínimo de argumentos.  <br/> |
|8   <br/> |**xlretInvXloper** <br/> |Se pasó **un XLOPER** o **XLOPER12** no válido a la función o se usó un argumento de tipo incorrecto.  <br/> |
|16   <br/> |**xlretStackOvfl** <br/> |Se produjo un desbordamiento de pila. Usa **xlStack para** supervisar la cantidad de espacio que queda en la pila. Evite asignar matrices y estructuras locales muy grandes (automáticas) en la pila siempre que sea posible; hacerlas estáticas. (Tenga en cuenta que puede producirse un desbordamiento de pila sin que se detecte).  <br/> |
|32  <br/> |**xlretFailed** <br/> |Error en una función equivalente a un comando. Esto equivale a un comando de macro que muestra el cuadro de diálogo de alerta de error de macro.  <br/> |
|64  <br/> |**xlretUncalced** <br/> |Se intentó desreferenciar una celda que aún no se ha calculado, porque está programada para volver a calcularse después de la celda actual. En este caso, la DLL debe devolver el control a Excel inmediatamente. La DLL solo puede llamar **a xlFree** antes de salir. No se permiten todas las demás llamadas a la API de C. Para obtener más información acerca de las funciones que pueden y no pueden tener acceso a los valores de celdas que no se han actualizado, vea [Comandos, funciones y estados de Excel](excel-commands-functions-and-states.md).  <br/> |
|128  <br/> |**xlretNotThreadSafe** <br/> |Se intentó llamar a una función que no es o podría no ser segura para subprocesos durante una actualización multiproceso del libro.  <br/> A partir de Excel 2007, se devuelve este valor y solo en las funciones de hoja de cálculo XLL declaradas como seguras para subprocesos.  <br/> |
|256  <br/> |**xlRetInvAsynchronousContext** <br/> |El controlador de la función asincrónica no es válido.  <br/> Este valor solo lo usa Excel 2010.  <br/> |
|512  <br/> |**xlRetNotClusterSafe** <br/> |La llamada no se admite en clústeres.  <br/> Este valor solo lo usa Excel 2010.  <br/> |
   
## <a name="remarks"></a>Comentarios

### <a name="valid-ifunction-values"></a>Valores válidos de iFunction

Los **valores válidos** de iFunction son cualquiera de las constantes **xlf...** o **xlc...** definidas en el archivo de encabezado Xlcall.h o cualquiera de las siguientes funciones especiales. 
  
|||||
|:-----|:-----|:-----|:-----|
|**xlAbort** <br/> |**xlEnableXLMsgs** <br/> |**xlGetInst** <br/> |**xlSheetNm** <br/> |
|**xlCoerce** <br/> |**xlFree** <br/> |**xlGetName** <br/> |**xlStack** <br/> |
|**xlDefineBinaryName** <br/> |**xlGetBinaryName** <br/> |**xlSet** <br/> |**xlUDF** <br/> |
|**xlDisableXLMsgs** <br/> |**xlGetHwnd** <br/> |**xlSheetId** <br/> ||
   
### <a name="different-types-of-functions"></a>Diferentes tipos de funciones

 **Excel4** y **Excel12** distinguen entre tres clases de funciones. Las funciones se clasifican de acuerdo con los tres estados en los que Excel puede llamar a la DLL. 
  
- La clase 1 se aplica cuando se llama a la DLL desde una hoja de cálculo como resultado de la actualización. 
    
- La clase 2 se aplica cuando se llama a la DLL desde una macro de función o desde una hoja de cálculo donde se registró con un signo de número (#) en el texto de tipo.
    
- La clase 3 se aplica cuando se llama a una DLL desde un objeto, macro, menú, barra de herramientas, tecla de método abreviado, método **ExecuteExcel4Macro** o el comando **Herramientas/Macro/Ejecutar.** Para obtener más información, vea [Comandos, funciones y estados de Excel.](excel-commands-functions-and-states.md)
    
En la tabla siguiente se muestran las funciones que son válidas en cada clase.
  
|**Clase 1**|**Clase 2**|**Clase 3**|
|:-----|:-----|:-----|
|Cualquier función de hoja de cálculo  <br/> Cualquier función xl... solo **XLL** excepto **xlSet**.  <br/> **xlfCaller** <br/> |Cualquier función de hoja de cálculo  <br/> Cualquier **función xl...** excepto **xlSet**.  <br/> Funciones de hoja de macros, **incluido xlfCaller**, que devuelven un valor pero no realizan ninguna acción que afecte al área de trabajo ni a ningún libro abierto.  <br/> |Cualquier función, incluidas **las funciones xlSet** y equivalentes a comandos.  <br/> |
   
### <a name="displaying-the-dialog-box-for-a-command-equivalent-function"></a>Mostrar el cuadro de diálogo para una Command-Equivalent de búsqueda

Si una función equivalente a un comando tiene un cuadro de diálogo asociado, puede establecer el bit **xlPrompt** en **iFunction**. Esto significa que Excel muestra el cuadro de diálogo adecuado antes de ejecutar el comando.
  
### <a name="writing-international-dlls"></a>Escritura de ARCHIVOS DLL internacionales

Si establece el bit **xlIntl** en **iFunction**, la función o el comando se lleva a cabo como si se llamara desde una hoja de macros internacional. Esto significa que el comando se comporta como lo haría en la versión estadounidense de Excel, incluso si se ejecuta en una versión internacional (localizada).
  
### <a name="xlretuncalced-or-xlretabort"></a>xlretUncalced o xlretAbort

Después de recibir uno de estos valores devueltos, la DLL debe limpiar y devolver el control a Excel inmediatamente. Las devoluciones de llamada a Excel a través de la API de C, excepto **xlFree**, se deshabilitan después de recibir uno de estos valores devueltos.
  
## <a name="example"></a>Ejemplo

En el ejemplo siguiente se **usa la función Excel12** para seleccionar la celda desde la que se llamó. 
  
Este ejemplo de código forma parte de un ejemplo más grande proporcionado en el SDK de XLL de Excel 2010, en la siguiente ubicación donde instaló el SDK:
  
\Samples\Example\Example.c.
  
> [!NOTE]
> Esta función llama a una macro de comandos (xlcSelect) y, por lo tanto, sólo funciona si se llama desde una hoja de macros XLM. 
  
```cs
short WINAPI Excel12Example(void)
{
    XLOPER12 xRes;
    Excel12(xlfCaller, &xRes, 0);
    Excel12(xlcSelect, 0, 1, (LPXLOPER12)&xRes);
    Excel12(xlFree, 0, 1, (LPXLOPER12)&xRes);
    return 1;
}
```

## <a name="see-also"></a>Consulte también



[Excel4v/Excel12v](excel4v-excel12v.md)

