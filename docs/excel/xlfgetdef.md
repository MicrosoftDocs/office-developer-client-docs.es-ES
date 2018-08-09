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
ms.openlocfilehash: 030c4e501e8a9eb4b6ce29d7fe0e171324b50b5c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815746"
---
# <a name="xlfgetdef"></a><span data-ttu-id="b0ef8-104">xlfGetDef</span><span class="sxs-lookup"><span data-stu-id="b0ef8-104">xlfGetDef</span></span>

<span data-ttu-id="b0ef8-105">**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="b0ef8-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="b0ef8-106">Devuelve el nombre, como texto, que se define para un área determinada, un valor o una fórmula en un libro.</span><span class="sxs-lookup"><span data-stu-id="b0ef8-106">Returns the name, as text, that is defined for a particular area, value, or formula in a workbook.</span></span> <span data-ttu-id="b0ef8-107">En Excel, este valor se muestra en la columna **nombre** del cuadro de diálogo **Administrador de nombres** , que se muestra al hacer clic en **Administrador de nombres** en la sección **Nombres definidos** en la ficha **fórmulas** usar **xlfGetDef** para obtener el nombre que corresponde a una definición.</span><span class="sxs-lookup"><span data-stu-id="b0ef8-107">In Excel, this value is displayed in the **Name** column of the **Name Manager** dialog box, which is displayed when you click **Name Manager** in the **Defined Names** section on the **Formulas** tab. Use **xlfGetDef** to get the name that corresponds to a definition.</span></span> <span data-ttu-id="b0ef8-108">Para obtener la definición de un nombre, use [xlfGetName](xlfgetname.md).</span><span class="sxs-lookup"><span data-stu-id="b0ef8-108">To get the definition of a name, use [xlfGetName](xlfgetname.md).</span></span>
  
```cpp
Excel12(xlfGetDef, LPXLOPER12 pxRes, 3, LPXLOPER12 pxDefText, LPXLOPER12 pxDocumentText, LPXLOPER12 pxTypeNum);
```

## <a name="parameters"></a><span data-ttu-id="b0ef8-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b0ef8-109">Parameters</span></span>

<span data-ttu-id="b0ef8-110">_pxDefText_ (**xltypeStr**)</span><span class="sxs-lookup"><span data-stu-id="b0ef8-110">_pxDefText_ (**xltypeStr**)</span></span>
  
<span data-ttu-id="b0ef8-111">Puede ser cualquier cosa que se puede definir un nombre para hacer referencia a, incluida una referencia, un valor, un objeto o una fórmula.</span><span class="sxs-lookup"><span data-stu-id="b0ef8-111">Can be anything you can define a name to refer to, including a reference, a value, an object, or a formula.</span></span>
  
<span data-ttu-id="b0ef8-112">Referencias deberán incluirse en el estilo F1C1, tales como `"R3C5"`.</span><span class="sxs-lookup"><span data-stu-id="b0ef8-112">References must be given in R1C1 style, such as  `"R3C5"`.</span></span> <span data-ttu-id="b0ef8-113">Si _pxDefText_ es un valor o una fórmula, no es necesario incluir el signo de igual que se muestra en la columna **Hace referencia a** en el cuadro de diálogo **Administrador de nombres** .</span><span class="sxs-lookup"><span data-stu-id="b0ef8-113">If  _pxDefText_ is a value or formula, it is not necessary to include the equal sign that is displayed in the **Refers To** column in the **Name Manager** dialog box.</span></span> <span data-ttu-id="b0ef8-114">Si hay más de un nombre para _pxDefText_, **xlfGetDef** devuelve el nombre de la primera.</span><span class="sxs-lookup"><span data-stu-id="b0ef8-114">If there is more than one name for  _pxDefText_, **xlfGetDef** returns the first name.</span></span> <span data-ttu-id="b0ef8-115">Si ningún nombre coincide con _pxDefText_, **xlfGetDef** devuelve el `#NAME?` valor de error.</span><span class="sxs-lookup"><span data-stu-id="b0ef8-115">If no name matches  _pxDefText_, **xlfGetDef** returns the  `#NAME?` error value.</span></span> 
  
<span data-ttu-id="b0ef8-116">_pxDocumentText_ (**xltypeStr**)</span><span class="sxs-lookup"><span data-stu-id="b0ef8-116">_pxDocumentText_ (**xltypeStr**)</span></span>
  
<span data-ttu-id="b0ef8-117">Especifica la hoja que _pxDefText_ se encuentra en.</span><span class="sxs-lookup"><span data-stu-id="b0ef8-117">Specifies the sheet that  _pxDefText_ is on.</span></span> <span data-ttu-id="b0ef8-118">Si _pxDocumentText_ se omite, se supone que ésta la hoja de cálculo activa.</span><span class="sxs-lookup"><span data-stu-id="b0ef8-118">If  _pxDocumentText_ is omitted, it is assumed to be the active sheet.</span></span> 
  
<span data-ttu-id="b0ef8-119">_pxTypeNum_ (**xltypeNum**)</span><span class="sxs-lookup"><span data-stu-id="b0ef8-119">_pxTypeNum_ (**xltypeNum**)</span></span>
  
<span data-ttu-id="b0ef8-120">Un número de 1 a 3 que especifica qué tipos de nombres se devuelven.</span><span class="sxs-lookup"><span data-stu-id="b0ef8-120">A number from 1 to 3 specifying which types of names are returned.</span></span>
  
|<span data-ttu-id="b0ef8-121">**_pxTypeNum_**</span><span class="sxs-lookup"><span data-stu-id="b0ef8-121">**_pxTypeNum_**</span></span>|<span data-ttu-id="b0ef8-122">**Devuelve**</span><span class="sxs-lookup"><span data-stu-id="b0ef8-122">**Returns**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b0ef8-123">1 u omitido</span><span class="sxs-lookup"><span data-stu-id="b0ef8-123">1 or omitted</span></span>  <br/> |<span data-ttu-id="b0ef8-124">Nombres normales.</span><span class="sxs-lookup"><span data-stu-id="b0ef8-124">Normal names only.</span></span>  <br/> |
|<span data-ttu-id="b0ef8-125">2</span><span class="sxs-lookup"><span data-stu-id="b0ef8-125">2</span></span>  <br/> |<span data-ttu-id="b0ef8-126">Nombres ocultos.</span><span class="sxs-lookup"><span data-stu-id="b0ef8-126">Hidden names only.</span></span>  <br/> |
|<span data-ttu-id="b0ef8-127">3</span><span class="sxs-lookup"><span data-stu-id="b0ef8-127">3</span></span>  <br/> |<span data-ttu-id="b0ef8-128">Todos los nombres.</span><span class="sxs-lookup"><span data-stu-id="b0ef8-128">All names.</span></span>  <br/> |
   
## <a name="property-valuereturn-value"></a><span data-ttu-id="b0ef8-129">Valor de la propiedad/valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b0ef8-129">Property value/Return value</span></span>

 <span data-ttu-id="b0ef8-130">_pxRes_ (**xltypeStr** o **xltypeErr**)</span><span class="sxs-lookup"><span data-stu-id="b0ef8-130">_pxRes_ (**xltypeStr** or **xltypeErr**)</span></span>
  
<span data-ttu-id="b0ef8-131">Devuelve el nombre asociado a la definición especificada.</span><span class="sxs-lookup"><span data-stu-id="b0ef8-131">Returns the name associated with the specified definition.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="b0ef8-132">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b0ef8-132">Remarks</span></span>

<span data-ttu-id="b0ef8-133">En la siguiente tabla se enumera los cuatro ejemplos de los valores devueltos por una llamada a **xlfGetDef** con los argumentos especificados.</span><span class="sxs-lookup"><span data-stu-id="b0ef8-133">The following table lists four examples of the values returned by a call to **xlfGetDef** with the specified arguments.</span></span> 
  
|<span data-ttu-id="b0ef8-134">**Nombre definido en Excel**</span><span class="sxs-lookup"><span data-stu-id="b0ef8-134">**Name defined in Excel**</span></span>|<span data-ttu-id="b0ef8-135">**_pxDefText_**</span><span class="sxs-lookup"><span data-stu-id="b0ef8-135">**_pxDefText_**</span></span>|<span data-ttu-id="b0ef8-136">**_pxDocumentText_**</span><span class="sxs-lookup"><span data-stu-id="b0ef8-136">**_pxDocumentText_**</span></span>|<span data-ttu-id="b0ef8-137">**_pxTypeNum_**</span><span class="sxs-lookup"><span data-stu-id="b0ef8-137">**_pxTypeNum_**</span></span>|<span data-ttu-id="b0ef8-138">**Valor devuelto**</span><span class="sxs-lookup"><span data-stu-id="b0ef8-138">**Value Returned**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="b0ef8-139">El intervalo especificado en Sheet4 es denominado ventas.</span><span class="sxs-lookup"><span data-stu-id="b0ef8-139">The specified range in Sheet4 is named Sales.</span></span>  <br/> |<span data-ttu-id="b0ef8-140">"R2C2:R9C6"</span><span class="sxs-lookup"><span data-stu-id="b0ef8-140">"R2C2:R9C6"</span></span>  <br/> |<span data-ttu-id="b0ef8-141">"Sheet4"</span><span class="sxs-lookup"><span data-stu-id="b0ef8-141">"Sheet4"</span></span>  <br/> |<span data-ttu-id="b0ef8-142">\<se omite\></span><span class="sxs-lookup"><span data-stu-id="b0ef8-142">\<omitted\></span></span>  <br/> |<span data-ttu-id="b0ef8-143">"Ventas"</span><span class="sxs-lookup"><span data-stu-id="b0ef8-143">"Sales"</span></span>  <br/> |
|<span data-ttu-id="b0ef8-144">El valor 100 en Sheet4 se define como constante.</span><span class="sxs-lookup"><span data-stu-id="b0ef8-144">The value 100 in Sheet4 is defined as Constant.</span></span>  <br/> |<span data-ttu-id="b0ef8-145">"100"</span><span class="sxs-lookup"><span data-stu-id="b0ef8-145">"100"</span></span>  <br/> |<span data-ttu-id="b0ef8-146">"Sheet4"</span><span class="sxs-lookup"><span data-stu-id="b0ef8-146">"Sheet4"</span></span>  <br/> |<span data-ttu-id="b0ef8-147">\<se omite\></span><span class="sxs-lookup"><span data-stu-id="b0ef8-147">\<omitted\></span></span>  <br/> |<span data-ttu-id="b0ef8-148">"Constante"</span><span class="sxs-lookup"><span data-stu-id="b0ef8-148">"Constant"</span></span>  <br/> |
|<span data-ttu-id="b0ef8-149">La fórmula especificada en Sheet4 se denomina SumTotal.</span><span class="sxs-lookup"><span data-stu-id="b0ef8-149">The specified formula in Sheet4 is named SumTotal.</span></span>  <br/> |<span data-ttu-id="b0ef8-150">"SUM(R1C1:R10C1)"</span><span class="sxs-lookup"><span data-stu-id="b0ef8-150">"SUM(R1C1:R10C1)"</span></span>  <br/> |<span data-ttu-id="b0ef8-151">"Sheet4"</span><span class="sxs-lookup"><span data-stu-id="b0ef8-151">"Sheet4"</span></span>  <br/> |<span data-ttu-id="b0ef8-152">\<se omite\></span><span class="sxs-lookup"><span data-stu-id="b0ef8-152">\<omitted\></span></span>  <br/> |<span data-ttu-id="b0ef8-153">"SumTotal"</span><span class="sxs-lookup"><span data-stu-id="b0ef8-153">"SumTotal"</span></span>  <br/> |
|<span data-ttu-id="b0ef8-154">3 se define como el contador de nombre oculto en la hoja activa.</span><span class="sxs-lookup"><span data-stu-id="b0ef8-154">3 is defined as the hidden name Counter on the active sheet.</span></span>  <br/> |<span data-ttu-id="b0ef8-155">"3"</span><span class="sxs-lookup"><span data-stu-id="b0ef8-155">"3"</span></span>  <br/> |<span data-ttu-id="b0ef8-156">\<se omite\></span><span class="sxs-lookup"><span data-stu-id="b0ef8-156">\<omitted\></span></span>  <br/> |<span data-ttu-id="b0ef8-157">2</span><span class="sxs-lookup"><span data-stu-id="b0ef8-157">2</span></span>  <br/> |<span data-ttu-id="b0ef8-158">"Contador"</span><span class="sxs-lookup"><span data-stu-id="b0ef8-158">"Counter"</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b0ef8-159">Vea también</span><span class="sxs-lookup"><span data-stu-id="b0ef8-159">See also</span></span>

- [<span data-ttu-id="b0ef8-160">xlfGetName</span><span class="sxs-lookup"><span data-stu-id="b0ef8-160">xlfGetName</span></span>](xlfgetname.md)
- [<span data-ttu-id="b0ef8-161">Funciones esenciales y útiles XLM de API de C</span><span class="sxs-lookup"><span data-stu-id="b0ef8-161">Essential and Useful C API XLM Functions</span></span>](essential-and-useful-c-api-xlm-functions.md)

