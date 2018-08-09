---
title: Funciones esenciales y útiles XLM de API de C
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- funciones [excel 2007], xlm de api c
localization_priority: Normal
ms.assetid: dc80cb3d-0d7e-4cb9-9870-3acc84eeca82
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 410a6009bf6bbb8146dcc1354e7f5688c28d96c6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815547"
---
# <a name="essential-and-useful-c-api-xlm-functions"></a><span data-ttu-id="a8dc6-104">Funciones esenciales y útiles XLM de API de C</span><span class="sxs-lookup"><span data-stu-id="a8dc6-104">Essential and Useful C API XLM Functions</span></span>

 <span data-ttu-id="a8dc6-105">**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="a8dc6-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="a8dc6-106">Las funciones que se describen en esta sección son funciones de devolución de llamada de Microsoft Excel que son especialmente útiles para los desarrolladores de XLL y DLL.</span><span class="sxs-lookup"><span data-stu-id="a8dc6-106">The functions described in this section are Microsoft Excel callback functions that are particularly useful to DLL and XLL developers.</span></span> <span data-ttu-id="a8dc6-107">De éstos, la función **xlfRegister** es esencial para XLL y los archivos DLL que va a registrar sus funciones y comandos de modo que se les pueden llamar directamente desde Excel.</span><span class="sxs-lookup"><span data-stu-id="a8dc6-107">Of these, the **xlfRegister** function is essential for XLLs and DLLs that want to register their functions and commands so that they can be called directly from Excel.</span></span> <span data-ttu-id="a8dc6-108">Las funciones **xlfUnregister** y **xlfSetName** se usan en combinación para anular el registro de comandos y funciones DLL y XLL.</span><span class="sxs-lookup"><span data-stu-id="a8dc6-108">The functions **xlfUnregister** and **xlfSetName** are used in combination to unregister DLL and XLL functions and commands.</span></span> 
  
<span data-ttu-id="a8dc6-109">Muchas más funciones se exponen con Excel a través de la API de C que son útiles cuando está desarrollando XLL.</span><span class="sxs-lookup"><span data-stu-id="a8dc6-109">Many more functions are exposed by Excel via the C API that are useful when you are developing XLLs.</span></span> <span data-ttu-id="a8dc6-110">Se corresponden con la hoja de cálculo de Excel funciones y funciones y comandos que están disponibles en hojas de macro XLM.</span><span class="sxs-lookup"><span data-stu-id="a8dc6-110">They correspond to the Excel worksheet functions and functions and commands that are available from XLM macro sheets.</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="a8dc6-111">En esta sección</span><span class="sxs-lookup"><span data-stu-id="a8dc6-111">In this section</span></span>

[<span data-ttu-id="a8dc6-112">xlfCaller</span><span class="sxs-lookup"><span data-stu-id="a8dc6-112">xlfCaller</span></span>](xlfcaller.md)
  
[<span data-ttu-id="a8dc6-113">xlfEvaluate</span><span class="sxs-lookup"><span data-stu-id="a8dc6-113">xlfEvaluate</span></span>](xlfevaluate.md)
  
[<span data-ttu-id="a8dc6-114">xlfGetDef</span><span class="sxs-lookup"><span data-stu-id="a8dc6-114">xlfGetDef</span></span>](xlfgetdef.md)
  
[<span data-ttu-id="a8dc6-115">xlfGetName</span><span class="sxs-lookup"><span data-stu-id="a8dc6-115">xlfGetName</span></span>](xlfgetname.md)
  
[<span data-ttu-id="a8dc6-116">xlfRegister (Formulario 1)</span><span class="sxs-lookup"><span data-stu-id="a8dc6-116">xlfRegister (Form 1)</span></span>](xlfregister-form-1.md)
  
[<span data-ttu-id="a8dc6-117">xlfRegister (Formulario 2)</span><span class="sxs-lookup"><span data-stu-id="a8dc6-117">xlfRegister (Form 2)</span></span>](xlfregister-form-2.md)
  
[<span data-ttu-id="a8dc6-118">xlfRegisterId</span><span class="sxs-lookup"><span data-stu-id="a8dc6-118">xlfRegisterId</span></span>](xlfregisterid.md)
  
[<span data-ttu-id="a8dc6-119">xlfUnregister (Formulario 1)</span><span class="sxs-lookup"><span data-stu-id="a8dc6-119">xlfUnregister (Form 1)</span></span>](xlfunregister-form-1.md)
  
[<span data-ttu-id="a8dc6-120">xlfUnregister (Formulario 2)</span><span class="sxs-lookup"><span data-stu-id="a8dc6-120">xlfUnregister (Form 2)</span></span>](xlfunregister-form-2.md)
  
[<span data-ttu-id="a8dc6-121">xlfSetName</span><span class="sxs-lookup"><span data-stu-id="a8dc6-121">xlfSetName</span></span>](xlfsetname.md)
  

