---
title: CALLTHIS (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251403
localization_priority: Normal
ms.assetid: 461abfc1-d2cc-2354-1c2f-395c9e351a78
description: Llama a un procedimiento en Microsoft Visual Basic para el proyecto de aplicaciones (VBA).
ms.openlocfilehash: 04065384453e55b745daa89273fb4c23b32fb90c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19821694"
---
# <a name="callthis-function"></a><span data-ttu-id="e8490-103">Función CALLTHIS</span><span class="sxs-lookup"><span data-stu-id="e8490-103">CALLTHIS Function</span></span>

<span data-ttu-id="e8490-104">Llama a un procedimiento en Microsoft Visual Basic para el proyecto de aplicaciones (VBA).</span><span class="sxs-lookup"><span data-stu-id="e8490-104">Calls a procedure in a Microsoft Visual Basic for Applications (VBA) project.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="e8490-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e8490-105">Syntax</span></span>

<span data-ttu-id="e8490-106">CALLTHIS ("** *procedimiento* **", ["** *project* **"], [** *arg1* **, ** *arg2* **,...])</span><span class="sxs-lookup"><span data-stu-id="e8490-106">CALLTHIS(" ** *procedure* ** ",[" ** *project* ** "],[ ** *arg1* **, ** *arg2* **,...])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="e8490-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e8490-107">Parameters</span></span>

|<span data-ttu-id="e8490-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="e8490-108">**Name**</span></span>|<span data-ttu-id="e8490-109">**Obligatorio/opcional**</span><span class="sxs-lookup"><span data-stu-id="e8490-109">**Required/Optional**</span></span>|<span data-ttu-id="e8490-110">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="e8490-110">**Data Type**</span></span>|<span data-ttu-id="e8490-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="e8490-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="e8490-112">_procedimiento_</span><span class="sxs-lookup"><span data-stu-id="e8490-112">_procedure_</span></span> <br/> |<span data-ttu-id="e8490-113">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="e8490-113">Required</span></span>  <br/> |<span data-ttu-id="e8490-114">**String**</span><span class="sxs-lookup"><span data-stu-id="e8490-114">**String**</span></span> <br/> | <span data-ttu-id="e8490-115">Nombre del procedimiento al que se llama.</span><span class="sxs-lookup"><span data-stu-id="e8490-115">The name of the procedure to call.</span></span>  <br/> |
| <span data-ttu-id="e8490-116">_proyecto_</span><span class="sxs-lookup"><span data-stu-id="e8490-116">_project_</span></span> <br/> |<span data-ttu-id="e8490-117">Opcional</span><span class="sxs-lookup"><span data-stu-id="e8490-117">Optional</span></span>  <br/> |<span data-ttu-id="e8490-118">**String**</span><span class="sxs-lookup"><span data-stu-id="e8490-118">**String**</span></span> <br/> |<span data-ttu-id="e8490-119">Proyecto que contiene el procedimiento.</span><span class="sxs-lookup"><span data-stu-id="e8490-119">The project that contains the procedure.</span></span>  <br/> |
| <span data-ttu-id="e8490-120">_arg_</span><span class="sxs-lookup"><span data-stu-id="e8490-120">_arg_</span></span> <br/> |<span data-ttu-id="e8490-121">Opcional</span><span class="sxs-lookup"><span data-stu-id="e8490-121">Optional</span></span>  <br/> |<span data-ttu-id="e8490-122">**Number, String, Date o Currency**</span><span class="sxs-lookup"><span data-stu-id="e8490-122">**Number, String, Date, or Currency**</span></span> <br/> |<span data-ttu-id="e8490-123">Pasa como parámetro al procedimiento.</span><span class="sxs-lookup"><span data-stu-id="e8490-123">Passed as parameters to the procedure.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e8490-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e8490-124">Remarks</span></span>

<span data-ttu-id="e8490-125">En el proyecto VBA, el *procedimiento* se define como sigue:</span><span class="sxs-lookup"><span data-stu-id="e8490-125">In the VBA project,  *procedure*  is defined as follows:</span></span> 
  
<span data-ttu-id="e8490-126">procedimiento (*objForma* As Visio.Shape [arg1 As tipo; arg2 As tipo...])</span><span class="sxs-lookup"><span data-stu-id="e8490-126">procedure(*vsoShape*  As Visio.Shape [arg1 As type, arg2 As type...])</span></span> 
  
<span data-ttu-id="e8490-127">donde *objForma* es una referencia al objeto **Shape** que contiene la fórmula CALLTHIS que se está evaluando y _arg1_, *arg2* ... son los argumentos especificados en esa fórmula.</span><span class="sxs-lookup"><span data-stu-id="e8490-127">where  *vsoShape*  is a reference to the **Shape** object that contains the CALLTHIS formula being evaluated, and  _arg1_,  *arg2*  ... are the arguments specified in that formula.</span></span> 
  
<span data-ttu-id="e8490-128">Observe que *objForma* es muy parecido al argumento "this" pasado a un procedimiento miembro de C++; por lo tanto, el nombre "CALLTHIS".</span><span class="sxs-lookup"><span data-stu-id="e8490-128">Notice that  *vsoShape*  is very much like the "this" argument passed to a C++ member procedure; hence the name "CALLTHIS."</span></span> <span data-ttu-id="e8490-129">En efecto, una celda que contiene una fórmula que incluye CALLTHIS se puede leer como "Llamar a este procedimiento y pasar una referencia a esta forma".</span><span class="sxs-lookup"><span data-stu-id="e8490-129">In effect, a cell that contains a formula that includes CALLTHIS can be read as, "Call this procedure and pass it a reference to my shape."</span></span> 
  
<span data-ttu-id="e8490-130">Si se especifica un _proyecto_ , Microsoft Visio busca en todos los documentos abiertos el que contiene _proyecto_ y llama al _procedimiento_ en ese proyecto.</span><span class="sxs-lookup"><span data-stu-id="e8490-130">If  _project_ is specified, Microsoft Visio scans all open documents for the one containing  _project_ and calls  _procedure_ in that project.</span></span> <span data-ttu-id="e8490-131">Si el _proyecto_ se omite o es null (""), Visio supone que el _procedimiento_ se encuentra en el proyecto VBA del documento que contiene la fórmula CALLTHIS que se está evaluando.</span><span class="sxs-lookup"><span data-stu-id="e8490-131">If  _project_ is omitted or null (""), Visio assumes  _procedure_ is in the VBA project of the document that contains the CALLTHIS formula that is being evaluated.</span></span> 
  
<span data-ttu-id="e8490-132">Los números de _arg1_, _arg2..._ se pasan en unidades externas.</span><span class="sxs-lookup"><span data-stu-id="e8490-132">Numbers in  _arg1_,  _arg2..._ are passed in external units.</span></span> <span data-ttu-id="e8490-133">Por ejemplo, si se pasa el valor de la celda Height de una forma que es 3 cm de alto, se pasa 3.</span><span class="sxs-lookup"><span data-stu-id="e8490-133">For example, if you pass the value of the Height cell from a shape that is 3 cm tall, 3 is passed.</span></span> <span data-ttu-id="e8490-134">Para pasar unidades distintas junto con un número, use la función FORMATEX o forzar explícitamente las unidades mediante la adición de un par de número de unidad null, por ejemplo, 0 ft + alto.</span><span class="sxs-lookup"><span data-stu-id="e8490-134">To pass different units with a number, use the FORMATEX function or explicitly coerce units by adding a null number-unit pair, for example, 0 ft + Height.</span></span> 
  
<span data-ttu-id="e8490-135">El segundo punto y coma en la función CALLTHIS es opcional.</span><span class="sxs-lookup"><span data-stu-id="e8490-135">The second comma in the CALLTHIS function is optional.</span></span> <span data-ttu-id="e8490-136">Se corresponde con el número de parámetros adicionales agregados al procedimiento.</span><span class="sxs-lookup"><span data-stu-id="e8490-136">It corresponds to the number of additional parameters added to your procedure.</span></span> <span data-ttu-id="e8490-137">Si no usa ningún parámetro adicional, excepto `(vsoShape as Visio.Shape)` , no agregue el segundo punto y coma; Use CALLTHIS("",).</span><span class="sxs-lookup"><span data-stu-id="e8490-137">If you do not use any additional parameters, except  `(vsoShape as Visio.Shape)` , do not add the second comma; use CALLTHIS("",).</span></span> <span data-ttu-id="e8490-138">Si agrega dos parámetros adicionales, por ejemplo, use CALLTHIS("",,,).</span><span class="sxs-lookup"><span data-stu-id="e8490-138">If you add two additional parameters, for example, use CALLTHIS("",,,).</span></span> 
  
<span data-ttu-id="e8490-139">La función CALLTHIS siempre se evalúa como 0 y se produce la llamada al _procedimiento_ durante el tiempo de inactividad después de que finalice el proceso de actualización.</span><span class="sxs-lookup"><span data-stu-id="e8490-139">The CALLTHIS function always evaluates to 0, and the call to  _procedure_ occurs during idle time after the recalculation process finishes.</span></span>  <span data-ttu-id="e8490-140">_Procedimiento_ puede devolver un valor, pero Visio no lo usa.</span><span class="sxs-lookup"><span data-stu-id="e8490-140">_Procedure_ can return a value, but Visio ignores it.</span></span>  <span data-ttu-id="e8490-141">_Procedimiento_ devuelve un valor que puede reconocer Visio estableciendo la fórmula o resultado de otra celda del documento, pero no la celda que llama _procedimiento_, a menos que desee sobrescribir la fórmula CALLTHIS.</span><span class="sxs-lookup"><span data-stu-id="e8490-141">_Procedure_ returns a value that Visio can recognize by setting the formula or result of another cell in the document, but not the cell that called  _procedure_, unless you want to overwrite the CALLTHIS formula.</span></span>
  
<span data-ttu-id="e8490-142">La función CALLTHIS se diferencia de la función RUNADDON en que no es necesario que el proyecto de un documento haga referencia a otro proyecto para que se pueda llamar a ese proyecto.</span><span class="sxs-lookup"><span data-stu-id="e8490-142">The CALLTHIS function differs from the RUNADDON function in that a document's project does not need to reference another project in order to call into that project.</span></span> 
  
> [!NOTE]
>  <span data-ttu-id="e8490-143">El código VBA que se invoca cuando una copia de Visio evalúa una función CALLTHIS que forma parte de una fórmula no debe cerrar el documento que contiene la celda que utiliza la función, ya que, de hacerlo, se producirá un error de aplicación y la ejecución de Visio se terminará.</span><span class="sxs-lookup"><span data-stu-id="e8490-143">VBA code that is invoked when the Visio instance evaluates a CALLTHIS function in a formula should not close the document containing the cell using the function because an application error results and Visio terminates.</span></span> 
  
<span data-ttu-id="e8490-144">Si necesita cerrar el documento que contiene la celda que usa la función CALLTHIS, puede usar uno de los métodos siguientes:</span><span class="sxs-lookup"><span data-stu-id="e8490-144">If you need to close the document containing the cell that uses the CALLTHIS function, use one of the following techniques:</span></span> 
  
- <span data-ttu-id="e8490-145">Cerrar el documento mediante código que no sea de VBA.</span><span class="sxs-lookup"><span data-stu-id="e8490-145">Close the document from code that is not VBA.</span></span>
    
- <span data-ttu-id="e8490-146">Cerrar el documento desde un proyecto diferente al que se cierra.</span><span class="sxs-lookup"><span data-stu-id="e8490-146">Close the document from a project other than the one that is closing.</span></span>
    
- <span data-ttu-id="e8490-147">Enviar mensajes de ventana para cerrar las ventanas del documento en lugar de cerrar el documento.</span><span class="sxs-lookup"><span data-stu-id="e8490-147">Post window messages to close windows in the document rather than closing the document.</span></span>
    
<span data-ttu-id="e8490-148">Para obtener más información sobre cómo ejecutar código en Visio, vea [Acerca de la configuración de seguridad y la ejecución de código en Visio](about-security-settings-and-running-code-in-visio-shapesheet.md) en esta Referencia de ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="e8490-148">For more information about running code in Visio, see [About Security Settings and Running Code in Visio](about-security-settings-and-running-code-in-visio-shapesheet.md) in this ShapeSheet Reference.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="e8490-149">Ejemplo 1</span><span class="sxs-lookup"><span data-stu-id="e8490-149">Example 1</span></span>

<span data-ttu-id="e8490-150">CALLTHIS("p";;FORMATEX(Height;"#,00 u";;"cm"))</span><span class="sxs-lookup"><span data-stu-id="e8490-150">CALLTHIS("p",,FORMATEX(Height,"#.00 u",,"cm"))</span></span>
  
<span data-ttu-id="e8490-151">Llama a un procedimiento denominado p que se encuentra en un módulo y le pasa el valor de Height en centímetros, por ejemplo 7,62 cm.</span><span class="sxs-lookup"><span data-stu-id="e8490-151">Calls the procedure named p located in a module and passes the value of Height in centimeters, such as 7.62 cm.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="e8490-152">Ejemplo 2</span><span class="sxs-lookup"><span data-stu-id="e8490-152">Example 2</span></span>

<span data-ttu-id="e8490-153">CALLTHIS("q",,0 cm.+Height,Width)</span><span class="sxs-lookup"><span data-stu-id="e8490-153">CALLTHIS("q",,0 cm+Height,Width)</span></span>
  
<span data-ttu-id="e8490-154">Llama a un procedimiento denominado q que se encuentra en un módulo y le pasa el alto de la celda en centímetros y el ancho en unidades internas.</span><span class="sxs-lookup"><span data-stu-id="e8490-154">Calls the procedure named q located in a module and passes the cell's height in centimeters and width in internal units.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="e8490-155">Ejemplo 3</span><span class="sxs-lookup"><span data-stu-id="e8490-155">Example 3</span></span>

<span data-ttu-id="e8490-156">Use el procedimiento siguiente en el módulo de clase *ThisDocument* .</span><span class="sxs-lookup"><span data-stu-id="e8490-156">Use the following procedure in the  *ThisDocument*  class module.</span></span> 
  
<span data-ttu-id="e8490-157">Utilice alguna de las sintaxis siguientes en la celda EventDblClick de una forma con los procedimientos anteriores.</span><span class="sxs-lookup"><span data-stu-id="e8490-157">Use any of the following syntax in a shape's EventDblClick cell with the preceding procedures.</span></span>
  
<span data-ttu-id="e8490-158">CALLTHIS("ThisDocument.A",)</span><span class="sxs-lookup"><span data-stu-id="e8490-158">CALLTHIS("ThisDocument.A",)</span></span>
  
<span data-ttu-id="e8490-159">CALLTHIS("ThisDocument.B",,"Click")</span><span class="sxs-lookup"><span data-stu-id="e8490-159">CALLTHIS("ThisDocument.B",,"Click")</span></span>
  
<span data-ttu-id="e8490-160">CALLTHIS("ThisDocument.C",,"Click", " OK.")</span><span class="sxs-lookup"><span data-stu-id="e8490-160">CALLTHIS("ThisDocument.C",,"Click", " OK.")</span></span>
  

