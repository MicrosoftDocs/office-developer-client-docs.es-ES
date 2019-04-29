---
title: xlfRegisterId
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlfRegisterId
keywords:
- función xlfregisterid [Excel 2007]
localization_priority: Normal
ms.assetid: d34cf20c-a5cd-45fb-9dcb-d49eac2d99dd
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 05119226d0b6190a2c4b30846c03a59b5c3cd1d8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420062"
---
# <a name="xlfregisterid"></a><span data-ttu-id="423bd-104">xlfRegisterId</span><span class="sxs-lookup"><span data-stu-id="423bd-104">xlfRegisterId</span></span>

<span data-ttu-id="423bd-105">**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="423bd-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="423bd-106">Se puede llamar desde una DLL que ha sido llamada por Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="423bd-106">Can be called from a DLL that has itself been called by Microsoft Excel.</span></span> <span data-ttu-id="423bd-107">Si una función ya está registrada, devuelve el identificador de registro existente para esa función sin volver a registrarla.</span><span class="sxs-lookup"><span data-stu-id="423bd-107">If a function is already registered, it returns the existing register ID for that function without reregistering it.</span></span> <span data-ttu-id="423bd-108">Si una función todavía no está registrada, se registra y se devuelve el identificador de registro resultante.</span><span class="sxs-lookup"><span data-stu-id="423bd-108">If a function is not yet registered, it registers it and returns the resulting register ID.</span></span>
  
```cs
Excel12(xlfRegisterId, LPXLOPER12 pxRes, 3,     LPXLOPER12 pxModuleText, LPXLOPER12 pxProcedure, LPXLOPER12 pxTypeText);
```

## <a name="parameters"></a><span data-ttu-id="423bd-109">Parameters</span><span class="sxs-lookup"><span data-stu-id="423bd-109">Parameters</span></span>

<span data-ttu-id="423bd-110">_pxModuleText_ (**xltypeStr**)</span><span class="sxs-lookup"><span data-stu-id="423bd-110">_pxModuleText_ (**xltypeStr**)</span></span>
  
<span data-ttu-id="423bd-111">Nombre del archivo DLL que contiene la función.</span><span class="sxs-lookup"><span data-stu-id="423bd-111">The name of the DLL containing the function.</span></span>
  
<span data-ttu-id="423bd-112">_pxProcedure_ (**xltypeStr** o **xltypeNum**)</span><span class="sxs-lookup"><span data-stu-id="423bd-112">_pxProcedure_ (**xltypeStr** or **xltypeNum**)</span></span>
  
<span data-ttu-id="423bd-113">Si es una cadena, el nombre de la función a la que se llama.</span><span class="sxs-lookup"><span data-stu-id="423bd-113">If a string, the name of the function to call.</span></span> <span data-ttu-id="423bd-114">Si es un número, el número de exportación ordinal de la función que se va a llamar.</span><span class="sxs-lookup"><span data-stu-id="423bd-114">If a number, the ordinal export number of the function to call.</span></span> <span data-ttu-id="423bd-115">Para mayor claridad y solidez, use siempre el formato de cadena.</span><span class="sxs-lookup"><span data-stu-id="423bd-115">For clarity and robustness, always use the string form.</span></span>
  
<span data-ttu-id="423bd-116">_pxTypeText_ (**xltypeStr**)</span><span class="sxs-lookup"><span data-stu-id="423bd-116">_pxTypeText_ (**xltypeStr**)</span></span>
  
<span data-ttu-id="423bd-117">Una cadena opcional que especifica los tipos de todos los argumentos de la función y el tipo de valor devuelto de la función.</span><span class="sxs-lookup"><span data-stu-id="423bd-117">An optional string specifying the types of all the arguments to the function and the type of the return value of the function.</span></span> <span data-ttu-id="423bd-118">Si desea más información, vea la sección "Comentarios".</span><span class="sxs-lookup"><span data-stu-id="423bd-118">For more information, see the "Remarks" section.</span></span> <span data-ttu-id="423bd-119">Este argumento puede omitirse para una DLL independiente (XLL) que defina **xlAutoRegister**.</span><span class="sxs-lookup"><span data-stu-id="423bd-119">This argument can be omitted for a stand-alone DLL (XLL) defining **xlAutoRegister**.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="423bd-120">Valor de la propiedad/valor devuelto</span><span class="sxs-lookup"><span data-stu-id="423bd-120">Property value/Return value</span></span>

<span data-ttu-id="423bd-121">Devuelve el identificador de registro de la función (**xltypeNum**), que se puede usar en llamadas posteriores a **xlfUnregister**.</span><span class="sxs-lookup"><span data-stu-id="423bd-121">Returns the register ID of the function (**xltypeNum**), which can be used in subsequent calls to **xlfUnregister**.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="423bd-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="423bd-122">Remarks</span></span>

<span data-ttu-id="423bd-123">Esta función es útil cuando no desea preocuparse por mantener un identificador de registro, pero necesita uno más adelante para anular el registro.</span><span class="sxs-lookup"><span data-stu-id="423bd-123">This function is useful when you do not want to worry about maintaining a register ID, but you need one later for unregistering.</span></span> <span data-ttu-id="423bd-124">También es útil para asignar menús, herramientas y botones cuando la función que desea asignar está en una DLL.</span><span class="sxs-lookup"><span data-stu-id="423bd-124">It is also useful for assigning to menus, tools, and buttons when the function you want to assign is in a DLL.</span></span>
  
<span data-ttu-id="423bd-125">Cuando se ha registrado una función DLL o XLL con un argumento _pxFunctionText_ válido que se ha proporcionado a **xlfRegister**, también se puede obtener su identificador de registro pasando el _pxFunctionText_ a la función **xlfEvaluate**.</span><span class="sxs-lookup"><span data-stu-id="423bd-125">Where a DLL or XLL function has been registered with a valid  _pxFunctionText_ argument having been supplied to **xlfRegister**, its register ID can also be obtained by passing the  _pxFunctionText_ to the function **xlfEvaluate**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="423bd-126">Ver también</span><span class="sxs-lookup"><span data-stu-id="423bd-126">See also</span></span>

- [<span data-ttu-id="423bd-127">Registre</span><span class="sxs-lookup"><span data-stu-id="423bd-127">REGISTER</span></span>](xlfregister-form-1.md)
- [<span data-ttu-id="423bd-128">ANULAR el registro</span><span class="sxs-lookup"><span data-stu-id="423bd-128">UNREGISTER</span></span>](xlfunregister-form-1.md)
- [<span data-ttu-id="423bd-129">Funciones esenciales y útiles XLM de API de C</span><span class="sxs-lookup"><span data-stu-id="423bd-129">Essential and Useful C API XLM Functions</span></span>](essential-and-useful-c-api-xlm-functions.md)

