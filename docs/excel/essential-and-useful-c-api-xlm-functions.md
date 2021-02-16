---
title: Funciones XLM esenciales y útiles de la API de C
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- functions [excel 2007], c api xlm
localization_priority: Normal
ms.assetid: dc80cb3d-0d7e-4cb9-9870-3acc84eeca82
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: d6acd5bb171fb2494f2adb23584f4e7f088e1b83
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434518"
---
# <a name="essential-and-useful-c-api-xlm-functions"></a><span data-ttu-id="a9132-104">Funciones XLM esenciales y útiles de la API de C</span><span class="sxs-lookup"><span data-stu-id="a9132-104">Essential and Useful C API XLM Functions</span></span>

 <span data-ttu-id="a9132-105">**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="a9132-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="a9132-106">Las funciones descritas en esta sección son funciones de devolución de llamada de Microsoft Excel que son especialmente útiles para los desarrolladores de DLL y XLL.</span><span class="sxs-lookup"><span data-stu-id="a9132-106">The functions described in this section are Microsoft Excel callback functions that are particularly useful to DLL and XLL developers.</span></span> <span data-ttu-id="a9132-107">De estos, la función **xlfRegister** es esencial para XLL y DLL que desean registrar sus funciones y comandos para que se pueda llamar directamente desde Excel.</span><span class="sxs-lookup"><span data-stu-id="a9132-107">Of these, the **xlfRegister** function is essential for XLLs and DLLs that want to register their functions and commands so that they can be called directly from Excel.</span></span> <span data-ttu-id="a9132-108">Las funciones **xlfUnregister** y **xlfSetName** se usan en combinación para anular el registro de funciones y comandos DLL y XLL.</span><span class="sxs-lookup"><span data-stu-id="a9132-108">The functions **xlfUnregister** and **xlfSetName** are used in combination to unregister DLL and XLL functions and commands.</span></span> 
  
<span data-ttu-id="a9132-109">Excel expone muchas más funciones a través de la API de C que son útiles al desarrollar XLL.</span><span class="sxs-lookup"><span data-stu-id="a9132-109">Many more functions are exposed by Excel via the C API that are useful when you are developing XLLs.</span></span> <span data-ttu-id="a9132-110">Corresponden a las funciones de hoja de cálculo de Excel, así como a las funciones y comandos disponibles en las hojas de macros XLM.</span><span class="sxs-lookup"><span data-stu-id="a9132-110">They correspond to the Excel worksheet functions and functions and commands that are available from XLM macro sheets.</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="a9132-111">En esta sección</span><span class="sxs-lookup"><span data-stu-id="a9132-111">In this section</span></span>

[<span data-ttu-id="a9132-112">xlfCaller</span><span class="sxs-lookup"><span data-stu-id="a9132-112">xlfCaller</span></span>](xlfcaller.md)
  
[<span data-ttu-id="a9132-113">xlfEvaluate</span><span class="sxs-lookup"><span data-stu-id="a9132-113">xlfEvaluate</span></span>](xlfevaluate.md)
  
[<span data-ttu-id="a9132-114">xlfGetDef</span><span class="sxs-lookup"><span data-stu-id="a9132-114">xlfGetDef</span></span>](xlfgetdef.md)
  
[<span data-ttu-id="a9132-115">xlfGetName</span><span class="sxs-lookup"><span data-stu-id="a9132-115">xlfGetName</span></span>](xlfgetname.md)
  
[<span data-ttu-id="a9132-116">xlfRegister (Formulario 1)</span><span class="sxs-lookup"><span data-stu-id="a9132-116">xlfRegister (Form 1)</span></span>](xlfregister-form-1.md)
  
[<span data-ttu-id="a9132-117">xlfRegister (Formulario 2)</span><span class="sxs-lookup"><span data-stu-id="a9132-117">xlfRegister (Form 2)</span></span>](xlfregister-form-2.md)
  
[<span data-ttu-id="a9132-118">xlfRegisterId</span><span class="sxs-lookup"><span data-stu-id="a9132-118">xlfRegisterId</span></span>](xlfregisterid.md)
  
[<span data-ttu-id="a9132-119">xlfUnregister (Formulario 1)</span><span class="sxs-lookup"><span data-stu-id="a9132-119">xlfUnregister (Form 1)</span></span>](xlfunregister-form-1.md)
  
[<span data-ttu-id="a9132-120">xlfUnregister (Formulario 2)</span><span class="sxs-lookup"><span data-stu-id="a9132-120">xlfUnregister (Form 2)</span></span>](xlfunregister-form-2.md)
  
[<span data-ttu-id="a9132-121">xlfSetName</span><span class="sxs-lookup"><span data-stu-id="a9132-121">xlfSetName</span></span>](xlfsetname.md)
  

