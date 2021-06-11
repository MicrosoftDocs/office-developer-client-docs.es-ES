---
title: HYPERLINK (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251441
localization_priority: Normal
ms.assetid: 943636a6-e135-a626-7924-11e238156548
description: Navega a la dirección especificada, que puede ser una ruta de acceso de archivo, UNC o DIRECCIÓN URL.
ms.openlocfilehash: 5e4952c3d56eff0cb1e6518928a7b8259f645046
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329949"
---
# <a name="hyperlink-function"></a><span data-ttu-id="823f2-103">Función HYPERLINK</span><span class="sxs-lookup"><span data-stu-id="823f2-103">HYPERLINK Function</span></span>

<span data-ttu-id="823f2-104">Navega a la dirección especificada, que puede ser una ruta de acceso de archivo, UNC o DIRECCIÓN URL.</span><span class="sxs-lookup"><span data-stu-id="823f2-104">Navigates to the specified address, which can be a file, UNC, or URL path.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="823f2-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="823f2-105">Syntax</span></span>

<span data-ttu-id="823f2-106">HYPERLINK(" \*\* *address* \*\* "[," \*\* *subaddress* \*\* "," \*\* *extrainfo* \*\* ", \*\* *window* \*\*," \*\* *frame* \*\* "])</span><span class="sxs-lookup"><span data-stu-id="823f2-106">HYPERLINK(" \*\* *address* \*\* "[," \*\* *subaddress* \*\* "," \*\* *extrainfo* \*\* ", \*\* *window* \*\*," \*\* *frame* \*\* "])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="823f2-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="823f2-107">Parameters</span></span>

|<span data-ttu-id="823f2-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="823f2-108">**Name**</span></span>|<span data-ttu-id="823f2-109">**Necesario/Opcional**</span><span class="sxs-lookup"><span data-stu-id="823f2-109">**Required/Optional**</span></span>|<span data-ttu-id="823f2-110">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="823f2-110">**Data Type**</span></span>|<span data-ttu-id="823f2-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="823f2-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="823f2-112">_address_</span><span class="sxs-lookup"><span data-stu-id="823f2-112">_address_</span></span> <br/> |<span data-ttu-id="823f2-113">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="823f2-113">Required</span></span>  <br/> |<span data-ttu-id="823f2-114">**String**</span><span class="sxs-lookup"><span data-stu-id="823f2-114">**String**</span></span> <br/> |<span data-ttu-id="823f2-115">Ruta de acceso completa o relativa.</span><span class="sxs-lookup"><span data-stu-id="823f2-115">A full path or a relative path.</span></span>  <br/> |
| <span data-ttu-id="823f2-116">_subaddress_</span><span class="sxs-lookup"><span data-stu-id="823f2-116">_subaddress_</span></span> <br/> |<span data-ttu-id="823f2-117">Opcional</span><span class="sxs-lookup"><span data-stu-id="823f2-117">Optional</span></span>  <br/> |<span data-ttu-id="823f2-118">**String**</span><span class="sxs-lookup"><span data-stu-id="823f2-118">**String**</span></span> <br/> |<span data-ttu-id="823f2-p101">Especifica la ubicación, dentro de la dirección especificada, con la que debe establecerse el vínculo. Por ejemplo, si dirección es un archivo de Microsoft Visio, subdirección puede ser un nombre de página. Si se trata de un archivo de Microsoft Excel, subdirección puede ser una hoja de cálculo o un rango de celdas en ella. Si se trata de la dirección URL de una página HTML, la subdirección puede ser un delimitador.</span><span class="sxs-lookup"><span data-stu-id="823f2-p101">Specifies a location within address to link to. For example, if address is a Microsoft Visio file, subaddress can be a page name; if a Microsoft Excel file, subaddress can be a worksheet or range within a worksheet; if a URL for an HTML page, subaddress can be an anchor.</span></span>  <br/> |
| <span data-ttu-id="823f2-121">_extrainfo_</span><span class="sxs-lookup"><span data-stu-id="823f2-121">_extrainfo_</span></span> <br/> |<span data-ttu-id="823f2-122">Opcional</span><span class="sxs-lookup"><span data-stu-id="823f2-122">Optional</span></span>  <br/> |<span data-ttu-id="823f2-123">**String**</span><span class="sxs-lookup"><span data-stu-id="823f2-123">**String**</span></span> <br/> |<span data-ttu-id="823f2-124">Pasa información que se usa en una dirección URL, como las coordenadas de un mapa de imagen.</span><span class="sxs-lookup"><span data-stu-id="823f2-124">Passes information used in resolving the URL, such as the coordinates of an image map.</span></span>  <br/> |
| <span data-ttu-id="823f2-125">_ventana_</span><span class="sxs-lookup"><span data-stu-id="823f2-125">_window_</span></span> <br/> |<span data-ttu-id="823f2-126">Opcional</span><span class="sxs-lookup"><span data-stu-id="823f2-126">Optional</span></span>  <br/> |<span data-ttu-id="823f2-127">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="823f2-127">**Boolean**</span></span> <br/> |<span data-ttu-id="823f2-p102">Especifica si el hipervínculo se debe abrir o no en una ventana nueva. El valor predeterminado es FALSE.</span><span class="sxs-lookup"><span data-stu-id="823f2-p102">Specifies whether the hyperlink is opened in a new window. The default value is FALSE.</span></span>  <br/> |
| <span data-ttu-id="823f2-130">_marco_</span><span class="sxs-lookup"><span data-stu-id="823f2-130">_frame_</span></span> <br/> |<span data-ttu-id="823f2-131">Opcional</span><span class="sxs-lookup"><span data-stu-id="823f2-131">Optional</span></span>  <br/> |<span data-ttu-id="823f2-132">**String**</span><span class="sxs-lookup"><span data-stu-id="823f2-132">**String**</span></span> <br/> | <span data-ttu-id="823f2-p103">Especifica el nombre de un marco de destino cuando Visio se abre como un documento Active en un explorador ActiveX, por ejemplo, en Microsoft Internet Explorer 3.0 o posterior. El valor predeterminado es una cadena vacía.</span><span class="sxs-lookup"><span data-stu-id="823f2-p103">Specifies the name of a frame to target when Visio is open as an Active document in an ActiveX browser, such as Microsoft Internet Explorer 3.0 or later. The default is an empty string.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="823f2-135">Comentarios</span><span class="sxs-lookup"><span data-stu-id="823f2-135">Remarks</span></span>

<span data-ttu-id="823f2-p104">Si el documento no tiene ruta de acceso base, Visio se desplaza siguiendo la ruta de acceso del documento. Si no se ha guardado el documento, el hipervínculo no está definido.</span><span class="sxs-lookup"><span data-stu-id="823f2-p104">If the document has no base path, Visio navigates according to the document path. If the document has not been saved, the hyperlink is undefined.</span></span> 
  
<span data-ttu-id="823f2-138">Las rutas de acceso relativas basadas en el campo **Base de hipervínculo** especificado en el cuadro de diálogo **Propiedades de Visio**.</span><span class="sxs-lookup"><span data-stu-id="823f2-138">Relative paths are based on the **Hyperlink base** field specified in the **Visio Properties** dialog box.</span></span> 
  
<span data-ttu-id="823f2-139">Se puede usar la función GOTOPAGE para desplazarse a las páginas de un documento.</span><span class="sxs-lookup"><span data-stu-id="823f2-139">You can use the GOTOPAGE function to navigate to pages of a document.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="823f2-140">Ejemplo 1</span><span class="sxs-lookup"><span data-stu-id="823f2-140">Example 1</span></span>

 `HYPERLINK("C:\My Documents\Drawing1.vsdx")`
  
## <a name="example-2"></a><span data-ttu-id="823f2-141">Ejemplo 2</span><span class="sxs-lookup"><span data-stu-id="823f2-141">Example 2</span></span>

 `HYPERLINK("\\Server\Share\Drawing1.vsdx")`
  
## <a name="example-3"></a><span data-ttu-id="823f2-142">Ejemplo 3</span><span class="sxs-lookup"><span data-stu-id="823f2-142">Example 3</span></span>

 `HYPERLINK("https://www.microsoft.com")`
  
## <a name="example-4"></a><span data-ttu-id="823f2-143">Ejemplo 4</span><span class="sxs-lookup"><span data-stu-id="823f2-143">Example 4</span></span>

 `HYPERLINK("..\data.xlsx","sheet1!A1")`
  

