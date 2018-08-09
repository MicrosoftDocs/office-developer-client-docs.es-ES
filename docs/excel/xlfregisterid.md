---
title: xlfRegisterId
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlfRegisterId
keywords:
- xlfregisterid (función) [excel 2007]
localization_priority: Normal
ms.assetid: d34cf20c-a5cd-45fb-9dcb-d49eac2d99dd
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: cd401393b7465442cef9342b942a27456871c68b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815740"
---
# <a name="xlfregisterid"></a><span data-ttu-id="e1690-104">xlfRegisterId</span><span class="sxs-lookup"><span data-stu-id="e1690-104">xlfRegisterId</span></span>

<span data-ttu-id="e1690-105">**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="e1690-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="e1690-106">Se pueden llamar desde un archivo DLL que se ha llamado propio por Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="e1690-106">Can be called from a DLL that has itself been called by Microsoft Excel.</span></span> <span data-ttu-id="e1690-107">Si una función ya está registrada, devuelve el identificador de registro existente para esa función sin volver a registrarlo.</span><span class="sxs-lookup"><span data-stu-id="e1690-107">If a function is already registered, it returns the existing register ID for that function without reregistering it.</span></span> <span data-ttu-id="e1690-108">Si una función aún no esté registrada, registra y devuelve el identificador del registro resultante.</span><span class="sxs-lookup"><span data-stu-id="e1690-108">If a function is not yet registered, it registers it and returns the resulting register ID.</span></span>
  
```cs
Excel12(xlfRegisterId, LPXLOPER12 pxRes, 3,     LPXLOPER12 pxModuleText, LPXLOPER12 pxProcedure, LPXLOPER12 pxTypeText);
```

## <a name="parameters"></a><span data-ttu-id="e1690-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e1690-109">Parameters</span></span>

<span data-ttu-id="e1690-110">_pxModuleText_ (**xltypeStr**)</span><span class="sxs-lookup"><span data-stu-id="e1690-110">_pxModuleText_ (**xltypeStr**)</span></span>
  
<span data-ttu-id="e1690-111">El nombre del archivo DLL que contiene la función.</span><span class="sxs-lookup"><span data-stu-id="e1690-111">The name of the DLL containing the function.</span></span>
  
<span data-ttu-id="e1690-112">_pxProcedure_ (**xltypeStr** o **xltypeNum**)</span><span class="sxs-lookup"><span data-stu-id="e1690-112">_pxProcedure_ (**xltypeStr** or **xltypeNum**)</span></span>
  
<span data-ttu-id="e1690-113">Si hay una cadena, el nombre de la función que se llama.</span><span class="sxs-lookup"><span data-stu-id="e1690-113">If a string, the name of the function to call.</span></span> <span data-ttu-id="e1690-114">Si un número, el ordinal exportar el número de la función que se llama.</span><span class="sxs-lookup"><span data-stu-id="e1690-114">If a number, the ordinal export number of the function to call.</span></span> <span data-ttu-id="e1690-115">Para mayor claridad y solidez, use siempre el formato de cadena.</span><span class="sxs-lookup"><span data-stu-id="e1690-115">For clarity and robustness, always use the string form.</span></span>
  
<span data-ttu-id="e1690-116">_pxTypeText_ (**xltypeStr**)</span><span class="sxs-lookup"><span data-stu-id="e1690-116">_pxTypeText_ (**xltypeStr**)</span></span>
  
<span data-ttu-id="e1690-117">Una cadena opcional que especifica los tipos de todos los argumentos a la función y el tipo del valor devuelto de la función.</span><span class="sxs-lookup"><span data-stu-id="e1690-117">An optional string specifying the types of all the arguments to the function and the type of the return value of the function.</span></span> <span data-ttu-id="e1690-118">Para obtener más información, vea la sección "Comentarios".</span><span class="sxs-lookup"><span data-stu-id="e1690-118">For more information, see the "Remarks" section.</span></span> <span data-ttu-id="e1690-119">Este argumento puede omitirse para un archivo DLL independiente (XLL) definición **xlAutoRegister**.</span><span class="sxs-lookup"><span data-stu-id="e1690-119">This argument can be omitted for a stand-alone DLL (XLL) defining **xlAutoRegister**.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="e1690-120">Valor de la propiedad/valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e1690-120">Property value/Return value</span></span>

<span data-ttu-id="e1690-121">Devuelve el identificador de registro de la función (**xltypeNum**), que se puede utilizar en las llamadas subsiguientes a **xlfUnregister**.</span><span class="sxs-lookup"><span data-stu-id="e1690-121">Returns the register ID of the function (**xltypeNum**), which can be used in subsequent calls to **xlfUnregister**.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="e1690-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e1690-122">Remarks</span></span>

<span data-ttu-id="e1690-123">Esta función es útil cuando no desea preocuparse de mantener un identificador de registro, pero necesita una más adelante para anular el registro.</span><span class="sxs-lookup"><span data-stu-id="e1690-123">This function is useful when you do not want to worry about maintaining a register ID, but you need one later for unregistering.</span></span> <span data-ttu-id="e1690-124">También es útil para asignar a los menús, herramientas y los botones cuando la función que desea asignar está en un archivo DLL.</span><span class="sxs-lookup"><span data-stu-id="e1690-124">It is also useful for assigning to menus, tools, and buttons when the function you want to assign is in a DLL.</span></span>
  
<span data-ttu-id="e1690-125">Cuando una función DLL o XLL se ha registrado con un argumento válido _pxFunctionText_ tener ha proporcionado para **xlfRegister**, su identificador de registro también puede obtenerse pasando el _pxFunctionText_ a la función **xlfEvaluate**.</span><span class="sxs-lookup"><span data-stu-id="e1690-125">Where a DLL or XLL function has been registered with a valid  _pxFunctionText_ argument having been supplied to **xlfRegister**, its register ID can also be obtained by passing the  _pxFunctionText_ to the function **xlfEvaluate**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="e1690-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="e1690-126">See also</span></span>

- [<span data-ttu-id="e1690-127">REGISTRAR</span><span class="sxs-lookup"><span data-stu-id="e1690-127">REGISTER</span></span>](xlfregister-form-1.md)
- [<span data-ttu-id="e1690-128">ANULAR EL REGISTRO</span><span class="sxs-lookup"><span data-stu-id="e1690-128">UNREGISTER</span></span>](xlfunregister-form-1.md)
- [<span data-ttu-id="e1690-129">Funciones esenciales y útiles XLM de API de C</span><span class="sxs-lookup"><span data-stu-id="e1690-129">Essential and Useful C API XLM Functions</span></span>](essential-and-useful-c-api-xlm-functions.md)

