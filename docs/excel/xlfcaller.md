---
title: xlfCaller
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlfCaller
keywords:
- Función xlfcaller [excel 2007]
localization_priority: Normal
ms.assetid: de4b119c-ae2e-4207-9783-8d5692a4d052
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: fb788375504cefab75fde9513147c1d54acdaa07
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405733"
---
# <a name="xlfcaller"></a><span data-ttu-id="3ba3e-104">xlfCaller</span><span class="sxs-lookup"><span data-stu-id="3ba3e-104">xlfCaller</span></span>

 <span data-ttu-id="3ba3e-105">**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="3ba3e-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="3ba3e-106">Devuelve información sobre la celda, el rango de celdas, el comando de un menú, la herramienta de una barra de herramientas u objeto que llamó al comando DLL o la función que se está ejecutando actualmente.</span><span class="sxs-lookup"><span data-stu-id="3ba3e-106">Returns information about the cell, range of cells, command on a menu, tool on a toolbar, or object that called the DLL command or function that is currently running.</span></span>
  
|<span data-ttu-id="3ba3e-107">**Código llamado desde**</span><span class="sxs-lookup"><span data-stu-id="3ba3e-107">**Code called from**</span></span>|<span data-ttu-id="3ba3e-108">**Devuelve**</span><span class="sxs-lookup"><span data-stu-id="3ba3e-108">**Returns**</span></span>|
|:-----|:-----|
|<span data-ttu-id="3ba3e-109">DLL</span><span class="sxs-lookup"><span data-stu-id="3ba3e-109">DLL</span></span>  <br/> |<span data-ttu-id="3ba3e-110">El id. de registro.</span><span class="sxs-lookup"><span data-stu-id="3ba3e-110">The Register ID.</span></span>  <br/> |
|<span data-ttu-id="3ba3e-111">Una sola celda</span><span class="sxs-lookup"><span data-stu-id="3ba3e-111">A single cell</span></span>  <br/> |<span data-ttu-id="3ba3e-112">Referencia de una sola celda.</span><span class="sxs-lookup"><span data-stu-id="3ba3e-112">A single-cell reference.</span></span>  <br/> |
|<span data-ttu-id="3ba3e-113">Una fórmula de matriz de varias celdas</span><span class="sxs-lookup"><span data-stu-id="3ba3e-113">A multi-cell array formula</span></span>  <br/> |<span data-ttu-id="3ba3e-114">Referencia de varias celdas.</span><span class="sxs-lookup"><span data-stu-id="3ba3e-114">A multi-cell reference.</span></span>  <br/> |
|<span data-ttu-id="3ba3e-115">Expresión de formato condicional</span><span class="sxs-lookup"><span data-stu-id="3ba3e-115">A conditional formatting expression</span></span>  <br/> |<span data-ttu-id="3ba3e-116">Referencia a la celda a la que se aplica la condición de formato.</span><span class="sxs-lookup"><span data-stu-id="3ba3e-116">A reference to the cell to which the formatting condition is applied.</span></span>  <br/> |
|<span data-ttu-id="3ba3e-117">Un menú</span><span class="sxs-lookup"><span data-stu-id="3ba3e-117">A menu</span></span>  <br/> | <span data-ttu-id="3ba3e-118">Una matriz de fila única de cuatro elementos:</span><span class="sxs-lookup"><span data-stu-id="3ba3e-118">A four-element single-row array:</span></span>  <br/>  <span data-ttu-id="3ba3e-119">Identificador de la barra.</span><span class="sxs-lookup"><span data-stu-id="3ba3e-119">The bar ID.</span></span>  <br/>  <span data-ttu-id="3ba3e-120">Posición del menú.</span><span class="sxs-lookup"><span data-stu-id="3ba3e-120">The menu position.</span></span>  <br/>  <span data-ttu-id="3ba3e-121">Posición del submenú.</span><span class="sxs-lookup"><span data-stu-id="3ba3e-121">The submenu position.</span></span>  <br/>  <span data-ttu-id="3ba3e-122">Posición del comando.</span><span class="sxs-lookup"><span data-stu-id="3ba3e-122">The command position.</span></span>  <br/> |
|<span data-ttu-id="3ba3e-123">Una barra de herramientas</span><span class="sxs-lookup"><span data-stu-id="3ba3e-123">A toolbar</span></span>  <br/> | <span data-ttu-id="3ba3e-124">Una matriz de fila única de dos elementos:</span><span class="sxs-lookup"><span data-stu-id="3ba3e-124">A two-element single-row array:</span></span>  <br/>  <span data-ttu-id="3ba3e-125">El número de barra de herramientas de las barras de herramientas integradas o el nombre de la barra de herramientas de las barras de herramientas personalizadas.</span><span class="sxs-lookup"><span data-stu-id="3ba3e-125">The toolbar number for built-in toolbars or the toolbar name for custom toolbars.</span></span>  <br/>  <span data-ttu-id="3ba3e-126">Posición en la barra de herramientas.</span><span class="sxs-lookup"><span data-stu-id="3ba3e-126">The position on the toolbar.</span></span>  <br/> |
|<span data-ttu-id="3ba3e-127">Un objeto gráfico</span><span class="sxs-lookup"><span data-stu-id="3ba3e-127">A graphic object</span></span>  <br/> |<span data-ttu-id="3ba3e-128">Identificador de objeto (nombre del objeto).</span><span class="sxs-lookup"><span data-stu-id="3ba3e-128">The object identifier (object name).</span></span>  <br/> |
|<span data-ttu-id="3ba3e-129">Un comando asociado a un xlcOnEnter, ON. ENTRAR, captura de eventos</span><span class="sxs-lookup"><span data-stu-id="3ba3e-129">A command associated with an xlcOnEnter, ON.ENTER, event trap</span></span>  <br/> |<span data-ttu-id="3ba3e-130">Una referencia a la celda o celdas que se están escribió.</span><span class="sxs-lookup"><span data-stu-id="3ba3e-130">A reference to the cell or cells being entered.</span></span>  <br/> |
|<span data-ttu-id="3ba3e-131">Comando asociado a xlcOnDoubleclick, ON. DOUBLECLICK, captura de eventos.</span><span class="sxs-lookup"><span data-stu-id="3ba3e-131">A command associated with an xlcOnDoubleclick, ON.DOUBLECLICK, event trap.</span></span>  <br/> |<span data-ttu-id="3ba3e-132">Celda en la que se hizo doble clic (no necesariamente la celda activa).</span><span class="sxs-lookup"><span data-stu-id="3ba3e-132">The cell that was double-clicked (not necessarily the active cell).</span></span>  <br/> |
|<span data-ttu-id="3ba3e-133">Auto_Open, AutoClose, Auto_Activate o Auto_Deactivate macro</span><span class="sxs-lookup"><span data-stu-id="3ba3e-133">Auto_Open, AutoClose, Auto_Activate or Auto_Deactivate macro</span></span>  <br/> |<span data-ttu-id="3ba3e-134">Nombre de la hoja de llamadas.</span><span class="sxs-lookup"><span data-stu-id="3ba3e-134">The name of the calling sheet.</span></span>  <br/> |
|<span data-ttu-id="3ba3e-135">Otros métodos no enumerados</span><span class="sxs-lookup"><span data-stu-id="3ba3e-135">Other methods not listed</span></span>  <br/> |<span data-ttu-id="3ba3e-136">#REF!</span><span class="sxs-lookup"><span data-stu-id="3ba3e-136">#REF!</span></span> <span data-ttu-id="3ba3e-137">Error</span><span class="sxs-lookup"><span data-stu-id="3ba3e-137">Error.</span></span>  <br/> |
   
```cs
Excel12(xlfCaller, (LPXLOPER12) pxRes,0);
```

## <a name="property-valuereturn-value"></a><span data-ttu-id="3ba3e-138">Valor de la propiedad/valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3ba3e-138">Property value/Return value</span></span>

<span data-ttu-id="3ba3e-139">El valor devuelto es uno de los siguientes tipos de datos  /  **XLOPER XLOPER12:** **xltypeRef**, **xltypeSRef**, **xltypeNum**, **xltypeStr**, **xltypeErr** o **xltypeMulti**.</span><span class="sxs-lookup"><span data-stu-id="3ba3e-139">The return value is one of the following **XLOPER**/ **XLOPER12** data types: **xltypeRef**, **xltypeSRef**, **xltypeNum**, **xltypeStr**, **xltypeErr**, or **xltypeMulti**.</span></span> <span data-ttu-id="3ba3e-140">Dado que tres de estos tipos apuntan a memoria asignada, el valor devuelto de **xlfCaller** siempre debe liberarse en una llamada a la función [xlFree](xlfree.md) cuando ya no se necesite.</span><span class="sxs-lookup"><span data-stu-id="3ba3e-140">Since three of these types point to allocated memory, the return value of **xlfCaller** should always be freed in a call to the [xlFree function](xlfree.md) when it is no longer needed.</span></span> 
  
<span data-ttu-id="3ba3e-141">Para obtener más información **acerca de** /  **XLOPER12** XLOPERs, vea [Administración de memoria en Excel.](memory-management-in-excel.md)</span><span class="sxs-lookup"><span data-stu-id="3ba3e-141">For more information about **XLOPERs**/ **XLOPER12s** see [Memory Management in Excel](memory-management-in-excel.md).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="3ba3e-142">Comentarios</span><span class="sxs-lookup"><span data-stu-id="3ba3e-142">Remarks</span></span>

<span data-ttu-id="3ba3e-143">Esta función es la única función que no es de hoja de cálculo a la que se puede llamar desde una función de hoja de cálculo DLL/XLL.</span><span class="sxs-lookup"><span data-stu-id="3ba3e-143">This function is the only non-worksheet function that can be called from a DLL/XLL worksheet function.</span></span> <span data-ttu-id="3ba3e-144">Solo se puede llamar a otras funciones de información XLM desde comandos o funciones equivalentes de hoja de macros.</span><span class="sxs-lookup"><span data-stu-id="3ba3e-144">Other XLM information functions can only be called from commands or macro-sheet equivalent functions.</span></span>
  
## <a name="example"></a><span data-ttu-id="3ba3e-145">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="3ba3e-145">Example</span></span>

 <span data-ttu-id="3ba3e-146">`\SAMPLES\EXAMPLE\EXAMPLE.C`.</span><span class="sxs-lookup"><span data-stu-id="3ba3e-146">`\SAMPLES\EXAMPLE\EXAMPLE.C`.</span></span> <span data-ttu-id="3ba3e-147">Esta función llama a una macro de comandos (xlcSelect) y sólo funcionará correctamente cuando se llame desde una hoja de macros.</span><span class="sxs-lookup"><span data-stu-id="3ba3e-147">This function calls a command macro (xlcSelect) and will work correctly only when called from a macro sheet.</span></span>
  
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

## <a name="see-also"></a><span data-ttu-id="3ba3e-148">Consulte también</span><span class="sxs-lookup"><span data-stu-id="3ba3e-148">See also</span></span>



[<span data-ttu-id="3ba3e-149">Funciones esenciales y útiles XLM de API de C</span><span class="sxs-lookup"><span data-stu-id="3ba3e-149">Essential and Useful C API XLM Functions</span></span>](essential-and-useful-c-api-xlm-functions.md)

