---
title: xlAutoFree/xlAutoFree12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlAutoFree
keywords:
- xlautofree (función) [Excel 2007]
localization_priority: Normal
ms.assetid: f73d292c-d6d8-4be5-89c0-bef15db236d6
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 3dfba5ae98b0635c95308eac01bf2f10867678e1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303972"
---
# <a name="xlautofreexlautofree12"></a>xlAutoFree/xlAutoFree12

 **Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio 
  
Llamado por Microsoft Excel inmediatamente después de que una función XLL de hoja de cálculo devuelve un **XLOPER**/ **XLOPER12** para él con un conjunto de marcas que le indica que hay memoria que el XLL todavía tiene que liberar. Esto permite al XLL devolver matrices, cadenas y referencias externas asignadas dinámicamente a la hoja de cálculo sin pérdidas de memoria. Para obtener más información, consulte [Administración de memoria en Excel](memory-management-in-excel.md).
  
A partir de Excel 2007, se admiten la función **xlAutoFree12** y el tipo de datos **XLOPER12** . 
  
Excel no requiere un XLL que implemente y exporte cualquiera de estas funciones. Sin embargo, debe hacerlo si las funciones XLL devuelven XLOPER o XLOPER12 que se ha asignado dinámicamente o que contiene punteros a la memoria asignada dinámicamente. Asegúrese de que su elección de cómo administrar la memoria para estos tipos es coherente en todo el XLL y con cómo implementó **xlAutoFree** y **xlAutoFree12**.
  
Dentro de la función **xlAutoFree**/ **xlAutoFree12** , las devoluciones de llamada en Excel están deshabilitadas, con una excepción: se puede llamar a **xlFree** para liberar la memoria asignada a Excel. 
  
```cs
void WINAPI xlAutoFree(LPXLOPER pxFree);
void WINAPI xlAutoFree12(LPXLOPER12 pxFree);
```

## <a name="parameters"></a>Parameters

 _pxFree_ (**LPXLOPER en el caso de xlAutoFree**)
  
 _pxFree_ (**LPXLOPER12 en el caso de xlAutoFree12**)
  
Un puntero a **XLOPER** o **XLOPER12** que tiene memoria que debe liberarse. 
  
## <a name="property-valuereturn-value"></a>Valor de la propiedad/valor devuelto

Esta función no devuelve un valor y debe declararse como devolución void.
  
## <a name="remarks"></a>Comentarios

Cuando Excel está configurado para usar el recálculo de un libro multiproceso, se llama a **xlAutoFree**/ **xlAutoFree12** en el mismo subproceso usado para llamar a la función que lo devolvió. La llamada a **xlAutoFree**/ **xlAutoFree12** siempre se realiza antes de que las celdas de la hoja de cálculo siguientes se evalúen en dicho subproceso. Esto simplifica el diseño de subprocesos seguros en tu XLL. 
  
Si la función de **xlAutoFree**/ **xlAutoFree12** que ha proporcionado busca en el campo **xltype** de _pxFree_, recuerde que el bit **xlbitDLLFree** se establecerá todavía. 
  
## <a name="example"></a>Ejemplo

 **Ejemplo de implementación 1**
  
El primer código de `\SAMPLES\EXAMPLE\EXAMPLE.C` muestra una implementación muy específica de **xlAutoFree**, diseñada para funcionar con una sola función, **fArray**. En general, el XLL tendrá más de una función que devuelve una memoria que debe liberarse, en cuyo caso se necesita una implementación menos restringida. 
  
 **Ejemplo de implementación 2**
  
La segunda implementación de ejemplo es coherente con los supuestos que se usan en los ejemplos de creación de **XLOPER12** de las secciones 1.6.3, Xl12_Str_example, Xl12_Ref_example y xl12_Multi_example. Los supuestos son que, cuando se ha establecido el bit **xlbitDLLFree** , todas las cadenas, matrices y memoria de referencia externa se han asignado dinámicamente mediante **malloc**y, por lo tanto, es necesario liberarla en una llamada a Free.
  
 **Ejemplo de implementación 3**
  
La tercera implementación de ejemplo es coherente con un XLL en el que las funciones exportadas que devuelven **XLOPER12**s asignan cadenas, referencias externas y matrices que utilizan **malloc**, y donde el **XLOPER12** también se asigna de forma dinámica. Devolver un puntero a un **XLOPER12** asignado dinámicamente es una forma de garantizar que la función es segura para subprocesos. 
  
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

