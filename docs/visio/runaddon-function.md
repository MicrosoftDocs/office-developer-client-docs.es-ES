---
title: RUNADDON (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251492
localization_priority: Normal
ms.assetid: 122c1d30-3cb9-7e7d-b4cc-e93ab8e4da4f
description: Ejecuta un complemento o una macro en un Microsoft proyecto Visual Basic para aplicaciones (VBA).
ms.openlocfilehash: 31ac32c742827311d8aaee4547024ad97d2c48e8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823097"
---
# <a name="runaddon-function"></a><span data-ttu-id="7b8b8-103">Función RUNADDON</span><span class="sxs-lookup"><span data-stu-id="7b8b8-103">RUNADDON Function</span></span>

<span data-ttu-id="7b8b8-104">Ejecuta un complemento o una macro en un Microsoft proyecto Visual Basic para aplicaciones (VBA).</span><span class="sxs-lookup"><span data-stu-id="7b8b8-104">Executes an add-on or a macro in a Microsoft Visual Basic for Applications (VBA) project.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="7b8b8-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7b8b8-105">Syntax</span></span>

<span data-ttu-id="7b8b8-106">RUNADDON (" *cadena* ")</span><span class="sxs-lookup"><span data-stu-id="7b8b8-106">RUNADDON(" *string*  ")</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="7b8b8-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7b8b8-107">Parameters</span></span>

|<span data-ttu-id="7b8b8-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="7b8b8-108">**Name**</span></span>|<span data-ttu-id="7b8b8-109">**Obligatorio/opcional**</span><span class="sxs-lookup"><span data-stu-id="7b8b8-109">**Required/Optional**</span></span>|<span data-ttu-id="7b8b8-110">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="7b8b8-110">**Data Type**</span></span>|<span data-ttu-id="7b8b8-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="7b8b8-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="7b8b8-112">_string_</span><span class="sxs-lookup"><span data-stu-id="7b8b8-112">_string_</span></span> <br/> |<span data-ttu-id="7b8b8-113">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="7b8b8-113">Required</span></span>  <br/> |<span data-ttu-id="7b8b8-114">**String**</span><span class="sxs-lookup"><span data-stu-id="7b8b8-114">**String**</span></span> <br/> | <span data-ttu-id="7b8b8-115">Nombre de un complemento de la colección **Addons** o de una macro de un proyecto VBA.</span><span class="sxs-lookup"><span data-stu-id="7b8b8-115">The name of an add-on in the **Addons** collection or a macro in a VBA project.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7b8b8-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="7b8b8-116">Remarks</span></span>

<span data-ttu-id="7b8b8-117">Si el proyecto del documento que contiene la llamada a la función RUNADDON (u otro proyecto, si se hace referencia a) no tiene una macro (un procedimiento sin argumentos) denominada _cadena_, Microsoft Visio se ejecuta el complemento llamado _cadena_.</span><span class="sxs-lookup"><span data-stu-id="7b8b8-117">If the project of the document that contains the RUNADDON function call (or another project if it is referenced) does not have a macro (a procedure with no arguments) named  _string_, Microsoft Visio runs the add-on named  _string_.</span></span> <span data-ttu-id="7b8b8-118">Si no se encuentra ningún complemento denominado _cadena_ , Visio no realiza ninguna acción y devuelve ningún error.</span><span class="sxs-lookup"><span data-stu-id="7b8b8-118">If no add-on named  _string_ can be found, Visio does nothing and reports no error.</span></span> <span data-ttu-id="7b8b8-119">(Puede usar la propiedad **TraceFlags** para supervisar los procedimientos y complementos que intente ejecutar Visio).</span><span class="sxs-lookup"><span data-stu-id="7b8b8-119">(You can use the **TraceFlags** property to monitor the procedures and add-ons that Visio attempts to run.)</span></span> 
  
<span data-ttu-id="7b8b8-120">Cuando se llama a un procedimiento en un módulo estándar, se recomienda anteponer a la cadena con el nombre del módulo que contiene el procedimiento (por ejemplo, *nombreMódulo.nombreProc*), debido a que más de un módulo puede tener un procedimiento con el mismo nombre.</span><span class="sxs-lookup"><span data-stu-id="7b8b8-120">When you call a procedure in a standard module, it is recommended that you prefix the string with the module name that contains the procedure (for example,  *moduleName.procName*), because more than one module can have a procedure with the same name.</span></span> 
  
<span data-ttu-id="7b8b8-121">Para llamar a un procedimiento en un proyecto que no sea el proyecto del documento que contiene la llamada a la función RUNADDON, utilice la sintaxis *nombreProy.nombreMód.nombreProc* (es necesario haber establecido explícitamente una referencia a *projName* en el proyecto de VBA).</span><span class="sxs-lookup"><span data-stu-id="7b8b8-121">To call a procedure in a project other than the project of the document that contains the RUNADDON function call, use the syntax  *projName.modName.procName*  (you must have explicitly set a reference to  *projName*  in your VBA project).</span></span> 
  
> [!NOTE]
>  <span data-ttu-id="7b8b8-p102">A partir de Visio 2002, la función RUNADDON no es capaz de ejecutar una cadena que contenga código VBA arbitrario. El código pasado anteriormente a la función RUNADDON se puede mover a un procedimiento de un proyecto VBA de un documento, llamado desde la función RUNADDON.</span><span class="sxs-lookup"><span data-stu-id="7b8b8-p102">Beginning with Visio 2002, the RUNADDON function cannot execute a string containing arbitrary VBA code. Code that was formerly passed to the RUNADDON function can be moved to a procedure in a document's VBA project that is called from the RUNADDON function.</span></span> 
  
<span data-ttu-id="7b8b8-124">Para obtener más información acerca de cómo ejecutar código en Visio, vea [Acerca de la configuración de seguridad y la ejecución de código en Visio](about-security-settings-and-running-code-in-visio-shapesheet.md) en esta Referencia de ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="7b8b8-124">For more information about running code in Visio, see [About Security Settings and Running Code in Visio](about-security-settings-and-running-code-in-visio-shapesheet.md) in this ShapeSheet Reference.</span></span> 
  
<span data-ttu-id="7b8b8-p103">En versiones anteriores de Visio, esta función se denominaba _RUNADDON. La versión 4.0 de Visio y las posteriores aceptan cualquiera de las dos denominaciones.</span><span class="sxs-lookup"><span data-stu-id="7b8b8-p103">In earlier versions of Visio, this function appears as _RUNADDON. Visio versions 4.0 and later accept either style.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="7b8b8-127">Ejemplo 1</span><span class="sxs-lookup"><span data-stu-id="7b8b8-127">Example 1</span></span>

<span data-ttu-id="7b8b8-128">RUNADDON("Calendar.exe")</span><span class="sxs-lookup"><span data-stu-id="7b8b8-128">RUNADDON("Calendar.exe")</span></span>
  
<span data-ttu-id="7b8b8-129">Inicia un complemento llamado Calendar.exe.</span><span class="sxs-lookup"><span data-stu-id="7b8b8-129">Launches an add-on called Calendar.exe.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="7b8b8-130">Ejemplo 2</span><span class="sxs-lookup"><span data-stu-id="7b8b8-130">Example 2</span></span>

<span data-ttu-id="7b8b8-131">RUNADDON("Colocar formas en matriz")</span><span class="sxs-lookup"><span data-stu-id="7b8b8-131">RUNADDON("Array Shapes")</span></span>
  
<span data-ttu-id="7b8b8-132">Inicia el complemento (implementado por VSL) denominado Colocar formas en matriz.</span><span class="sxs-lookup"><span data-stu-id="7b8b8-132">Launches the (VSL-implemented) add-on whose name is Array Shapes.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="7b8b8-133">Ejemplo 3</span><span class="sxs-lookup"><span data-stu-id="7b8b8-133">Example 3</span></span>

<span data-ttu-id="7b8b8-134">RUNADDON("ThisDocument.ReportStatistics")</span><span class="sxs-lookup"><span data-stu-id="7b8b8-134">RUNADDON("ThisDocument.ReportStatistics")</span></span>
  
<span data-ttu-id="7b8b8-135">Llama a la macro ReportStatistics del módulo **ThisDocument** en el proyecto del documento que contiene esta llamada a función.</span><span class="sxs-lookup"><span data-stu-id="7b8b8-135">Calls the ReportStatistics macro in the **ThisDocument** module in the document project containing this function call.</span></span> 
  
> [!NOTE]
>  <span data-ttu-id="7b8b8-136">Para invocar una macro del módulo **ThisDocument**, es preciso anteponer "ThisDocument" a la cadena, como muestra el ejemplo.</span><span class="sxs-lookup"><span data-stu-id="7b8b8-136">To invoke a macro in the **ThisDocument** module, you must preface the string with "ThisDocument" as shown.</span></span> 
  
## <a name="example-4"></a><span data-ttu-id="7b8b8-137">Ejemplo 4</span><span class="sxs-lookup"><span data-stu-id="7b8b8-137">Example 4</span></span>

<span data-ttu-id="7b8b8-138">RUNADDON (" *NombreMódulo* . ReportStatistics")</span><span class="sxs-lookup"><span data-stu-id="7b8b8-138">RUNADDON(" *ModuleName*  .ReportStatistics")</span></span> 
  
<span data-ttu-id="7b8b8-139">Llama a la macro ReportStatistics de *NombreMódulo* en el proyecto del documento que contiene esta llamada a función.</span><span class="sxs-lookup"><span data-stu-id="7b8b8-139">Calls the ReportStatistics macro in  *ModuleName*  in the document project that contains this function call.</span></span> 
  

