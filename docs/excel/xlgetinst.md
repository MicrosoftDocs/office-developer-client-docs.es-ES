---
title: xlGetInst
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlGetInst
keywords:
- función xlgetinst [Excel 2007]
localization_priority: Normal
ms.assetid: 631a8f4e-ea7c-4743-9ee1-b2233fd7d98d
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: e113ddbf55e2b4651d578549802c44e2c6413a18
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303853"
---
# <a name="xlgetinst"></a><span data-ttu-id="8fd32-104">xlGetInst</span><span class="sxs-lookup"><span data-stu-id="8fd32-104">xlGetInst</span></span>

 <span data-ttu-id="8fd32-105">**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="8fd32-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="8fd32-106">Devuelve el identificador de instancia de la instancia de Microsoft Excel que actualmente está llamando a un archivo DLL.</span><span class="sxs-lookup"><span data-stu-id="8fd32-106">Returns the instance handle of the instance of Microsoft Excel that is currently calling a DLL.</span></span>
  
```cs
Excel4(xlGetInst, LPXLOPER pxRes, 0); /* returns low part only */
Excel12(xlGetInst, LPXLOPER12 pxRes, 0); /* returns full handle */
```

## <a name="parameters"></a><span data-ttu-id="8fd32-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="8fd32-107">Parameters</span></span>

<span data-ttu-id="8fd32-108">Esta función no tiene argumentos.</span><span class="sxs-lookup"><span data-stu-id="8fd32-108">This function has no arguments.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="8fd32-109">Valor de la propiedad/valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8fd32-109">Property value/Return value</span></span>

<span data-ttu-id="8fd32-110">El identificador de instancia (**xltypeInt**) estará en el campo **Val. w** .</span><span class="sxs-lookup"><span data-stu-id="8fd32-110">The instance handle (**xltypeInt**) will be in the **val.w** field.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="8fd32-111">Comentarios</span><span class="sxs-lookup"><span data-stu-id="8fd32-111">Remarks</span></span>

<span data-ttu-id="8fd32-112">Esta función se puede usar para distinguir entre varias instancias en ejecución de Excel que llaman a la DLL.</span><span class="sxs-lookup"><span data-stu-id="8fd32-112">This function can be used to distinguish between multiple running instances of Excel that are calling the DLL.</span></span>
  
<span data-ttu-id="8fd32-113">Cuando se llama a esta función mediante [Excel4](excel4-excel12.md) o [Excel4v](excel4v-excel12v.md), la variable de entero del XLOPER que se devuelve es un int Short de 16 bits firmado. Esto solo puede contener los 16 bits bajos del controlador de Windows de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="8fd32-113">When you are calling this function using [Excel4](excel4-excel12.md) or [Excel4v](excel4v-excel12v.md), the returned XLOPER integer variable is a signed 16-bit short int. This is only capable of containing the low 16 bits of the 32-bit Windows handle.</span></span> <span data-ttu-id="8fd32-114">A partir de Excel 2007, la variable de entero de **XLOPER12** es un int de 32 bits firmado y, por lo tanto, contiene todo el identificador, lo que elimina la necesidad de recorrer en iteración todas las ventanas abiertas.</span><span class="sxs-lookup"><span data-stu-id="8fd32-114">Starting in Excel 2007, the integer variable of the **XLOPER12** is a signed 32-bit int and therefore contains the entire handle, removing the need to iterate all open windows.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="8fd32-115">Si se usa la función **xlGetInst** con la versión de 64 bits de Microsoft Excel, se producirá un error en la función.</span><span class="sxs-lookup"><span data-stu-id="8fd32-115">If the **xlGetInst** function is used with the 64-bit version of Microsoft Excel, then the function will fail.</span></span> <span data-ttu-id="8fd32-116">Esto se debe a que el tipo de valor **xltypeInt** no es lo suficientemente ancho como para contener el identificador largo de 64 bits devuelto por Excel en este caso.</span><span class="sxs-lookup"><span data-stu-id="8fd32-116">This is because the **xltypeInt** value type is not wide enough to hold the 64-bit long handle returned by Excel in this case.</span></span> <span data-ttu-id="8fd32-117">Con este propósito, Excel 2010 incorpora una nueva función denominada [xlGetInstPtr](xlgetinstptr.md), que se ejecuta correctamente con las versiones de 32 bits y de 64 bits de Excel.</span><span class="sxs-lookup"><span data-stu-id="8fd32-117">For this purpose, Excel 2010 introduced a new function named [xlGetInstPtr](xlgetinstptr.md), which runs correctly with both the 32-bit and 64-bit versions of Excel.</span></span> 
  
## <a name="example"></a><span data-ttu-id="8fd32-118">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="8fd32-118">Example</span></span>

<span data-ttu-id="8fd32-119">En el siguiente ejemplo se compara la instancia de la última copia de Excel que la ha llamado con la copia actual de Excel que la ha llamado.</span><span class="sxs-lookup"><span data-stu-id="8fd32-119">The following example compares the instance of the last copy of Excel that called it to the current copy of Excel that called it.</span></span> <span data-ttu-id="8fd32-120">Si son iguales, devuelve 1; Si no es así, devuelve 0; Si se produce un error en la función, devuelve-1.</span><span class="sxs-lookup"><span data-stu-id="8fd32-120">If they are the same, it returns 1; if not, it returns 0; if the function fails, it returns -1.</span></span>
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI xlGetInstExample(void)
{
    XLOPER12 xRes;
    static HANDLE hOld = 0;
    short iRet;
    if (Excel12(xlGetInst, &xRes, 0) != xlretSuccess)
        iRet = -1;
    else
    {
    HANDLE hNew;
    hNew = (HANDLE)xRes.val.w;
    if (hNew != hOld)
            iRet = 0;
    else
            iRet = 1;
    hOld = hNew;
    }
    return iRet;
}
```

## <a name="see-also"></a><span data-ttu-id="8fd32-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="8fd32-121">See also</span></span>



[<span data-ttu-id="8fd32-122">xlGetHwnd</span><span class="sxs-lookup"><span data-stu-id="8fd32-122">xlGetHwnd</span></span>](xlgethwnd.md)
  
[<span data-ttu-id="8fd32-123">xlGetInstPtr</span><span class="sxs-lookup"><span data-stu-id="8fd32-123">xlGetInstPtr</span></span>](xlgetinstptr.md)


[<span data-ttu-id="8fd32-124">Funciones de la API de C que se pueden llamar solo desde una DLL o XLL</span><span class="sxs-lookup"><span data-stu-id="8fd32-124">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

