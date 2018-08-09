---
title: RUNMACRO (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033809
localization_priority: Normal
ms.assetid: 86b0f071-5e0b-56de-ff5b-63c114ad823a
description: Llama a una macro de Microsoft Visual Basic para el proyecto de aplicaciones (VBA).
ms.openlocfilehash: e3dd989956ce9c5f795ae3ef0d8535ab2776d6d7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823094"
---
# <a name="runmacro-function"></a><span data-ttu-id="0a274-103">Función RUNMACRO</span><span class="sxs-lookup"><span data-stu-id="0a274-103">RUNMACRO Function</span></span>

<span data-ttu-id="0a274-104">Llama a una macro de Microsoft Visual Basic para el proyecto de aplicaciones (VBA).</span><span class="sxs-lookup"><span data-stu-id="0a274-104">Calls a macro in a Microsoft Visual Basic for Applications (VBA) project.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="0a274-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0a274-105">Syntax</span></span>

<span data-ttu-id="0a274-106">RUNMACRO (** *macroname* ** [, ** *nombreproy_opc* **])</span><span class="sxs-lookup"><span data-stu-id="0a274-106">RUNMACRO (** *macroname* ** [, ** *projname_opt* ** ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="0a274-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0a274-107">Parameters</span></span>

|<span data-ttu-id="0a274-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="0a274-108">**Name**</span></span>|<span data-ttu-id="0a274-109">**Obligatorio/opcional**</span><span class="sxs-lookup"><span data-stu-id="0a274-109">**Required/Optional**</span></span>|<span data-ttu-id="0a274-110">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="0a274-110">**Data Type**</span></span>|<span data-ttu-id="0a274-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="0a274-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="0a274-112">_macroname_</span><span class="sxs-lookup"><span data-stu-id="0a274-112">_macroname_</span></span> <br/> |<span data-ttu-id="0a274-113">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="0a274-113">Required</span></span>  <br/> |<span data-ttu-id="0a274-114">**String**</span><span class="sxs-lookup"><span data-stu-id="0a274-114">**String**</span></span> <br/> |<span data-ttu-id="0a274-115">Nombre de la macro por llamar.</span><span class="sxs-lookup"><span data-stu-id="0a274-115">The name of the macro to call.</span></span>  <br/> |
| <span data-ttu-id="0a274-116">_nombreproy_opc_</span><span class="sxs-lookup"><span data-stu-id="0a274-116">_projname_opt_</span></span> <br/> |<span data-ttu-id="0a274-117">Opcional</span><span class="sxs-lookup"><span data-stu-id="0a274-117">Optional</span></span>  <br/> |<span data-ttu-id="0a274-118">**String**</span><span class="sxs-lookup"><span data-stu-id="0a274-118">**String**</span></span> <br/> | <span data-ttu-id="0a274-119">Proyecto que contiene la macro.</span><span class="sxs-lookup"><span data-stu-id="0a274-119">The project that contains the macro.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0a274-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0a274-120">Remarks</span></span>

<span data-ttu-id="0a274-121">Si se especifica un proyecto, Microsoft Visio busca en todos los documentos abiertos para el uno que contiene _nombreproy_opc_ y llamadas _macroname_ en ese proyecto.</span><span class="sxs-lookup"><span data-stu-id="0a274-121">If a project is specified, Microsoft Visio scans all open documents for the one containing  _projname_opt_ and calls  _macroname_ in that project.</span></span> <span data-ttu-id="0a274-122">Si _nombreproy_opc_ se omite o es null (""), _macroname_ se supone que en el proyecto de VBA del documento que contiene la fórmula RUNMACRO que se está evaluando.</span><span class="sxs-lookup"><span data-stu-id="0a274-122">If  _projname_opt_ is omitted or null (""),  _macroname_ is assumed to be in the VBA project of the document that contains the RUNMACRO formula being evaluated.</span></span> 
  
<span data-ttu-id="0a274-123">La función RUNMACRO difiere de la función CALLTHIS en que no pasa una referencia a la forma propietaria de la fórmula que se evalúa para _macroname_.</span><span class="sxs-lookup"><span data-stu-id="0a274-123">The RUNMACRO function differs from the CALLTHIS function in that it does not pass a reference to the shape that owns the formula being evaluated to  _macroname_.</span></span> <span data-ttu-id="0a274-124">Al igual que CALLTHIS, la función RUNMACRO no requiere una referencia a _nombreproy_opc_ para que llamen a él.</span><span class="sxs-lookup"><span data-stu-id="0a274-124">Like CALLTHIS, the RUNMACRO function doesn't require a reference to  _projname_opt_ to call into it.</span></span> 
  
 <span data-ttu-id="0a274-125">El código VBA que se invoca cuando una copia de Visio evalúa una función RUNMACRO que forma parte de una fórmula no debe cerrar el documento que contiene la celda que utiliza la función, ya que, de hacerlo, se producirá un error de aplicación y la ejecución de Visio se terminará.</span><span class="sxs-lookup"><span data-stu-id="0a274-125">VBA code that is invoked when the Visio instance evaluates a RUNMACRO function in a formula should not close the document containing the cell using the function because an application error results and Visio terminates.</span></span> 
  
<span data-ttu-id="0a274-126">Si necesita cerrar el documento que contiene la celda que usa la función RUNMACRO, puede usar uno de los métodos siguientes:</span><span class="sxs-lookup"><span data-stu-id="0a274-126">If you need to close the document containing the cell that uses the RUNMACRO function, use one of the following techniques:</span></span>
  
- <span data-ttu-id="0a274-127">Cerrar el documento mediante código que no sea de VBA.</span><span class="sxs-lookup"><span data-stu-id="0a274-127">Close the document from code that is not VBA.</span></span>
    
- <span data-ttu-id="0a274-128">Cerrar el documento desde un proyecto diferente al que se cierra.</span><span class="sxs-lookup"><span data-stu-id="0a274-128">Close the document from a project other than the one that is closing.</span></span>
    
- <span data-ttu-id="0a274-129">Enviar mensajes de ventana para cerrar las ventanas del documento en lugar de cerrar el documento.</span><span class="sxs-lookup"><span data-stu-id="0a274-129">Post window messages to close windows in the document rather than closing the document.</span></span>
    
<span data-ttu-id="0a274-130">Para obtener más información acerca cómo ejecutar código en Visio, vea [Acerca de la configuración de seguridad y la ejecución de código en Visio](about-security-settings-and-running-code-in-visio-shapesheet.md) en esta Referencia de ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="0a274-130">For more information about running code in Visio, see [About security settings and running code in Visio](about-security-settings-and-running-code-in-visio-shapesheet.md) in this ShapeSheet Reference.</span></span> 
  
## <a name="example"></a><span data-ttu-id="0a274-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="0a274-131">Example</span></span>

<span data-ttu-id="0a274-132">En el ejemplo siguiente, se invoca una macro llamada MiPrueba en el módulo de clase ThisDocument del proyecto VBA que contiene la fórmula RUNMACRO.</span><span class="sxs-lookup"><span data-stu-id="0a274-132">The following example invokes a macro called MyTest in the ThisDocument class module of the VBA project containing the RUNMACRO formula.</span></span> 
  
<span data-ttu-id="0a274-133">RUNMACRO ("ThisDocument.MiPrueba")</span><span class="sxs-lookup"><span data-stu-id="0a274-133">RUNMACRO ("ThisDocument.MyTest")</span></span> 
  

