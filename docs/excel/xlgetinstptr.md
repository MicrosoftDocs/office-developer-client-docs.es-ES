---
title: xlGetInstPtr
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a166f39c-f10b-4e56-8b5d-e6a54ee08c8f
description: 'Hace referencia a: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 7cc07093e5db335d01fe85527746594d34d4d938
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815748"
---
# <a name="xlgetinstptr"></a><span data-ttu-id="b33bb-103">xlGetInstPtr</span><span class="sxs-lookup"><span data-stu-id="b33bb-103">xlGetInstPtr</span></span>

<span data-ttu-id="b33bb-104">**Se aplica a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="b33bb-104">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="b33bb-105">Devuelve el identificador de instancia de la instancia de Microsoft Excel que actualmente se está llamando a un archivo DLL.</span><span class="sxs-lookup"><span data-stu-id="b33bb-105">Returns the instance handle of the instance of Microsoft Excel that is currently calling a DLL.</span></span>
  
```cs
Excel4(xlGetInstPtr, LPXLOPER pxRes, 0);Excel12(xlGetInstPtr, LPXLOPER12 pxRes, 0);
```

## <a name="parameters"></a><span data-ttu-id="b33bb-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b33bb-106">Parameters</span></span>

<span data-ttu-id="b33bb-107">Esta función no tiene argumentos.</span><span class="sxs-lookup"><span data-stu-id="b33bb-107">This function has no arguments.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="b33bb-108">Propiedad valor y valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b33bb-108">Property value/Return value</span></span>

<span data-ttu-id="b33bb-109">El identificador de instancia (**xltypeBigData**) estará en el campo **val.bigdata.h.hdata** .</span><span class="sxs-lookup"><span data-stu-id="b33bb-109">The instance handle (**xltypeBigData**) will be in the **val.bigdata.h.hdata** field.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="b33bb-110">Notas</span><span class="sxs-lookup"><span data-stu-id="b33bb-110">Remarks</span></span>

<span data-ttu-id="b33bb-111">Esta función puede usarse para distinguir entre varias instancias en ejecución de Excel que se va a llamar a la DLL.</span><span class="sxs-lookup"><span data-stu-id="b33bb-111">This function can be used to distinguish between multiple running instances of Excel that are calling the DLL.</span></span>
  
<span data-ttu-id="b33bb-112">Esta función devuelve un valor correcto con las versiones de 32 bits y 64 bits de Excel.</span><span class="sxs-lookup"><span data-stu-id="b33bb-112">This function returns a correct value with both 32-bit and 64-bit versions of Excel.</span></span> <span data-ttu-id="b33bb-113">Se introdujo en Excel 2010, como una extensión a la función [xlGetInst](xlgetinst.md) , que funciona correctamente sólo con las versiones de 32 bits de Excel.</span><span class="sxs-lookup"><span data-stu-id="b33bb-113">It was introduced in Excel 2010 as an extension to the [xlGetInst](xlgetinst.md) function, which works correctly only with 32-bit versions of Excel.</span></span> 
  
<span data-ttu-id="b33bb-114">Esta función funciona correctamente cuando se llama mediante el uso de las variedades [Excel4 y Excel12](excel4-excel12.md) de las funciones de devolución de llamada de API, porque **XLOPER** y **XLOPER12** tienen la misma estructura que admite el valor **xltypeBigData** Escriba.</span><span class="sxs-lookup"><span data-stu-id="b33bb-114">This function works correctly when it is called by using both the [Excel4 and Excel12](excel4-excel12.md) varieties of the API callback functions, because both **XLOPER** and **XLOPER12** have the same structure that supports the **xltypeBigData** value type.</span></span> 
  
## <a name="example"></a><span data-ttu-id="b33bb-115">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="b33bb-115">Example</span></span>

<span data-ttu-id="b33bb-116">En el ejemplo siguiente se compara la instancia de la última copia de Excel que llama a la copia actual de Excel que lo llamó.</span><span class="sxs-lookup"><span data-stu-id="b33bb-116">The following example compares the instance of the last copy of Excel that called it to the current copy of Excel that called it.</span></span> <span data-ttu-id="b33bb-117">Si son iguales, devuelve 1; en caso contrario, devuelve 0; Si se produce un error en la función, devuelve -1.</span><span class="sxs-lookup"><span data-stu-id="b33bb-117">If they are the same, it returns 1; if not, it returns 0; if the function fails, it returns -1.</span></span> <span data-ttu-id="b33bb-118">Este ejemplo funciona con versiones de 32 bits y 64 bits de Excel.</span><span class="sxs-lookup"><span data-stu-id="b33bb-118">This sample works with both 32-bit and 64-bit versions of Excel.</span></span>
  
`\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI xlGetInstPtrExample(void)
{
    XLOPER12 xRes;
    static HANDLE hOld = 0;
    short iRet;
    if (Excel12(xlGetInstPtr, &xRes, 0) != xlretSuccess)
    iRet = -1;
    else
    {
    HANDLE hNew;
    hNew =  xRes.val.bigdata.h.hdata;
    if (hNew != hOld)
    iRet = 0;
    else
    iRet = 1;
    hOld = hNew;
    }
    return iRet;
}
```

## <a name="see-also"></a><span data-ttu-id="b33bb-119">Ver también</span><span class="sxs-lookup"><span data-stu-id="b33bb-119">See also</span></span>

- [<span data-ttu-id="b33bb-120">xlGetHwnd</span><span class="sxs-lookup"><span data-stu-id="b33bb-120">xlGetHwnd</span></span>](xlgethwnd.md)
- [<span data-ttu-id="b33bb-121">xlGetInst</span><span class="sxs-lookup"><span data-stu-id="b33bb-121">xlGetInst</span></span>](xlgetinst.md)
- [<span data-ttu-id="b33bb-122">Funciones de la API de C que se pueden llamar solo desde una DLL o XLL</span><span class="sxs-lookup"><span data-stu-id="b33bb-122">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

