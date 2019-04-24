---
title: xlfGetDef
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
keywords:
- xlfgetdef
localization_priority: Normal
ms.assetid: 68f5edbd-9040-46d3-acd5-dd51ca82f6fa
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 014db553156849d84bd07e0e416f8cb3fefb4e0b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310244"
---
# <a name="xlfgetdef"></a><span data-ttu-id="62b66-104">xlfGetDef</span><span class="sxs-lookup"><span data-stu-id="62b66-104">xlfGetDef</span></span>

<span data-ttu-id="62b66-105">**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="62b66-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="62b66-106">Devuelve el nombre, como texto, que se define para un área, un valor o una fórmula en particular en un libro.</span><span class="sxs-lookup"><span data-stu-id="62b66-106">Returns the name, as text, that is defined for a particular area, value, or formula in a workbook.</span></span> <span data-ttu-id="62b66-107">En Excel, este valor se muestra en la columna **nombre** del cuadro de diálogo **Administrador de nombres** , que se muestra al hacer clic en Administrador de **nombres** en la sección **nombres definidos** de la ficha **fórmulas** . use **xlfGetDef** para obtener la nombre que corresponde a una definición.</span><span class="sxs-lookup"><span data-stu-id="62b66-107">In Excel, this value is displayed in the **Name** column of the **Name Manager** dialog box, which is displayed when you click **Name Manager** in the **Defined Names** section on the **Formulas** tab. Use **xlfGetDef** to get the name that corresponds to a definition.</span></span> <span data-ttu-id="62b66-108">Para obtener la definición de un nombre, use [xlfGetName](xlfgetname.md).</span><span class="sxs-lookup"><span data-stu-id="62b66-108">To get the definition of a name, use [xlfGetName](xlfgetname.md).</span></span>
  
```cpp
Excel12(xlfGetDef, LPXLOPER12 pxRes, 3, LPXLOPER12 pxDefText, LPXLOPER12 pxDocumentText, LPXLOPER12 pxTypeNum);
```

## <a name="parameters"></a><span data-ttu-id="62b66-109">Parameters</span><span class="sxs-lookup"><span data-stu-id="62b66-109">Parameters</span></span>

<span data-ttu-id="62b66-110">_pxDefText_ (**xltypeStr**)</span><span class="sxs-lookup"><span data-stu-id="62b66-110">_pxDefText_ (**xltypeStr**)</span></span>
  
<span data-ttu-id="62b66-111">Puede ser cualquier elemento al que se pueda hacer referencia, incluida una referencia, un valor, un objeto o una fórmula.</span><span class="sxs-lookup"><span data-stu-id="62b66-111">Can be anything you can define a name to refer to, including a reference, a value, an object, or a formula.</span></span>
  
<span data-ttu-id="62b66-112">Las referencias se deben dar en estilo F1C1, como `"R3C5"`.</span><span class="sxs-lookup"><span data-stu-id="62b66-112">References must be given in R1C1 style, such as  `"R3C5"`.</span></span> <span data-ttu-id="62b66-113">Si _pxDefText_ es un valor o una fórmula, no es necesario incluir el signo igual que se muestra en la columna se **refiere a** en el cuadro de diálogo **Administrador de nombres** .</span><span class="sxs-lookup"><span data-stu-id="62b66-113">If  _pxDefText_ is a value or formula, it is not necessary to include the equal sign that is displayed in the **Refers To** column in the **Name Manager** dialog box.</span></span> <span data-ttu-id="62b66-114">Si hay más de un nombre para _pxDefText_, **xlfGetDef** devuelve el primer nombre.</span><span class="sxs-lookup"><span data-stu-id="62b66-114">If there is more than one name for  _pxDefText_, **xlfGetDef** returns the first name.</span></span> <span data-ttu-id="62b66-115">Si no hay ningún __ nombre que coincida con pxDefText `#NAME?` , **xlfGetDef** devuelve el valor de error.</span><span class="sxs-lookup"><span data-stu-id="62b66-115">If no name matches  _pxDefText_, **xlfGetDef** returns the  `#NAME?` error value.</span></span> 
  
<span data-ttu-id="62b66-116">_pxDocumentText_ (**xltypeStr**)</span><span class="sxs-lookup"><span data-stu-id="62b66-116">_pxDocumentText_ (**xltypeStr**)</span></span>
  
<span data-ttu-id="62b66-117">Especifica la hoja en la que se encuentra _pxDefText_ .</span><span class="sxs-lookup"><span data-stu-id="62b66-117">Specifies the sheet that  _pxDefText_ is on.</span></span> <span data-ttu-id="62b66-118">Si se omite _pxDocumentText_ , se supone que es la hoja activa.</span><span class="sxs-lookup"><span data-stu-id="62b66-118">If  _pxDocumentText_ is omitted, it is assumed to be the active sheet.</span></span> 
  
<span data-ttu-id="62b66-119">_pxTypeNum_ (**xltypeNum**)</span><span class="sxs-lookup"><span data-stu-id="62b66-119">_pxTypeNum_ (**xltypeNum**)</span></span>
  
<span data-ttu-id="62b66-120">Un número entre 1 y 3 que especifica qué tipos de nombres se devuelven.</span><span class="sxs-lookup"><span data-stu-id="62b66-120">A number from 1 to 3 specifying which types of names are returned.</span></span>
  
|<span data-ttu-id="62b66-121">**_pxTypeNum_**</span><span class="sxs-lookup"><span data-stu-id="62b66-121">**_pxTypeNum_**</span></span>|<span data-ttu-id="62b66-122">**Devuelve**</span><span class="sxs-lookup"><span data-stu-id="62b66-122">**Returns**</span></span>|
|:-----|:-----|
|<span data-ttu-id="62b66-123">1 u omitido</span><span class="sxs-lookup"><span data-stu-id="62b66-123">1 or omitted</span></span>  <br/> |<span data-ttu-id="62b66-124">Solo nombres normales.</span><span class="sxs-lookup"><span data-stu-id="62b66-124">Normal names only.</span></span>  <br/> |
|<span data-ttu-id="62b66-125">segundo</span><span class="sxs-lookup"><span data-stu-id="62b66-125">2</span></span>  <br/> |<span data-ttu-id="62b66-126">Solo nombres ocultos.</span><span class="sxs-lookup"><span data-stu-id="62b66-126">Hidden names only.</span></span>  <br/> |
|<span data-ttu-id="62b66-127">3</span><span class="sxs-lookup"><span data-stu-id="62b66-127">3</span></span>  <br/> |<span data-ttu-id="62b66-128">Todos los nombres.</span><span class="sxs-lookup"><span data-stu-id="62b66-128">All names.</span></span>  <br/> |
   
## <a name="property-valuereturn-value"></a><span data-ttu-id="62b66-129">Valor de la propiedad/valor devuelto</span><span class="sxs-lookup"><span data-stu-id="62b66-129">Property value/Return value</span></span>

 <span data-ttu-id="62b66-130">_pxRes_ (**xltypeStr** o **xltypeErr**)</span><span class="sxs-lookup"><span data-stu-id="62b66-130">_pxRes_ (**xltypeStr** or **xltypeErr**)</span></span>
  
<span data-ttu-id="62b66-131">Devuelve el nombre asociado a la definición especificada.</span><span class="sxs-lookup"><span data-stu-id="62b66-131">Returns the name associated with the specified definition.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="62b66-132">Comentarios</span><span class="sxs-lookup"><span data-stu-id="62b66-132">Remarks</span></span>

<span data-ttu-id="62b66-133">En la siguiente tabla se enumeran cuatro ejemplos de los valores devueltos por una llamada a **xlfGetDef** con los argumentos especificados.</span><span class="sxs-lookup"><span data-stu-id="62b66-133">The following table lists four examples of the values returned by a call to **xlfGetDef** with the specified arguments.</span></span> 
  
|<span data-ttu-id="62b66-134">**Nombre definido en Excel**</span><span class="sxs-lookup"><span data-stu-id="62b66-134">**Name defined in Excel**</span></span>|<span data-ttu-id="62b66-135">**_pxDefText_**</span><span class="sxs-lookup"><span data-stu-id="62b66-135">**_pxDefText_**</span></span>|<span data-ttu-id="62b66-136">**_pxDocumentText_**</span><span class="sxs-lookup"><span data-stu-id="62b66-136">**_pxDocumentText_**</span></span>|<span data-ttu-id="62b66-137">**_pxTypeNum_**</span><span class="sxs-lookup"><span data-stu-id="62b66-137">**_pxTypeNum_**</span></span>|<span data-ttu-id="62b66-138">**Valor deVuelto**</span><span class="sxs-lookup"><span data-stu-id="62b66-138">**Value Returned**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="62b66-139">El rango especificado en Sheet4 se llama ventas.</span><span class="sxs-lookup"><span data-stu-id="62b66-139">The specified range in Sheet4 is named Sales.</span></span>  <br/> |<span data-ttu-id="62b66-140">"R2C2: R9C6"</span><span class="sxs-lookup"><span data-stu-id="62b66-140">"R2C2:R9C6"</span></span>  <br/> |<span data-ttu-id="62b66-141">Sheet4</span><span class="sxs-lookup"><span data-stu-id="62b66-141">"Sheet4"</span></span>  <br/> |<span data-ttu-id="62b66-142">\<Address\></span><span class="sxs-lookup"><span data-stu-id="62b66-142">\<omitted\></span></span>  <br/> |<span data-ttu-id="62b66-143">Lín</span><span class="sxs-lookup"><span data-stu-id="62b66-143">"Sales"</span></span>  <br/> |
|<span data-ttu-id="62b66-144">El valor 100 de Sheet4 se define como constante.</span><span class="sxs-lookup"><span data-stu-id="62b66-144">The value 100 in Sheet4 is defined as Constant.</span></span>  <br/> |<span data-ttu-id="62b66-145">"100"</span><span class="sxs-lookup"><span data-stu-id="62b66-145">"100"</span></span>  <br/> |<span data-ttu-id="62b66-146">Sheet4</span><span class="sxs-lookup"><span data-stu-id="62b66-146">"Sheet4"</span></span>  <br/> |<span data-ttu-id="62b66-147">\<Address\></span><span class="sxs-lookup"><span data-stu-id="62b66-147">\<omitted\></span></span>  <br/> |<span data-ttu-id="62b66-148">Constante</span><span class="sxs-lookup"><span data-stu-id="62b66-148">"Constant"</span></span>  <br/> |
|<span data-ttu-id="62b66-149">La fórmula especificada en Sheet4 se denomina SumTotal.</span><span class="sxs-lookup"><span data-stu-id="62b66-149">The specified formula in Sheet4 is named SumTotal.</span></span>  <br/> |<span data-ttu-id="62b66-150">"SUM (F1C1: R10C1)"</span><span class="sxs-lookup"><span data-stu-id="62b66-150">"SUM(R1C1:R10C1)"</span></span>  <br/> |<span data-ttu-id="62b66-151">Sheet4</span><span class="sxs-lookup"><span data-stu-id="62b66-151">"Sheet4"</span></span>  <br/> |<span data-ttu-id="62b66-152">\<Address\></span><span class="sxs-lookup"><span data-stu-id="62b66-152">\<omitted\></span></span>  <br/> |<span data-ttu-id="62b66-153">"SumTotal"</span><span class="sxs-lookup"><span data-stu-id="62b66-153">"SumTotal"</span></span>  <br/> |
|<span data-ttu-id="62b66-154">3 se define como el contador de nombres ocultos de la hoja activa.</span><span class="sxs-lookup"><span data-stu-id="62b66-154">3 is defined as the hidden name Counter on the active sheet.</span></span>  <br/> |<span data-ttu-id="62b66-155">3</span><span class="sxs-lookup"><span data-stu-id="62b66-155">"3"</span></span>  <br/> |<span data-ttu-id="62b66-156">\<Address\></span><span class="sxs-lookup"><span data-stu-id="62b66-156">\<omitted\></span></span>  <br/> |<span data-ttu-id="62b66-157">segundo</span><span class="sxs-lookup"><span data-stu-id="62b66-157">2</span></span>  <br/> |<span data-ttu-id="62b66-158">Produzca</span><span class="sxs-lookup"><span data-stu-id="62b66-158">"Counter"</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="62b66-159">Vea también</span><span class="sxs-lookup"><span data-stu-id="62b66-159">See also</span></span>

- [<span data-ttu-id="62b66-160">xlfGetName</span><span class="sxs-lookup"><span data-stu-id="62b66-160">xlfGetName</span></span>](xlfgetname.md)
- [<span data-ttu-id="62b66-161">Funciones esenciales y útiles XLM de API de C</span><span class="sxs-lookup"><span data-stu-id="62b66-161">Essential and Useful C API XLM Functions</span></span>](essential-and-useful-c-api-xlm-functions.md)

