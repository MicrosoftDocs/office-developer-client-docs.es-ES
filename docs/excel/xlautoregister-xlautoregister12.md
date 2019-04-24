---
title: xlAutoRegister/xlAutoRegister12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlAutoRegister
keywords:
- función xlautoregister [Excel 2007]
localization_priority: Normal
ms.assetid: aa4673cf-8e97-4678-b8d4-6a74426334f9
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: f043558f3f642001e9ba11ee5b18a2721c3dddfb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303951"
---
# <a name="xlautoregisterxlautoregister12"></a><span data-ttu-id="0732f-104">xlAutoRegister/xlAutoRegister12</span><span class="sxs-lookup"><span data-stu-id="0732f-104">xlAutoRegister/xlAutoRegister12</span></span>

 <span data-ttu-id="0732f-105">**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="0732f-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="0732f-106">Excel llama a la [función xlAutoRegister](xlautoregister-xlautoregister12.md) siempre que se ha realizado una llamada al **registro**de la función XLM o a la [función xlfRegister](xlfregister-form-1.md)equivalente de la API de C, con los tipos devuelto y argumento de la función que se está registrando.</span><span class="sxs-lookup"><span data-stu-id="0732f-106">Excel calls the [xlAutoRegister function](xlautoregister-xlautoregister12.md) whenever a call has been made to the XLM function **REGISTER**, or the C API equivalent [xlfRegister function](xlfregister-form-1.md), with the return and argument types of the function being registered missing.</span></span> <span data-ttu-id="0732f-107">Permite al XLL buscar en sus listas internas de funciones y comandos exportados para registrar la función con los tipos de devoluciones y argumentos especificados.</span><span class="sxs-lookup"><span data-stu-id="0732f-107">It allows the XLL to search its internal lists of exported functions and commands to register the function with the argument and return types specified.</span></span>
  
<span data-ttu-id="0732f-108">A partir de Excel 2007, Excel llama a la función **xlAutoRegister12** en prioridad a la función **xlAutoRegister** si la exporta el XLL.</span><span class="sxs-lookup"><span data-stu-id="0732f-108">Starting in Excel 2007, Excel calls the **xlAutoRegister12** function in preference to the **xlAutoRegister** function if it is exported by the XLL.</span></span> 
  
<span data-ttu-id="0732f-109">Excel no requiere un XLL que implemente y exporte cualquiera de estas funciones.</span><span class="sxs-lookup"><span data-stu-id="0732f-109">Excel does not require an XLL to implement and export either of these functions.</span></span>
  
> [!NOTE]
> <span data-ttu-id="0732f-110">Si **xlAutoRegister**/ **xlAutoRegister12** intenta registrar la función sin proporcionar el argumento y los tipos de valor devuelto, se produce un bucle de llamada recursivo que finalmente desborda la pila de llamadas y bloquea Excel.</span><span class="sxs-lookup"><span data-stu-id="0732f-110">If **xlAutoRegister**/ **xlAutoRegister12** tries to register the function without supplying the argument and return types, a recursive calling loop occurs which eventually overflows the call stack and crashes Excel.</span></span> 
  
```cs
LPXLOPER12 WINAPI xlAutoRegister12(LPXLOPER12 pxName);
LPXLOPER WINAPI xlAutoRegister(LPXLOPER pxName);
```

## <a name="parameters"></a><span data-ttu-id="0732f-111">Parameters</span><span class="sxs-lookup"><span data-stu-id="0732f-111">Parameters</span></span>

 <span data-ttu-id="0732f-112">_pxName_ (**xltypeStr**)</span><span class="sxs-lookup"><span data-stu-id="0732f-112">_pxName_ (**xltypeStr**)</span></span>
  
<span data-ttu-id="0732f-113">El nombre de la función XLL que se está registrando.</span><span class="sxs-lookup"><span data-stu-id="0732f-113">The name of the XLL function that is being registered.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="0732f-114">Valor de la propiedad/valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0732f-114">Property value/Return value</span></span>

<span data-ttu-id="0732f-115">La función debe devolver el resultado del intento de registrar la función XLL _pxName_ mediante la función **xlfRegister** .</span><span class="sxs-lookup"><span data-stu-id="0732f-115">The function should return the result of the attempt to register the XLL function  _pxName_ using the **xlfRegister** function.</span></span> <span data-ttu-id="0732f-116">Si la función especificada no es una de las exportaciones del XLL, debe devolver el **#VALUE!**</span><span class="sxs-lookup"><span data-stu-id="0732f-116">If the specified function is not one of the XLL's exports, it should return the **#VALUE!**</span></span> <span data-ttu-id="0732f-117">error o **null** que Excel interpretará en **#VALUE!**.</span><span class="sxs-lookup"><span data-stu-id="0732f-117">error, or **NULL** which Excel will interpret at **#VALUE!**.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="0732f-118">Comentarios</span><span class="sxs-lookup"><span data-stu-id="0732f-118">Remarks</span></span>

<span data-ttu-id="0732f-119">La implementación de **xlAutoRegister** debe realizar una búsqueda sin distinción entre mayúsculas y minúsculas a través de las listas internas de los XLL de las funciones y comandos que exporta buscando una coincidencia con el nombre pasado.</span><span class="sxs-lookup"><span data-stu-id="0732f-119">Your implementation of **xlAutoRegister** should perform a case-insensitive search through your XLL's internal lists of the functions and commands it exports looking for a match with the passed-in name.</span></span> <span data-ttu-id="0732f-120">Si se encuentra la función o el comando, **xlAutoRegister** debe intentar registrarla, mediante la función **xlfRegister** , asegurándose de proporcionar la cadena que le indica a Excel los tipos de argumento y devolución de la función, así como cualquier otro tipo de argumento necesario información sobre la función.</span><span class="sxs-lookup"><span data-stu-id="0732f-120">If the function or command is found, **xlAutoRegister** should attempt to register it, using the **xlfRegister** function, making sure to provide the string that tells Excel the return and argument types of the function, as well as any other required information about the function.</span></span> <span data-ttu-id="0732f-121">A continuación, debe volver a Excel cualquiera que sea la llamada a **xlfRegister** devuelta.</span><span class="sxs-lookup"><span data-stu-id="0732f-121">It should then return to Excel whatever the call to **xlfRegister** returned.</span></span> <span data-ttu-id="0732f-122">Si la función se registró correctamente, **xlfRegister** devuelve un valor de **xltypeNum** que contiene el identificador de registro de la función.</span><span class="sxs-lookup"><span data-stu-id="0732f-122">If the function was registered successfully, **xlfRegister** returns an **xltypeNum** value containing the Register ID of the function.</span></span> 
  
### <a name="example"></a><span data-ttu-id="0732f-123">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="0732f-123">Example</span></span>

<span data-ttu-id="0732f-124">Vea el archivo `SAMPLES\EXAMPLE\EXAMPLE.C` para obtener un ejemplo de implementación de esta función.</span><span class="sxs-lookup"><span data-stu-id="0732f-124">See the file  `SAMPLES\EXAMPLE\EXAMPLE.C` for an example implementation of this function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="0732f-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="0732f-125">See also</span></span>



[<span data-ttu-id="0732f-126">Registre</span><span class="sxs-lookup"><span data-stu-id="0732f-126">REGISTER</span></span>](xlfregister-form-1.md)
  
[<span data-ttu-id="0732f-127">ANULAR el registro</span><span class="sxs-lookup"><span data-stu-id="0732f-127">UNREGISTER</span></span>](xlfunregister-form-1.md)

