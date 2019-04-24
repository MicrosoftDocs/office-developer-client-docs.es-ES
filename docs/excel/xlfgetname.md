---
title: xlfGetName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
keywords:
- xlfgetname
localization_priority: Normal
ms.assetid: 65780435-aaa2-47af-b44f-07be7aa769ee
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: fdee0146ae2199097828e98abb96ffe43a64fc80
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303888"
---
# <a name="xlfgetname"></a><span data-ttu-id="bae0e-104">xlfGetName</span><span class="sxs-lookup"><span data-stu-id="bae0e-104">xlfGetName</span></span>

<span data-ttu-id="bae0e-105">**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="bae0e-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="bae0e-106">Devuelve la definición de un nombre tal como aparece en la columna se **refiere a** del cuadro de diálogo **Administrador de nombres** , que se muestra al hacer clic en **Administrador de nombres** en la sección **nombres definidos** de la ficha **fórmulas** . Si la definición contiene referencias, se proporcionan como referencias de estilo F1C1.</span><span class="sxs-lookup"><span data-stu-id="bae0e-106">Returns the definition of a name as it appears in the **Refers to** column of the **Name Manager** dialog box, which is displayed when you click **Name Manager** in the **Defined Names** section on the **Formulas** tab. If the definition contains references, they are given as R1C1-style references.</span></span> <span data-ttu-id="bae0e-107">Use **xlfGetName** para comprobar el valor definido por un nombre.</span><span class="sxs-lookup"><span data-stu-id="bae0e-107">Use **xlfGetName** to check the value defined by a name.</span></span> <span data-ttu-id="bae0e-108">Para obtener el nombre que corresponda a una definición, use [xlfGetDef](xlfgetdef.md).</span><span class="sxs-lookup"><span data-stu-id="bae0e-108">To get the name that corresponds to a definition, use [xlfGetDef](xlfgetdef.md).</span></span>
  
```cpp
Excel12(xlfGetName, LPXLOPER12 pxRes, 2, LPXLOPER12 pxNameText, LPXLOPER12 pxInfoType);
```

## <a name="parameters"></a><span data-ttu-id="bae0e-109">Parameters</span><span class="sxs-lookup"><span data-stu-id="bae0e-109">Parameters</span></span>

<span data-ttu-id="bae0e-110">_pxNameText_ (**xltypeStr**)</span><span class="sxs-lookup"><span data-stu-id="bae0e-110">_pxNameText_ (**xltypeStr**)</span></span>
  
<span data-ttu-id="bae0e-111">Puede ser un nombre definido en la hoja; una referencia externa a un nombre definido en el libro activo; por ejemplo, `"!Sales"`; o una referencia externa a un nombre definido en un libro abierto en particular, por ejemplo `"[Book1]SHEET1!Sales"`,.</span><span class="sxs-lookup"><span data-stu-id="bae0e-111">Can be a name defined on the sheet; an external reference to a name defined on the active workbook, for example,  `"!Sales"`; or an external reference to a name defined on a particular open workbook, for example,  `"[Book1]SHEET1!Sales"`.</span></span>  <span data-ttu-id="bae0e-112">_pxNameText_ también puede ser un nombre oculto.</span><span class="sxs-lookup"><span data-stu-id="bae0e-112">_pxNameText_ can also be a hidden name.</span></span> 
  
<span data-ttu-id="bae0e-113">_pxInfoType_ (**xltypeBool**)</span><span class="sxs-lookup"><span data-stu-id="bae0e-113">_pxInfoType_ (**xltypeBool**)</span></span>
  
<span data-ttu-id="bae0e-114">Especifica el tipo de información que se va a devolver sobre el nombre.</span><span class="sxs-lookup"><span data-stu-id="bae0e-114">Specifies the type of information to return about the name.</span></span> <span data-ttu-id="bae0e-115">Si es **false** o se omite, se devuelve la definición.</span><span class="sxs-lookup"><span data-stu-id="bae0e-115">If **FALSE** or omitted, the definition is returned.</span></span> <span data-ttu-id="bae0e-116">Si es **true**, devuelve **true** si el nombre está definido sólo para la hoja, **false** si el nombre está definido para todo el libro.</span><span class="sxs-lookup"><span data-stu-id="bae0e-116">If **TRUE**, returns **TRUE** if the name is defined for just the sheet, **FALSE** if the name is defined for the entire workbook.</span></span> 
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="bae0e-117">Valor de la propiedad/valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bae0e-117">Property value/Return value</span></span>

<span data-ttu-id="bae0e-118">_pxRes_ (**xltypeStr**, **xltypeBool**o **xltypeErr**)</span><span class="sxs-lookup"><span data-stu-id="bae0e-118">_pxRes_ (**xltypeStr**, **xltypeBool**, or **xltypeErr**)</span></span>
  
<span data-ttu-id="bae0e-119">Dependiendo del valor pasado para _pxInfoType_, devuelve la definición del nombre especificado (**XltypeStr**) o **true** o **false** (**xltypeBool**).</span><span class="sxs-lookup"><span data-stu-id="bae0e-119">Depending on the value passed for  _pxInfoType_, returns the definition of the specified name (**xltypeStr**), or **TRUE** or **FALSE** (**xltypeBool**).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="bae0e-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="bae0e-120">Remarks</span></span>

<span data-ttu-id="bae0e-121">Si la casilla de verificación **proteger hoja y contenido de celdas bloqueadas** está activada en el cuadro de diálogo **proteger hoja** para proteger el libro que contiene el nombre, `#N/A` **xlfGetName** devuelve el valor de error.</span><span class="sxs-lookup"><span data-stu-id="bae0e-121">If the **Protect worksheet and contents of locked cells** check box has been selected in the **Protect Sheet** dialog box to protect the workbook containing the name, **xlfGetName** returns the  `#N/A` error value.</span></span> <span data-ttu-id="bae0e-122">Para ver el cuadro de diálogo **proteger hoja** , haga clic en **proteger hoja** en la sección **cambios** de la ficha **revisar** .</span><span class="sxs-lookup"><span data-stu-id="bae0e-122">To see the **Protect Sheet** dialog box, click **Protect Sheet** in the **Changes** section of the **Review** tab.</span></span> 
  
<span data-ttu-id="bae0e-123">En la tabla siguiente se muestran tres ejemplos de los valores devueltos por una llamada a **xlfGetDef** con el argumento _pxNameText_ especificado.</span><span class="sxs-lookup"><span data-stu-id="bae0e-123">The following table lists three examples of the values returned by a call to **xlfGetDef** with the specified  _pxNameText_ argument.</span></span> 
  
|<span data-ttu-id="bae0e-124">**Definición en Excel**</span><span class="sxs-lookup"><span data-stu-id="bae0e-124">**Definition in Excel**</span></span>|<span data-ttu-id="bae0e-125">**_pxNameText_**</span><span class="sxs-lookup"><span data-stu-id="bae0e-125">**_pxNameText_**</span></span>|<span data-ttu-id="bae0e-126">**Valor deVuelto**</span><span class="sxs-lookup"><span data-stu-id="bae0e-126">**Value Returned**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="bae0e-127">El nombre sales en una hoja se define como el número 523.</span><span class="sxs-lookup"><span data-stu-id="bae0e-127">The name Sales on a sheet is defined as the number 523.</span></span>  <br/> |<span data-ttu-id="bae0e-128">Lín</span><span class="sxs-lookup"><span data-stu-id="bae0e-128">"Sales"</span></span>  <br/> |<span data-ttu-id="bae0e-129">"= 523"</span><span class="sxs-lookup"><span data-stu-id="bae0e-129">"=523"</span></span>  <br/> |
|<span data-ttu-id="bae0e-130">El beneficio del nombre de la hoja activa se define como la fórmula = ventas-costes.</span><span class="sxs-lookup"><span data-stu-id="bae0e-130">The name Profit on the active sheet is defined as the formula =Sales-Costs.</span></span>  <br/> |<span data-ttu-id="bae0e-131">"! Beneficios</span><span class="sxs-lookup"><span data-stu-id="bae0e-131">"!Profit"</span></span>  <br/> |<span data-ttu-id="bae0e-132">"= Costos de ventas"</span><span class="sxs-lookup"><span data-stu-id="bae0e-132">"=Sales-Costs"</span></span>  <br/> |
|<span data-ttu-id="bae0e-133">La base de datos de nombres de la hoja activa se define como el rango a1: F500.</span><span class="sxs-lookup"><span data-stu-id="bae0e-133">The name Database on the active sheet is defined as the range A1:F500.</span></span>  <br/> |<span data-ttu-id="bae0e-134">"! Base</span><span class="sxs-lookup"><span data-stu-id="bae0e-134">"!Database"</span></span>  <br/> |<span data-ttu-id="bae0e-135">"= F1C1: R500C6"</span><span class="sxs-lookup"><span data-stu-id="bae0e-135">"=R1C1:R500C6"</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="bae0e-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="bae0e-136">See also</span></span>

- [<span data-ttu-id="bae0e-137">xlfGetDef</span><span class="sxs-lookup"><span data-stu-id="bae0e-137">xlfGetDef</span></span>](xlfgetdef.md)
- [<span data-ttu-id="bae0e-138">Funciones esenciales y útiles XLM de API de C</span><span class="sxs-lookup"><span data-stu-id="bae0e-138">Essential and Useful C API XLM Functions</span></span>](essential-and-useful-c-api-xlm-functions.md)

