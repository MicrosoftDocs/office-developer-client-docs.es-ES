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
- función de Excel4 [excel 2007], Excel12 (función) [Excel 2007]
localization_priority: Normal
ms.assetid: 2404f10d-8641-4ee6-a909-1c5a26610f80
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: c7caf4923e336020928006f6838de5eaeba814a4
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586812"
---
# <a name="excel4excel12"></a>Excel4/Excel12

**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio 
  
Llama a un interno función de hoja de cálculo de Microsoft Excel, una función de hoja de macros o un comando, o un solo XLL función especial o un comando, desde dentro de un DLL o XLL o recurso de código.
  
Todas las versiones recientes de Excel admiten **Excel4**. Iniciar en Excel 2007, se admite **Excel12** . 
  
Estas funciones se pueden llamar sólo cuando Excel ha pasado el control a la DLL o XLL. También puede llamar cuando Excel ha pasado control indirectamente a través de una llamada a Visual Basic para aplicaciones (VBA). No se puede llamar en cualquier otro momento. Por ejemplo, no se puede llamar durante las llamadas a la función [DllMain](https://docs.microsoft.com/windows/desktop/dlls/dllmain) u otros momentos cuando el sistema operativo se llama a la DLL, o desde un subproceso creado por el archivo DLL. 
  
Las funciones [Excel4v y Excel12v](excel4v-excel12v.md) aceptan sus argumentos como una matriz, mientras que las funciones de **Excel4** y **Excel12** aceptan sus argumentos como una lista de longitud variable en la pila. En todos los demás aspectos, **Excel4** se comporta de la misma que la **Excel4v**y **Excel12** se comporta igual que **Excel12v**.
  
```cs
int Excel4(int iFunction, LPXLOPER pxRes, int iCount, LPXLOPER argument1, ...);
int Excel12(int iFunction, LPXLOPER12 pxRes, int iCount, LPXLOPER12 argument1, ...);
```

## <a name="parameters"></a>Parámetros

 _iFunction_ (**int**)
  
Un número que indica el comando, función o función especial que desea llamar. Para obtener una lista de valores válidos _iFunction_ , vea la siguiente sección de comentarios. 
  
 _pxRes_ (**LPXLOPER** o **LPXLOPER12**)
  
Un puntero a un **XLOPER** (con **Excel4**) o un **XLOPER12** (con **Excel12**) que contendrá el resultado de la función evaluada.
  
 _iCount_ (**int**)
  
El número de argumentos subsiguientes que se va a pasar a la función. En las versiones de Excel hasta 2003, esto puede ser cualquier número comprendido entre 0 y 30. Iniciar en Excel 2007, esto puede ser cualquier número comprendido entre 0 y 255.
  
 _argumento1..._ (**LPXLOPER** o **LPXLOPER12**)
  
Los argumentos opcionales a la función. Todos los argumentos deben ser punteros a valores **XLOPER** o **XLOPER12** . 
  
## <a name="return-value"></a>Valor devuelto

Devuelve uno de los siguientes valores enteros (**int**).
  
|**Valor**|**Código de retorno**|**Descripción**|
|:-----|:-----|:-----|
|0  <br/> |**xlretSuccess** <br/> |La función se ha llamado correctamente. Esto no significa que la función no devolvió un valor de error de Excel; Para averiguarlo, debe mirar el tipo y el valor del parámetro _pxRes_ resultante.  <br/> |
|1  <br/> |**xlretAbort** <br/> |El comando o la función ha terminado anormalmente (anulación interna). Esto puede ocurrir si una hoja de macros XLM se cierra llamando al método **CLOSE**, o si Excel no tiene memoria suficiente. Si Excel devuelve este error, debe salir inmediatamente de la función de llamada. El archivo DLL se le permite llamar a **xlFree** sólo antes de salir. No se admiten todas las demás llamadas a la API de C. El usuario puede guardar cualquier trabajo de forma interactiva mediante el comando **Guardar** en el menú **archivo** .  <br/> |
|2  <br/> |**xlretInvXlfn** <br/> |Se ha proporcionado un número de función no válido. Si usa constantes desde el archivo de encabezado Xlcall.h, esto no debe ocurrir a menos que se va a llamar a algo que no es compatible con la versión de Excel que se está ejecutando.  <br/> |
|4  <br/> |**xlretInvCount** <br/> |Se ha escrito un número incorrecto de argumentos. En las versiones hasta Excel 2003, el número máximo de argumentos que se puede realizar cualquier función es 30. Iniciar en Excel 2007, el número máximo es de 255. Algunas requieren un número fijo o mínimo de argumentos.  <br/> |
|8  <br/> |**xlretInvXloper** <br/> |Se pasó un **XLOPER** o **XLOPER12** no válido para la función o se usó un argumento de tipo no válido.  <br/> |
|16  <br/> |**xlretStackOvfl** <br/> |Se ha producido un desbordamiento de pila. Use **xlStack** para supervisar la cantidad de sala izquierda en la pila. Evitar la asignación de matrices (automáticas) locales muy grandes y estructuras en la pila siempre que sea posible; hacerlas estática. (Tenga en cuenta que es posible que se produzcan un desbordamiento de pila sin ser detectado.)  <br/> |
|32  <br/> |**xlretFailed** <br/> |Error en una función de comando equivalente. Esto es equivalente a un comando de macro mostrando el cuadro de diálogo de alerta de error de macro.  <br/> |
|64  <br/> |**xlretUncalced** <br/> |Se intentó eliminar la referencia una celda que no se ha calculado todavía, porque se encuentra programada para volver a calcularse después de la celda actual. En este caso, el archivo DLL debe devolver el control a Excel inmediatamente. El archivo DLL se le permite llamar a **xlFree** sólo antes de salir. No se admiten todas las demás llamadas a la API de C. Para obtener más información acerca de qué puede y no pueden obtener acceso a los valores de celdas que no se ha vuelto a calcular las funciones, vea [los comandos de Excel, funciones y los Estados](excel-commands-functions-and-states.md).  <br/> |
|128  <br/> |**xlretNotThreadSafe** <br/> |Se ha intentado llamar a una función que no es o no es posible, subprocesos durante un nuevo cálculo multiproceso del libro.  <br/> Iniciar en Excel 2007, se devuelve este valor, y sólo dentro de las funciones de hoja de cálculo XLL declaradas como seguros para subprocesos.  <br/> |
|256  <br/> |**xlRetInvAsynchronousContext** <br/> |El identificador de función asincrónica no es válido.  <br/> Este valor se usa solo en Excel 2010.  <br/> |
|512  <br/> |**xlRetNotClusterSafe** <br/> |La llamada no se admite en clústeres.  <br/> Este valor se usa solo en Excel 2010.  <br/> |
   
## <a name="remarks"></a>Comentarios

### <a name="valid-ifunction-values"></a>Valores válidos iFunction

Los valores válidos **iFunction** son cualquiera de las constantes **xlf...** o **xlc...** definidas en el archivo de encabezado Xlcall.h o cualquiera de las siguientes funciones especiales. 
  
|||||
|:-----|:-----|:-----|:-----|
|**xlAbort** <br/> |**xlEnableXLMsgs** <br/> |**xlGetInst** <br/> |**xlSheetNm** <br/> |
|**xlCoerce** <br/> |**xlFree** <br/> |**xlGetName** <br/> |**xlStack** <br/> |
|**xlDefineBinaryName** <br/> |**xlGetBinaryName** <br/> |**xlSet** <br/> |**xlUDF** <br/> |
|**xlDisableXLMsgs** <br/> |**xlGetHwnd** <br/> |**xlSheetId** <br/> ||
   
### <a name="different-types-of-functions"></a>Distintos tipos de funciones

 **Excel4** y **Excel12** distinguen entre tres clases de funciones. Las funciones se clasifican en los tres estados en los que Excel puede llamar a la DLL. 
  
- Clase 1 se aplica cuando se llama a la DLL desde una hoja de cálculo como consecuencia de recálculo. 
    
- Clase 2 se aplica cuando el archivo DLL se llama desde una macro de función o desde una hoja de cálculo en la que se ha registrado con un signo de número (#) en el tipo de texto.
    
- Clase 3 se aplica cuando se llama a un archivo DLL desde un objeto, macro, menú, la barra de herramientas, tecla de método abreviado, **ExecuteExcel4Macro** (método) o el comando de **Herramientas o Macro/ejecutar** . Para obtener más información, vea [comandos de Excel, funciones y los Estados](excel-commands-functions-and-states.md).
    
En la siguiente tabla muestra qué funciones son válidas en cada clase.
  
|**Clase 1**|**Clase 2**|**Clase 3**|
|:-----|:-----|:-----|
|Cualquier función de hoja de cálculo  <br/> Cualquier función solo XLL **xl...** excepto **xlSet**.  <br/> **xlfCaller** <br/> |Cualquier función de hoja de cálculo  <br/> Cualquier función **xl...** excepto **xlSet**.  <br/> Macro las funciones de hojas, incluidos **xlfCaller**, que devuelve un valor, pero realizan ninguna acción que afecta al área de trabajo o cualquier libro abierto.  <br/> |Cualquier función, incluidas las funciones de comando equivalente y **xlSet** .  <br/> |
   
### <a name="displaying-the-dialog-box-for-a-command-equivalent-function"></a>Mostrar el cuadro de diálogo para una función de comando equivalente

Si una función de comando equivalente tiene un cuadro de diálogo asociados, puede establecer el bit de **xlPrompt** en **iFunction**. Esto significa que Excel muestra el cuadro de diálogo adecuado antes de llevar a cabo el comando.
  
### <a name="writing-international-dlls"></a>Escribir archivos DLL internacionales

Si se establece el bit de **xlIntl** en **iFunction**, la función o el comando se lleva a cabo como si se llamó desde una hoja de macros internacional. Esto significa que el comando se comporta igual que lo haría en la versión de Excel, incluso si se está ejecutando en una versión internacional (localizada).
  
### <a name="xlretuncalced-or-xlretabort"></a>xlretUncalced o xlretAbort

Después de recibir uno de estos valores devueltos, el archivo DLL debe limpiar y devolver el control inmediatamente a Excel. Las devoluciones de llamada en Excel a través de la API de C, excepto **xlFree**, se deshabilitan después de recibir uno de estos valores devueltos.
  
## <a name="example"></a>Ejemplo

En el ejemplo siguiente se usa la función de **Excel12** para seleccionar la celda desde la que se ha llamado. 
  
Este ejemplo de código forma parte de un ejemplo más extenso en el SDK de XLL de Excel 2010, en la siguiente ubicación donde instaló el SDK:
  
\Samples\Example\Example.c.
  
> [!NOTE]
> Esta función llama a una macro de comando (xlcSelect) y, por lo tanto, sólo funciona si se llama desde una hoja de macros XLM. 
  
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

## <a name="see-also"></a>Recursos adicionales



[Excel4v/Excel12v](excel4v-excel12v.md)

