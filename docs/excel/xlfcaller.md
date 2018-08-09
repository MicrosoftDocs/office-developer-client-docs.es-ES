---
title: xlfCaller
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlfCaller
keywords:
- función xlfCaller [excel 2007]
localization_priority: Normal
ms.assetid: de4b119c-ae2e-4207-9783-8d5692a4d052
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 92d2d1877d7b315d178ef1fa36b47bd5f9f8e661
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815723"
---
# <a name="xlfcaller"></a><span data-ttu-id="48f6d-104">xlfCaller</span><span class="sxs-lookup"><span data-stu-id="48f6d-104">xlfCaller</span></span>

 <span data-ttu-id="48f6d-105">**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="48f6d-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="48f6d-106">Devuelve información acerca de la celda, el rango de celdas, el comando en un menú de la herramienta en una barra de herramientas o el objeto que llama el comando de la DLL o la función que se está ejecutando actualmente.</span><span class="sxs-lookup"><span data-stu-id="48f6d-106">Returns information about the cell, range of cells, command on a menu, tool on a toolbar, or object that called the DLL command or function that is currently running.</span></span>
  
|<span data-ttu-id="48f6d-107">**Llamar desde el código**</span><span class="sxs-lookup"><span data-stu-id="48f6d-107">**Code called from**</span></span>|<span data-ttu-id="48f6d-108">**Devuelve**</span><span class="sxs-lookup"><span data-stu-id="48f6d-108">**Returns**</span></span>|
|:-----|:-----|
|<span data-ttu-id="48f6d-109">ARCHIVO DLL</span><span class="sxs-lookup"><span data-stu-id="48f6d-109">DLL</span></span>  <br/> |<span data-ttu-id="48f6d-110">El identificador del registro.</span><span class="sxs-lookup"><span data-stu-id="48f6d-110">The Register ID.</span></span>  <br/> |
|<span data-ttu-id="48f6d-111">Una sola celda</span><span class="sxs-lookup"><span data-stu-id="48f6d-111">A single cell</span></span>  <br/> |<span data-ttu-id="48f6d-112">Una referencia de celda de un solo.</span><span class="sxs-lookup"><span data-stu-id="48f6d-112">A single-cell reference.</span></span>  <br/> |
|<span data-ttu-id="48f6d-113">Una fórmula de matriz de varias celdas</span><span class="sxs-lookup"><span data-stu-id="48f6d-113">A multi-cell array formula</span></span>  <br/> |<span data-ttu-id="48f6d-114">Una referencia de varias celda.</span><span class="sxs-lookup"><span data-stu-id="48f6d-114">A multi-cell reference.</span></span>  <br/> |
|<span data-ttu-id="48f6d-115">Una expresión de formato condicional</span><span class="sxs-lookup"><span data-stu-id="48f6d-115">A conditional formatting expression</span></span>  <br/> |<span data-ttu-id="48f6d-116">Una referencia a la celda a la que se aplica la condición de formato.</span><span class="sxs-lookup"><span data-stu-id="48f6d-116">A reference to the cell to which the formatting condition is applied.</span></span>  <br/> |
|<span data-ttu-id="48f6d-117">Un menú</span><span class="sxs-lookup"><span data-stu-id="48f6d-117">A menu</span></span>  <br/> | <span data-ttu-id="48f6d-118">Una matriz de fila única cuatro elementos:</span><span class="sxs-lookup"><span data-stu-id="48f6d-118">A four-element single-row array:</span></span>  <br/>  <span data-ttu-id="48f6d-119">Identificador de la barra.</span><span class="sxs-lookup"><span data-stu-id="48f6d-119">The bar ID.</span></span>  <br/>  <span data-ttu-id="48f6d-120">La posición del menú.</span><span class="sxs-lookup"><span data-stu-id="48f6d-120">The menu position.</span></span>  <br/>  <span data-ttu-id="48f6d-121">La posición del submenú.</span><span class="sxs-lookup"><span data-stu-id="48f6d-121">The submenu position.</span></span>  <br/>  <span data-ttu-id="48f6d-122">La posición del comando.</span><span class="sxs-lookup"><span data-stu-id="48f6d-122">The command position.</span></span>  <br/> |
|<span data-ttu-id="48f6d-123">Una barra de herramientas</span><span class="sxs-lookup"><span data-stu-id="48f6d-123">A toolbar</span></span>  <br/> | <span data-ttu-id="48f6d-124">Una matriz de fila única dos elementos:</span><span class="sxs-lookup"><span data-stu-id="48f6d-124">A two-element single-row array:</span></span>  <br/>  <span data-ttu-id="48f6d-125">El número de la barra de herramientas para barras de herramientas integradas o el nombre de la barra de herramientas de barras de herramientas personalizadas.</span><span class="sxs-lookup"><span data-stu-id="48f6d-125">The toolbar number for built-in toolbars or the toolbar name for custom toolbars.</span></span>  <br/>  <span data-ttu-id="48f6d-126">La posición en la barra de herramientas.</span><span class="sxs-lookup"><span data-stu-id="48f6d-126">The position on the toolbar.</span></span>  <br/> |
|<span data-ttu-id="48f6d-127">Un objeto gráfico</span><span class="sxs-lookup"><span data-stu-id="48f6d-127">A graphic object</span></span>  <br/> |<span data-ttu-id="48f6d-128">El identificador de objeto (nombre de objeto).</span><span class="sxs-lookup"><span data-stu-id="48f6d-128">The object identifier (object name).</span></span>  <br/> |
|<span data-ttu-id="48f6d-129">Un comando asociado con un xlcOnEnter, en. Escriba, captura (evento)</span><span class="sxs-lookup"><span data-stu-id="48f6d-129">A command associated with an xlcOnEnter, ON.ENTER, event trap</span></span>  <br/> |<span data-ttu-id="48f6d-130">Una referencia a la celda o celdas que se escriben.</span><span class="sxs-lookup"><span data-stu-id="48f6d-130">A reference to the cell or cells being entered.</span></span>  <br/> |
|<span data-ttu-id="48f6d-131">Un comando asociado con un xlcOnDoubleclick, en. DOUBLECLICK, captura de eventos.</span><span class="sxs-lookup"><span data-stu-id="48f6d-131">A command associated with an xlcOnDoubleclick, ON.DOUBLECLICK, event trap.</span></span>  <br/> |<span data-ttu-id="48f6d-132">La celda que se ha hecho doble clic (no necesariamente la celda activa).</span><span class="sxs-lookup"><span data-stu-id="48f6d-132">The cell that was double-clicked (not necessarily the active cell).</span></span>  <br/> |
|<span data-ttu-id="48f6d-133">Macro Auto_abrir, AutoClose, Auto_activar o Auto_desactivar</span><span class="sxs-lookup"><span data-stu-id="48f6d-133">Auto_Open, AutoClose, Auto_Activate or Auto_Deactivate macro</span></span>  <br/> |<span data-ttu-id="48f6d-134">El nombre de la hoja de llamada.</span><span class="sxs-lookup"><span data-stu-id="48f6d-134">The name of the calling sheet.</span></span>  <br/> |
|<span data-ttu-id="48f6d-135">Otros métodos que no se muestran</span><span class="sxs-lookup"><span data-stu-id="48f6d-135">Other methods not listed</span></span>  <br/> |<span data-ttu-id="48f6d-136">#REF!</span><span class="sxs-lookup"><span data-stu-id="48f6d-136">#REF!</span></span> <span data-ttu-id="48f6d-137">Error</span><span class="sxs-lookup"><span data-stu-id="48f6d-137">Error.</span></span>  <br/> |
   
```cs
Excel12(xlfCaller, (LPXLOPER12) pxRes,0);
```

## <a name="property-valuereturn-value"></a><span data-ttu-id="48f6d-138">Valor de la propiedad/valor devuelto</span><span class="sxs-lookup"><span data-stu-id="48f6d-138">Property value/Return value</span></span>

<span data-ttu-id="48f6d-139">El valor devuelto es uno de los siguientes **XLOPER**/ **XLOPER12** los tipos de datos: **xltypeRef**, **xltypeSRef**, **xltypeNum**, **xltypeStr**, **xltypeErr**o **xltypeMulti**.</span><span class="sxs-lookup"><span data-stu-id="48f6d-139">The return value is one of the following **XLOPER**/ **XLOPER12** data types: **xltypeRef**, **xltypeSRef**, **xltypeNum**, **xltypeStr**, **xltypeErr**, or **xltypeMulti**.</span></span> <span data-ttu-id="48f6d-140">Dado que tres de estos tipos de apuntar a memoria asignada, el valor devuelto de **xlfCaller** siempre debe liberarse en una llamada a la [función xlFree](xlfree.md) cuando ya no sea necesaria.</span><span class="sxs-lookup"><span data-stu-id="48f6d-140">Since three of these types point to allocated memory, the return value of **xlfCaller** should always be freed in a call to the [xlFree function](xlfree.md) when it is no longer needed.</span></span> 
  
<span data-ttu-id="48f6d-141">Para obtener más información acerca de **XLOPER**/ **XLOPER12s** vea [Administración de memoria en Excel](memory-management-in-excel.md).</span><span class="sxs-lookup"><span data-stu-id="48f6d-141">For more information about **XLOPERs**/ **XLOPER12s** see [Memory Management in Excel](memory-management-in-excel.md).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="48f6d-142">Comentarios</span><span class="sxs-lookup"><span data-stu-id="48f6d-142">Remarks</span></span>

<span data-ttu-id="48f6d-143">Esta función es la función sólo que no son hojas de cálculo que se puede llamar desde una función de hoja de cálculo DLL o XLL.</span><span class="sxs-lookup"><span data-stu-id="48f6d-143">This function is the only non-worksheet function that can be called from a DLL/XLL worksheet function.</span></span> <span data-ttu-id="48f6d-144">Otras funciones de información XLM sólo se pueden llamar desde los comandos o equivalente de hoja de macros funciones.</span><span class="sxs-lookup"><span data-stu-id="48f6d-144">Other XLM information functions can only be called from commands or macro-sheet equivalent functions.</span></span>
  
## <a name="example"></a><span data-ttu-id="48f6d-145">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="48f6d-145">Example</span></span>

 <span data-ttu-id="48f6d-146">`\SAMPLES\EXAMPLE\EXAMPLE.C`.</span><span class="sxs-lookup"><span data-stu-id="48f6d-146"></span></span> <span data-ttu-id="48f6d-147">Esta función llama a una macro de comando (xlcSelect) y funcionará correctamente sólo cuando se llame desde una hoja de macros.</span><span class="sxs-lookup"><span data-stu-id="48f6d-147">This function calls a command macro (xlcSelect) and will work correctly only when called from a macro sheet.</span></span>
  
```cs
short WINAPI CallerExample(void)
{
   XLOPER12 xRes;
   Excel12(xlfCaller, &xRes, 0);
   Excel12(xlcSelect, 0, 1, (LPXLOPER12)&xRes);
   Excel12(xlFree, 0, 1, (LPXLOPER12)&xRes);
   return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="48f6d-148">Vea también</span><span class="sxs-lookup"><span data-stu-id="48f6d-148">See also</span></span>



[<span data-ttu-id="48f6d-149">Funciones esenciales y útiles XLM de API de C</span><span class="sxs-lookup"><span data-stu-id="48f6d-149">Essential and Useful C API XLM Functions</span></span>](essential-and-useful-c-api-xlm-functions.md)

