---
title: xlAutoFree/xlAutoFree12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlAutoFree
keywords:
- función xlAutoFree [excel 2007]
localization_priority: Normal
ms.assetid: f73d292c-d6d8-4be5-89c0-bef15db236d6
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: a2d2b8e60b484ba8156acc80d543493e3ec9c564
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815721"
---
# <a name="xlautofreexlautofree12"></a>xlAutoFree/xlAutoFree12

 **Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio 
  
Microsoft Excel llama justo después de que una función de hoja de cálculo XLL devuelve un **XLOPER**/ **XLOPER12** a ella con un conjunto de marca que indica que hay que sigue necesitando el XLL para liberar memoria. Esto permite que el XLL devolver dinámicamente asignado matrices, cadenas y las referencias externas a la hoja de cálculo sin pérdidas de memoria. Para obtener m�s informaci�n, consulte [Administraci�n de memoria en Excel](memory-management-in-excel.md).
  
Iniciar en Excel 2007, la función **xlAutoFree12** y el tipo de datos **XLOPER12** son compatibles. 
  
Excel no requiere un XLL implementar y exportar a cualquiera de estas funciones. Sin embargo, debe hacerlo si sus funciones XLL devuelven un XLOPER o XLOPER12 que se han asignado dinámicamente o que contiene punteros a memoria asignada dinámicamente. Asegúrese de que su elección de cómo administrar la memoria de estos tipos es coherente en toda su XLL y con cómo implementa **xlAutoFree** y **xlAutoFree12**.
  
Dentro de la **xlAutoFree**/ **xlAutoFree12** función, las devoluciones de llamada en Excel están deshabilitadas, con una excepción: puede llamarse a **xlFree** para liberar memoria asignada en Excel. 
  
```cs
void WINAPI xlAutoFree(LPXLOPER pxFree);
void WINAPI xlAutoFree12(LPXLOPER12 pxFree);
```

## <a name="parameters"></a>Parámetros

 _pxFree_ (**LPXLOPER en el caso de xlAutoFree**)
  
 _pxFree_ (**LPXLOPER12 en el caso de xlAutoFree12**)
  
Un puntero a la **XLOPER** o **XLOPER12** que tiene memoria que necesita ser liberados. 
  
## <a name="property-valuereturn-value"></a>Valor de la propiedad/valor devuelto

Esta función no devuelve un valor y se debe declarar como devolver void.
  
## <a name="remarks"></a>Comentarios

Cuando Excel está configurado para usar el nuevo cálculo multiproceso libro, **xlAutoFree**/ **xlAutoFree12** se llama en el mismo subproceso utilizado para llamar a la función que se devuelve. La llamada a **xlAutoFree**/ **xlAutoFree12** siempre se realiza antes de que todas las celdas de la hoja de cálculo subsiguientes se evalúan en ese subproceso. Esto simplifica el diseño de subprocesos en su XLL. 
  
Si el **xlAutoFree**/ función**xlAutoFree12** proporciona examina el campo **xltype** de _pxFree_, recuerde que aún se establecerá el bit **xlbitDLLFree** . 
  
## <a name="example"></a>Ejemplo

 **Implementación de ejemplo 1**
  
El primer código de `\SAMPLES\EXAMPLE\EXAMPLE.C` , se muestra una implementación muy específica de **xlAutoFree**, que está diseñado para funcionar con una sola función, **fArray**. En general, su XLL tendrá más de un función de devolución de memoria que necesita liberarse, en cuyo caso se requiere una implementación menos restringida. 
  
 **Implementación de ejemplo 2**
  
El segundo ejemplo de implementación es coherente con los supuestos utilizados en los ejemplos de creación de **XLOPER12** en sección 1.6.3, xl12_Str_example, xl12_Ref_example y xl12_Multi_example. Los supuestos son, cuando el bit **xlbitDLLFree** ha sido conjunto, todas las cadena, matriz y memoria de referencia externa se ha asignado dinámicamente utilizando **malloc**y, por tanto, debe ser liberados en una llamada a libre.
  
 **Implementación de ejemplo 3**
  
El tercer ejemplo de implementación es coherente con un XLL donde exportado las funciones que devuelven **XLOPER12**s asignan cadenas, las referencias externas y las matrices mediante **malloc**, y se asigna también dinámicamente **XLOPER12** propio. Devolución de un puntero a asignados dinámicamente **XLOPER12** es una forma de garantizar que la función es segura para subprocesos. 
  
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

## <a name="see-also"></a>Vea también



[Administrador de complementos y funciones de la interfaz de XLL](add-in-manager-and-xll-interface-functions.md)

