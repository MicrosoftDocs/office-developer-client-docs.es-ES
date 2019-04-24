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
- función excel4 [Excel 2007], función Excel12 [Excel 2007]
localization_priority: Normal
ms.assetid: 2404f10d-8641-4ee6-a909-1c5a26610f80
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 7c3af5f380ae4144890b1f7b486a61a05c19de74
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32304112"
---
# <a name="excel4excel12"></a>Excel4/Excel12

**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio 
  
Llama a una función de hoja de cálculo de Microsoft Excel, a un comando o a una función de hoja de macros o a un comando especial sólo XLL, desde un archivo DLL/XLL o un recurso de código.
  
Todas las versiones recientes de Excel admiten **Excel4**. A partir de Excel 2007, **Excel12** es compatible. 
  
Estas funciones solo se pueden llamar cuando Excel ha pasado el control a la DLL o XLL. También se pueden llamar cuando Excel ha pasado el control indirectamente a través de una llamada a Visual Basic para aplicaciones (VBA). No se pueden llamar en ningún otro momento. Por ejemplo, no se pueden llamar durante las llamadas a la función [DllMain](https://docs.microsoft.com/windows/desktop/dlls/dllmain) u otras horas en las que el sistema operativo haya llamado a la dll, o de un subproceso creado por la dll. 
  
Las funciones [Excel4v y Excel12v](excel4v-excel12v.md) aceptan sus argumentos como una matriz, mientras que las funciones de **Excel4** y **Excel12** aceptan sus argumentos como una lista de longitud variable en la pila. En todos los demás aspectos, **Excel4** se comporta del mismo modo que **Excel4v**y **Excel12** se comporta del mismo modo que **Excel12v**.
  
```cs
int Excel4(int iFunction, LPXLOPER pxRes, int iCount, LPXLOPER argument1, ...);
int Excel12(int iFunction, LPXLOPER12 pxRes, int iCount, LPXLOPER12 argument1, ...);
```

## <a name="parameters"></a>Parameters

 _iFunction_ (**int**)
  
Número que indica el comando, la función o la función especial a la que se desea llamar. Para obtener una lista de los valores válidos de _iFunction_ , vea la siguiente sección de comentarios. 
  
 _pxRes_ (**LPXLOPER** o **LPXLOPER12**)
  
Un puntero a un **XLOPER** (con **Excel4**) o a un **XLOPER12** (con **Excel12**) que contendrá el resultado de la función evaluada.
  
 _iCount_ (**int**)
  
Número de argumentos subsiguientes que se van a pasar a la función. En las versiones de Excel de hasta 2003, puede ser cualquier número entre 0 y 30. A partir de Excel 2007, puede ser cualquier número comprendido entre 0 y 255.
  
 _argumento1,..._ (**LPXLOPER** o **LPXLOPER12**)
  
Argumentos opcionales de la función. Todos los argumentos deben ser punteros a valores **XLOPER** o **XLOPER12** . 
  
## <a name="return-value"></a>Valor devuelto

Devuelve uno de los siguientes valores enteros (**int**).
  
|**Value**|**Código deVuelto**|**Descripción**|
|:-----|:-----|:-----|
|comprendi  <br/> |**xlretSuccess** <br/> |Se ha llamado correctamente a la función. Esto no significa que la función no devolvió un valor de error de Excel; para averiguarlo, debe mirar el tipo y el valor del parámetro _pxRes_ resultante.  <br/> |
|1  <br/> |**xlretAbort** <br/> |El comando o la función se terminó anormalmente (anulación interna). Esto puede ocurrir si una hoja de macros XLM se cierra llamando a **Close**o si Excel no tiene memoria. Si Excel devuelve este error, la función de llamada debe salir inmediatamente. La DLL solo puede llamar a **xlFree** antes de salir. No se permiten todas las demás llamadas a la API de C. El usuario puede guardar cualquier trabajo de forma interactiva usando el comando **Guardar** en el menú **archivo** .  <br/> |
|segundo  <br/> |**xlretInvXlfn** <br/> |Se ha proporcionado un número de función no válido. Si usa constantes del archivo de encabezado xlcall. h, esto no debería ocurrir a menos que esté llamando a algo que no es compatible con la versión de Excel que está ejecutando.  <br/> |
|4  <br/> |**xlretInvCount** <br/> |Se especificó un número de argumentos no válido. En las versiones hasta Excel 2003, el número máximo de argumentos que puede tomar cualquier función es 30. A partir de Excel 2007, el número máximo es 255. Algunos requieren un número fijo o mínimo de argumentos.  <br/> |
|8,5  <br/> |**xlretInvXloper** <br/> |Se ha pasado un **XLOPER** o **XLOPER12** no válido a la función o se ha utilizado un argumento de tipo incorrecto.  <br/> |
|16  <br/> |**xlretStackOvfl** <br/> |Se ha producido un desbordamiento de pila. Use **xlStack** para supervisar la cantidad de espacio restante en la pila. Evite asignar matrices y estructuras locales (automáticas) muy grandes en la pila cuando sea posible; hacerlos estáticos. (Tenga en cuenta que es posible que se produzca un desbordamiento de pila sin que se detecte).  <br/> |
|32  <br/> |**xlretFailed** <br/> |Error en una función equivalente a un comando. Equivale a un comando de macro que muestra el cuadro de diálogo de alerta de error de macro.  <br/> |
|64  <br/> |**xlretUncalced** <br/> |Se intentó deshacer la referencia a una celda que aún no se ha calculado porque está programada para volver a calcularse después de la celda actual. En este caso, el archivo DLL debe devolver el control a Excel inmediatamente. La DLL solo puede llamar a **xlFree** antes de salir. No se permiten todas las demás llamadas a la API de C. Para obtener más información sobre las funciones que pueden y no pueden tener acceso a los valores de las celdas que no se han recalculado, consulte [comandos, funciones y Estados de Excel](excel-commands-functions-and-states.md).  <br/> |
|128  <br/> |**xlretNotThreadSafe** <br/> |Se intentó llamar a una función que no es o podría no ser segura para subprocesos durante una actualización multiproceso del libro.  <br/> A partir de Excel 2007, se devuelve este valor y solo dentro de las funciones de hoja de cálculo XLL declaradas como seguras para subprocesos.  <br/> |
|256  <br/> |**xlRetInvAsynchronousContext** <br/> |El controlador de la función asincrónica no es válido.  <br/> Este valor solo se usa en Excel 2010.  <br/> |
|512  <br/> |**xlRetNotClusterSafe** <br/> |La llamada no es compatible con los clústeres.  <br/> Este valor solo se usa en Excel 2010.  <br/> |
   
## <a name="remarks"></a>Comentarios

### <a name="valid-ifunction-values"></a>Valores válidos de iFunction

Los valores **IFunction** válidos son cualquiera de las constantes **XLF..** . o **XLC...** que se definen en el archivo de encabezado xlcall. h o cualquiera de las siguientes funciones especiales. 
  
|||||
|:-----|:-----|:-----|:-----|
|**xlAbort** <br/> |**xlEnableXLMsgs** <br/> |**xlGetInst** <br/> |**xlSheetNm** <br/> |
|**xlCoerce** <br/> |**xlFree** <br/> |**xlGetName** <br/> |**xlStack** <br/> |
|**xlDefineBinaryName** <br/> |**xlGetBinaryName** <br/> |**xlSet** <br/> |**xlUDF** <br/> |
|**xlDisableXLMsgs** <br/> |**xlGetHwnd** <br/> |**xlSheetId** <br/> ||
   
### <a name="different-types-of-functions"></a>Diferentes tipos de funciones

 **Excel4** y **Excel12** distinguen entre tres clases de funciones. Las funciones se clasifican de acuerdo con los tres Estados en los que Excel puede llamar a la DLL. 
  
- La clase 1 se aplica cuando se llama a la DLL desde una hoja de cálculo como resultado de una actualización. 
    
- La clase 2 se aplica cuando se llama a la DLL desde dentro de una macro de función o desde una hoja de cálculo donde se registró con un signo de número (#) en el texto del tipo.
    
- La clase 3 se aplica cuando se llama a un archivo DLL desde un objeto, una macro, un menú, una barra de herramientas, una tecla de método abreviado, un método **ExecuteExcel4Macro** o el comando **Tools/macro/Run** . Para obtener más información, vea [comandos, funciones y Estados de Excel](excel-commands-functions-and-states.md).
    
En la siguiente tabla se muestran las funciones válidas en cada clase.
  
|**Clase 1**|**Clase 2**|**Clase 3**|
|:-----|:-----|:-----|
|Cualquier función de hoja de cálculo  <br/> Cualquier función **XL...** solo XLL, excepto **xlSet**.  <br/> **xlfCaller** <br/> |Cualquier función de hoja de cálculo  <br/> Cualquier **XL...** function excepto **xlSet**.  <br/> Funciones de hoja de macros, incluida **xlfCaller**, que devuelven un valor pero no realizan ninguna acción que afecte al área de trabajo o a cualquier libro abierto.  <br/> |Cualquier función, incluidas las funciones **xlSet** y equivalentes a comandos.  <br/> |
   
### <a name="displaying-the-dialog-box-for-a-command-equivalent-function"></a>Mostrar el cuadro de diálogo de una función equivalente a un comando

Si una función equivalente a un comando tiene asociado un cuadro de diálogo, puede establecer el bit **xlPrompt** en **iFunction**. Esto significa que Excel muestra el cuadro de diálogo apropiado antes de ejecutar el comando.
  
### <a name="writing-international-dlls"></a>Escribir archivos dll internacionales

Si establece el bit **xlIntl** en **iFunction**, la función o el comando se lleva a cabo como si se hubiese llamado desde una hoja de macros internacional. Esto significa que el comando se comporta como lo haría en la versión de Excel para Estados Unidos, incluso si se está ejecutando en una versión internacional (localizada).
  
### <a name="xlretuncalced-or-xlretabort"></a>xlretUncalced o xlretAbort

Después de recibir uno de estos valores devueltos, el DLL debe limpiar y devolver el control a Excel inmediatamente. Las deVoluciones de llamada en Excel a través de la API de C, excepto **xlFree**, se deshabilitan después de recibir uno de estos valores devueltos.
  
## <a name="example"></a>Ejemplo

En el siguiente ejemplo, se usa la función **Excel12** para seleccionar la celda desde la que se ha llamado. 
  
Este ejemplo de código forma parte de un ejemplo más extenso proporcionado en el SDK de XLL de Excel 2010, en la siguiente ubicación donde instaló el SDK:
  
\Samples\Example\Example.c.
  
> [!NOTE]
> Esta función llama a una macro de comando (xlcSelect) y, por lo tanto, solo funciona si se le llama desde una hoja de macros XLM. 
  
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

## <a name="see-also"></a>Vea también



[Excel4v/Excel12v](excel4v-excel12v.md)

