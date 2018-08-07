---
title: Administración de memoria en Excel
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
keywords:
- xloper12 memory [excel 2007],managing memory in Excel,Excel stack,strings [Excel 2007], managing memory,memory management in Excel,XLOPER memory [Excel 2007],memory [Excel 2007], management guidelines
localization_priority: Normal
ms.assetid: 3bf5195b-6235-43cf-8795-0c7b0a63a095
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 97c76d762fdc5e575c571804816e5581a7bec8bb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815691"
---
# <a name="memory-management-in-excel"></a>Administración de memoria en Excel

 **Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio 
  
La administración de memoria es la mayor preocupación si quiere crear XLL eficaces y estables. Si no se administra bien la memoria, pueden surgir una serie de problemas en Microsoft Excel: desde pequeños problemas, como una asignación e inicialización de memoria ineficiente y pequeñas pérdidas de memoria, hasta problemas importantes, como la desestabilización de Excel.
  
Una mala administración de memoria es el origen más común de los problemas relacionados con complementos. Por lo tanto, debe compilar el proyecto con una estrategia coherente y bien planeada a través de la administración de memoria. 
  
La administración de memoria es más compleja en Microsoft Office Excel 2007 gracias a la Introducción de las actualizaciones de los libros multiproceso. Si quiere crear y exportar funciones de hoja de cálculo seguras para subprocesos, debe administrar los conflictos resultantes que se pueden producir cuando varios subprocesos compiten por el acceso.
  
Existen consideraciones de memoria para los siguientes tres tipos de estructura de datos:
  
- **XLOPER** y **XLOPER12**
    
- Cadenas que no se encuentran en **XLOPER** o **XLOPER12**
    
- Matrices de **FP** y **FP12** 
    
## <a name="xloperxloper12-memory"></a>Memoria XLOPER y XLOPER12

La estructura de datos **XLOPER**/ **XLOPER12** tiene algunos subtipos que contienen punteros a bloques de memoria, concretamente cadenas (**xltypeStr**), matrices (**xltypeMulti**) y referencias externas (**xltypeRef**). Tenga en cuenta que las matrices **xltypeMulti** pueden contener cadenas **XLOPER**/ **XLOPER12s** que apuntan a su vez a otros bloques de memoria. 
  
Un **XLOPER**/ **XLOPER12** puede crearse de varias maneras: 
  
- Mediante Excel al preparar los argumentos para pasarlos a una función XLL
    
- Mediante Excel al devolver **XLOPER** o **XLOPER12** en una llamada a la API de C 
    
- Mediante el DLL al crear los argumentos para pasarlos a la llamada de la API de C
    
- Mediante el DLL al crear un valor devuelto de la función XLL
    
Se puede asignar un bloque de memoria en uno de los tipos que apuntan a memoria de varias maneras:
  
- Puede ser un bloque estático dentro del DLL fuera de cualquier código de la función, en cuyo caso no tiene que asignar o liberar memoria.
    
- Puede ser un bloque estático dentro del DLL dentro de algún código de la función, en cuyo caso no tiene que asignar o liberar memoria.
    
- El DLL puede asignarlo y liberarlo de forma dinámica de distintas formas: **malloc** y **free**, **new** y **delete**, etc.
    
- Excel puede asignarlo de forma dinámica.
    
Dado el número de posibles orígenes de la memoria **XLOPER**/ **XLOPER12** y el número de situaciones en las que **XLOPER**/ **XLOPER12** pueden tener memoria asignada, no es sorprendente que este asunto pueda parecer difícil. Sin embargo, la complejidad se puede reducir en gran medida si sigue varias instrucciones y reglas. 
  
### <a name="rules-for-working-with-xloperxloper12"></a>Reglas para trabajar con XLOPER y XLOPER12

- No intente liberar memoria ni sobrescribir **XLOPER**/ **XLOPER12** que se pasan como argumentos a la función XLL. Debe tratar dichos argumentos como de solo lectura. Para obtener más información, vea "Devolver **XLOPER** o **XLOPER12** modificando argumentos locales" en [Problemas conocidos del desarrollo de XLL de Excel](known-issues-in-excel-xll-development.md).
    
- Si Excel asigna memoria para un **XLOPER**/ **XLOPER12** devuelto al DLL en una llamada a la API de C: 
    
  - Debe liberar la memoria cuando ya no necesita el **XLOPER**/ **XLOPER12** mediante una llamada a [xlFree](xlfree.md). No use cualquier otro método, como liberar ni eliminar, para liberar la memoria.
    
  - Si el tipo devuelto es **xltypeMulti**, no sobrescriba ningún **XLOPER**/ **XLOPER12** dentro de la matriz, especialmente si contienen cadenas, y especialmente no donde intenta sobrescribir con una cadena.
    
  - Si quiere devolver **XLOPER**/ **XLOPER12** a Excel como valor devuelto de la función de DLL, debe indicarle a Excel que hay memoria que debe liberar al terminar. 
    
- Solo debe llamar **xlFree** en **XLOPER**/ **XLOPER12** creado como el valor devuelto para una llamada a la API de C. 
    
- Si el DLL asigna memoria para **XLOPER**/ **XLOPER12** que quiere devolver a Excel como valor devuelto de la función de DLL, debe indicarle a Excel que hay memoria que DLL debe liberar. 
    
### <a name="guidelines-for-memory-management"></a>Directrices para la administración de memoria

- Sea coherente en el DLL del método que usa para asignar y liberar memoria. Evite mezclar métodos. Un buen enfoque es ajustar el método que use en una clase o estructura de memoria, en el que puede cambiar el método usado sin alterar el código en muchos lugares.
    
- Al crear matrices de **xltypeMulti** dentro del DLL, sea coherente en la forma en que asigna memoria para las cadenas: asigne siempre dinámicamente la memoria para ellos o use siempre la memoria estática. Para ello, al liberar memoria, sabrá que debe liberar siempre o nunca las cadenas. 
    
- Haga copias en profundidad de memoria asignada a Excel al copiar un **XLOPER**/ **XLOPER12** creado en Excel.
    
- No incluya cadenas asignadas a Excel **XLOPER**/ **XLOPER12** dentro de las matrices de **xltypeMulti**. Haga copias en profundidad de las cadenas y los punteros de almacenamiento para las copias de la matriz. 
    
## <a name="freeing-excel-allocated-xloperxloper12-memory"></a>Liberar memoria XLOPER o XLOPER12 asignada a Excel

Tenga en cuenta el siguiente comando XLL que usa **xlGetName** para obtener una cadena que contenga la ruta de acceso y el nombre del DLL y que los muestra en un cuadro de diálogo de alerta con **xlcAlert**.
  
```cs
int WINAPI show_DLL_name(void)
{
    XLOPER12 xDllName;
    if(Excel12(xlfGetName, &xDllName, 0) == xlretSuccess)
    {
        // Display the name.
        Excel12(xlcAlert, 0, 1, &xDllName);
        // Free the memory that Excel allocated for the string.
        Excel12(xlFree, 0, 1, &xDllName);
    }
    return 1;
}

```

Cuando la función ya no necesita la memoria a la que **xDllName** apunta, puede liberarla con una llamada a la [función xlFree](xlfree.md), una de las funciones de la API de C solo de DLL. 
  
La función **xlFree** se documenta en la sección de referencia de la función (consulte [Funciones de la API de C que se pueden llamar solo desde una DLL o XLL](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)), pero tenga en cuenta lo siguiente:
  
- Puede pasar punteros a más de un **XLOPER**/ **XLOPER12** en una sola llamada a **xlFree**, limitado solo por el número de argumentos de función admitidos en la versión en ejecución de Excel (30 en Excel 2003, 255 a partir de Excel 2007).
    
- **xlFree** configura el puntero contenido en **NULL** para asegurarse de que un intento de liberar **XLOPER**/ **XLOPER12** que ya se ha liberado es seguro. **xlFree** es la única función de la API de C que modifica los argumentos. 
    
- Puede llamar de forma segura a **xlFree** en cualquier **XLOPER**/ **XLOPER12** usado para el valor devuelto de una llamada a la API de C, independientemente de si contiene un puntero a la memoria. 
    
## <a name="returning-xloperxloper12s-to-be-freed-by-excel"></a>Devolver XLOPER o XLOPER12 para que Excel los libere

Suponga que desea modificar el comando de ejemplo en la sección anterior y lo cambia a una función de hoja de cálculo que devuelve el nombre de archivo y la ruta DLL cuando pasa un argumento **verdadero** **booleano** y **#N/A** en caso contrario. Evidentemente no puede llamar a **xlFree** para liberar la memoria de cadena antes de devolverla a Excel. Sin embargo, si no se ha liberado en algún momento, el complemento pierde memoria cada vez que se llama a la función. Para solucionar este problema, puede establecer un bit en el campo **xltype** del **XLOPER**/ **XLOPER12**, definido como **xlbitXLFree** en xlcall.h. Esta configuración le indica a Excel que debe liberar la memoria devuelta cuando ha terminado de copiar el valor. 
  
### <a name="example"></a>Ejemplo

En el siguiente ejemplo de código se muestra el comando XLL de la sección anterior convertido en una función de hoja de cálculo XLL.
  
```cs
LPXLOPER12 WINAPI get_DLL_name(int calculation_trigger)
{
    static XLOPER12 xRtnValue; // Not thread-safe
    Excel12(xlfGetName, &xRtnValue, 0);
// If xlfGetName failed, xRtnValue will be #VALUE!
    if(xRtnValue.xltype == xltypeStr)
    {
// Tell Excel to free the string memory after
// it has copied out the return value.
        xRtnValue.xltype |= xlbitXLFree;
    }
    return &xRtnValue;
}
```

Las funciones de XLL que usan **XLOPER**/ **XLOPER12** deben declararse como que toman y devuelven punteros a **XLOPER**/ **XLOPER12**. El uso en este ejemplo de un **XLOPER12** estático dentro de la función no es seguro para subprocesos. Puede registrar incorrectamente esta función como segura para subprocesos, pero correría el riesgo de que un subproceso sobrescriba **xRtnValue** antes de que otro haya terminado de usarlo. 
  
Debe establecer **xlbitXLFree** después de la llamada a la devolución de llamada de Excel que lo asigna. Si lo establece antes de esta, se sobrescribe y no tiene el efecto deseado. Si desea usar el valor como un argumento en una llamada a otra función de la API de C antes de volver a la hoja de cálculo, debe establecer este bit después de cualquier llamada. En caso contrario, confundirá las funciones que no lo enmascaran poco antes de proteger el tipo **XLOPER**/ **XLLOPER12**. 
  
## <a name="returning-xloperxloper12s-to-be-freed-by-the-dll"></a>Devolver XLOPER o XLOPER12 para que el DLL los libere

Un problema similar a este se produce cuando el XLL ha asignado memoria para un **XLOPER**/ **XLOPER12** y desea devolverla a Excel. Excel reconoce otro bit que se puede establecer en el campo **xltype** del **XLOPER**/ **XLOPER12**, definido como un **xlbitDLLFree** en xlcall.h. 
  
Cuando Excel recibe **un XLOPER**/ **XLOPER12** con este conjunto de bits, intenta llamar a una función que debería exportar el XLL denominado [xlAutoFree](xlautofree-xlautofree12.md) (para **XLOPER**) o **xlAutoFree12** (para **XLOPER12**). Esta función se describe más detalladamente en la referencia de la función (vea [Administrador de complementos y funciones de la interfaz de XLL](add-in-manager-and-xll-interface-functions.md)), pero aquí se proporciona una implementación mínima. Su objetivo es liberar la memoria de **XLOPER**/ **XLOPER12** de forma coherente con la que se asignó originalmente. 
  
### <a name="examples"></a>Ejemplos

La siguiente función del ejemplo realiza lo mismo que la función anterior excepto en que incluye el texto "El nombre de la ruta de acceso completa de este DLL es" delante del nombre del DLL.
  
```cs
#include <string.h>
LPXLOPER12 WINAPI get_DLL_name_2(int calculation_trigger)
{
    static XLOPER12 xRtnValue; // Not thread-safe
    Excel12(xlfGetName, &xRtnValue, 0);
// If xlfGetName failed, xRtnValue will be #VALUE!
    if(xRtnValue.xltype != xltypeStr)
        return &xRtnValue;
// Make a copy of the DLL path and file name.
    wchar_t *leader = L"The full pathname for this DLL is ";
    size_t leader_len = wcslen(leader);
    size_t dllname_len = xRtnValue.val.str[0];
    size_t msg_len = leader_len + dllname_len;
    wchar_t *msg_text = (wchar_t *)malloc(msg_len + 1);
    wcsncpy_s(msg_text + 1, leader, leader_len);
    wcsncpy_s(msg_text + 1 + leader_len, xRtnValue.val.str + 1,
        dllname_len);
    msg_text[0] = msg_len;
// Now the original string has been copied Excel can free it.
    Excel12(xlFree, 0, 1, &xRtnValue);
// Now reuse the XLOPER12 for the new string.
    xRtnValue.val.str = msg_text;
// Tell Excel to call back into the DLL to free the string
// memory after it has copied out the return value.
    xRtnValue.xltype     = xltypeStr | xlbitDLLFree;
    return &xRtnValue;
}
```

Una implementación mínima suficiente de **xlAutoFree12** en el XLL que exporta la función anterior sería la siguiente. 
  
```cs
void WINAPI xlAutoFree12(LPXLOPER12 p_oper)
{
    if(p_oper->xltype == (xltypeStr | xlbitDLLFree))
        free(p_oper->val.str);
}
```

Esta implementación solo es suficiente si el XLL solo devuelve la cadena **XLOPER12** y estas cadenas solo se asignan con **malloc**. Tenga en cuenta que la prueba 
  
 ` if(p_oper->xltype == xltypeStr) `
  
producirá un error en este caso porque **xlbitDLLFree** está configurado. 
  
En general, **xlAutoFree** y **xlAutoFree12** se deben implementar para que liberen la memoria asociada con las matrices de **xltypeMulti** creadas con XLL y las referencias externas de **xltypeRef**. 
  
Puede decidir implementar sus funciones XLL para que todas devuelvan **XLOPER** y **XLOPER12** asignados dinámicamente. En este caso, debe configurar **xlbitDLLFree** en todos los **XLOPER** y **XLOPER12** independientemente del tipo secundario. También necesitará implementar **xlAutoFree** y **xlAutoFree12** para que se libere esta memoria y también cualquier memoria a la que se apunta dentro del **XLOPER**/ **XLOPER12**. Este método es una forma de hacer el valor de la conversación devuelto seguro. Por ejemplo, la función anterior podría modificarse como se indica.
  
```cs
#include <string.h>
LPXLOPER12 WINAPI get_DLL_name_3(int calculation_trigger)
{
// Thread-safe
    LPXLOPER12 pxRtnValue = (LPXLOPER12)malloc(sizeof(XLOPER12));
    Excel12(xlfGetName, pxRtnValue, 0);
// If xlfGetName failed, pxRtnValue will be #VALUE!
    if(pxRtnValue->xltype != xltypeStr)
    {
// Even though an error type does not point to memory,
// Excel needs to pass this oper to xlAutoFree12 to
// free pxRtnValue itself.
        pxRtnValue->xltype |= xlbitDLLFree;
        return pxRtnValue;
    }
// Make a copy of the DLL path and file name.
    wchar_t *leader = L"The full pathname for this DLL is ";
    size_t leader_len = wcslen(leader);
    size_t dllname_len = pxRtnValue->val.str[0];
    size_t msg_len = leader_len + dllname_len;
    wchar_t *msg_text = (wchar_t *)malloc(msg_len + 1);
    wcsncpy_s(msg_text + 1, leader, leader_len);
    wcsncpy_s(msg_text + 1 + leader_len, pxRtnValue->val.str + 1,
        dllname_len);
    msg_text[0] = msg_len;
// Now the original string has been copied Excel can free it.
    Excel12(xlFree, 0, 1, pxRtnValue);
// Now reuse the XLOPER12 for the new string.
    pxRtnValue->val.str = msg_text;
    pxRtnValue->xltype = xltypeStr | xlbitDLLFree;
    return pxRtnValue;
}
void WINAPI xlAutoFree12(LPXLOPER12 p_oper)
{
    if(p_oper->xltype == (xltypeStr | xlbitDLLFree))
        free(p_oper->val.str);
    free(p_oper);
}
```

Para obtener más información de **xlAutoFree** y **xlAutoFree12**, consulte [xlAutoFree/xlAutoFree12](xlautofree-xlautofree12.md).
  
## <a name="returning-modify-in-place-arguments"></a>Devolver argumentos Modificación local

Excel permite que una función XLL devuelva un valor modificando un argumento local. Solo se puede hacer con un argumento que se pasa como puntero. Para que funcione así, se debe registrar la función de modo que indique a Excel el argumento que se modificará. 
  
Este método de devolución de un valor se admite con todos los tipos de datos que el puntero puede pasar, pero es especialmente útil para los siguientes tipos:
  
- Cadenas de bytes ASCII de longitud contada y terminada en valor nulo
    
- Cadenas de caracteres anchos Unicode de longitud contada y terminada en valor nulo (a partir de Excel 2007)
    
- Matrices **FP** de número de punto flotante 
    
- Matrices **FP12**de número de punto flotante (a partir de Excel 2007) 
    
> [!NOTE]
> No debe intentar devolver **XLOPER** o **XLOPER12** de este modo. Para obtener más información, consulte [Problemas conocidos en el desarrollo de XLL de Excel](known-issues-in-excel-xll-development.md). 
  
La ventaja de usar esta técnica, en lugar de solo usar la instrucción return, es que Excel asigna la memoria para los valores devueltos. Una vez que termina la lectura de los datos devueltos, libera la memoria. Esto aleja las tareas de administración de memoria de la función XLL. Esta técnica es segura para subprocesos: si Excel lo llama simultáneamente en subprocesos distintos, cada llamada a la función de cada subproceso tiene su propio búfer.
  
Es útil para los datos enumerados anteriormente, en particular porque el mecanismo de devolución de llamada al DLL para liberar memoria posterior a la devolución que existe para **XLOPER**/ **XLOPER12** no existe para las cadenas simples y las matrices de **FP**/ **FP12**. Por lo tanto, al devolver una cadena creada por DLL o una matriz de número de punto flotante, tiene las siguientes opciones: 
  
- Configurar un puntero persistente para un búfer asignado dinámicamente, devolver el puntero. En la siguiente llamada a la función (1) compruebe que el puntero no sea nulo, (2) libre los recursos asignados en la llamada anterior y restablezca el puntero a nulo, (3) reutilice el puntero para un bloque de memoria asignado recientemente.
    
- Crear las cadenas y las matrices en un búfer estático que no se tenga que liberar y devolver un puntero.
    
- Modificar un argumento local, escribiendo la cadena o la matriz directamente en el espacio reservado por Excel.
    
De lo contrario, debe crear un **XLOPER**/ **XLOPER12**, y usar **xlbitDLLFree** y **xlAutoFree**/ **xlAutoFree12** para liberar los recursos. 
  
La última opción puede ser la más sencilla en los casos en los que se pasa un argumento del mismo tipo como el valor devuelto. El punto clave que debe recordar es que se limitan los tamaños de búfer y debe tener mucho cuidado de no saturarlos. Hacerlo de forma incorrecta puede llevar a que se bloquee Excel. Los tamaños de búfer de las cadenas y las matrices **FP**/ **FP12** se describen a continuación. 
  
## <a name="strings"></a>Strings

Los problemas con la administración de la memoria de la cadena son probablemente la causa más común de inestabilidad en las aplicaciones y los complementos. Quizá es comprensible dadas las diversas formas en las que se gestionan las cadenas: terminada en null o longitud contada (o ambos); búferes estáticos o dinámicos; longitud fija o casi ilimitada; memoria administrada por el sistema operativo (por ejemplo, OLE Bstr) o cadenas no administradas, etc.
  
Los programadores de C/C ++ están más familiarizados con las cadenas terminada en null. La biblioteca estándar de C está diseñada para trabajar con estas cadenas. Los literales de cadena estática del código se compilan en cadenas terminadas en null. Como alternativa, Excel funciona con cadenas de longitud contada que normalmente no están terminadas en null. La combinación de estos hechos necesita un enfoque claro y coherente dentro de la DLL o  XLL sobre cómo gestionar las cadenas y la memoria de la cadena.
  
Los problemas más comunes son los siguientes:
  
- Pasar un puntero nulo o no válido a una función que espera un puntero válido y no tiene o no puede comprobar la validez del puntero.
    
- Saturar los límites de un búfer de cadena por una función que no tiene o no puede comprobar la longitud del búfer con la longitud de la cadena que se escribe.
    
- Intentar liberar la memoria de búfer de cadena que es estática, que ya se ha liberado o no se ha asignado de forma coherente con la forma en que se libera.
    
- Pérdidas de memoria que son el resultado de las cadenas que se asignan y que no se liberan, normalmente en una función a la que se llama con frecuencia.
    
### <a name="rules-for-strings"></a>Reglas para las cadenas

Al igual que con los **XLOPER**/ **XLOPER**, hay reglas e instrucciones que debe seguir. Las instrucciones son las mismas que las indicadas en la sección anterior. Las reglas que se presentan aquí son una extensión de las reglas específicas para las cadenas.
  
 **Reglas:**
  
- No intente liberar memoria o sobrescribir **XLOPER**/ **XLOPER12** de cadena, o cadenas de longitud contada simples o terminadas en null que se pasan como argumentos para la función XLL. Debe tratar dichos argumentos como de solo lectura.
    
- Cuando Excel asigna memoria para**XLOPER**/ **XLOPER12** de cadena para el valor devuelto de una función de devolución de llamada de la API de C, use **xlFree** para liberarla, o configure **xlbitXLFree** si la devuelve a Excel desde una función XLL. 
    
- Cuando el DLL asigna dinámicamente un búfer de cadena para **XLOPER**/ **XLOPER12**, libérelo de forma coherente con la forma en la que lo asignó, o configure **xlbitDLLFree** si lo devuelve a Excel desde una función XLL y libérelo en **xlAutoFree**/ **xlAutoFree12**.
    
- Si Excel ha asignado la memoria para una matriz **xltypeMulti** devuelta al DLL en una llamada a la API de C, no sobrescriba cualquier cadena **XLOPER**/ **XLOPER12** dentro de la matriz. Estas matrices solo deben liberarse mediante **xlFree**, o bien, si las devuelve una función XLL, estableciendo **xlbitXLFree**.
    
### <a name="string-types-supported"></a>Tipos de cadena admitidos

**XLOPER o XLOPER12 de xltypeStr de la API de C**

|**Cadenas de bytes: **XLOPER****|**Cadenas de caracteres anchos: **XLOPER12****|
|:-----|:-----|
|Todas las versiones de Excel  <br/> |A partir de Excel 2007  <br/> |
|Longitud máxima: 255 caracteres ASCII ampliados  <br/> |Longitud máxima 32.767 caracteres Unicode  <br/> |
|Primer byte (no asignado) = longitud  <br/> |Primer carácter Unicode = longitud  <br/> |
   
> [!IMPORTANT]
> No asuma la terminación null de las cadenas **XLOPER** o **XLOPER12**. 
  
**Cadenas C/C++**

|**Cadenas de bytes**|**Cadenas de caracteres anchos**|
|:-----|:-----|
|Longitud máxima de "C" terminada en null (**char** *): 255 bytes ASCII ampliados  <br/> |Longitud máxima "C%" terminada en null (**wchar_t** *) 32 767 caracteres Unicode  <br/> |
|"D" de longitud contada (**unsigned char** *)  <br/> |"% D" de longitud contada (**wchar_t** *)  <br/> |
   
### <a name="strings-in-xltypemulti-xloperxloper12-arrays"></a>Cadenas de las matrices XLOPER o XLOPER12 de xltypeMulti

En muchos casos, Excel crea una matriz **xltypeMulti** para su uso en los XLL o DLL. Varias de las funciones de información XLM devuelven estas matrices. Por ejemplo, la función de la API de C **xlfGetWorkspace**, cuando pasa el argumento  *44*  , devuelve una matriz que contiene las cadenas que describen todos los procedimientos DLL registrados actualmente. La función de la API de C **xlfDialogBox** devuelve una copia modificada del argumento de la matriz, que contiene copias en profundidad de las cadenas. Posiblemente, el modo más común en que un XLL encuentra una matriz de **xltypeMulti** es donde se ha pasado como argumento a una función XLL, o se ha forzado para este tipo desde una referencia de rango. En estos últimos casos, Excel crea copias en profundidad de las cadenas en las celdas de origen y apunta a estos dentro de la matriz. 
  
Debe hacer sus propias copias en profundidad donde desee modificar estas cadenas en el DLL. Al crear su propias matrices **xltypeMulti**, no debe colocar las cadenas asignadas a Excel **XLOPER**/ **XLOPER12** en ellas. Hacer esto implica el riesgo de no liberarlas correctamente más adelante, o no liberarlas en absoluto. De nuevo, debe hacer copias en profundidad de las cadenas y los punteros de almacenamiento para las copias de la matriz.
  
 **Ejemplos**
  
La siguiente función del ejemplo crea una copia asignada dinámicamente de una cadena Unicode de longitud contada. Tenga en cuenta que, en última instancia, el llamador debe liberar la memoria asignada en este ejemplo con **delete**[], y que no se supone que la cadena de origen termine en null. La cadena de copia se trunca si es necesario por motivos de seguridad y no termina en null.
  
```cs
#include <string.h>
#define MAX_V12_STRBUFFLEN    32678
    
wchar_t * deep_copy_wcs(const wchar_t *p_source)
{
    if(!p_source)
        return NULL;
    size_t source_len = p_source[0];
    bool truncated = false;
    if(source_len >= MAX_V12_STRBUFFLEN)
    {
        source_len = MAX_V12_STRBUFFLEN - 1; // Truncate the copy
        truncated = true;
    }
    wchar_t *p_copy = new wchar_t[source_len + 1];
    wcsncpy_s(p_copy, p_source, source_len + 1);
    if(truncated)
        p_copy[0] = source_len;
    return p_copy;
}
```

Luego, esta función se puede usar con seguridad para copiar **XLOPER12**, como se muestra en la siguiente función XLL que se puede exportar y que devuelve una copia de su argumento, si es una cadena. El resto de tipos se devuelve como una cadena de longitud cero. Tenga en cuenta que no se gestionan los rangos; la función devuelve **#VALUE!**. se debe registrar la función como que toma un argumento de tipo U, de modo que las referencias se pasen como valores. Esto es igual a la función de hoja de cálculo integrada **T()**, excepto en que **AsText** también convierte los errores en cadenas de longitud cero. Este ejemplo de código asume que **xlAutoFree12** libera el puntero pasado, y también su contenido, con **delete**.
  
```cs
LPXLOPER12 WINAPI AsText(LPXLOPER12 pArg)
{
    LPXLOPER12 pRtnVal = new XLOPER12;
// If the input was an array, only operate on the top-left element.
    LPXLOPER *pTemp;
    if(pArg->xltype == xltypeMulti)
        pTemp = pArg->val.array.lparray;
    else
        pTemp = pArg;
    switch(pTemp->xltype)
    {
        case xltypeErr:
        case xltypeNum:
        case xltypeMissing:
        case xltypeNil:
        case xltypeBool:
            pRtnVal->xltype = xltypeStr | xlbitDLLFree;
            pRtnVal->val.str = deep_copy_wcs(L"\000");
            return pRtnVal;
        case xltypeStr:
            pRtnVal->xltype = xltypeStr | xlbitDLLFree;
            pRtnVal->val.str = deep_copy_wcs(pTemp->val.str);
            return pRtnVal;
        
        default: // xltypeSRef, xltypeRef, xltypeFlow, xltypeInt
            pRtnVal->xltype = xltypeErr | xlbitDLLFree;
            pRtnVal->val.err = xlerrValue;
            return pRtnVal;
    }
}
```

### <a name="returning-modify-in-place-string-arguments"></a>Devolver argumentos de cadena Modificación local

Los argumentos registrados como tipos **F**, **G**, **F%** y **G%** se pueden modificar de forma local. Cuando Excel prepara argumentos de cadena para estos tipos, se crea un búfer de longitud máxima. Luego, copia la cadena del argumento en él, incluso si esta cadena es mucho más corta. Esto permite que la función XLL escriba el valor devuelto directamente en la misma memoria. 
  
Los tamaños de búfer configurados aparte para estos tipos son los siguientes:
  
- **Cadenas de bytes:** 256 bytes, incluido el contador de longitud (tipo G) o la terminación null (tipo F). 
    
- **Cadenas Unicode:** 32.768 caracteres anchos (65.536 bytes), incluido el contador de longitud (tipo G%) o la terminación null (tipo F%). 
    
> [!NOTE]
> No puede llamar a esta función directamente desde Visual Basic para aplicaciones (VBA) porque no puede garantizar que se haya asignado un búfer suficientemente grande. Solo puede llamar de forma segura a esta función desde otra DLL si pasa explícitamente un búfer lo suficientemente grande. 
  
Este es un ejemplo de una función XLL que invierte una cadena de caracteres anchos terminada en null con la función de biblioteca estándar **wcsrev**. El argumento en este caso se registrará como tipo **F%**.
  
```cs
void WINAPI reverse_text_xl12(wchar_t *text)
{
    _wcsrev(text);
}
```

## <a name="persistent-storage-binary-names"></a>Almacenamiento persistente (nombres binarios)

Los nombres binarios se definen y asocian con bloques de archivos binarios, es decir, datos no estructurados almacenados con el libro. Se crean con la función [xlDefineBinaryName](xldefinebinaryname.md) y los datos se recuperan con la función [xlGetBinaryName](xlgetbinaryname.md). Ambas funciones se describen con más detalle en la referencia de función (vea [Funciones de la API de C que pueden llamarse solo desde una DLL o XLL](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)), y que usan el **XLOPER**/ **XLOPER12** **xltypeBigData**. 
  
Para obtener información sobre los problemas conocidos que limitan las aplicaciones prácticas de los nombres binarios, consulte [Problemas conocidos en el desarrollo de XLL de Excel](known-issues-in-excel-xll-development.md).
  
## <a name="excel-stack"></a>Pila de Excel

Excel comparte su espacio de pila con todos los DLL que tiene cargados. Normalmente, el espacio de pila es más adecuado para su uso normal y no es necesario preocuparse por él, siempre y cuando siga unas directrices: 
  
- No pase estructuras muy grandes como argumentos a funciones por valor de la pila. En su lugar, pase punteros o referencias.
    
- No devuelva estructuras grandes en la pila. Devuelva punteros para la memoria estática o asignada dinámicamente, o use argumentos que pase la referencia.
    
- No declare estructuras de variables automáticas muy grandes al código de función. Si las necesita, declárelas como estáticos.
    
- No llame a las funciones recursivamente a menos que esté seguro de que la profundidad de la recursividad sea siempre superficial. En su lugar, intente usar un bucle.
    
Cuando un archivo DLL devuelve la llamada a Excel con la API de C, Excel comprueba primero si hay suficiente espacio en la pila para la peor llamada de uso que se pueda realizar. Si piensa que no puede haber espacio suficiente, la llamada no será segura, aunque sea posible que realmente haya suficiente espacio para esa llamada concreta. En este caso, las devoluciones de llamada devuelven el código**xlretFailed**. Para el uso normal de la API de C y la pila, esta no es una causa probable del error de una llamada a la API de C.
  
Si le preocupa o le interesa, quiere eliminar la falta de espacio de pila como un motivo de un error inesperado, puede averiguar cuánto espacio de pila hay con una llamada a la función [xlStack](xlstack.md). 
  
## <a name="see-also"></a>Vea también



[Actualización multiproceso en Excel](multithreaded-recalculation-in-excel.md)
  
[Multiproceso y conflictos de memoria en Excel](multithreading-and-memory-contention-in-excel.md)
  
[Desarrollo de XLL de Excel de 2013](developing-excel-xlls.md)

