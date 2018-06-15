---
title: xlAutoRegister/xlAutoRegister12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlAutoRegister
keywords:
- xlautoregister (función) [excel 2007]
localization_priority: Normal
ms.assetid: aa4673cf-8e97-4678-b8d4-6a74426334f9
description: 'Hace referencia a: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: e6430a54b0c0ed3b6e08d3c9256cae7dcde926ab
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/15/2018
ms.locfileid: "19815715"
---
# <a name="xlautoregisterxlautoregister12"></a><span data-ttu-id="d68b9-104">xlAutoRegister/xlAutoRegister12</span><span class="sxs-lookup"><span data-stu-id="d68b9-104">xlAutoRegister/xlAutoRegister12</span></span>

 <span data-ttu-id="d68b9-105">**Se aplica a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="d68b9-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="d68b9-106">Excel llama a la [función xlAutoRegister](xlautoregister-xlautoregister12.md) cada vez que se ha realizado una llamada a la función XLM **registrar**o la [función xlfRegister](xlfregister-form-1.md)de API de C equivalente, con los tipos de devolución y el argumento de la función que se está registrando que faltan.</span><span class="sxs-lookup"><span data-stu-id="d68b9-106">Excel calls the [xlAutoRegister function](xlautoregister-xlautoregister12.md) whenever a call has been made to the XLM function **REGISTER**, or the C API equivalent [xlfRegister function](xlfregister-form-1.md), with the return and argument types of the function being registered missing.</span></span> <span data-ttu-id="d68b9-107">Permite que los XLL buscar sus listas internas de funciones exportadas y comandos para registrar la función con el argumento y devolver los tipos especificados.</span><span class="sxs-lookup"><span data-stu-id="d68b9-107">It allows the XLL to search its internal lists of exported functions and commands to register the function with the argument and return types specified.</span></span>
  
<span data-ttu-id="d68b9-108">Iniciar en Excel 2007, Excel llama a la función **xlAutoRegister12** preferencia a la función **xlAutoRegister** si lo exporta el XLL.</span><span class="sxs-lookup"><span data-stu-id="d68b9-108">Starting in Excel 2007, Excel calls the **xlAutoRegister12** function in preference to the **xlAutoRegister** function if it is exported by the XLL.</span></span> 
  
<span data-ttu-id="d68b9-109">Excel no requiere un XLL implementar y exportar a cualquiera de estas funciones.</span><span class="sxs-lookup"><span data-stu-id="d68b9-109">Excel does not require an XLL to implement and export either of these functions.</span></span>
  
> [!NOTE]
> <span data-ttu-id="d68b9-110">Si **xlAutoRegister**/ **xlAutoRegister12** intenta registrar la función sin proporcionar el argumento y tipos de valores devueltos, produce un bucle llamada recursiva que finalmente desbordamientos de la pila de llamadas y bloquea Excel.</span><span class="sxs-lookup"><span data-stu-id="d68b9-110">If **xlAutoRegister**/ **xlAutoRegister12** tries to register the function without supplying the argument and return types, a recursive calling loop occurs which eventually overflows the call stack and crashes Excel.</span></span> 
  
```cs
LPXLOPER12 WINAPI xlAutoRegister12(LPXLOPER12 pxName);
LPXLOPER WINAPI xlAutoRegister(LPXLOPER pxName);
```

## <a name="parameters"></a><span data-ttu-id="d68b9-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d68b9-111">Parameters</span></span>

 <span data-ttu-id="d68b9-112">_pxName_ (**xltypeStr**)</span><span class="sxs-lookup"><span data-stu-id="d68b9-112">_pxName_ (**xltypeStr**)</span></span>
  
<span data-ttu-id="d68b9-113">El nombre de la función XLL que se está registrando.</span><span class="sxs-lookup"><span data-stu-id="d68b9-113">The name of the XLL function that is being registered.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="d68b9-114">Propiedad valor y valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d68b9-114">Property value/Return value</span></span>

<span data-ttu-id="d68b9-115">La función debe devolver el resultado del intento de registrar la función XLL _pxName_ mediante la función **xlfRegister** .</span><span class="sxs-lookup"><span data-stu-id="d68b9-115">The function should return the result of the attempt to register the XLL function  _pxName_ using the **xlfRegister** function.</span></span> <span data-ttu-id="d68b9-116">Si la función especificada no es una de las exportaciones de XLL, debe devolver el **#VALUE!**</span><span class="sxs-lookup"><span data-stu-id="d68b9-116">If the specified function is not one of the XLL's exports, it should return the **#VALUE!**</span></span> <span data-ttu-id="d68b9-117">error, o **NULL** que Excel interpretará en **#VALUE!**.</span><span class="sxs-lookup"><span data-stu-id="d68b9-117">error, or **NULL** which Excel will interpret at **#VALUE!**.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d68b9-118">Notas</span><span class="sxs-lookup"><span data-stu-id="d68b9-118">Remarks</span></span>

<span data-ttu-id="d68b9-119">Su implementación de **xlAutoRegister** debe realizar una búsqueda a través de listas interno de los XLL de las funciones y comandos que exporta busca una coincidencia con el nombre pasado entre mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="d68b9-119">Your implementation of **xlAutoRegister** should perform a case-insensitive search through your XLL's internal lists of the functions and commands it exports looking for a match with the passed-in name.</span></span> <span data-ttu-id="d68b9-120">Si se encuentra la función o el comando, **xlAutoRegister** debe intentar registrarlo, mediante la función **xlfRegister** , asegurándose de proporcionar la cadena que indica los tipos de retorno y el argumento de la función, así como cualquier otro necesarios a Excel información sobre la función.</span><span class="sxs-lookup"><span data-stu-id="d68b9-120">If the function or command is found, **xlAutoRegister** should attempt to register it, using the **xlfRegister** function, making sure to provide the string that tells Excel the return and argument types of the function, as well as any other required information about the function.</span></span> <span data-ttu-id="d68b9-121">A continuación, debe devolver a Excel todo lo que devuelve la llamada a **xlfRegister** .</span><span class="sxs-lookup"><span data-stu-id="d68b9-121">It should then return to Excel whatever the call to **xlfRegister** returned.</span></span> <span data-ttu-id="d68b9-122">Si la función se ha registrado correctamente, **xlfRegister** devuelve un valor de **xltypeNum** que contiene el identificador de registro de la función.</span><span class="sxs-lookup"><span data-stu-id="d68b9-122">If the function was registered successfully, **xlfRegister** returns an **xltypeNum** value containing the Register ID of the function.</span></span> 
  
### <a name="example"></a><span data-ttu-id="d68b9-123">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="d68b9-123">Example</span></span>

<span data-ttu-id="d68b9-124">Consulte el archivo `SAMPLES\EXAMPLE\EXAMPLE.C` para una implementación de ejemplo de esta función.</span><span class="sxs-lookup"><span data-stu-id="d68b9-124">See the file  `SAMPLES\EXAMPLE\EXAMPLE.C` for an example implementation of this function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="d68b9-125">Ver también</span><span class="sxs-lookup"><span data-stu-id="d68b9-125">See also</span></span>



[<span data-ttu-id="d68b9-126">REGISTRAR</span><span class="sxs-lookup"><span data-stu-id="d68b9-126">REGISTER</span></span>](xlfregister-form-1.md)
  
[<span data-ttu-id="d68b9-127">ANULAR EL REGISTRO</span><span class="sxs-lookup"><span data-stu-id="d68b9-127">UNREGISTER</span></span>](xlfunregister-form-1.md)

