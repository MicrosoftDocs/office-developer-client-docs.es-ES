---
title: Administraci�n de memoria en Excel
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
keywords:
- xloper12 memory [excel 2007],managing memory in Excel,Excel stack,strings [Excel 2007], managing memory,memory management in Excel,XLOPER memory [Excel 2007],memory [Excel 2007], management guidelines
localization_priority: Normal
ms.assetid: 3bf5195b-6235-43cf-8795-0c7b0a63a095
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: f129dac2971f01c8ada15f0028958132b1945746
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419544"
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
    
Given the number of possible origins for **XLOPER**/ **XLOPER12** memory and the number of situations in which the **XLOPER**/ **XLOPER12** might have had that memory assigned, it is not surprising that this subject can seem very difficult. However, the complexity can be greatly reduced if you follow several rules and guidelines. 
  
### <a name="rules-for-working-with-xloperxloper12"></a>Reglas para trabajar con XLOPER y XLOPER12

- Do not try to free memory or overwrite **XLOPERs**/ **XLOPER12**s that are passed as arguments to your XLL function. You should treat such arguments as read-only. For more information, see "Returning **XLOPER** or **XLOPER12** by Modifying Arguments in Place" in [Known Issues in Excel XLL Development](known-issues-in-excel-xll-development.md).
    
- Si Excel asigna memoria para un **XLOPER**/ **XLOPER12** devuelto al DLL en una llamada a la API de C: 
    
  - You must free the memory when you no longer need the **XLOPER**/ **XLOPER12** using a call to [xlFree](xlfree.md). Do not use any other method, such as free or delete, to release the memory.
    
  - Si el tipo devuelto es **xltypeMulti**, no sobrescriba ningún **XLOPER**/ **XLOPER12** dentro de la matriz, especialmente si contienen cadenas, y especialmente no donde intenta sobrescribir con una cadena.
    
  - Si quiere devolver **XLOPER**/ **XLOPER12** a Excel como valor devuelto de la función de DLL, debe indicarle a Excel que hay memoria que debe liberar al terminar. 
    
- Solo debe llamar **xlFree** en **XLOPER**/ **XLOPER12** creado como el valor devuelto para una llamada a la API de C. 
    
- Si el DLL asigna memoria para **XLOPER**/ **XLOPER12** que quiere devolver a Excel como valor devuelto de la función de DLL, debe indicarle a Excel que hay memoria que DLL debe liberar. 
    
### <a name="guidelines-for-memory-management"></a>Directrices para la administración de memoria

- Sea coherente en el DLL del método que usa para asignar y liberar memoria. Evite mezclar métodos. Un buen enfoque es ajustar el método que use en una clase o estructura de memoria, en el que puede cambiar el método usado sin alterar el código en muchos lugares.
    
- Al crear matrices de **xltypeMulti** dentro del DLL, sea coherente en la forma en que asigna memoria para las cadenas: asigne siempre dinámicamente la memoria para ellos o use siempre la memoria estática. Para ello, al liberar memoria, sabrá que debe liberar siempre o nunca las cadenas. 
    
- Haga copias en profundidad de memoria asignada a Excel al copiar un **XLOPER**/ **XLOPER12** creado en Excel.
    
- Do not put Excel-allocated string **XLOPER**/ **XLOPER12**s within **xltypeMulti** arrays. Make deep copies of the strings and store pointers to the copies in the array. 
    
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
    
- **xlFree** sets the contained pointer to **NULL** to ensure that an attempt to free an **XLOPER**/ **XLOPER12** that has already been freed is safe. **xlFree** is the only C API function that modifies its arguments. 
    
- Puede llamar de forma segura a **xlFree** en cualquier **XLOPER**/ **XLOPER12** usado para el valor devuelto de una llamada a la API de C, independientemente de si contiene un puntero a la memoria. 
    
## <a name="returning-xloperxloper12s-to-be-freed-by-excel"></a>Devolver XLOPER o XLOPER12 para que Excel los libere

Suppose you wanted to modify the example command in the previous section and change it to a worksheet function that returns the DLL path and file name when passed a **Boolean** **true** argument, and **#N/A** otherwise. Clearly you cannot call **xlFree** to release the string memory before returning it to Excel. However, if it is not freed at some point, the add-in will leak memory every time the function is called. To work around this problem, you can set a bit in the **xltype** field of the **XLOPER**/ **XLOPER12**, defined as **xlbitXLFree** in xlcall.h. Setting this tells Excel that it must free the returned memory when it has finished copying the value out. 
  
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

XLL functions that use **XLOPER**/ **XLOPER12**s must be declared as taking and returning pointers to **XLOPER**/ **XLOPER12**s. The use in this example of a static **XLOPER12** within the function is not thread safe. You could incorrectly register this function as thread safe, but you would risk **xRtnValue** being overwritten by one thread before another thread had finished with it. 
  
You must set **xlbitXLFree** after the call to the Excel callback that allocates it. If you set it before this, it is overwritten and does not have the effect that you want. If you intend to use the value as an argument in a call to another C API function before returning it to the worksheet, you should set this bit after any such call. Otherwise, you will confuse functions that do not mask this bit before checking the **XLOPER**/ **XLLOPER12** type. 
  
## <a name="returning-xloperxloper12s-to-be-freed-by-the-dll"></a>Devolver XLOPER o XLOPER12 para que el DLL los libere

A similar problem to this occurs when your XLL has allocated memory for an **XLOPER**/ **XLOPER12** and wants to return it to Excel. Excel recognizes another bit that can be set in the **xltype** field of the **XLOPER**/ **XLOPER12**, defined as **xlbitDLLFree** in xlcall.h. 
  
When Excel receives **an XLOPER**/ **XLOPER12** with this bit set, it tries to call a function that should be exported by the XLL called [xlAutoFree](xlautofree-xlautofree12.md) (for **XLOPER**s) or **xlAutoFree12** (for **XLOPER12**s). This function is described more fully in the function reference (see [Add-in Manager and XLL Interface Functions](add-in-manager-and-xll-interface-functions.md)), but an example minimal implementation is given here. Its purpose is to free the **XLOPER**/ **XLOPER12** memory in a way that is consistent with how it was originally allocated. 
  
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
  
You might decide to implement your XLL functions so that they ALL return dynamically allocated **XLOPER**s and **XLOPER12**s. In this case, you would need to set **xlbitDLLFree** on all such **XLOPER**s and **XLOPER12**s regardless of the sub-type. You would also need to implement **xlAutoFree** and **xlAutoFree12** so that this memory was freed and also any memory pointed to within the **XLOPER**/ **XLOPER12**. This approach is one way to make the return value thread safe. For example, the previous function could be rewritten as follows.
  
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
  
It is useful for the previously listed data types in particular because the mechanism for calling back into the DLL to free memory post-return that exists for **XLOPER**/ **XLOPER12**s does not exist for simple strings and **FP**/ **FP12** arrays. Therefore, when returning a DLL-created string or floating-point array, you have the following choices: 
  
- Configurar un puntero persistente para un búfer asignado dinámicamente, devolver el puntero. En la siguiente llamada a la función (1) compruebe que el puntero no sea nulo, (2) libre los recursos asignados en la llamada anterior y restablezca el puntero a nulo, (3) reutilice el puntero para un bloque de memoria asignado recientemente.
    
- Crear las cadenas y las matrices en un búfer estático que no se tenga que liberar y devolver un puntero.
    
- Modificar un argumento local, escribiendo la cadena o la matriz directamente en el espacio reservado por Excel.
    
De lo contrario, debe crear un **XLOPER**/ **XLOPER12**, y usar **xlbitDLLFree** y **xlAutoFree**/ **xlAutoFree12** para liberar los recursos. 
  
The last option might be the simplest in those cases in which you are being passed an argument of the same type as the return value. The key point to remember is that the buffer sizes are limited and you must be very careful not to overrun them. Getting this wrong could crash Excel. Buffer sizes for strings and **FP**/ **FP12** arrays are discussed next. 
  
## <a name="strings"></a>Strings

Los problemas con la administración de la memoria de la cadena son probablemente la causa más común de inestabilidad en las aplicaciones y los complementos. Quizá es comprensible dadas las diversas formas en las que se gestionan las cadenas: terminada en null o longitud contada (o ambos); búferes estáticos o dinámicos; longitud fija o casi ilimitada; memoria administrada por el sistema operativo (por ejemplo, OLE Bstr) o cadenas no administradas, etc.
  
Los programadores de C/C ++ están más familiarizados con las cadenas terminada en null. La biblioteca estándar de C está diseñada para trabajar con estas cadenas. Los literales de cadena estática del código se compilan en cadenas terminadas en null. Como alternativa, Excel funciona con cadenas de longitud contada que normalmente no están terminadas en null. La combinación de estos hechos necesita un enfoque claro y coherente dentro de la DLL o  XLL sobre cómo gestionar las cadenas y la memoria de la cadena.
  
Los problemas más comunes son los siguientes:
  
- Pasar un puntero nulo o no válido a una función que espera un puntero válido y no tiene o no puede comprobar la validez del puntero.
    
- Saturar los límites de un búfer de cadena por una función que no tiene o no puede comprobar la longitud del búfer con la longitud de la cadena que se escribe.
    
- Intentar liberar la memoria de búfer de cadena que es estática, que ya se ha liberado o no se ha asignado de forma coherente con la forma en que se libera.
    
- Pérdidas de memoria que son el resultado de las cadenas que se asignan y que no se liberan, normalmente en una función a la que se llama con frecuencia.
    
### <a name="rules-for-strings"></a>Reglas para las cadenas

As with **XLOPER**/ **XLOPER**s, there are rules and guidelines you should follow. The guidelines are the same as given in the previous section. The rules here are an extension of the rules specifically for strings.
  
 **Reglas:**
  
- Do not try to free memory or overwrite string **XLOPER**/ **XLOPER12**s or simple length-counted or null-terminated strings passed as arguments to your XLL function. You should treat such arguments as read-only.
    
- Cuando Excel asigna memoria para**XLOPER**/ **XLOPER12** de cadena para el valor devuelto de una función de devolución de llamada de la API de C, use **xlFree** para liberarla, o configure **xlbitXLFree** si la devuelve a Excel desde una función XLL. 
    
- Cuando el DLL asigna dinámicamente un búfer de cadena para **XLOPER**/ **XLOPER12**, libérelo de forma coherente con la forma en la que lo asignó, o configure **xlbitDLLFree** si lo devuelve a Excel desde una función XLL y libérelo en **xlAutoFree**/ **xlAutoFree12**.
    
- If Excel has allocated memory for an **xltypeMulti** array returned to your DLL in a call to the C API, do not overwrite any string **XLOPER**/ **XLOPER12**s within the array. Such arrays must only be freed using **xlFree**, or, if being returned by an XLL function, by setting **xlbitXLFree**.
    
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
  
Where you want to modify these strings in your DLL, you should make your own deep copies. When you are creating your own **xltypeMulti** arrays, you should not place Excel-allocated string **XLOPER**/ **XLOPER12**s within them. This risks you not freeing them correctly later, or not freeing them at all. Again, you should make deep copies of the strings and store pointers to the copies in the array.
  
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

Binary names are defined and associated with blocks of binary, that is, unstructured, data that is stored together with the workbook. They are created using the function [xlDefineBinaryName](xldefinebinaryname.md), and the data is retrieved using the function [xlGetBinaryName](xlgetbinaryname.md). Both functions are described in more detail in the function reference (see [C API Functions That Can Be Called Only from a DLL or XLL](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)), and both use the **xltypeBigData** **XLOPER**/ **XLOPER12**. 
  
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
  
[Desarrollar archivos XLL de Excel](developing-excel-xlls.md)

