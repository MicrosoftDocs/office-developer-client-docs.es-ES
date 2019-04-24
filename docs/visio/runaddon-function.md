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
description: Ejecuta un complemento o una macro en un proyecto de Microsoft Visual Basic para aplicaciones (VBA).
ms.openlocfilehash: 280f6eaf1e5db045d8c1d22965df00960d188112
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32319064"
---
# <a name="runaddon-function"></a><span data-ttu-id="8a0e7-103">Función RUNADDON</span><span class="sxs-lookup"><span data-stu-id="8a0e7-103">RUNADDON Function</span></span>

<span data-ttu-id="8a0e7-104">Ejecuta un complemento o una macro en un proyecto de Microsoft Visual Basic para aplicaciones (VBA).</span><span class="sxs-lookup"><span data-stu-id="8a0e7-104">Executes an add-on or a macro in a Microsoft Visual Basic for Applications (VBA) project.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="8a0e7-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8a0e7-105">Syntax</span></span>

<span data-ttu-id="8a0e7-106">RUNADDON (" *cadena* ")</span><span class="sxs-lookup"><span data-stu-id="8a0e7-106">RUNADDON(" *string*  ")</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="8a0e7-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8a0e7-107">Parameters</span></span>

|<span data-ttu-id="8a0e7-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="8a0e7-108">**Name**</span></span>|<span data-ttu-id="8a0e7-109">**Necesario/Opcional**</span><span class="sxs-lookup"><span data-stu-id="8a0e7-109">**Required/Optional**</span></span>|<span data-ttu-id="8a0e7-110">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="8a0e7-110">**Data Type**</span></span>|<span data-ttu-id="8a0e7-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="8a0e7-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="8a0e7-112">_string_</span><span class="sxs-lookup"><span data-stu-id="8a0e7-112">_string_</span></span> <br/> |<span data-ttu-id="8a0e7-113">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="8a0e7-113">Required</span></span>  <br/> |<span data-ttu-id="8a0e7-114">**String**</span><span class="sxs-lookup"><span data-stu-id="8a0e7-114">**String**</span></span> <br/> | <span data-ttu-id="8a0e7-115">Nombre de un complemento de la colección **Addons** o de una macro de un proyecto VBA.</span><span class="sxs-lookup"><span data-stu-id="8a0e7-115">The name of an add-on in the **Addons** collection or a macro in a VBA project.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8a0e7-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="8a0e7-116">Remarks</span></span>

<span data-ttu-id="8a0e7-117">Si el proyecto del documento que contiene la llamada a la función RUNADDON (u otro proyecto, si se hace referencia a él) no tiene una macro (un procedimiento sin argumentos) llamada _String_, Microsoft Visio ejecuta el complemento denominado _String_.</span><span class="sxs-lookup"><span data-stu-id="8a0e7-117">If the project of the document that contains the RUNADDON function call (or another project if it is referenced) does not have a macro (a procedure with no arguments) named  _string_, Microsoft Visio runs the add-on named  _string_.</span></span> <span data-ttu-id="8a0e7-118">Si no se encuentra ningún complemento denominado _cadena_ , Visio no realiza ninguna acción y no informa de ningún error.</span><span class="sxs-lookup"><span data-stu-id="8a0e7-118">If no add-on named  _string_ can be found, Visio does nothing and reports no error.</span></span> <span data-ttu-id="8a0e7-119">(Puede usar la propiedad **TraceFlags** para supervisar los procedimientos y complementos que intente ejecutar Visio).</span><span class="sxs-lookup"><span data-stu-id="8a0e7-119">(You can use the **TraceFlags** property to monitor the procedures and add-ons that Visio attempts to run.)</span></span> 
  
<span data-ttu-id="8a0e7-120">Cuando se llama a un procedimiento en un módulo estándar, se recomienda anteponer a la cadena el nombre del módulo que contiene el procedimiento (por ejemplo, *nombreMódulo. NombreProc*), ya que puede haber más de un procedimiento con el mismo nombre en un mismo módulo.</span><span class="sxs-lookup"><span data-stu-id="8a0e7-120">When you call a procedure in a standard module, it is recommended that you prefix the string with the module name that contains the procedure (for example,  *moduleName.procName*), because more than one module can have a procedure with the same name.</span></span> 
  
<span data-ttu-id="8a0e7-121">Para llamar a un procedimiento en un proyecto distinto del proyecto del documento que contiene la llamada a la función RUNADDON, utilice la sintaxis *nombreproy. nombremód. procName* (debe haber establecido explícitamente una referencia a *nombreproy* en el proyecto de VBA).</span><span class="sxs-lookup"><span data-stu-id="8a0e7-121">To call a procedure in a project other than the project of the document that contains the RUNADDON function call, use the syntax  *projName.modName.procName*  (you must have explicitly set a reference to  *projName*  in your VBA project).</span></span> 
  
> [!NOTE]
>  <span data-ttu-id="8a0e7-p102">A partir de Visio 2002, la función RUNADDON no es capaz de ejecutar una cadena que contenga código VBA arbitrario. El código pasado anteriormente a la función RUNADDON se puede mover a un procedimiento de un proyecto VBA de un documento, llamado desde la función RUNADDON.</span><span class="sxs-lookup"><span data-stu-id="8a0e7-p102">Beginning with Visio 2002, the RUNADDON function cannot execute a string containing arbitrary VBA code. Code that was formerly passed to the RUNADDON function can be moved to a procedure in a document's VBA project that is called from the RUNADDON function.</span></span> 
  
<span data-ttu-id="8a0e7-124">Para obtener más información acerca de cómo ejecutar código en Visio, vea [Acerca de la configuración de seguridad y la ejecución de código en Visio](about-security-settings-and-running-code-in-visio-shapesheet.md) en esta Referencia de ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="8a0e7-124">For more information about running code in Visio, see [About Security Settings and Running Code in Visio](about-security-settings-and-running-code-in-visio-shapesheet.md) in this ShapeSheet Reference.</span></span> 
  
<span data-ttu-id="8a0e7-p103">En versiones anteriores de Visio, esta función se denominaba _RUNADDON. La versión 4.0 de Visio y las posteriores aceptan cualquiera de las dos denominaciones.</span><span class="sxs-lookup"><span data-stu-id="8a0e7-p103">In earlier versions of Visio, this function appears as _RUNADDON. Visio versions 4.0 and later accept either style.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="8a0e7-127">Ejemplo 1</span><span class="sxs-lookup"><span data-stu-id="8a0e7-127">Example 1</span></span>

<span data-ttu-id="8a0e7-128">RUNADDON ("calendario. exe")</span><span class="sxs-lookup"><span data-stu-id="8a0e7-128">RUNADDON("Calendar.exe")</span></span>
  
<span data-ttu-id="8a0e7-129">Inicia un complemento denominado Calendar. exe.</span><span class="sxs-lookup"><span data-stu-id="8a0e7-129">Launches an add-on called Calendar.exe.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="8a0e7-130">Ejemplo 2</span><span class="sxs-lookup"><span data-stu-id="8a0e7-130">Example 2</span></span>

<span data-ttu-id="8a0e7-131">RUNADDON("Colocar formas en matriz")</span><span class="sxs-lookup"><span data-stu-id="8a0e7-131">RUNADDON("Array Shapes")</span></span>
  
<span data-ttu-id="8a0e7-132">Inicia el complemento (implementado por VSL) denominado Colocar formas en matriz.</span><span class="sxs-lookup"><span data-stu-id="8a0e7-132">Launches the (VSL-implemented) add-on whose name is Array Shapes.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="8a0e7-133">Ejemplo 3</span><span class="sxs-lookup"><span data-stu-id="8a0e7-133">Example 3</span></span>

<span data-ttu-id="8a0e7-134">RUNADDON ("ThisDocument. ReportStatistics")</span><span class="sxs-lookup"><span data-stu-id="8a0e7-134">RUNADDON("ThisDocument.ReportStatistics")</span></span>
  
<span data-ttu-id="8a0e7-135">Llama a la macro ReportStatistics del módulo **ThisDocument** en el proyecto del documento que contiene esta llamada a función.</span><span class="sxs-lookup"><span data-stu-id="8a0e7-135">Calls the ReportStatistics macro in the **ThisDocument** module in the document project containing this function call.</span></span> 
  
> [!NOTE]
>  <span data-ttu-id="8a0e7-136">Para invocar una macro del módulo **ThisDocument**, es preciso anteponer "ThisDocument" a la cadena, como muestra el ejemplo.</span><span class="sxs-lookup"><span data-stu-id="8a0e7-136">To invoke a macro in the **ThisDocument** module, you must preface the string with "ThisDocument" as shown.</span></span> 
  
## <a name="example-4"></a><span data-ttu-id="8a0e7-137">Ejemplo 4</span><span class="sxs-lookup"><span data-stu-id="8a0e7-137">Example 4</span></span>

<span data-ttu-id="8a0e7-138">RUNADDON (" *ModuleName* . ReportStatistics ")</span><span class="sxs-lookup"><span data-stu-id="8a0e7-138">RUNADDON(" *ModuleName*  .ReportStatistics")</span></span> 
  
<span data-ttu-id="8a0e7-139">Llama a la macro ReportStatistics en *ModuleName* en el proyecto de documento que contiene esta llamada a la función.</span><span class="sxs-lookup"><span data-stu-id="8a0e7-139">Calls the ReportStatistics macro in  *ModuleName*  in the document project that contains this function call.</span></span> 
  

