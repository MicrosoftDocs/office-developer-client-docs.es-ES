---
title: xlAutoFree/xlAutoFree12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlAutoFree
keywords:
- función xlautofree [excel 2007]
localization_priority: Normal
ms.assetid: f73d292c-d6d8-4be5-89c0-bef15db236d6
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 3dfba5ae98b0635c95308eac01bf2f10867678e1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413293"
---
# <a name="xlautofreexlautofree12"></a>xlAutoFree/xlAutoFree12

 **Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio 
  
Llamado por Microsoft Excel justo después de que una función de hoja de cálculo XLL devuelva un /  **XLOPER XLOPER12** con un conjunto de marcas que le indica que hay memoria que el XLL aún necesita liberar. Esto permite al XLL devolver matrices, cadenas y referencias externas asignadas dinámicamente a la hoja de cálculo sin pérdidas de memoria. Para obtener más información, consulte [Administración de memoria en Excel](memory-management-in-excel.md).
  
A partir de Excel 2007, se admiten la función **xlAutoFree12** y el tipo de datos **XLOPER12.** 
  
Excel no requiere un XLL para implementar y exportar ninguna de estas funciones. Sin embargo, debe hacerlo si las funciones XLL devuelven un XLOPER o XLOPER12 que se ha asignado dinámicamente o que contiene punteros a la memoria asignada dinámicamente. Asegúrese de que la elección de cómo administrar la memoria para estos tipos es coherente en todo el XLL y en la forma en que implementó **xlAutoFree** y **xlAutoFree12**.
  
Dentro de la función **xlAutoFree** /  **xlAutoFree12,** las devoluciones de llamada a Excel están deshabilitadas, con una excepción: se puede llamar a **xlFree** para liberar memoria asignada a Excel. 
  
```cs
void WINAPI xlAutoFree(LPXLOPER pxFree);
void WINAPI xlAutoFree12(LPXLOPER12 pxFree);
```

## <a name="parameters"></a>Parámetros

 _pxFree_ (**LPXLOPER en el caso de xlAutoFree**)
  
 _pxFree_ (**LPXLOPER12 en el caso de xlAutoFree12**)
  
Puntero a **XLOPER** o **XLOPER12** que tiene memoria que debe liberarse. 
  
## <a name="property-valuereturn-value"></a>Valor de la propiedad/valor devuelto

Esta función no devuelve un valor y debe declararse como nula de devolución.
  
## <a name="remarks"></a>Comentarios

Cuando Excel está configurado para usar la actualización de libros multiproceso, se llama a **xlAutoFree** /  **xlAutoFree12** en el mismo subproceso usado para llamar a la función que la devolvió. La llamada a **xlAutoFree**/ **xlAutoFree12** siempre se realiza antes de que las celdas de la hoja de cálculo siguientes se evalúen en dicho subproceso. Esto simplifica el diseño de subprocesos seguros en tu XLL. 
  
Si la **función xlAutoFree** /  **xlAutoFree12** que proporcionas examina el campo **xltype** de _pxFree,_ recuerda que el bit **xlbitDLLFree** seguirá estando establecido. 
  
## <a name="example"></a>Ejemplo

 **Ejemplo de implementación 1**
  
El primer código de muestra una implementación muy específica de xlAutoFree , que está diseñada para funcionar con una sola `\SAMPLES\EXAMPLE\EXAMPLE.C` función, **fArray**.  En general, el XLL tendrá más de una función que devuelve memoria que debe liberarse, en cuyo caso se requiere una implementación menos restringida. 
  
 **Ejemplo de implementación 2**
  
La segunda implementación de ejemplo es coherente con las suposiciones usadas en los ejemplos de creación de **XLOPER12** de la sección 1.6.3, xl12_Str_example, xl12_Ref_example y xl12_Multi_example. Se supone que, cuando se ha establecido el bit **xlbitDLLFree,** toda la cadena, matriz y memoria de referencia externa se ha asignado dinámicamente mediante **malloc,** por lo que debe liberarse en una llamada para liberar.
  
 **Ejemplo de implementación 3**
  
La tercera implementación de ejemplo es coherente con un XLL donde las funciones exportadas que devuelven **XLOPER12** asignan cadenas, referencias externas y matrices mediante **malloc,** y donde el propio **XLOPER12** también se asigna dinámicamente. Devolver un puntero a un **XLOPER12** asignado dinámicamente es una forma de garantizar que la función es segura para subprocesos. 
  
```cs
//////////////////////////////////////////
//       BEGIN EXAMPLE IMPLEMENTATION 1
//////////////////////////////////////////
LPXLOPER12 WINAPI fArray(void)
{
    LPXLOPER12 pxArray;
    static XLOPER12 xMulti;
    int i;
    int rwcol;
    xMulti.xltype = xltypeMulti | xlbitDLLFree;
    xMulti.val.array.columns = 1;
    xMulti.val.array.rows = 8;
    // For large values of rows and columns, this would overflow
    // use __int64 in that case and return an error if rwcol
    // contains a number that won't fit in sizeof(int) bytes
    rwcol = xMulti.val.array.columns * xMulti.val.array.rows; 
    pxArray = (LPXLOPER12)GlobalLock(hArray = GlobalAlloc(GMEM_ZEROINIT, rwcol * sizeof(XLOPER12)));
    xMulti.val.array.lparray = pxArray;
    for(i = 0; i < rwcol; i++) 
    {
        pxArray[i].xltype = xltypeInt;
        pxArray[i].val.w = i;
    }
// Word of caution - returning static XLOPERs/XLOPER12s is not thread safe
// for UDFs declared as thread safe, use alternate memory allocation mechanisms
    return (LPXLOPER12)&xMulti;
}
void WINAPI xlAutoFree12(LPXLOPER12 pxFree)
{
    GlobalUnlock(hArray);
    GlobalFree(hArray);
    return;
}
//////////////////////////////////////////
//       BEGIN EXAMPLE IMPLEMENTATION 2
//////////////////////////////////////////
void WINAPI xlAutoFree12(LPXLOPER12 pxFree)
{
    if(pxFree->xltype & xltypeMulti)
    {
/* Assume all string elements were allocated using malloc, and
** need to be freed using free.  Then free the array itself.
*/
        int size = pxFree->val.array.rows *
            pxFree->val.array.columns;
        LPXLOPER12 p = pxFree->val.array.lparray;
        for(; size-- > 0; p++) // check elements for strings
            if(p->xltype == xltypeStr)
                free(p->val.str);
        free(pxFree->val.array.lparray);
    }
    else if(pxFree->xltype & xltypeStr)
    {
        free(pxFree->val.str);
    }
    else if(pxFree->xltype & xltypeRef)
    {
        free(pxFree->val.mref.lpmref);
    }
}
//////////////////////////////////////////
//       BEGIN EXAMPLE IMPLEMENTATION 3
//////////////////////////////////////////
LPXLOPER12 WINAPI example_xll_function(LPXLOPER12 pxArg)
{
// Thread-safe return value. Every invocation of this function
// gets its own piece of memory.
    LPXLOPER12 pxRtnValue = (LPXLOPER12)malloc(sizeof(XLOPER12));
// Initialize to a safe default
    pxRtnValue->xltype = xltypeNil;
// Set the value of pxRtnValue making sure that strings, external
// references, arrays, and strings within arrays are all dynamically
// allocated using malloc.
//    (code omitted)
//    ...
// Set xlbitDLLFree regardless of the type of the return value to
// ensure xlAutoFree12 is called and pxRtnValue is freed.
    pxRtnValue->xltype |= xlbitDLLFree;
    return pxRtnValue;
}
void WINAPI xlAutoFree12(LPXLOPER pxFree)
{
    if(pxFree->xltype & xltypeMulti)
    {
// Assume all string elements were allocated using malloc, and
// need to be freed using free. Then free the array itself.
        int size = pxFree->val.array.rows *
            pxFree->val.array.columns;
        LPXLOPER12 p = pxFree->val.array.lparray;
        for(; size-- > 0; p++) // check elements for strings
            if(p->xltype == xltypeStr)
                free(p->val.str);
        free(pxFree->val.array.lparray);
    }
    else if(pxFree->xltype & xltypeStr)
    {
        free(pxFree->val.str);
    }
    else if(pxFree->xltype & xltypeRef)
    {
        free(pxFree->val.mref.lpmref);
    }
// Assume pxFree was itself dynamically allocated using malloc.
    free(pxFree);
}
```

## <a name="see-also"></a>Consulte también



[Administrador de complementos y funciones de la interfaz de XLL](add-in-manager-and-xll-interface-functions.md)

