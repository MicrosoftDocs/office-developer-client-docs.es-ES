---
title: xlAutoRegister/xlAutoRegister12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlAutoRegister
keywords:
- función xlautoregister [excel 2007]
localization_priority: Normal
ms.assetid: aa4673cf-8e97-4678-b8d4-6a74426334f9
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: f043558f3f642001e9ba11ee5b18a2721c3dddfb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421168"
---
# <a name="xlautoregisterxlautoregister12"></a><span data-ttu-id="66230-104">xlAutoRegister/xlAutoRegister12</span><span class="sxs-lookup"><span data-stu-id="66230-104">xlAutoRegister/xlAutoRegister12</span></span>

 <span data-ttu-id="66230-105">**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="66230-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="66230-106">Excel llama a la función [xlAutoRegister](xlautoregister-xlautoregister12.md) siempre que se ha realizado una llamada a la función **XLM REGISTER** o a la función [xlfRegister](xlfregister-form-1.md)equivalente de la API de C, sin que se registren los tipos de valor devuelto y argumento de la función.</span><span class="sxs-lookup"><span data-stu-id="66230-106">Excel calls the [xlAutoRegister function](xlautoregister-xlautoregister12.md) whenever a call has been made to the XLM function **REGISTER**, or the C API equivalent [xlfRegister function](xlfregister-form-1.md), with the return and argument types of the function being registered missing.</span></span> <span data-ttu-id="66230-107">Permite que el XLL busque en sus listas internas de comandos y funciones exportadas para registrar la función con el argumento y los tipos devueltos especificados.</span><span class="sxs-lookup"><span data-stu-id="66230-107">It allows the XLL to search its internal lists of exported functions and commands to register the function with the argument and return types specified.</span></span>
  
<span data-ttu-id="66230-108">A partir de Excel 2007, Excel llama a la función **xlAutoRegister12** en preferencia a la función **xlAutoRegister** si la exporta el XLL.</span><span class="sxs-lookup"><span data-stu-id="66230-108">Starting in Excel 2007, Excel calls the **xlAutoRegister12** function in preference to the **xlAutoRegister** function if it is exported by the XLL.</span></span> 
  
<span data-ttu-id="66230-109">Excel no requiere un XLL para implementar y exportar ninguna de estas funciones.</span><span class="sxs-lookup"><span data-stu-id="66230-109">Excel does not require an XLL to implement and export either of these functions.</span></span>
  
> [!NOTE]
> <span data-ttu-id="66230-110">Si **xlAutoRegister** /  **xlAutoRegister12** intenta registrar la función sin proporcionar el argumento y los tipos devueltos, se produce un bucle de llamada recursiva que finalmente desborda la pila de llamadas y bloquea Excel.</span><span class="sxs-lookup"><span data-stu-id="66230-110">If **xlAutoRegister**/ **xlAutoRegister12** tries to register the function without supplying the argument and return types, a recursive calling loop occurs which eventually overflows the call stack and crashes Excel.</span></span> 
  
```cs
LPXLOPER12 WINAPI xlAutoRegister12(LPXLOPER12 pxName);
LPXLOPER WINAPI xlAutoRegister(LPXLOPER pxName);
```

## <a name="parameters"></a><span data-ttu-id="66230-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="66230-111">Parameters</span></span>

 <span data-ttu-id="66230-112">_pxName_ (**xltypeStr**)</span><span class="sxs-lookup"><span data-stu-id="66230-112">_pxName_ (**xltypeStr**)</span></span>
  
<span data-ttu-id="66230-113">Nombre de la función XLL que se está registrando.</span><span class="sxs-lookup"><span data-stu-id="66230-113">The name of the XLL function that is being registered.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="66230-114">Valor de la propiedad/valor devuelto</span><span class="sxs-lookup"><span data-stu-id="66230-114">Property value/Return value</span></span>

<span data-ttu-id="66230-115">La función debe devolver el resultado del intento de registrar la función XLL _pxName_ mediante la **función xlfRegister.**</span><span class="sxs-lookup"><span data-stu-id="66230-115">The function should return the result of the attempt to register the XLL function  _pxName_ using the **xlfRegister** function.</span></span> <span data-ttu-id="66230-116">Si la función especificada no es una de las exportaciones de XLL, debe devolver el **#VALUE!**</span><span class="sxs-lookup"><span data-stu-id="66230-116">If the specified function is not one of the XLL's exports, it should return the **#VALUE!**</span></span> <span data-ttu-id="66230-117">o **NULL** que Excel interpretará en **#VALUE!**.</span><span class="sxs-lookup"><span data-stu-id="66230-117">error, or **NULL** which Excel will interpret at **#VALUE!**.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="66230-118">Comentarios</span><span class="sxs-lookup"><span data-stu-id="66230-118">Remarks</span></span>

<span data-ttu-id="66230-119">La implementación de **xlAutoRegister** debe realizar una búsqueda que no coincida con mayúsculas de minúsculas a través de las listas internas de XLL de las funciones y comandos que exporta en busca de una coincidencia con el nombre pasado.</span><span class="sxs-lookup"><span data-stu-id="66230-119">Your implementation of **xlAutoRegister** should perform a case-insensitive search through your XLL's internal lists of the functions and commands it exports looking for a match with the passed-in name.</span></span> <span data-ttu-id="66230-120">Si se encuentra la función o el comando, **xlAutoRegister** debe intentar registrarla, mediante la función **xlfRegister,** asegurándose de proporcionar la cadena que indica a Excel los tipos devueltos y de argumentos de la función, así como cualquier otra información necesaria sobre la función.</span><span class="sxs-lookup"><span data-stu-id="66230-120">If the function or command is found, **xlAutoRegister** should attempt to register it, using the **xlfRegister** function, making sure to provide the string that tells Excel the return and argument types of the function, as well as any other required information about the function.</span></span> <span data-ttu-id="66230-121">A continuación, debe volver a Excel lo que devuelva la llamada **a xlfRegister.**</span><span class="sxs-lookup"><span data-stu-id="66230-121">It should then return to Excel whatever the call to **xlfRegister** returned.</span></span> <span data-ttu-id="66230-122">Si la función se registró correctamente, **xlfRegister** devuelve un valor **xltypeNum** que contiene el identificador de registro de la función.</span><span class="sxs-lookup"><span data-stu-id="66230-122">If the function was registered successfully, **xlfRegister** returns an **xltypeNum** value containing the Register ID of the function.</span></span> 
  
### <a name="example"></a><span data-ttu-id="66230-123">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="66230-123">Example</span></span>

<span data-ttu-id="66230-124">Vea el archivo  `SAMPLES\EXAMPLE\EXAMPLE.C` para obtener un ejemplo de implementación de esta función.</span><span class="sxs-lookup"><span data-stu-id="66230-124">See the file  `SAMPLES\EXAMPLE\EXAMPLE.C` for an example implementation of this function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="66230-125">Consulte también</span><span class="sxs-lookup"><span data-stu-id="66230-125">See also</span></span>



[<span data-ttu-id="66230-126">REGISTER</span><span class="sxs-lookup"><span data-stu-id="66230-126">REGISTER</span></span>](xlfregister-form-1.md)
  
[<span data-ttu-id="66230-127">UNREGISTER</span><span class="sxs-lookup"><span data-stu-id="66230-127">UNREGISTER</span></span>](xlfunregister-form-1.md)

