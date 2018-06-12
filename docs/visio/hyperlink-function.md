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
description: Se desplaza a la dirección especificada, que puede ser un archivo, UNC o dirección URL de ruta de acceso.
ms.openlocfilehash: 4e86fd3682d5d9e26c52839e76d2016d654b3141
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822294"
---
# <a name="hyperlink-function"></a><span data-ttu-id="a8c37-103">HYPERLINK (función)</span><span class="sxs-lookup"><span data-stu-id="a8c37-103">HYPERLINK Function</span></span>

<span data-ttu-id="a8c37-104">Se desplaza a la dirección especificada, que puede ser un archivo, UNC o dirección URL de ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="a8c37-104">Navigates to the specified address, which can be a file, UNC, or URL path.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="a8c37-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a8c37-105">Syntax</span></span>

<span data-ttu-id="a8c37-106">HYPERLINK ("** *dirección* **" ["," ** *subaddress* ** "," ** *extrainfo* ** ", ** *ventana* **," ** *marco* ** "])</span><span class="sxs-lookup"><span data-stu-id="a8c37-106">HYPERLINK(" ** *address* ** "[," ** *subaddress* ** "," ** *extrainfo* ** ", ** *window* **," ** *frame* ** "])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="a8c37-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a8c37-107">Parameters</span></span>

|<span data-ttu-id="a8c37-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="a8c37-108">**Name**</span></span>|<span data-ttu-id="a8c37-109">**Obligatorio/opcional**</span><span class="sxs-lookup"><span data-stu-id="a8c37-109">**Required/Optional**</span></span>|<span data-ttu-id="a8c37-110">**Tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="a8c37-110">**Data Type**</span></span>|<span data-ttu-id="a8c37-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a8c37-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="a8c37-112">_dirección_</span><span class="sxs-lookup"><span data-stu-id="a8c37-112">_address_</span></span> <br/> |<span data-ttu-id="a8c37-113">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="a8c37-113">Required</span></span>  <br/> |<span data-ttu-id="a8c37-114">**String**</span><span class="sxs-lookup"><span data-stu-id="a8c37-114">**String**</span></span> <br/> |<span data-ttu-id="a8c37-115">Ruta de acceso completa o relativa.</span><span class="sxs-lookup"><span data-stu-id="a8c37-115">A full path or a relative path.</span></span>  <br/> |
| <span data-ttu-id="a8c37-116">_subdirección_</span><span class="sxs-lookup"><span data-stu-id="a8c37-116">_subaddress_</span></span> <br/> |<span data-ttu-id="a8c37-117">Opcional</span><span class="sxs-lookup"><span data-stu-id="a8c37-117">Optional</span></span>  <br/> |<span data-ttu-id="a8c37-118">**String**</span><span class="sxs-lookup"><span data-stu-id="a8c37-118">**String**</span></span> <br/> |<span data-ttu-id="a8c37-119">Especifica una ubicación dentro de la dirección que se vincularán.</span><span class="sxs-lookup"><span data-stu-id="a8c37-119">Specifies a location within address to link to.</span></span> <span data-ttu-id="a8c37-120">Por ejemplo, si la dirección es un archivo de Microsoft Visio, subdirección puede ser un nombre de página. Si un archivo de Microsoft Excel, subdirección puede ser una hoja de cálculo o un intervalo dentro de una hoja de cálculo; Si una dirección URL de una página HTML, subdirección puede ser un delimitador.</span><span class="sxs-lookup"><span data-stu-id="a8c37-120">For example, if address is a Microsoft Visio file, subaddress can be a page name; if a Microsoft Excel file, subaddress can be a worksheet or range within a worksheet; if a URL for an HTML page, subaddress can be an anchor.</span></span>  <br/> |
| <span data-ttu-id="a8c37-121">_ExtraInfo_</span><span class="sxs-lookup"><span data-stu-id="a8c37-121">_extrainfo_</span></span> <br/> |<span data-ttu-id="a8c37-122">Opcional</span><span class="sxs-lookup"><span data-stu-id="a8c37-122">Optional</span></span>  <br/> |<span data-ttu-id="a8c37-123">**String**</span><span class="sxs-lookup"><span data-stu-id="a8c37-123">**String**</span></span> <br/> |<span data-ttu-id="a8c37-124">Pasa información que se usa en una dirección URL, como las coordenadas de un mapa de imagen.</span><span class="sxs-lookup"><span data-stu-id="a8c37-124">Passes information used in resolving the URL, such as the coordinates of an image map.</span></span>  <br/> |
| <span data-ttu-id="a8c37-125">_ventana_</span><span class="sxs-lookup"><span data-stu-id="a8c37-125">_window_</span></span> <br/> |<span data-ttu-id="a8c37-126">Opcional</span><span class="sxs-lookup"><span data-stu-id="a8c37-126">Optional</span></span>  <br/> |<span data-ttu-id="a8c37-127">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="a8c37-127">**Boolean**</span></span> <br/> |<span data-ttu-id="a8c37-p102">Especifica si el hipervínculo se debe abrir o no en una ventana nueva. El valor predeterminado es FALSE.</span><span class="sxs-lookup"><span data-stu-id="a8c37-p102">Specifies whether the hyperlink is opened in a new window. The default value is FALSE.</span></span>  <br/> |
| <span data-ttu-id="a8c37-130">_marco_</span><span class="sxs-lookup"><span data-stu-id="a8c37-130">_frame_</span></span> <br/> |<span data-ttu-id="a8c37-131">Opcional</span><span class="sxs-lookup"><span data-stu-id="a8c37-131">Optional</span></span>  <br/> |<span data-ttu-id="a8c37-132">**String**</span><span class="sxs-lookup"><span data-stu-id="a8c37-132">**String**</span></span> <br/> | <span data-ttu-id="a8c37-p103">Especifica el nombre de un marco de destino cuando Visio se abre como un documento Active en un explorador ActiveX, por ejemplo, en Microsoft Internet Explorer 3.0 o posterior. El valor predeterminado es una cadena vacía.</span><span class="sxs-lookup"><span data-stu-id="a8c37-p103">Specifies the name of a frame to target when Visio is open as an Active document in an ActiveX browser, such as Microsoft Internet Explorer 3.0 or later. The default is an empty string.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a8c37-135">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a8c37-135">Remarks</span></span>

<span data-ttu-id="a8c37-p104">Si el documento no tiene ruta de acceso base, Visio se desplaza siguiendo la ruta de acceso del documento. Si no se ha guardado el documento, el hipervínculo no está definido.</span><span class="sxs-lookup"><span data-stu-id="a8c37-p104">If the document has no base path, Visio navigates according to the document path. If the document has not been saved, the hyperlink is undefined.</span></span> 
  
<span data-ttu-id="a8c37-138">Rutas de acceso relativas se basan en el campo **base de hipervínculo** especificado en el cuadro de diálogo **Propiedades de Visio** .</span><span class="sxs-lookup"><span data-stu-id="a8c37-138">Relative paths are based on the **Hyperlink base** field specified in the **Visio Properties** dialog box.</span></span> 
  
<span data-ttu-id="a8c37-139">Se puede usar la función GOTOPAGE para desplazarse a las páginas de un documento.</span><span class="sxs-lookup"><span data-stu-id="a8c37-139">You can use the GOTOPAGE function to navigate to pages of a document.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="a8c37-140">Ejemplo 1</span><span class="sxs-lookup"><span data-stu-id="a8c37-140">Example 1</span></span>

 `HYPERLINK("C:\My Documents\Drawing1.vsdx")`
  
## <a name="example-2"></a><span data-ttu-id="a8c37-141">Ejemplo 2</span><span class="sxs-lookup"><span data-stu-id="a8c37-141">Example 2</span></span>

 `HYPERLINK("\\Server\Share\Drawing1.vsdx")`
  
## <a name="example-3"></a><span data-ttu-id="a8c37-142">Ejemplo 3</span><span class="sxs-lookup"><span data-stu-id="a8c37-142">Example 3</span></span>

 `HYPERLINK("http://www.microsoft.com")`
  
## <a name="example-4"></a><span data-ttu-id="a8c37-143">Ejemplo 4</span><span class="sxs-lookup"><span data-stu-id="a8c37-143">Example 4</span></span>

 `HYPERLINK("..\data.xlsx","sheet1!A1")`
  

